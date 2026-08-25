> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | [02 Product PRD](02_PRODUCT_PRD.md) | [03 AI Strategy](03_AI_DOMAIN_STRATEGY.md) | **04 Tech Architecture** | [05 UX/UI Demo](05_UX_UI_DEMO.md) | [06 Execution & Pitch](06_EXECUTION_PITCH_JUDGING.md) | [07 Evidence & Knowledge](07_EVIDENCE_DECISIONS_KNOWLEDGE.md)

---

# 04 — TECHNICAL ARCHITECTURE
## Everything Engineers Need

This document outlines the technical architecture for the "AI-Based Cognitive Gaming and Memory Assistance Platform for Elderly Dementia Patients in NER" (PS ID: 26003, MDoNER). It is designed for maximum speed during the hackathon while remaining technically sound and scalable.

### Technology Decisions

| Area | Technology | Why | Alternatives Considered |
|---|---|---|---|
| Frontend | React Native with Expo | Cross-platform (Android tablets are common in NER), fast prototyping, offline capabilities via Expo SQLite. | PWA (less native feel on low-end devices), Flutter (steeper learning curve for our team). |
| Backend | Python with FastAPI | Excellent for AI/ML integration, fast execution, easy to build REST APIs quickly. | Node.js/Express (harder AI integration), Django (too heavy for hackathon). |
| Database (Cloud) | Supabase (PostgreSQL) | Instant REST/GraphQL APIs, real-time subscriptions, built-in auth, fast setup. | Firebase (NoSQL can be tricky for complex analytical queries), raw Postgres (too much ops). |
| Database (Local) | SQLite (via Expo) | Essential for offline functionality in NER. | Async Storage (not good for relational game data). |
| AI / ML | FastAPI + Whisper/TTS API | Fast deployment, easy to swap local/cloud models based on hardware. | On-device ML (too risky/slow for hackathon timeframe). |
| UI Framework | React Native Paper | Material Design compliance, accessible components, large touch targets suitable for elderly. | NativeBase (deprecated), building from scratch (too slow). |

### Frontend
- **Framework:** React Native with Expo for rapid prototyping and cross-platform support (focus on Android tablets and phones).
- **Elderly-Friendly UI Considerations:**
    - High contrast color schemes (WCAG AAA compliant where possible).
    - Large touch targets (minimum 48x48 dp).
    - Simple, linear navigation (avoid complex tab/drawer hierarchies).
    - Clear, readable typography (sans-serif, large font sizes).
    - Use of recognizable icons with text labels.

### Backend
- **Framework:** FastAPI (Python).
- **Architecture:** RESTful API design.
- **Real-time:** WebSocket implementation for caregiver dashboard updates (e.g., when a patient completes a game, update the dashboard immediately).

### Database
- **Primary/Cloud:** Supabase (PostgreSQL) for structured data and fast hackathon setup.
- **Local/Offline:** Expo SQLite for local storage of game progress and metrics when offline.
- **Cache:** In-memory caching in FastAPI (or Redis if necessary for complex session handling, but keep it simple initially).

### AI / ML
- **Adaptive Difficulty:** Simple reinforcement learning or decision tree logic implemented in Python on the backend (or locally in TS if fully offline).
- **Speech-to-Text (STT):** OpenAI Whisper API (or local Whisper model if running a heavy backend) for parsing patient voice input.
- **Text-to-Speech (TTS):** Google Cloud TTS or local Android TTS engine with support for NER languages (Assamese, Bengali, etc.).
- **Report Generation (Optional):** Integration with Gemini API to generate natural language summaries for caregivers based on weekly cognitive metrics.

### External APIs
| API | Purpose | Fallback | Risk |
|---|---|---|---|
| OpenAI Whisper | Voice command recognition | On-device speech recognition | Latency on slow connections |
| Google Cloud TTS | High-quality localized voice prompts | OS native TTS | API rate limits/costs |
| Gemini API | Caregiver report generation | Template-based hardcoded reports | API key exposure, timeouts |
| Supabase Auth | User authentication | Local mock auth | Network dependency |

### System Architecture

```mermaid
flowchart TD
    subgraph Client [Tablet / Phone (Patient & Caregiver)]
        UI[React Native UI]
        OfflineStore[(SQLite Local Store)]
        SyncMgr[Sync Manager]
        UI <--> OfflineStore
        UI <--> SyncMgr
    end

    subgraph Backend [FastAPI Server]
        API[REST API / WebSockets]
        AIEngine[AI / Game Logic Engine]
        API <--> AIEngine
    end

    subgraph External [External Services]
        Supabase[(Supabase / Postgres)]
        Whisper[Whisper STT]
        Gemini[Gemini API]
    end

    SyncMgr <-->|Sync (when online)| API
    API <--> Supabase
    AIEngine <--> Whisper
    AIEngine <--> Gemini
```

### Data Flow

**1. Patient plays a game (Online):**
1. Patient interacts with React Native UI.
2. Game logic executes.
3. Upon completion, `POST /api/game/result` is called.
4. FastAPI validates and stores data in Supabase.
5. AI engine triggers difficulty recalculation.

**2. Offline → Online sync flow:**
1. Patient plays game offline.
2. Results saved to local SQLite via React Native.
3. Device detects network connection.
4. Sync Manager reads un-synced records from SQLite.
5. Batch `POST /api/sync` sent to Backend.
6. Backend processes and acknowledges.
7. Local records marked as synced.

