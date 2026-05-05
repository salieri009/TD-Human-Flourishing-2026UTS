# Design Deliverable A — Strategy & Rationale
**Project:** Copilot for Education — Learning Mode  
**Audience:** Microsoft Education Team  
**Purpose:** Present the problem, evidence base, and design rationale that justify the Learning Mode proposal.  
**Scope:** Strategic argument and decision framing only. Detailed workflow and UI spec are in Deliverable B.

---

## Executive Summary

Copilot improves academic outputs, but current usage patterns weaken learning. The evidence shows students offload higher-order thinking to AI, leading to better artefacts with no knowledge gains. This deliverable argues for a Learning Mode that adds structured friction, prompts, and reflection to move cognitive work back to the student while keeping access to Answer Mode.

## Problem Statement

AI tools are already embedded in tertiary education. The problem is not adoption; it is how students use them. Fan et al. (2025) found that AI-assisted essays scored higher (Cohen's d = 0.7) but showed no difference in knowledge retention. This is the Performance Paradox: output improves, learning does not.

The mechanism is cognitive offloading. Fan et al. (2025) report that 39.8% of student interactions delegate *Creating* tasks and 30.2% delegate *Analysing* tasks. These are the cognitive acts that build expertise. When AI performs them, students produce better work but do not build the reasoning behind it.

Marin Diaz (2025) identifies three user profiles from 1,273 interactions: Dependent, Moderate, and Critical-Autonomous. Most students trend toward dependence unless the tool forces reflection and self-explanation.

## Human Story (Design Anchor)

Yuna is a second-year IT student with 200+ Copilot sessions. Her work looks strong. When asked to explain her own data model, she cannot. She never built the reasoning; Copilot did. Yuna is not failing. She is hollow. This is the student we are designing for.

## Evidence Snapshot

- Fan et al. (2025) RCT (n=117): higher essay scores, no learning gains.
- Fan et al. (2025): 47% of tasks delegated to AI; highest delegation at Creating (39.8%) and Analysing (30.2%).
- Singh, Guan, and Rieh (2025): metacognitive prompts increase topic exploration (p = 0.006) and persistent inquiry (p = 0.047).
- Exintaris et al. (2023): critique-first prompting improves metacognitive engagement.
- Marin Diaz (2025): three cognitive profiles support adaptive scaffolding.
- Castillo (2024): AI does not reliably improve critical thinking in controlled studies.

## Design Goals

1. Shift cognitive effort back to the student during high-level tasks.
2. Preserve access to direct answers while making Learning Mode the default in education tenants.
3. Make thinking visible through reflection and session logging.
4. Calibrate friction based on user profile and task difficulty.

## Recommendations

**1. Learning Mode / Answer Mode toggle**  
Introduce two explicit modes. Answer Mode remains for quick retrieval. Learning Mode intercepts the question and prompts a student attempt before any answer is given.

**2. Default to interrogative prompting in education tenants**  
Use metacognitive prompts that ask for goals, prior knowledge, and expected qualities of the answer before providing content. This shifts agency without blocking access.

**3. Profile-adaptive scaffolding**  
Use interaction patterns (acceptance rate, follow-up depth, edits) to classify users into three profiles and adjust scaffolding depth accordingly (Marin Diaz 2025).

**4. Reflection logging**  
Provide a short session summary: topic, Bloom level, cues used, attempts, and a learner-written reflection. This turns each interaction into a learning event, not a transaction.

## Risks and Limitations

- Evidence is early-stage and sample sizes are modest; effects may vary by subject.
- Too much friction can reduce adoption, especially under deadline pressure.
- Profile inference can be noisy; defaults must be conservative.
- Reflection logs should be opt-in and scoped to education tenants to avoid privacy pushback.

## Decision Ask

Approve Learning Mode as the default experience in education tenants, with Answer Mode available as an explicit switch. The design is low-risk, uses existing capabilities, and targets the exact point of learning loss.

---

## References

- Fan, Y. et al. (2025). Beware of metacognitive laziness. *British Journal of Educational Technology*, 56(2), 489–530.
- Marin Diaz, G. (2025). Cognitive profiles of university students in the use of generative AI. *Education Sciences*, 15(7), 923.
- Exintaris, B., Karunaratne, N., & Yuriev, E. (2023). Metacognition and critical thinking using ChatGPT-generated responses as prompts for critique. *Journal of Chemical Education*, 100, 2972–2980.
- Castillo, R. (2024). Artificial intelligence and critical thinking: A systematic review. *Journal of Systemics, Cybernetics and Informatics*, 22(7), 109–112.
- Singh, A., Guan, Z., & Rieh, S. Y. (2025). Enhancing Critical Thinking in Generative AI Search with Metacognitive Prompts. *ASIS&T Annual Meeting 2025*.
