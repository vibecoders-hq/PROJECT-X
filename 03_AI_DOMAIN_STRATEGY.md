> **HACKATHON OS NAVIGATION**
> [00 Master State](00_MASTER_STATE.md) | [01 Problem & Research](01_PROBLEM_RESEARCH_COMPETITION.md) | [02 Product PRD](02_PRODUCT_PRD.md) | **03 AI Strategy** | [04 Tech Architecture](04_TECH_ARCHITECTURE.md) | [05 UX/UI Demo](05_UX_UI_DEMO.md) | [06 Execution & Pitch](06_EXECUTION_PITCH_JUDGING.md) | [07 Evidence & Knowledge](07_EVIDENCE_DECISIONS_KNOWLEDGE.md)

# 03 — AI & DOMAIN STRATEGY
## Intelligence Layer — Biology, Cognition & AI Architecture

> [!IMPORTANT]
> This document defines our primary competitive moat. While other teams may build generic games, our solution is rooted in clinical cognitive science, dementia progression realities, and North Eastern Region (NER) cultural resonance. The AI serves to dynamically map these domains.

---

## Biology / Domain Knowledge

### What is Dementia?
Dementia is an umbrella term for loss of memory, language, problem-solving, and other thinking abilities that are severe enough to interfere with daily life. 
**Types:**
- **Alzheimer's Disease:** The most common form (60-80% of cases), characterized by memory loss and cognitive decline.
- **Vascular Dementia:** Linked to strokes or issues with blood supply to the brain, affecting reasoning and judgment.
- **Lewy Body Dementia:** Characterized by abnormal protein deposits in the brain, affecting movement, cognition, and sleep.
- **Frontotemporal Dementia:** Affects the frontal and temporal lobes, primarily impacting personality, behavior, and language.

### Progression Stages
- **Mild (Early Stage):** Individuals may function independently but experience memory lapses (e.g., forgetting familiar words or locations).
- **Moderate (Middle Stage):** The longest stage. Individuals may require more care, experiencing confusion, difficulty recognizing family/friends, and behavioral changes.
- **Severe (Late Stage):** Individuals lose the ability to respond to their environment, carry on a conversation, and, eventually, control movement.

### How Cognitive Stimulation Therapy (CST) Works
CST is an evidence-based intervention for people with mild to moderate dementia. It involves active engagement and stimulation of memory, language, and problem-solving skills through themed activities. It has been shown to improve cognitive function and quality of life.

### Evidence Base for Gaming-Based Cognitive Interventions
Serious games and computerized cognitive training can delay cognitive decline by promoting neuroplasticity. Active engagement requires sustained attention and working memory, which helps build cognitive reserve.

### WHO Guidelines on Cognitive Decline Prevention
The WHO emphasizes cognitive training and physical activity to reduce the risk of cognitive decline and dementia. Social engagement and managing vascular risk factors are also critical components.

### India-Specific Dementia Statistics and NER Context
India has a growing elderly population, with dementia cases expected to triple by 2050. The North Eastern Region (NER) presents unique challenges:
- High prevalence of vascular risk factors.
- Cultural stigma around dementia, often dismissed as "normal aging."
- Language barriers and lower digital literacy among the elderly.
- Geographically dispersed populations with limited access to specialized neurological care.

---

## Cognitive Domains

Detailed breakdown of the cognitive domains our games target and how we address them:

### 1. Memory
- **What it means:** The ability to encode, store, and retrieve information (episodic, semantic, working, procedural).
- **How dementia affects it:** Difficulty recalling recent events, recognizing faces, or remembering instructions.
- **How games can help:** Spaced repetition, associative learning, and visual cues.
- **Game design implications:** Avoid complex, multi-step instructions. Focus on short-term recall and familiar visual stimuli.

### 2. Attention
- **What it means:** The ability to focus on specific stimuli while ignoring others (sustained, selective, divided).
- **How dementia affects it:** Easily distracted, difficulty following conversations or completing tasks.
- **How games can help:** Tasks requiring sustained focus on a single objective.
- **Game design implications:** Clean, uncluttered UI. Visual and auditory highlights on active elements.

