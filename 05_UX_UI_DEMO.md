# 05 — UX/UI DESIGN & DEMO
## Experience + Demo — The Visual Bible

> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | [02 Product PRD](02_PRODUCT_PRD.md) | [03 AI Strategy](03_AI_DOMAIN_STRATEGY.md) | [04 Tech Architecture](04_TECH_ARCHITECTURE.md) | **05 UX/UI Demo** | [06 Execution & Pitch](06_EXECUTION_PITCH_JUDGING.md) | [07 Evidence & Knowledge](07_EVIDENCE_DECISIONS_KNOWLEDGE.md)

---

### Design Principles
1. **Simplicity First** — Every screen must be usable by a 75-year-old with cognitive decline
2. **Cultural Warmth** — Use familiar NER visual elements (Bihu, local textiles, familiar landscapes), not clinical/sterile design
3. **Large Everything** — Large text (min 18px), large buttons (min 48x48dp), large icons
4. **High Contrast** — WCAG AAA compliance for elderly vision
5. **Minimal Cognitive Load** — One action per screen, clear visual hierarchy
6. **Forgiving Design** — No penalties, easy undo, confirmation for critical actions
7. **Emotional Safety** — Warm colors, gentle animations, encouraging feedback (never say "wrong", say "let's try again")

### Design Tokens

#### Typography
- **Primary Font**: Noto Sans (excellent support for Assamese, Manipuri, Bengali, and Devanagari scripts)
- **Heading**: 24-32px, Bold (High visibility)
- **Body**: 18-20px, Regular (Easy to read without glasses)
- **Button**: 20px, Semi-bold
- **Line height**: 1.6 (Breathes easily)

#### Colors
Warm, accessible palette deeply rooted in NER aesthetics:
- **Primary**: `#2E7D32` (Forest Green — evokes nature, peace, NER landscapes)
- **Secondary**: `#FF8F00` (Warm Amber — represents warmth, care, morning sun)
- **Background**: `#FFF8E1` (Warm Cream — avoids harsh white glare)
- **Text**: `#212121` (Dark Charcoal — softer than pure black, extremely readable)
- **Success**: `#43A047` (Bright Green)
- **Warning**: `#F57F17` (Orange)
- **Error**: `#D32F2F` (Soft Red)
- **Surface**: `#FFFFFF` (White)

#### Spacing
- **Base unit**: 8px
- **Screen padding**: 24px (Prevents edge-tapping errors)
- **Button padding**: 16px 32px (Creates massive tap targets)
- **Card padding**: 20px
- **Between elements**: 16-24px (Clear separation of interactive elements)

### Components
List of UI components needed:
- **Large Button**: Primary (Green), Secondary (Amber), Game Action (Extra large)
- **Card**: Game Card (with big image), Stat Card, Reminder Card (with clear icon)
- **Navigation**: Bottom tab (3 items max), Simple back button
- **Modal**: Confirmation (Are you sure?), Alert (Time for medicine)
- **Progress indicators**: Circular (for game timer), Bar (for overall progress)
- **Game components**: Timer (visual, not just numbers), Score (stars/flowers), Difficulty indicator
- **Voice input indicator**: Pulsing microphone icon
- **Language selector**: Flag/Region-based big buttons

### React Component Sources
Recommended component libraries:
- **React Native Paper / NativeBase**: For quick, accessible prototyping
- **Custom components**: SVG-based NER-themed game elements (woven patterns, local items)
- **Lottie**: For lightweight, gentle animations (success stars, pulsing mic)

### Component Integration Rules
- Never use standard OS alerts; always use custom accessible modals.
- All touch targets must be wrapped in `TouchableHighlight` or `TouchableOpacity` with at least `hitSlop={{top: 10, bottom: 10, left: 10, right: 10}}`.
- Text components must have `allowFontScaling={true}` but max out at a reasonable multiplier to avoid breaking layout.

### Shared UI/UX Component Selection Strategy
This is a shared selection task separate from primary coding roles. Team members select components from provided asset libraries/sources that fit their section (no coding required from Vikas, Sahil, Soumya, or Yamini):
- **Vikas:** Architecture, analytics & data-related components
- **Sahil:** Landing page, information & impact components
- **Soumya:** Dashboard, impressive visuals & demo components
- **Yamini:** Elderly-friendly UI, accessibility & interaction components
- **Bharat:** Responsible for final integration and consistency of all selected components

