> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | [02 Product PRD](02_PRODUCT_PRD.md) | [03 AI Strategy](03_AI_DOMAIN_STRATEGY.md) | [04 Tech Architecture](04_TECH_ARCHITECTURE.md) | [05 UX/UI Demo](05_UX_UI_DEMO.md) | **06 Execution & Pitch** | [07 Evidence & Knowledge](07_EVIDENCE_DECISIONS_KNOWLEDGE.md)

# 06 — EXECUTION, PITCH & JUDGING
## The War Room

### 9-Day Schedule
Assuming a 9-day hackathon timeline.

| Day | Date | Phase | Primary Objective | Deliverables |
|---|---|---|---|---|
| 1 | Aug 24, 2026 | Discovery | Problem research, PS analysis | 01 doc complete |
| 2 | Aug 25, 2026 | Validation | Domain research, competitor analysis | 03 doc complete |
| 3 | Aug 26, 2026 | Architecture | Tech stack, system design | 04 doc complete |
| 4 | Aug 27, 2026 | Core Build | Game engine, adaptive AI | 2 games working |
| 5 | Aug 28, 2026 | Core Build | Voice, reminders, offline | Core features done |
| 6 | Aug 29, 2026 | Integration | Caregiver dashboard, sync | Integration complete |
| 7 | Aug 30, 2026 | Polish | UI polish, demo data, testing | Demo ready |
| 8 | Aug 31, 2026 | Demo + Pitch | Demo rehearsal, pitch prep | Pitch ready |
| 9 | Sep 01, 2026 | Final Lock | Final testing, submission | Submitted |

### Daily Objectives
- **Day 1:** Break down the MDoNER PS. Set up repositories. Define personas.
- **Day 2:** Finalize technology choices. Sketch UI flows. Research NER cultural elements.
- **Day 3:** Establish backend API contracts, database schemas, and AI evaluation logic.
- **Day 4:** Develop initial React Native game engine and the baseline adaptive difficulty AI model.
- **Day 5:** Add voice capabilities (Hindi/English) and robust local storage / offline caching.
- **Day 6:** Complete the caregiver dashboard interface and hook up real-time (and offline) sync.
- **Day 7:** Add styling, animations, error boundaries, and generate realistic demo data.
- **Day 8:** Record demo videos, finalize pitch deck, practice pacing.
- **Day 9:** Code freeze. Execute final QA, deploy to staging, submit required forms.

### Team Responsibilities

#### 1. Vikas — Official Team Leader + Architecture & Planning
- **Core Responsibilities:**
  - Coordinate the team and track overall project progress.
  - Keep everyone aligned with deadlines and tasks.
  - Plan how different parts of the project connect.
  - Break the project into manageable modules/tasks.
  - Maintain the overall project/technical plan with Bharat.
  - Identify dependencies or problems early.
  - Coordinate testing and final integration.
  - Communicate with organizers when required.
- **Component Selection Ownership:** Architecture, analytics & data-related components.
- **Presentation Segment:** Team introduction + overall system & architecture overview.

#### 2. Sahil — Research & User Impact
- **Core Responsibilities:**
  - Problem and domain research.
  - Understand user pain points and requirements.
  - Research existing solutions and competitors.
  - Collect useful evidence, statistics, and clinical research.
  - Help with testing and feedback collection.
  - Identify what users actually need.
- **Component Selection Ownership:** Landing page, information & impact components.
- **Presentation Segment:** Problem + target users + why our solution matters.

#### 3. Soumya — Demo & Presentation
- **Core Responsibilities:**
  - Structure and practice the pitch presentation.
  - Own the main live demo flow.
  - Prepare answers for possible judge questions.
  - Help explain the product simply and convincingly.
  - Maintain a smooth backup demo (video/screenshots).
  - Review overall presentation and demo quality.
- **Component Selection Ownership:** Dashboard, impressive visuals & demo components.
- **Presentation Segment:** Killer feature + live demo execution.

#### 4. Yamini — UX/UI & Product Experience
- **Core Responsibilities:**
  - Review overall UI/UX quality and consistency.
  - Focus on elderly-friendly design and accessibility (contrast, typography, tap targets).
  - Check whether screens are simple and understandable for dementia patients.
  - Review final UI and suggest actionable improvements.
  - Help refine presentation visuals and slide design.
- **Component Selection Ownership:** Elderly-friendly UI, accessibility & interaction components.
- **Presentation Segment:** Elderly user experience + accessibility.

