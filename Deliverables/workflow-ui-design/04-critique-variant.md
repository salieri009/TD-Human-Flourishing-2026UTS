## Critique Variant — 3 Actors (Student, AI Tool, Tutor)

This operational view separates the roles: the Student critiques, Copilot provides the draft and cues, and the Tutor supervises the session using checkpoints and logs (Exintaris 2023 · SMARTCHEMPer; Singh 2025).

```
        STUDENT                    AI TOOL (COPILOT)                      TUTOR
          │                               │                                  │
          │   "Solve this stoichiometry   │                                  │
          │    problem."                  │                                  │
          ├──────────────────────────────►│                                  │
          │                               │                                  │
          │                               │  [policy active: critique mode]  │
          │                               │◄─────────────────────────────────┤
          │                               │                                  │
          │     CRITIQUE INVITATION       │                                  │
          │  "Here is a draft solution.   │                                  │
          │   It may contain mistakes.    │                                  │
          │   List flaws and missing      │                                  │
          │   steps before I confirm."    │                                  │
          │◄──────────────────────────────┤                                  │
          │                               │                                  │
          │  "Step 2 skipped dilution.    │                                  │
          │   Step 4 has wrong units."    │                                  │
          ├──────────────────────────────►│                                  │
          │                               │                                  │
          │     🟡 MONITORING (Singh 2025)│                                  │
          │  "Good catches - anything     │                                  │
          │   else that doesn't match a   │                                  │
          │   correct solution pattern?"  │                                  │
          │◄──────────────────────────────┤                                  │
          │                               │                                  │
          │                               │  [checkpoint: critique quality]  │
          │                               ├─────────────────────────────────►│
          │                               │                                  │
          │                               │  ... (loop continues through     │
          │                               │      Steps 2-3 + cues)           │
          │                               │                                  │
          ▼                               ▼                                  ▼
```

This variant still inverts the role: instead of *receiving* an explanation, the student *interrogates* one. Exintaris et al. (2023) showed this worked with n=204 pharmacy students. The 3-actor framing adds delivery realism: AI runs the cue loop and critique flow, while the Tutor handles policy and oversight.