**Submission Specification Format for Each Selected Component:**
1. Component Name
2. Screenshot / Visual Example
3. Target Usage Location in Application

### Elderly Mode (Patient Interface)
Design specifications for the patient-facing interface:
- **Home screen**: Large game cards, warm greeting with patient's name ("Namaskar, Kamala"), current time/date (analog clock visual).
- **Game screen**: Full screen, zero distractions. Large interactive elements. Minimal HUD.
- **Reminder screen**: Simple list with large checkboxes. Audio readout button next to each.
- **Settings**: Minimal. Only volume and immediate language toggle. Caregiver manages the rest.
- **Voice mode**: Always available via floating, non-obtrusive button.
- **Feedback**: Haptic feedback on all interactions, pleasant audio chimes.

### Caregiver Mode (Dashboard Interface)
Design specifications for the caregiver dashboard (Mobile/Web):
- **Overview**: Patient status, today's activity completion, critical alerts.
- **Progress charts**: Line graphs for cognitive domains over time (Memory, Attention).
- **Game history**: Session-by-session breakdown, noting where AI adjusted difficulty.
- **Reminder management**: Create/edit reminders (Medicine, Water, Walk).
- **Settings**: Language selection for patient, difficulty preferences, alert thresholds.
- **Reports**: Generate Weekly/Monthly cognitive performance summaries (PDF export).

### Screen-by-Screen Specification
Detailed specification for each screen:

1. **Splash Screen** — App logo (PROJECT-X), warm gradient, auto-detect language based on device settings, quick transition.
2. **Login/Setup** — Large PIN entry pad for patient (4 digits), standard OAuth/email login for caregiver.
3. **Patient Home** — "Good Morning, Kamala". 2 Big Game Cards (Recommended by AI). Today's reminders. Simple mood check-in (3 big smileys).
4. **Game Selection** — Category cards: Memory (Elephants), Attention (Weaving Patterns), Language, Daily Recall.
5. **Game Screen** — Full-screen. Example: Match the Assamese Pitha (rice cakes). Difficulty indicator, visual timer (progress bar).
6. **Game Result** — Encouraging result screen, 3 large stars filling up, applause sound, "Play Again" or "Next Game" buttons.
7. **Reminders** — Today's reminders with visual icons (medicine pill, water glass, clock). Tap to check off.
8. **Caregiver Dashboard** — Multi-patient view (if applicable), cognitive trend charts (smooth curves), missed reminder alerts.
9. **Patient Profile** — Cognitive domain scores (radar chart), game history log, granular settings.
10. **Reports** — Downloadable/shareable cognitive reports for doctors.

### Interaction Design
- **Single tap** for all primary actions. No double taps.
- **Swipe** for navigation (optional, always provide a button alternative).
- **Long press** for help/info (with visual tooltip hinting).
- **No complex gestures** (no pinch-to-zoom required for core loop).
- **Visual and audio feedback** for every interaction (button press state, pleasant click sound).

### Animations
- **Gentle transitions**: 300ms ease-in-out for screen changes. No sudden flashes.
- **Encouraging animations**: On game completion (gentle confetti, blooming local flowers).
- **Subtle loading**: Spinning traditional motif instead of standard spinner.
- **Strict Rule**: No rapid, strobing, or disorienting animations (trigger risk).

### Accessibility
- **Screen reader support**: Full Aria labels/Content descriptions on all elements.
- **Voice navigation**: "Play memory game" voice command support.
- **High contrast mode**: Toggle available in caregiver settings.
- **Adjustable text size**: OS-level dynamic type support.
- **Color blind friendly**: Use textures/patterns in addition to color (e.g., striped green vs solid red).
- **Motor impairment friendly**: Minimum 48x48dp touch targets, spaced out.

---

### Demo Architecture
The demo is structured as a dual-device presentation (or split-screen):
1. **Tablet/Large Phone**: Patient Interface (Elderly Mode).
2. **Laptop/Secondary Phone**: Caregiver Dashboard.
A local network or cloud backend syncs state in real-time to show immediate updates.