#### 5. Bharat — Technical & Product Lead
- **Core Responsibilities:**
  - Lead overall product decisions.
  - Main development and vibe coding execution.
  - AI and technical implementation (adaptive logic, backend integration).
  - Integrate the different parts of the project.
  - Integrate selected UI components.
  - Debug and fix major technical issues.
  - Ensure the final product actually works reliably.
  - Lead final technical and demo preparation.
- **Component Selection Ownership:** Responsible for final integration and consistency of selected components.
- **Presentation Segment:** Technology + AI + how the system works.

### Presentation Flow
1. **Vikas** → Team Introduction & Overall System/Architecture
2. **Sahil** → Problem, Users & Why Our Solution Matters
3. **Soumya** → Killer Feature & Live Demo
4. **Yamini** → UX/UI, Elderly Experience & Accessibility
5. **Bharat** → Technology, AI & How System Works

### Task Assignments Matrix
| Task / Module | Primary Owner | Secondary / Support |
|---|---|---|
| Project Coordination & Trackers | Vikas | Bharat |
| Domain Research & Evidence | Sahil | Vikas |
| User Experience & Accessibility Review | Yamini | Soumya |
| Pitch Structuring & Demo Rehearsal | Soumya | Vikas |
| Core Development & AI Integration | Bharat | Vikas |
| UI Component Selection (Architecture/Data) | Vikas | Bharat |
| UI Component Selection (Landing/Impact) | Sahil | Yamini |
| UI Component Selection (Dashboard/Visuals) | Soumya | Yamini |
| UI Component Selection (Elderly UI/Accessibility) | Yamini | Sahil |
| UI Component Integration & Bug Fixes | Bharat | Vikas |

### P0 / P1 / P2 / P3 / P4
Current priority matrix:

**P0 — CRITICAL (Demo will fail without these)**
- [ ] Core game engine with 2-3 games
- [ ] Adaptive difficulty (basic version)
- [ ] Elderly-friendly UI
- [ ] Basic offline support

**P1 — WINNING (Directly increases judging score)**
- [ ] Voice commands (at least Hindi/English)
- [ ] Cultural NER themes in games
- [ ] Caregiver dashboard with charts
- [ ] Reminder system

**P2 — IMPORTANT (Improves quality)**
- [ ] Assamese language support
- [ ] Cognitive performance reports
- [ ] Multiple game categories
- [ ] Smooth animations

**P3 — POLISH**
- [ ] Additional NER languages
- [ ] Social features
- [ ] Data export
- [ ] Achievement system

**P4 — DISTRACTION (Do NOT build)**
- [ ] Video calling
- [ ] AR/VR features
- [ ] Complex social network
- [ ] Marketplace

### Build Log
Template for tracking progress:

#### [DATE] [TIME]
**Completed:** [WHAT]
**Learned:** [WHAT]
**Problem:** [WHAT]
**Decision:** [WHAT]
**Next:** [WHAT]

---

### Testing Plan
- **Unit tests for AI adaptation logic:** Ensure difficulty scales correctly based on simulated win/loss streaks.
- **Integration tests for offline sync:** Verify that PouchDB/SQLite merges local states smoothly upon reconnect.
- **UI tests for elderly usability:** Check touch target sizes, contrast ratios, and screen reader compatibility.
- **Demo dry runs:** Scripted walk-throughs of the user journey with a timer.
- **Stress test:** What breaks when network is spotty? What happens if an API key is revoked?

### Validation Plan
- **Test with actual elderly person if possible:** Gather organic feedback on UI/UX.
- **Caregiver feedback:** Ask a nurse or caregiver to evaluate the dashboard utility.
- **Cultural appropriateness review:** Verify that NER themes (Bihu, Muga silk) are used respectfully and accurately.
- **Accessibility audit:** Run automated color contrast and font-scaling checks.

---

### Pitch

#### 30-Second Pitch
"Millions of elderly in India's North East suffer from dementia with almost zero access to cognitive therapy. PROJECT-X is an AI-powered cognitive gaming platform that uses culturally familiar themes — Bihu dances, Muga silk patterns, tribal art — to keep their minds active. Our AI adapts every game to each patient's cognitive level, works completely offline, and gives caregivers real-time insights into cognitive health. This isn't just another brain training app — it's a bridge to dignity for NER's forgotten elderly."

#### 60-Second Pitch
"There are over 5 million dementia patients in India, and in the North Eastern Region, specialized care is scarce, compounded by connectivity challenges and cultural disconnects. Traditional brain training apps are too complex, westernized, and require constant internet.
Enter PROJECT-X. We've built an offline-first cognitive therapy platform designed specifically for the NER. Instead of abstract shapes, our patients match Muga silk patterns and Bihu instruments. Our edge-AI monitors reaction times and accuracy, seamlessly adjusting difficulty to keep the patient engaged without frustration. For the family, a caregiver dashboard provides actionable insights into cognitive decline or stability. PROJECT-X brings culturally resonant, AI-driven healthcare directly to the most remote villages, restoring dignity and extending cognitive vitality."

