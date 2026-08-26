# 02 — PRODUCT REQUIREMENTS DOCUMENT
## Everything About WHAT We're Building

> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | **02 Product PRD** | [03 AI Strategy](03_AI_DOMAIN_STRATEGY.md) | [04 Tech Architecture](04_TECH_ARCHITECTURE.md) | [05 UX/UI Demo](05_UX_UI_DEMO.md) | [06 Execution & Pitch](06_EXECUTION_PITCH_JUDGING.md) | [07 Evidence & Knowledge](07_EVIDENCE_DECISIONS_KNOWLEDGE.md)

---

### Product Vision
A culturally-rooted, AI-powered cognitive gaming platform that transforms dementia care in India's North Eastern Region through adaptive games, voice-enabled interaction, and intelligent caregiver support.

### One-Sentence Solution
"PROJECT-X is an AI-powered, offline-capable cognitive gaming platform that uses culturally familiar NER themes and adaptive difficulty to improve cognitive engagement for elderly dementia patients while enabling caregivers to monitor progress."

### Value Proposition
For elderly dementia patients in NER who lack access to cognitive therapy, PROJECT-X provides engaging, culturally relevant cognitive games that adapt to their abilities, work offline, and support their native languages — unlike generic brain-training apps that are Western-centric, require constant internet, and ignore the cultural context of NER communities.

### Primary User
**Elderly Patient (60-85+ years) with mild-to-moderate dementia in NER**
- **Profile Details:** Prefers regional language (Assamese, Bengali, Khasi, etc.). Might have physical tremors, poor eyesight, and varying daily cognitive clarity. Familiar with local customs, foods, and festivals. Often overwhelmed by complex UI or small buttons.
- **Pain Points:** Loneliness, frustration at forgetting, rapid cognitive decline, feeling useless, digital illiteracy.

### Secondary User
**Family Caregiver (Adult child or spouse, 30-55 years)**
- **Profile Details:** Busy, stressed, balancing work and caregiving. Might not live in the same house but visits often. Needs peace of mind.
- **Pain Points:** Caregiver burnout, lack of awareness about dementia progression, forgetting to give medication, inability to constantly engage the patient.

### User Journey

#### 1. Elderly Patient Journey
- **First Use:** App opens directly to a large, clear interface welcoming them by name in their native language. A simple, familiar game (e.g., sorting familiar local fruits or matching traditional textile patterns) begins.
- **Daily Engagement:** Voice prompt reminds them to "play a game for 10 minutes". The AI adjusts the difficulty so the patient always achieves a "win" (building confidence) while subtly challenging their memory.
- **Progression:** Over time, the app introduces new cultural themes. If the patient struggles, it seamlessly downgrades difficulty to avoid frustration.

#### 2. Caregiver Journey
- **Setup:** Creates an account, inputs patient details (name, preferred language, stage of dementia, medication schedule), and uploads family photos for familiarization games.
- **Monitoring:** Checks the dashboard on their phone to see "Engagement Score", "Memory Retention Index", and time spent playing.
- **Alerts:** Receives push notifications if the patient misses medication, or if the AI detects a sudden drop in cognitive performance (signaling a potential health issue).

### Core Workflow
1. **App Launch:** Caregiver configures app; sets it to "Patient Mode".
2. **Daily Prompt:** System verbally prompts patient in native language.
3. **Gameplay:** Patient interacts (touch or voice). Game elements reflect NER culture (e.g., Bihu festival themes, Muga silk motifs).
4. **Real-time Adaptation:** AI engine tracks response time and accuracy; adjusts next level's difficulty instantly.
5. **Data Sync:** When online, game data syncs to the cloud.
6. **Caregiver Review:** Caregiver reviews dashboard insights and modifies routines if needed.

### Killer Feature
**AI-Adaptive Cultural Cognitive Games:** Games that use familiar NER cultural elements (Bihu dance sequences, traditional textile patterns like Muga silk motifs, familiar regional foods, local festivals) with an AI engine that continuously adapts difficulty based on real-time cognitive performance metrics.

### Functional Requirements

**Cognitive Games Module**
- Library of culturally themed games (Matching, Sorting, Sequencing).
- Large UI elements, high contrast, tremor-tolerant touch targets.
- Audio feedback in regional languages.

**Adaptive AI Engine**
- Real-time adjustment of difficulty (time limits, number of items, distractor elements).
- Algorithm to calculate "Cognitive Engagement Score".
- Behavioral pattern recognition (detecting frustration vs. engagement).

