# 07 — EVIDENCE, DECISIONS & KNOWLEDGE
## The Memory Layer

> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | [02 Product PRD](02_PRODUCT_PRD.md) | [03 AI Strategy](03_AI_DOMAIN_STRATEGY.md) | [04 Tech Architecture](04_TECH_ARCHITECTURE.md) | [05 UX/UI Demo](05_UX_UI_DEMO.md) | [06 Execution & Pitch](06_EXECUTION_PITCH_JUDGING.md) | **07 Evidence & Knowledge**

---

### Decision Log

| # | Date | Decision | Alternatives | Why We Chose | Tradeoff | Reversible? |
|---|---|---|---|---|---|---|
| 1 | 2026-08-24 | Adopted 8-file Hackathon OS structure | Single monolith file, 120+ files | Better for AI agents, clear purpose per file, manageable | Requires initial setup time | Yes |
| 2 | 2026-08-24 | Product name: SmritiSetu | NeuroCare, MindBridge, CogniPlay | Cultural resonance, Hindi+Sanskrit roots, meaningful (Memory Bridge) | May need NER language variant | Yes |
| 3 | | [Future decisions] | | | | |

### Alternative Decisions
*For major decisions, document what we considered and why we rejected them.*
- **Rejected generic UI:** Decided against a standard, modern minimal UI because it lacks the cultural familiarity required by the elderly in the NER region.
- **Rejected Cloud-only ML:** Decided against doing all AI inferences on the cloud because of intermittent connectivity in remote NER areas; opted for on-device/hybrid AI.

### Why We Chose
*Detailed rationale for key decisions.*
- **Local/Hybrid AI for Difficulty Adaptation:** To ensure the core gameplay remains functional without internet, which is critical for the target demographic.
- **Culturally Familiar Themes:** Dementia patients respond better to familiar, nostalgic, and culturally relevant stimuli, which aids memory retrieval and cognitive engagement.

### Tradeoffs
*What we gave up with each decision.*
- **On-device AI:** Gave up complex, parameter-heavy LLMs for lightweight models, sacrificing some nuance for offline reliability.

### Failed Approaches

| # | Attempt | Failure | Cause | Lesson | Replacement |
|---|---|---|---|---|---|
| | [None yet] | | | | |

*Rule: Do not repeatedly attempt the same failed solution without new evidence.*

### Lessons
*Accumulated lessons learned.*
- **Day 1 Lesson:** Ensuring accessibility for elderly patients means larger tap targets, high contrast, and voice-guided interfaces, not just simplified menus.

### User Feedback

| Source | Date | Feedback | Action Taken | Impact |
|---|---|---|---|---|
| | [None yet] | | | |

### Testing Results

| Test | Date | Result | Issues Found | Fixed? |
|---|---|---|---|---|
| | [None yet] | | | |

### Validation Evidence
*Evidence that our approach is correct:*
- **Research studies on cognitive gaming for dementia:** Studies show active cognitive stimulation delays cognitive decline.
- **WHO guidelines on cognitive stimulation:** WHO recommends cognitive stimulation therapy (CST) for individuals with mild to moderate dementia.
- **NER demographic data:** Aging population in NER requires scalable, accessible care solutions.
- **Healthcare access statistics:** Low doctor-to-patient ratio in rural NER makes digital assistance vital.
- **User interviews/feedback:** [TO BE FILLED]

### Impact Metrics

| Metric | Baseline | Current | Target | Source |
|---|---|---|---|---|
| NER elderly population (60+) | ~3.5M | — | — | Census data |
| Dementia prevalence in India | ~5.3M | — | — | ARDSI |
| Cognitive care access in NER | <10% | — | — | Estimated |
| Smartphone penetration in NER | ~45% | — | — | TRAI data |

### Research Sources
*Key research papers and sources:*
1. "Cognitive Stimulation Therapy for Dementia" — Cochrane Review
2. WHO Guidelines on Risk Reduction of Cognitive Decline
3. Alzheimer's & Related Disorders Society of India (ARDSI) reports
4. Census of India — NER demographics
5. TRAI — Digital connectivity in NER
6. [More to be added]

### Important Discoveries
*Significant findings during research.*
- [TO BE FILLED] — Insights from data or domain experts during the hackathon.

### Competitor Discoveries
*What we learned about competitors.*
- Most existing brain training apps (Lumosity, Elevate) are English-first and lack cultural localization for Indian/NER users.
- Most apps require constant internet connectivity and do not integrate a caregiver dashboard.

### Judge Feedback
[TO BE FILLED] — after internal hackathon/practice sessions.

### Internal Hackathon Results
[TO BE FILLED]

#### What Worked
[TO BE FILLED]

#### What Failed
[TO BE FILLED]

#### What We Would Change
[TO BE FILLED]

### PS Re-evaluation
*Periodic re-evaluation of problem statement interpretation:*
- Are we addressing all requirements (a-h)? Yes, tracking via checklist.
- Are we missing anything? Need to ensure NER specific languages are well-supported.
- Has our understanding changed? [TO BE FILLED]

*Problem Statement Requirements Checklist:*
- [ ] a. Interactive cognitive games (memory, attention, daily recall, pattern recognition, emotional engagement)
- [ ] b. AI/ML adaptive difficulty
- [ ] c. Multilingual + voice-assisted for NER elderly
- [ ] d. Culturally familiar themes, visuals, sounds, regional language
- [ ] e. Reminders (medicines, hydration, daily activities, appointments)
- [ ] f. Caregiver/healthcare worker dashboard
- [ ] g. Low-connectivity/offline support
- [ ] h. Mobile/tablet, elderly-friendly interface

### Grand Finale Strategy
[TO BE FILLED] — End-game strategy for maximum impact.

### Reusable Knowledge

#### Winning Patterns
- Cultural personalization wins over generic solutions
- Offline-first architecture impresses for NER context
- Domain depth (cognitive science) > feature breadth
- Real demo with real adaptation > slides about adaptation

#### Losing Patterns
- Generic brain training app clone
- Too many features, none working well
- Ignoring offline requirement
- Western-centric design for NER elderly
- Medical claims without evidence
- Over-engineering AI without clear purpose