#### Full Pitch Segment Breakdown
1. **Introduction & System Vision (Vikas - 15s):** Welcome judges, present team & overall architecture vision.
2. **Problem & User Impact (Sahil - 45s):** Highlight the rural NER healthcare gap, user pain points, and current solution failures.
3. **Killer Feature & Live Demo (Soumya - 90s):** Showcase the core NER-themed cognitive games, real-time adaptation, and live caregiver sync.
4. **UX & Elderly Accessibility (Yamini - 30s):** Explain elderly-focused design principles, high contrast, large touch targets, and voice interaction.
5. **Technology, AI Engine & Future (Bharat - 45s):** Detail the offline-first SQLite sync, AI adaptive difficulty logic, system reliability, and future roadmap.

### Slide Plan
| Slide # | Title | Speaker | Key Message | Visual | Time |
|---|---|---|---|---|---|
| 1 | Team & Vision | **Vikas** | PROJECT-X: AI Cognitive Care for NER | Clean logo, team intro | 10s |
| 2 | System Overview | **Vikas** | High-level system architecture & modules | Architecture diagram | 15s |
| 3 | The Crisis & Gap | **Sahil** | Dementia care gap & why generic apps fail in NER | Graph/Map of NER healthcare gap | 25s |
| 4 | User Impact | **Sahil** | Empowering elderly patients & stressed caregivers | User personas & pain points | 20s |
| 5 | Killer Feature & Demo | **Soumya** | Culturally immersive cognitive games in action | Live screen mirror / demo | 90s |
| 6 | Elderly UX & Accessibility | **Yamini** | Zero-friction UI for 75+ seniors with dementia | Screen specs, typography & touch targets | 30s |
| 7 | AI Adaptive Engine | **Bharat** | Dynamic difficulty scaling based on reaction & accuracy | Skill vs challenge adaptation curve | 25s |
| 8 | Tech Stack & Offline Sync | **Bharat** | Local-first SQLite + FastAPI + Supabase backend | System data flow & sync queue | 20s |
| 9 | Conclusion | **All** | Restoring dignity to NER's elderly population | Final impactful visual & Q&A transition | 10s |

---

### Judge Questions

1. **"How is this different from Lumosity?"**
   → Lumosity is generalized, westernized, requires internet, and assumes high baseline digital literacy. PROJECT-X is culturally localized for the NER, operates offline, is designed for the specific cognitive constraints of dementia patients, and integrates a caregiver loop.
2. **"Does this actually help dementia?"**
   → While not a cure, cognitive stimulation therapy (CST) is clinically proven to slow cognitive decline. By keeping patients engaged through familiar cultural elements and adaptive AI, we maximize the benefits of CST.
3. **"How do you handle offline?"**
   → We use a local-first architecture (SQLite/PouchDB) that stores game logic and patient analytics locally. Background workers sync this data to the cloud only when connectivity is detected.
4. **"What about data privacy for elderly patients?"**
   → We adhere to HIPAA-inspired guidelines and the Digital Personal Data Protection (DPDP) Act. All patient data is anonymized, end-to-end encrypted, and caregivers access it via secure, role-based authentication.
5. **"How scalable is this?"**
   → Highly scalable. The core engine is modular. Translating to new languages or adding new cultural asset packs (e.g., from Assamese to Mizo) takes minimal effort without changing the underlying architecture.
6. **"Why NER specifically?"**
   → The MDoNER problem statement requires it, but strategically, NER represents a high-need area with unique cultural diversity and connectivity challenges. Solving for NER proves our offline-first, highly-localized model works anywhere.
7. **"What's the AI doing that's non-trivial?"**
   → It's not just checking right/wrong. It analyzes reaction times, touch precision, and streak patterns to classify cognitive fatigue versus task difficulty, adjusting variables (speed, visual clutter) in real-time.
8. **"How did you validate this?"**
   → We consulted with [mock/real name] healthcare professionals and applied UX guidelines specific to gerontology (large targets, high contrast, non-punitive feedback).
9. **"What happens when the AI is wrong?"**
   → We err on the side of making it easier. The primary goal is engagement, not rigorous testing. The caregiver can also manually override difficulty settings via the dashboard.
10. **"Can this work without internet?"**
   → Yes, 100%. The AI models (decision trees/heuristics) are small enough to run on-device. The internet is only needed to push analytics to the caregiver.

---

