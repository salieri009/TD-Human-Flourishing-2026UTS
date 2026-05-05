# TD Assignment 3 — Shaping Technologies That Shape Us
**Course:** 95005/95013 Technology and Design  
**Assessment:** Assessment 2 — Group Presentation (7 min) + Briefing Document (350–500 words)  
**Due:** May 8, 2026  
**Audience:** Microsoft Education Team  
**Topic:** How AI tools like Microsoft Copilot affect student cognition, critical thinking, and human flourishing — and what Microsoft should do about it.

---

## Directory Structure

```
Assignment3/
├── Presentation/
│   └── Shaping Technologies that Shape Us.pdf   ← local export, ignored by git
├── Research/
│   └── source PDFs stored locally only; git ignores them
├── Deliverables/
│   ├── briefing-document.md                      ← 470-word draft for submission
│   ├── slide-notes.md                            ← speaker notes + citations per slide
│   └── workflow-ui-design.md                     ← Copilot Learning Mode specs for Canva
└── README.md                                     ← this file
```

---

## Research Papers — Key Findings

| Paper | DOI / Link | Key Stats / Finding |
|-------|------------|---------------------|
| Fan, Y. et al. (2025) | DOI not confirmed in current notes | **47%** of students delegate tasks directly to AI; **Creating** (39.8%) and **Analyzing** (30.2%) are most delegated; RCT n=117 — AI improved essay scores (Cohen's d=0.7) but **zero knowledge gain** |
| Marín Díaz, G. (2025) | https://doi.org/10.3390/educsci15070923 | n=1,273 users; identified **3 cognitive profiles**: Dependent, Moderate, Critical-Autonomous |
| Exintaris, Karunaratne & Yuriev (2023) | https://doi.org/10.1021/acs.jchemed.3c00487 | SMARTCHEMPer study; n=204 pharmacy students; using AI responses as prompts for critique improved metacognitive engagement |
| Castillo, R. (2024) | DOI not confirmed in current notes | AI does **not** significantly enhance critical thinking vs. traditional methods |
| Singh, Guan & Rieh (2025) | DOI not confirmed in current notes | n=40 university students; metacognitive prompts → significantly more topics explored (p=0.006) and greater persistent inquiry (p=0.047) |
| Jiang & Jiang (2024) | DOI not confirmed in current notes | Physics-STAR framework; n=12 students; **100% improvement** in complex information questions vs. general LLM tutoring |
| Li, Nong, Liu & Evans (2025) | arXiv:2507.18949 | Adaptive learning systems using LLM analytics; GPT-4 achieved 87.5% knowledge retention rate |
| Almelweth, H. (2022) | DOI not confirmed in current notes | n=60 female secondary students; AI apps in geography teaching significantly improved higher-order thinking skills (η²=0.940, high effect) |

## Reference Links

Use these links in the presentation and briefing notes instead of tracking PDF files in git.

- Marín Díaz (2025): https://doi.org/10.3390/educsci15070923
- Exintaris, Karunaratne, and Yuriev (2023): https://doi.org/10.1021/acs.jchemed.3c00487
- Li et al. (2025): arXiv:2507.18949

The remaining papers are kept as local source PDFs for reading, but they are ignored by git and not meant to be committed.

---

## Presentation Structure

### Existing 11 Slides (Canva)

| # | Slide | Key Message | Citation to Add |
|---|-------|-------------|-----------------|
| 1 | Title | "Shaping Technologies That Shape Us" | — |
| 2 | AI Is Inevitable | AI adoption in education is accelerating | — |
| 3 | Context | Who uses AI, how often | — |
| 4 | Shift to Cognitive Offloading | Students delegate Higher-Order Thinking to AI | Fan et al. (2025): 47% direct delegation; Creating 39.8%, Analyzing 30.2% |
| 5 | Impact on Human Flourishing | Performance paradox: better outputs, no learning | Fan et al. (2025): d=0.7 essay improvement, zero knowledge gain |
| 6 | Designing AI (divider) | — | — |
| 7 | Interrogative Prompts | AI that asks instead of answers | Exintaris et al. (2023); Singh et al. (2025) |
| 8 | Learning vs Answer Mode | Proposed Copilot feature toggle | Marín Díaz (2025): 3 cognitive profiles |
| 9 | Self-Reflection | Session logging, metacognitive scaffolding | Singh et al. (2025): p=0.047 persistent inquiry |
| 10 | Limitations | Small samples, self-report bias | Castillo (2024) |
| 11 | Thank You | — | — |

### New Slides to Add in Canva

**Slide 4.5 — Human Story (insert between slides 4 and 5)**
> Meet Yuna. She's a second-year IT student. She submits every assignment on time. Her grades are fine. But when her tutor asks her to explain her reasoning — she can't. She used Copilot for everything. Yuna isn't failing. She's hollow.
>
> *This is the Performance Paradox. AI raises the floor — but removes the ceiling.*

**Slide 10.5 — Call to Action (insert before Thank You)**
> Microsoft, you built tools that billions trust. Now build tools that make them think.
>
> **Our ask:**
> 1. Add a Learning Mode / Answer Mode toggle to Copilot
> 2. Default to interrogative prompting in academic contexts
> 3. Log metacognitive reflection sessions
> 4. Adapt to three cognitive profiles (Marín Díaz, 2025)
>
> *The technology to do this already exists inside Copilot. This is a design choice.*

**Slide 12 — References**
> - Fan, Y. et al. (2025). *British Journal of Educational Technology*, 56(2), 489–530.
> - Marín Díaz, G. (2025). *Education Sciences*, 15(7), 923.
> - Exintaris, B., Karunaratne, N., & Yuriev, E. (2023). *J. Chem. Educ.*, 100, 2972–2980.
> - Castillo, R. (2024). *J. Systemics, Cybernetics & Informatics*, 22(7), 109–112.
> - Singh, A., Guan, Z., & Rieh, S. Y. (2025). ASIS&T Annual Meeting 2025.
> - Jiang, Z. & Jiang, M. (2024). ACM CHI. arXiv:2406.10934.

---

## Proposed Feature: Copilot Learning Mode

### Core Concept
A **mode toggle** inside Microsoft Copilot for Education:
- **Answer Mode** (current behaviour): student submits question → Copilot returns complete answer
- **Learning Mode** (proposed): student submits question → Copilot returns interrogative prompt → scaffolded hints → student attempts → metacognitive feedback

### Workflow (for Canva slide)
```
Student opens Copilot for Education
        │
        ▼
[Mode Toggle]  ──────────────────────────┐
LEARNING MODE                       ANSWER MODE
        │                                │
        ▼                                ▼
Student submits question          Direct answer returned
        │                           (current behaviour)
        ▼
Copilot returns INTERROGATIVE PROMPT
  "What do you already know about this?"
  "What approach might you try first?"
        │
        ▼
Student attempts response
        │
   ┌────┴────┐
Correct?    Stuck?
   │            │
   ▼            ▼
Metacognitive   Scaffolded hint
feedback        (not the answer)
"What made         │
your reasoning     ▼
work here?"   Student re-attempts
   │                │
   └────────┬───────┘
            ▼
    Session summary logged
    (topic, time, attempt count,
     reflection score)
```

### UI/UX Design (2-panel Canva slide)

**Left panel — Answer Mode (current Copilot)**
- Background: #F2F2F2
- Label: "ANSWER MODE" (grey tag)
- Input: "Explain photosynthesis for my biology assignment"
- Output box: Full paragraph answer immediately shown
- No friction, no prompting

**Right panel — Learning Mode (proposed)**
- Background: #E8F4E8
- Label: "LEARNING MODE" (green #107C10 tag)
- Input: same question
- Output: "Before I explain — what do you already know about how plants make energy? Try writing 2 sentences."
- [Try First] button (green, Fluent Design)
- [I need a hint] secondary button
- Progress indicator: "Attempt 1/3"

**Toggle bar (top)**
- Microsoft Fluent Design System
- Toggle: ○ Answer Mode  ●  Learning Mode
- Color: #0078D4 (Microsoft Blue) when Learning Mode active

**Color palette:**
- Microsoft Blue: `#0078D4`
- Learning Mode Green: `#107C10`
- Background white: `#FFFFFF`
- Surface grey: `#F2F2F2`
- Text: `#323130`

---

## Rubric Checklist

| Criterion | Status | Notes |
|-----------|--------|-------|
| Persuasive argument to Microsoft | ✅ | Call to Action slide + Briefing Doc |
| Evidence from research | ✅ | 8 papers with specific stats cited |
| Human story / emotional hook | ✅ | "Yuna" slide added |
| Clear design recommendation | ✅ | Learning Mode feature with workflow + UI |
| Feasibility addressed | ✅ | "Technology already exists inside Copilot" |
| Limitations acknowledged | ✅ | Slide 10 + Briefing Doc section |
| References slide | ✅ | Slide 12 added |
| Citations on slides | ✅ | Added to slides 4, 5, 7, 8, 9 |
| 7-minute time limit | ⚠️ | ~13 slides — time each section carefully |
| Briefing Document 350–500 words | ✅ | See Deliverables/briefing-document.md |