### 3. Executive Function
- **What it means:** Higher-level cognitive skills including planning, problem-solving, and mental flexibility.
- **How dementia affects it:** Poor judgment, inability to plan sequences, difficulty adapting to new situations.
- **How games can help:** Simple logic puzzles and categorization tasks.
- **Game design implications:** Start with very simple rules. Avoid sudden rule changes.

### 4. Language
- **What it means:** Comprehension, production, and naming.
- **How dementia affects it:** Struggling to find the right word (aphasia), repeating questions, losing train of thought.
- **How games can help:** Word-picture matching, completing familiar phrases.
- **Game design implications:** Use highly localized, familiar regional terms and proverbs.

### 5. Visuospatial
- **What it means:** Pattern recognition, spatial orientation, and visual perception.
- **How dementia affects it:** Getting lost in familiar places, difficulty judging distances or recognizing objects.
- **How games can help:** Shape matching, spatial arrangement puzzles.
- **Game design implications:** High contrast colors, clear boundaries, avoid abstract shapes.

### 6. Processing Speed
- **What it means:** The time it takes to perform mental tasks.
- **How dementia affects it:** Slowed reaction times and thought processes.
- **How games can help:** Gradually increasing the pace of simple tasks.
- **Game design implications:** Generous time limits. Time pressure should be adaptive and strictly controlled to avoid anxiety.

---

## Cognitive Activity Design

Table mapping cognitive domains to specific game types tailored for the NER cultural context:

| Domain | Game Type | NER Cultural Theme | Difficulty Levels | Metrics Tracked |
| :--- | :--- | :--- | :--- | :--- |
| **Memory** | Sequence Recall | "Festival Recall" — remember sequences of Bihu dance steps | 1-10 (number of steps, speed) | Accuracy, Time to recall |
| **Attention** | Visual Search | "Tea Garden Picker" — identify specific tea leaves among others | 1-10 (distractor density, similarity) | Search time, False positives |
| **Visuospatial** | Pattern Recognition | "Muga Silk Weaver" — complete traditional textile patterns | 1-10 (pattern complexity, missing pieces) | Completion rate, Errors |
| **Language** | Phrase Matching | "Proverb Match" — match NER proverbs to their meanings | 1-10 (vocabulary difficulty, options) | Attempts needed, Accuracy |
| **Executive Function** | Daily Routine Sequencing | "My Day" — reconstruct daily routine from morning to evening | 1-10 (number of events, logical complexity) | Correct sequence placement |
| **Processing Speed** | Quick Sorting | "Market Day" — quickly sort local produce into correct baskets | 1-10 (speed limit, number of items) | Time per item, Error rate |

---

## AI Role

Why AI is essential (not just a buzzword):
- **Adaptive difficulty calibration:** Prevents frustration (too hard) or boredom (too easy).
- **Real-time cognitive performance assessment:** Continuous, unobtrusive monitoring.
- **Personalization based on patient profile:** Tailoring content to their specific cultural background, interests, and current cognitive stage.
- **Anomaly detection:** Sudden cognitive decline alerts for caregivers (e.g., a sharp drop in performance might indicate a UTI or minor stroke).
- **Natural language understanding:** For voice commands in NER languages, lowering the barrier to entry.
- **Predictive analytics:** For caregiver dashboard to forecast potential challenges and suggest interventions.

### Why AI Is Necessary
Fixed-difficulty games cause frustration (too hard) or boredom (too easy) in dementia patients, leading to high abandonment rates. AI enables **real-time calibration** that a static app cannot provide. Each patient's cognitive profile is unique and changes over time, requiring a dynamic system that adapts to their daily fluctuations in capability.

### Adaptive Difficulty Logic

