[🔙 Home](./00_HOME.md) | [01 Problem & Scope](./01_PROBLEM_SCOPE.md) | [02 Design & UX](./02_DESIGN_UX.md) | [03 Tech Stack](./03_TECH_STACK.md) | [04 Architecture](./04_ARCHITECTURE.md) | [05 Development Plan](./05_DEVELOPMENT_PLAN.md)

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
[TO BE FILLED] based on team composition.

Suggested role distribution:
- **Lead Developer (Frontend + Games):** Focuses on React Native, animations, and game rendering logic.
- **Backend + AI Developer:** Handles Python/FastAPI, AI adaptation logic, offline sync endpoints, and database.
- **UI/UX + Design:** Creates elderly-friendly interfaces, cultural assets, layout styling.
- **Research + Domain + Pitch:** Gathers medical guidelines, manages NER localization, writes the pitch, leads the demo.

### Task Assignments
[TO BE FILLED] after team is known.

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
"Millions of elderly in India's North East suffer from dementia with almost zero access to cognitive therapy. SmritiSetu is an AI-powered cognitive gaming platform that uses culturally familiar themes — Bihu dances, Muga silk patterns, tribal art — to keep their minds active. Our AI adapts every game to each patient's cognitive level, works completely offline, and gives caregivers real-time insights into cognitive health. This isn't just another brain training app — it's a bridge to dignity for NER's forgotten elderly."

#### 60-Second Pitch
"There are over 5 million dementia patients in India, and in the North Eastern Region, specialized care is scarce, compounded by connectivity challenges and cultural disconnects. Traditional brain training apps are too complex, westernized, and require constant internet.
Enter SmritiSetu. We've built an offline-first cognitive therapy platform designed specifically for the NER. Instead of abstract shapes, our patients match Muga silk patterns and Bihu instruments. Our edge-AI monitors reaction times and accuracy, seamlessly adjusting difficulty to keep the patient engaged without frustration. For the family, a caregiver dashboard provides actionable insights into cognitive decline or stability. SmritiSetu brings culturally resonant, AI-driven healthcare directly to the most remote villages, restoring dignity and extending cognitive vitality."

#### Full Pitch
1. **Hook (15s):** Start with a personal story or a stark statistic about dementia care in rural NER.
2. **Problem (30s):** Highlight the gap: no local therapy, western apps fail, zero connectivity.
3. **Insight (15s):** Cultural familiarity is clinically proven to improve engagement in dementia patients.
4. **Solution (30s):** Introduce SmritiSetu: culturally localized games, offline-first, caregiver integrated.
5. **Demo (90s):** Show the patient playing a simple, NER-themed game. Show the AI dynamically lowering difficulty when they struggle. Show the sync to the caregiver app.
6. **Technology (30s):** Highlight the offline sync architecture and the real-time AI adaptation model.
7. **Impact (20s):** Scalability across all 8 NER states and beyond. Measurable cognitive maintenance.
8. **Future (15s):** Integration with clinical trial data, expanding local languages, predictive decline models.
9. **Close (15s):** "SmritiSetu: Bridging the gap in cognitive care. Thank you."

### Slide Plan
| Slide # | Title | Key Message | Visual | Time |
|---|---|---|---|---|
| 1 | Title | SmritiSetu: AI Cognitive Care | Clean logo, tagline | 10s |
| 2 | The Crisis | Dementia in NER is unmanaged | Graph/Map of NER healthcare gap | 20s |
| 3 | The Gap | Existing apps don't work | Screenshots of complex/western apps with red X | 20s |
| 4 | Our Solution | Culturally aware, offline-first | Mockups of patient and caregiver apps | 30s |
| 5 | Demo | See it in action | Live video or high-fidelity GIF | 90s |
| 6 | Technology | Offline AI + Sync | High-level architecture diagram | 30s |
| 7 | AI Edge | Adaptive Difficulty | Graph showing user skill matching game challenge | 20s |
| 8 | Market/Impact| Scalable across all 8 states | Market sizing, rollout phases | 20s |
| 9 | Team & Future| Who we are & what's next | Headshots, brief roadmap timeline | 20s |
| 10 | Conclusion | SmritiSetu brings dignity | Final impactful image of elderly user | 10s |

---

### Judge Questions

1. **"How is this different from Lumosity?"**
   → Lumosity is generalized, westernized, requires internet, and assumes high baseline digital literacy. SmritiSetu is culturally localized for the NER, operates offline, is designed for the specific cognitive constraints of dementia patients, and integrates a caregiver loop.
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