**Voice & Language Module**
- Multi-lingual support (English, Hindi, Assamese, etc. - MVP: Assamese + English/Hindi).
- Voice commands for simple interactions ("Start", "Yes", "No", "Help").
- Text-to-Speech (TTS) for game instructions and reminders.

**Reminder System**
- Medication, hydration, and activity reminders with visual and audio cues.
- Caregiver setup interface.

**Caregiver Dashboard**
- Real-time analytics of gameplay metrics.
- Trend graphs (weekly/monthly).
- Notification center.

**Progress Tracking**
- Secure storage of session data.
- Exportable reports (PDF) for doctors.

**Offline Support**
- Local database for offline gameplay and data caching.
- Auto-sync when internet is restored.

### Non-Functional Requirements
- **Performance:** Games must load within 2 seconds. Smooth animations (60fps) to prevent motion sickness.
- **Accessibility:** WCAG 2.1 AA compliant. High contrast mode, large fonts, screen reader compatible. Tremor support (debouncing touch inputs).
- **Security:** End-to-end encryption for patient data. HIPAA/local healthcare data compliance.
- **Scalability:** Cloud backend capable of supporting thousands of concurrent users (post-MVP).

### MUST HAVE (MVP)
- [ ] 3-4 core cognitive games (Memory Match, Sequencing, Sorting) themed for NER.
- [ ] Adaptive difficulty engine (Basic ML or rules-based algorithm).
- [ ] Basic voice commands and audio instructions.
- [ ] Language Support: Assamese + Hindi + English.
- [ ] Offline mode (local storage & sync mechanism).
- [ ] Basic caregiver view (dashboard with simple metrics).
- [ ] Reminder system (medications, daily tasks).

### SHOULD HAVE
- [ ] Integration of personal family photos into memory games.
- [ ] More regional languages (Bengali, Khasi, Manipuri).
- [ ] Advanced AI behavioral analysis (frustration detection via touch patterns).
- [ ] SMS/WhatsApp alerts for caregivers.

### NICE TO HAVE
- [ ] Wearable integration (smartwatch for heart rate/stress monitoring).
- [ ] Multi-player mode with other patients or family members.
- [ ] Advanced voice conversation capabilities (LLM integration for chatting).

### CUT
- [ ] **Complex 3D Games:** Rejected due to performance issues on low-end devices and potential to confuse elderly users.
- [ ] **Social Media Sharing:** Rejected due to privacy concerns and irrelevance to the primary user.
- [ ] **Live Video Calling:** Rejected to focus on the core offline-first cognitive gaming experience (MVP scope).

### Feature ROI

| Feature | Dev Cost | Judge Impact | User Impact | Demo Impact | Risk | Decision |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Cultural Theme Games** | Medium | High | High | High | Low | **DO IT** |
| **Adaptive AI Engine** | High | High | High | High | Medium | **DO IT** |
| **Offline Mode** | Medium | High | High | Low | Low | **DO IT** |
| **Assamese Voice TTS** | Medium | High | High | High | Medium | **DO IT** |
| **Family Photo Game** | Medium | Medium | High | High | Low | **SHOULD** |
| **Wearable Integration** | High | Medium | Medium | Medium | High | **CUT (MVP)** |

### MVP Definition
- **What must work (real, functional):** The core UI, at least 2 fully playable games (with cultural themes), the adaptive difficulty logic (even if rules-based for MVP), language switching, offline caching, and the caregiver dashboard displaying real data from the session.
- **What can be mocked (simulated but looks real):** Deep historical data on the dashboard (pre-load mock data to show trends), advanced voice conversation (hardcode specific responses), SMS/WhatsApp notifications (show UI prompt instead).
- **What can be simplified (reduced scope):** The AI engine can start as a smart decision tree/rules engine rather than a complex neural network. Limit languages to 3.

### What Is Real
- 2 playable cognitive games (e.g., Muga silk pattern match, local fruit sorting).
- Adaptive difficulty mechanism.
- Local storage and sync logic.
- Caregiver dashboard UI and basic metrics.
- Multi-language UI toggles.

### What Can Be Mocked
- Long-term trend charts on the dashboard.
- Push notifications to the caregiver phone (simulate via on-screen alerts).
- Voice recognition for complex phrases (limit to simple "yes/no/start").

### What Can Be Simplified
- User authentication (use simple pin or bypass for demo).
- AI model (use heuristics for MVP demo).

### Future Roadmap
**Post-Hackathon Vision (Months 1-6):**
- Expand language support to all 8 NER states.
- Partner with local NGOs and memory clinics for beta testing.
- Implement advanced machine learning for behavioral analysis.
- Add wearable device integration for physical health monitoring.
- Develop a provider portal for doctors to monitor multiple patients.