**Algorithm Design:**
- **Input Metrics:** Response time, accuracy, hint usage, completion rate, error patterns (e.g., spatial vs. memory errors).
- **Processing:** Sliding window analysis over the last N sessions. Calculation of a composite cognitive domain score.
- **Output:** Difficulty level (1-10) for the next task within that specific domain, personalized game selection, and recommended session length.
- **Edge Cases:** 
  - *Frustration/Fatigue:* If response time spikes and accuracy plummets, the system immediately drops the difficulty by 2 levels or suggests a break.
  - *Bad Day:* If performance is consistently below baseline across multiple domains, the system shifts to 'comfort mode' (highly familiar, easy tasks) and alerts the caregiver.
- **Safeguards:** 
  - Difficulty never drops too fast (preserves dignity, avoids making the patient feel 'stupid').
  - Difficulty never rises too fast (prevents sudden frustration).

### Performance Metrics

| Metric | What It Measures | Clinical Relevance | How We Track It |
| :--- | :--- | :--- | :--- |
| **Response Time (RT)** | Processing speed | Slowing RT is an early indicator of cognitive decline | Milliseconds from prompt to first action |
| **Accuracy Rate** | Domain-specific competence | Identifies which specific domains are degrading faster | % of correct first attempts |
| **Hint Usage** | Self-awareness & task difficulty | High hint usage indicates the task is at the upper bound of capability | Number of hints requested per session |
| **Abandonment Rate** | Frustration/Fatigue levels | High abandonment correlates with excessive task difficulty or mood disturbances | Session termination before completion |

### AI System Flow

- **AI Inputs:** Touch interactions (speed, accuracy, coordinates), voice input (audio streams), session duration, time of day, historical performance baselines.
- **AI Processing:** 
  - *Real-time:* Lightweight decision trees or reinforcement learning agents (e.g., contextual bandits) for immediate difficulty scaling.
  - *Batch (Post-session):* Statistical anomaly detection comparing current session to historical baseline.
- **AI Outputs:** Next-task difficulty parameter, updated cognitive profile tensor, caregiver summary report, medical anomaly alerts.

---

## AI Implementation Strategy

### Prompt / Agent Strategy (LLM Integration)
For caregiver reports and voice interactions:
- **Caregiver Report Prompt:** "Analyze the following JSON metrics representing a week of gameplay for an elderly dementia patient. Summarize the changes in memory and attention scores. Highlight any sudden declines. Provide 2 actionable, non-medical recommendations for the caregiver to support the patient this week. Keep tone empathetic and clear."
- **Game Narration/Encouragement Prompt:** "Generate a short, encouraging phrase in [Assamese/Hindi/English] for an elderly user who just successfully completed a memory puzzle. Use culturally respectful terms of address."
- [TO BE FILLED - Add more specific prompts as the product evolves]

### Model Choice
- **On-Device Inference (Critical for NER offline capability):** TensorFlow Lite for adaptive difficulty logic and basic pattern recognition.
- **Speech-to-Text:** Whisper (fine-tuned or smaller variants) for transcribing voice commands.
- **Caregiver Analytics:** Cloud-based LLM API (e.g., Gemini/GPT-4o) for generating readable weekly reports from raw metrics.

### Evaluation
- **Accuracy of difficulty adaptation:** Does the patient stay in the "flow state" (measured by sustained engagement without high abandonment)?
- **Response time:** Does the AI adjust within <500ms to avoid UI lag?
- **Patient engagement metrics:** Weekly Active Days, Average Session Length.
- **Caregiver satisfaction:** [TO BE FILLED - Define target NPS or survey metrics for caregivers]

### Failure Handling
- **Network Failure:** Fall back to on-device TFLite models for difficulty adjustment. Offline caching of session data.
- **AI Inference Failure:** Default to the last known comfortable difficulty level (rule-based fallback).
- **Graceful Degradation:** If speech-to-text fails, revert entirely to touch-based UI with visual prompts.

---

## Medical Claim Boundaries

