## Student ↔ Teacher Communication Diagram (2-actor sequence)

**Why this view matters.** The Learning Mode workflow is, at its core, a *teacher* dialogue. Copilot is simply the **scaled substitute for the Teacher role** — every cue and step replicates what a skilled tutor naturally does. Reducing the diagram to two actors (Student, Teacher) makes the pedagogical authenticity visible and reframes the design from "AI feature" to "teacher pattern, delivered at scale".

> Read the right column as either *human teacher* or *Copilot Learning Mode* — the dialogue is identical. That equivalence is the design's claim.

```
        STUDENT                                              TEACHER
          │                                                     │
          │   "Explain photosynthesis for                       │
          │    my biology assignment."                          │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │                       🟢 ORIENTING       (Singh 2025)│
          │   "Before I answer — what qualities do              │
          │    you want this explanation to have?               │
          │    What would make it useful for you?"              │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "Clear, with the chemistry, not                   │
          │    just an analogy."                                │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │              STEP 1 · KNOWLEDGE PROBE   (Jiang 2024) │
          │   "Good. Try first — write 2 sentences              │
          │    on what you already know about how               │
          │    plants make energy."                             │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "Plants eat sunlight and use it                   │
          │    to make food."                                   │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │                      🟡 MONITORING       (Singh 2025)│
          │   "Hmm — is *eat* the right word?                   │
          │    What's actually being absorbed,                  │
          │    and what is it absorbed by?"                     │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "Light energy? By chlorophyll?"                   │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │              STEP 2 · ERROR ANALYSIS    (Jiang 2024) │
          │   "Yes — and what does the plant DO                 │
          │    with that absorbed energy? Think                 │
          │    about cause first, then effect."                 │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "It converts CO₂ and water into                   │
          │    glucose."                                        │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │                  🟡 COMPREHENSION        (Singh 2025)│
          │   "Anything in your own answer you're               │
          │    not fully sure about?"                           │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "Why does it have to happen in                    │
          │    chloroplasts specifically?"                      │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │       🟡 BROADENING PERSPECTIVES        (Singh 2025) │
          │   "Good question. What if we looked                 │
          │    at this from the plant's *energy                 │
          │    budget* angle instead of structure?"             │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │           STEP 3 · REVIEW & MASTERY     (Jiang 2024) │
          │   "Quick check: which step actually                 │
          │    requires sunlight — light reactions              │
          │    or the Calvin cycle?"                            │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   "The light reactions."                            │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │                  🟢 CONSOLIDATION        (Singh 2025)│
          │   "Excellent. Now write me a 2–3                    │
          │    sentence summary of what you                     │
          │    just figured out."                               │
          │◄────────────────────────────────────────────────────┤
          │                                                     │
          │   [writes reflective summary]                       │
          ├────────────────────────────────────────────────────►│
          │                                                     │
          │                       ✓ MASTERY ACHIEVED            │
          │                       Session log written.          │
          │                                                     │
          ▼                                                     ▼
```

**The equivalence claim (for the slide).**

| What a good teacher does | What Copilot Learning Mode does |
|---|---|
| Asks what you want from the explanation before giving one | 🟢 Orienting cue (Singh 2025) |
| Makes you try first with what you already know | Step 1 · Knowledge Probe (Jiang 2024) |
| Catches loose wording — "is *eat* the right word?" | 🟡 Monitoring cue (Singh 2025) |
| Re-routes you toward the cause before the effect | Step 2 · Error Analysis (Jiang 2024) |
| Checks: "anything you're unsure of?" | 🟡 Comprehension cue (Singh 2025) |
| Reframes when you're stuck on one angle | 🟡 Broadening Perspectives (Singh 2025) |
| Quick mastery check before moving on | Step 3 · Review (Jiang 2024) |
| "Now tell me what you learned, in your own words" | 🟢 Consolidation cue (Singh 2025) |

The right column is the design specification for the AI. The left column is the *evidence base* for why that specification exists — every cue is a teacher behaviour first, an AI behaviour second.
