## Workflow Diagram (paper-grounded)

Use this for a dedicated diagram slide or as the visual inside slide 8.

```
┌────────────────────────────────────────────────────────────────┐
│           Student opens Copilot for Education                  │
└──────────────────────────────┬─────────────────────────────────┘
                               │
                               ▼
        ┌──────────────────────────────────────────────┐
        │   COGNITIVE PROFILE DETECTION                │
        │   (Marín Díaz 2025 — n=1,273)                │
        │   Cluster 0  Moderate Engagement             │
        │   Cluster 1  High Confidence / Low Reflect.  │  ──► strongest scaffold
        │   Cluster 2  High Reflection / Verification  │  ──► lighter touch
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  MODE TOGGLE (top-right of Copilot canvas)   │
        │  ○ Answer    ● Learning  (default in edu     │
        │                          tenants)            │
        └──────────────┬──────────────────┬────────────┘
                       │                  │
              LEARNING MODE          ANSWER MODE
                       │                  │
                       ▼                  ▼
            Student submits          Direct answer
            question                 returned ─────────► END
                       │              (current Copilot)
                       ▼
        ┌──────────────────────────────────────────────┐
        │  BLOOM'S LEVEL CLASSIFIER  (Fan 2025)        │
        │  Creating / Analysing   ──► HIGH friction    │
        │  Applying / Evaluating  ──► MEDIUM friction  │
        │  Remembering / Underst. ──► LOW friction     │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  🟢 ORIENTING CUE   (Singh 2025)             │
        │  "Before we start — think about the          │
        │   qualities you want Copilot's response      │
        │   to have. What would make it useful for     │
        │   your learning?"                            │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  STEP 1 — KNOWLEDGE PROBE                    │
        │  (Physics-STAR · Knowledge Explanation)      │
        │  "Try writing 2 sentences first about what   │
        │   you already know."        [Try First ▶]    │
        └──────────────────────────┬───────────────────┘
                                   │
              ┌────────────────────┴────────────────────┐
              │                                         │
              ▼                                         ▼
   ┌─────────────────────┐              ┌────────────────────────────┐
   │  STANDARD PATH      │              │  CRITIQUE PATH (optional)  │
   │                     │              │  (Exintaris 2023 ·         │
   │  Student writes     │              │   SMARTCHEMPer)            │
   │  attempt            │              │  Copilot shows DRAFT       │
   │                     │              │  answer with possible      │
   │                     │              │  flaws. Student lists      │
   │                     │              │  mistakes / missing logic. │
   └─────────┬───────────┘              └──────────────┬─────────────┘
             │                                         │
             └──────────────────┬──────────────────────┘
                                │
                                ▼
        ┌──────────────────────────────────────────────┐
        │  🟡 MONITORING CUE   (Singh 2025)            │
        │  Triggered AFTER each AI response.           │
        │  "How closely does the response align        │
        │   with what you expected? Did you find       │
        │   anything unexpected?"                      │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  STEP 2 — ERROR ANALYSIS                     │
        │  (Physics-STAR · Error Analysis)             │
        │  If stuck/incorrect → scaffolded hint        │
        │  (NOT the answer):                           │
        │  "Think about the cause first, then the      │
        │   effect. What changes between them?"        │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  🟡 COMPREHENSION CUE   (Singh 2025)         │
        │  Triggered on inactivity / no follow-up.     │
        │  "Is there anything in the response you      │
        │   don't fully understand? If yes, ask a      │
        │   follow-up or check the source."            │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  🟡 BROADENING PERSPECTIVES   (Singh 2025)   │
        │  Triggered on single-viewpoint focus.        │
        │  "What perspectives might you be missing     │
        │   from your current understanding?"          │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  STEP 3 — REVIEW & MASTERY CHECK             │
        │  (Physics-STAR · Review Suggestion)          │
        │  Brief check question.                       │
        │  PASS  ──► proceed to Consolidation          │
        │  FAIL  ──► loop back to Step 1               │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │  🟢 CONSOLIDATION CUE   (Singh 2025)         │
        │  "Write a summary of the main points you     │
        │   have learned about this topic."            │
        └──────────────────────────┬───────────────────┘
                                   │
                                   ▼
        ┌──────────────────────────────────────────────┐
        │             SESSION SUMMARY LOG              │
        │                                              │
        │   Topic:       Photosynthesis                │
        │   Bloom level: Analysing (high friction)     │
        │   Profile:     Cluster 1 (heavy scaffold)    │
        │   Cues fired:  Orient ✓ Monitor ✓ Compr ✓    │
        │                Broaden — Consol ✓            │
        │   STAR loops:  2  (mastery on 2nd review)    │
        │   Hints used:  1                             │
        │   Reflection:  "I learned that light energy  │
        │                drives the conversion of CO₂  │
        │                and water into glucose…"      │
        └──────────────────────────────────────────────┘

  Cue legend:  🟢 = scheduled (start / end)    🟡 = behaviour-triggered
```

**Why this loop and not a one-shot prompt?**
Singh et al. (2025) found cues delivered at *different phases* of search activity produced significantly more topic exploration (p = 0.006) and persistent inquiry (p = 0.047). A single "interrogative prompt" captures only the Orienting phase. The five-cue architecture mirrors the Self-Regulated Learning loop the paper validated.