> [!CAUTION]
> **CRITICAL REGULATORY COMPLIANCE**
> We are building a software tool, not a medical device. Our language must strictly adhere to these boundaries to avoid regulatory issues (e.g., CDSCO in India).

- **What we CAN claim:** "Cognitive engagement tool," "cognitive stimulation activity," "caregiver support platform," "tracks gameplay performance."
- **What we CANNOT claim:** "Treatment," "cure," "diagnosis," "medical device," "prevents dementia," "assesses dementia severity."
- **Disclaimers required:** "This application is for recreational and cognitive engagement purposes only. It is not intended to diagnose, treat, cure, or prevent any disease. Always consult a healthcare professional for medical advice."
- **Regulatory considerations:** [TO BE FILLED - Team to verify any state-specific health app guidelines]

---

## Safety Considerations

- **Patient safety during gameplay:** UI must prevent accidental emergency calls or system lockouts.
- **Data privacy (health data sensitivity):** Health-adjacent data (cognitive performance) must be encrypted at rest and in transit. Comply with DPDP Act 2023.
- **Avoiding anxiety/frustration triggers:** No harsh "Game Over" screens, loud buzzer sounds, or aggressive red flashing lights. Use positive reinforcement only.
- **Emergency contact integration:** Caregiver dashboard includes quick-access emergency numbers.
- **Age-appropriate content:** Respectful tone. No "childish" graphics or condescending language.

---

## Cultural / Regional Personalization

> [!NOTE]
> The NER is highly diverse. Localization is not just language translation; it is cultural adaptation.

| State | Language | Cultural Elements | Festivals | Foods | Music/Dance |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Assam** | Assamese, Bodo, Bengali | Tea gardens, Kaziranga, Brahmaputra | Bihu, Majuli Festival | Pitha, Masor Tenga | Bihu dance, Satriya |
| **Meghalaya** | Khasi, Garo, English | Living root bridges, Monoliths | Wangala, Nongkrem | Jadoh, Pumaloi | Shad Suk Mynsiem |
| **Manipur** | Manipuri (Meitei) | Loktak Lake, Sangai | Yaoshang, Lai Haraoba | Eromba, Singju | Manipuri Raas Leela |
| **Mizoram** | Mizo, English | Bamboo hills, Handloom | Chapchar Kut | Bai, Vawksa Rep | Cheraw (Bamboo dance) |
| **Nagaland** | Nagamese, English, Ao, Angami | Hornbill bird, Morungs | Hornbill Festival, Moatsu | Smoked Pork, Bamboo shoot | Naga warrior dances |
| **Tripura** | Bengali, Kokborok | Ujjayanta Palace, Bamboo crafts | Kharchi Puja, Garia Puja | Mui Borok, Chakhwi | Hojagiri |
| **Arunachal Pradesh** | Hindi, English, Monpa, Nyishi | Monasteries, Himalayas | Losar, Ziro Festival | Thukpa, Apong | Lion and Peacock dance |
| **Sikkim** | Nepali, Sikkimese, Lepcha | Kanchenjunga, Orchids | Losoong, Saga Dawa | Momo, Gundruk | Mask dance (Cham) |

---

## Voice / Language Strategy

Elderly users may struggle with touch interfaces due to tremors or arthritis. Voice is a critical accessibility feature.

- **Phase 1 (MVP):** Hindi, English, Assamese (covering a large demographic base in the region).
- **Phase 2:** Manipuri, Mizo, Bengali (Tripura focus).
- **Phase 3:** Naga languages, Khasi, Garo, etc.
- **Voice command design for elderly users:** 
  - High tolerance for pauses and filler words.
  - Keyword spotting rather than full sentence parsing (e.g., listening for "yes", "no", "help", "next").
- **Text-to-Speech (TTS):** Must use natural-sounding, elder-appropriate voices, not robotic or overly fast speech.
- **Speech-to-Text (STT):** Fine-tuning models for regional accents and code-mixing (e.g., Assamese interspersed with English or Hindi).