### Judge Simulation

#### Technical Judge
- **Focus:** Offline architecture, AI implementation, code cleanliness.
- **Likely Score:** 8/10
- **Weaknesses to address:** Ensure we can clearly explain our conflict resolution for offline data sync and the specific algorithms used for difficulty adaptation.

#### Business Judge
- **Focus:** Scalability, go-to-market strategy, cost of operation.
- **Likely Score:** 7/10
- **Weaknesses to address:** Need to clarify how we onboard users (B2B via clinics vs. B2C) and the cost of maintaining localized asset packs.

#### Domain Judge (MDoNER Rep)
- **Focus:** Relevance to NER, cultural accuracy, real-world feasibility in remote areas.
- **Likely Score:** 9/10
- **Weaknesses to address:** Must ensure the NER cultural references are authentic and not stereotyped. Emphasize the offline capability.

#### Skeptical Judge
- **Focus:** Why bother with an app? "Old people don't use smartphones."
- **Likely Score:** 6/10
- **Weaknesses to address:** Have a strong defense ready: Smartphone penetration in rural India is skyrocketing, and the app is often facilitated by a younger caregiver (multi-generational households).

---

### Red Team
8 attacks on our project with answers:

1. **NOVELTY — "This is just Lumosity for old people"**
   *Answer:* It's targeted therapy. Lumosity doesn't track dementia-specific decline markers or integrate with a caregiver's offline environment in rural India.
2. **TECHNICAL — "The AI is just if-else statements"**
   *Answer:* Even deterministic AI (heuristics) is highly effective here, but we also utilize dynamic time warping on reaction speeds to predict fatigue, which goes beyond simple thresholds.
3. **BUSINESS — "Elderly dementia patients won't use apps"**
   *Answer:* They won't use *complex* apps. Our UI is a zero-learning-curve interface (tap the big picture). Furthermore, the caregiver initiates the session.
4. **COMPETITION — "Google could build this in a week"**
   *Answer:* Google focuses on mass-market global tools. The hyper-localization required for NER cultural therapy is a niche that requires dedicated, localized focus.
5. **AI — "Why does this need AI?"**
   *Answer:* Dementia patients have highly fluctuating "good" and "bad" days. Static difficulty leads to frustration and abandonment. Real-time adaptation is critical.
6. **SCALE — "NER is a tiny market"**
   *Answer:* NER is the proving ground. The architectural model (offline-first, hyper-localized) scales to rural populations globally.
7. **FAILURE — "What if the AI gives wrong difficulty?"**
   *Answer:* The system is designed to "fail soft" — it gracefully lowers the difficulty if it detects repeated failures to prevent patient distress.
8. **IMPACT — "How do you prove cognitive improvement?"**
   *Answer:* We don't claim to reverse dementia. We track engagement time and baseline stability. Success is defined by sustained daily engagement and slowed rate of decline.

---

### Final Win Score
| Category | Max Score | Our Target | Notes |
|---|---|---|---|
| Innovation | 20 | 18 | Hyper-localization + AI adaptation |
| Technical Execution | 30 | 28 | Flawless offline sync is key |
| Impact/Relevance | 25 | 24 | Directly addresses the PS |
| UI/UX | 15 | 14 | Elderly-friendly design |
| Presentation | 10 | 9 | Strong pitch delivery |
| **TOTAL** | **100** | **93** | |

---

### Submission Checklist
- [ ] Source code pushed to main repository (clean history).
- [ ] README.md finalized with setup instructions and architecture diagram.
- [ ] Pitch deck exported to PDF.
- [ ] Demo video (max 3 minutes) uploaded and linked.
- [ ] All team members registered on the submission portal.
- [ ] Final APK/Web URL tested on a fresh device/incognito window.
- [ ] MDoNER specific requirements (PS ID, tags) verified.

### Final 3-Hour Protocol
- **T-Minus 3:00:** CODE FREEZE. No new features. Only P0 bug fixes.
- **T-Minus 2:30:** Record the final demo video. (Do not wait!)
- **T-Minus 1:30:** Finalize and proofread the pitch deck and README.
- **T-Minus 1:00:** Deploy the final build. Run the acceptance test script.
- **T-Minus 0:30:** Submit everything. Do not wait for the last minute.

### Final 60-Minute Protocol
- **Minutes 1-15:** Upload demo video to YouTube/Drive (ensure permissions are public).
- **Minutes 15-30:** Compile all links (repo, video, deck, live demo) into a single document.
- **Minutes 30-45:** Submit on the platform. Verify all uploads.
- **Minutes 45-60:** Relax, hydrate, and prepare mentally for the live Q&A.