### Demo Flow
8-step demo script (Total Time: ~4 mins):
1. **HOOK** (30s) — "Meet Kamala Devi, 72, from Jorhat, Assam. Like 5 million others in India, she struggles with early-stage dementia. Her daughter, Priya, lives in Guwahati and worries daily."
2. **PROBLEM** (20s) — Show the gap in localized, culturally relevant cognitive care in NER. Standard apps feel alien and confusing.
3. **ACTION** (30s) — Kamala opens PROJECT-X. She sees a warm, familiar interface in Assamese. She selects a memory game based on Bihu festival items.
4. **SYSTEM RESPONSE** (30s) — AI detects she is struggling (high latency). The game seamlessly adapts difficulty downwards.
5. **KILLER MOMENT** (40s) — Show the AI adaptation in real-time + Kamala uses Voice Command in Assamese: "Moi aji ki dhoribo lage?" (What should I take today?). App reads out medicine reminder.
6. **PROOF** (30s) — Switch to Caregiver dashboard. Priya sees the real-time alert and the 2-week cognitive trend showing stabilization in Memory.
7. **IMPACT** (20s) — Statistics on potential reach: 8 states in NER, 15+ local languages supported via our localized NLP model.
8. **FUTURE** (20s) — Vision for pan-India rollout with Ayushman Bharat integration.

### Demo Script
Minute-by-minute execution:
- **0:00-0:30**: Intro slides. Set the emotional stakes.
- **0:30-1:00**: Switch to Mirroring. Show Patient Home Screen. Highlight UI simplicity.
- **1:00-2:00**: Play 'Pattern Match' game. Intentionally make mistakes. Watch difficulty drop (show visual indicator).
- **2:00-2:40**: Trigger voice assistant. Ask for reminders. Mark medicine as taken.
- **2:40-3:20**: Open Caregiver Web Dashboard. Show the medicine marked 'done' instantly. Show analytics graph.
- **3:20-4:00**: Conclude with impact and Q&A transition.

### Killer Moment
**The Seamless AI Degradation + Cultural Context:**
When the patient hesitates for >5 seconds on a complex matching task, the app doesn't timeout or show an error. Instead, the screen gently transitions to a simpler version of the same task (e.g., matching 2 items instead of 4), using localized imagery (e.g., matching traditional Assamese Japi hats), accompanied by a gentle voice prompt in the local language.

### Demo Data
Pre-loaded demo data (Crucial for a lived-in feel):
- **Demo patient profiles**: Kamala Devi (Assam, 72), Biren Singh (Manipur, 68).
- **Historical Data**: 14 days of varied game session data showing a slight upward trend in 'Attention' and 'Memory' domains.
- **Reminders**: Past due (Red), Today (Active), Tomorrow.
- **Analytics**: Mocked API responses to ensure instant chart rendering.

### Live Components
What works live during demo:
- UI Navigation and Game Loop.
- Difficulty adaptation logic (runs locally).
- Voice to Text (using device native APIs or mocked fallback).
- Real-time sync between Patient app and Caregiver dashboard (via Firebase/Supabase).

### Mocked Components
What is simulated but looks real:
- Heavy LLM processing (pre-baked responses for specific voice queries to ensure zero latency).
- 2-week historical data generation.
- Doctor report generation (loads a pre-made PDF).

### Backup Screens
- Directory `docs/demo-backups/` contains high-res screenshots of every single step.
- An interactive Figma prototype is pre-loaded on a backup iPad.
- Screen recording of the perfect demo flow saved as `demo_video.mp4` on the desktop.

### Offline Demo Path
How to demo if internet fails:
- The Patient App functions 100% offline (local SQLite + local ML models for difficulty adjustment).
- Caregiver dashboard will be shown using localhost server data.
- Voice commands will gracefully fallback to local keyword matching (if cloud STT fails).

### Demo Failure Scenarios

| Failure | Expected Behavior | Fallback |
| :--- | :--- | :--- |
| **Internet Drops** | Cloud sync pauses, app continues | App uses local storage, show offline indicator |
| **Voice API Fails** | Timeout after 3s | App says "Tap here instead" and highlights button |
| **Mirroring Fails** | Screen goes black | Hold tablet up to camera/judges + play backup video |
| **Dashboard Login Fails** | Auth error | Use hardcoded bypass URL (`/dashboard?demo=true`) |
| **Device Battery Dies** | N/A | Have backup device on desk, unlocked and on the app |