**3. Caregiver checks dashboard:**
1. Caregiver opens app/web view.
2. `GET /api/dashboard/{caregiver_id}` is called.
3. Backend retrieves aggregated metrics from Supabase.
4. UI renders charts and insights.

### Component Architecture (Frontend)
```
/src
  /components
    /common      (Buttons, Cards, Typography - styled for elderly)
    /games       (MemoryMatrix, SequenceRecall, AudioMatch)
    /dashboard   (Charts, PatientList)
  /screens
    PatientHome
    GameScreen
    CaregiverDashboard
    Settings
  /services
    api.ts       (Axios config, API calls)
    sync.ts      (Offline sync logic)
    audio.ts     (TTS/STT wrappers)
  /store
    (State management - Zustand or Context)
```

### API Contracts

**`POST /api/game/result`**
- Request:
  ```json
  {
    "patient_id": "uuid",
    "game_type": "memory_matrix",
    "difficulty_level": 2,
    "score": 85,
    "completion_time_ms": 12000,
    "errors": 1,
    "timestamp": "2026-08-24T10:00:00Z"
  }
  ```
- Response: `201 Created`

**`GET /api/patient/{id}/progress`**
- Response:
  ```json
  {
    "patient_id": "uuid",
    "current_levels": {
      "memory": 3,
      "attention": 2
    },
    "recent_scores": [ ... ]
  }
  ```

### Data Model

*   **Patient:** `id` (UUID), `name`, `age`, `language_pref`, `state` (NER state), `baseline_cognitive_score`, `created_at`
*   **Caregiver:** `id` (UUID), `name`, `email`, `phone_number`
*   **PatientCaregiverMap:** `patient_id`, `caregiver_id`, `relation`
*   **GameSession:** `id` (UUID), `patient_id`, `game_type`, `cognitive_domain`, `difficulty_level`, `score`, `completion_time`, `error_count`, `timestamp`, `is_synced` (local only)
*   **Reminder:** `id`, `patient_id`, `title`, `audio_prompt_url`, `scheduled_time`, `is_recurring`, `status`

### Authentication
- **Caregivers:** Standard Email/Password via Supabase Auth.
- **Patients (Elderly):** Simple 4-digit PIN or picture-based login linked to the caregiver's account to minimize cognitive load.

### Offline Strategy (CRITICAL FOR NER)
Given connectivity issues in the North Eastern Region:
1. **Local First:** All game assets (images, basic audio) must be bundled with the app.
2. **Local Storage:** Use Expo SQLite to store all game sessions and metrics.
3. **Queueing:** A background task (or AppState listener) checks for network connectivity.
4. **Syncing:** When online, push a batch of completed sessions to the backend.
5. **Conflict Resolution:** Last-write-wins based on client timestamp for simple metrics.

### Voice Architecture
1. **Trigger:** Large, explicit microphone button (wake words are too battery intensive/complex for hackathon).
2. **STT Pipeline:** Record audio in React Native -> compress -> send to backend `POST /api/voice/intent` -> backend calls Whisper API -> extracts intent (e.g., "start game", "call daughter").
3. **TTS Pipeline:** Backend determines response -> calls Google TTS -> sends audio URL back to client -> client plays audio.

### Multilingual Architecture
- **Framework:** `react-i18next`.
- **Structure:** JSON files for each language (e.g., `en.json`, `as.json` for Assamese, `bn.json` for Bengali).
- **Fonts:** Ensure bundled fonts support necessary scripts (e.g., Assamese/Bengali script).
- **Audio:** Pre-record static voice prompts in local languages to save API calls and ensure offline availability.

### Storage
- **Media:** Supabase Storage buckets for storing user avatars and custom audio reminders.

### Deployment
- **Frontend (Mobile):** Expo Go for live demo; build APK via EAS Build if time permits.
- **Backend:** Railway or Render (easy FastAPI deployment from GitHub).
- **Database:** Supabase (hosted).

### Environment Variables
```
# Backend (.env)
DATABASE_URL=postgresql://...
SUPABASE_URL=https://...
SUPABASE_SERVICE_KEY=...
OPENAI_API_KEY=sk-...
GEMINI_API_KEY=...

# Frontend (.env)
EXPO_PUBLIC_API_URL=https://our-backend.railway.app
EXPO_PUBLIC_SUPABASE_URL=...
EXPO_PUBLIC_SUPABASE_ANON_KEY=...
```

### Security & Privacy
- **Encryption:** Data in transit encrypted via HTTPS.
- **Data Minimization:** Only store necessary metrics; avoid collecting PII where not strictly required.
- **Access Control:** Row Level Security (RLS) in Supabase to ensure caregivers can only see their linked patients.

### Threat Model & Risks
| Risk | Probability | Impact | Prevention | Backup |
|---|---|---|---|---|
| Backend deployment fails | Medium | High | Test deployment early (Day 1) | Run backend locally via ngrok |
| Whisper API slow/rate-limited | High | Medium | Implement timeout handlers | Fallback to button-only navigation |
| Offline sync conflicts | Low | Medium | Keep data model append-only | Clear local DB and fetch from cloud |
| Expo build fails on Demo day | Medium | High | Test builds early | Run directly via Expo Go app |

### Known Limitations (Hackathon Prototype)
- True real-time adaptive AI might be simplified to rule-based logic (e.g., "if score > 80% 3 times, increase difficulty").
- Voice recognition may struggle with heavy regional accents due to generic STT models.
- iOS support is not tested (focusing on Android for NER demographic).
- Sophisticated conflict resolution for offline sync is simplified.
