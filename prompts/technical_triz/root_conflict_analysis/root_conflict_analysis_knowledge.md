# Root Conflict Analysis (RCA+) Knowledge File

This knowledge file contains the complete RCA+ methodology for `root_conflict_analysis.xml`, based on Souchkov's approach. The XML prompt should stay compact; this file holds the extended methodology, definitions, tables, examples, and report structure.

---

## 1. Purpose of RCA+

Root Conflict Analysis (RCA+) was developed by Valeri Souchkov. It combines ideas from Root Cause Analysis, Theory of Constraints, and TRIZ. RCA+ extends classical Root Cause Analysis in two fundamental ways:

1. **Contradictions, not just causes.** Often a cause contributes to both a negative and a positive effect. Simply eliminating the cause would destroy the positive effect. RCA+ identifies these contradiction causes so they can be resolved inventively rather than by brute elimination.

2. **Closer to the problem is better.** Instead of drilling to the deepest root cause, RCA+ targets contradictions that reside as close as possible to the general negative effect. Experience with hundreds of problems shows that solving a contradiction closer to the top problem provides more ideal solutions.

RCA+ is domain-independent and applies equally to technical/engineering systems and business/management systems.

---

## 2. Core Concepts

### Four Problem Categories

1. **Negative effect** — something happens that we do not want at all (a failure, defect, damage, loss, complaint).
2. **Insufficient effect** — a desired result is not achieved with the required degree of performance, quality, or completeness.
3. **Excessive effect** — a desired result is achieved but wastes too much of a costly resource.
4. **Ineffective control** — we have the means of control but the process of control is too slow, inaccurate, or unreliable.

### Four Types of Causes

| Tag | Type | Meaning |
|---|---|---|
| **N** | Negative | The cause is entirely negative; we want to eliminate it. Can be factual (verified) or assumptive (unverified). |
| **N+P** | Negative + Positive | The same cause produces both a negative and a positive effect. This is a **contradiction cause** — the core discovery of RCA+. |
| **NC** | Non-Changeable | The cause contributes negatively but cannot be eliminated or modified (beyond our control). |
| **P** | Positive | A positive effect produced by a contradiction cause. Listed for completeness. |

### Cause Formulation

A cause must be stated as one of:

- A **function**: subject + action + object (e.g. "Knife scratches table surface", "Manager delays decisions").
- A **relative parameter value**: property + relative value (e.g. "Temperature is too high", "Marketing budget is too low").
- A **change of a property**: direction + property + relative value (e.g. "Decrease of temperature is too fast").
- A **radical state change**: (e.g. "Ice melts", "Key employee leaves").

Each cause must be a sentence, not a single word. Avoid "Why?" — always ask "What causes ...?"

### AND / OR Relationships

- **AND**: Multiple causes are all required together. Removing any single one eliminates the effect.
- **OR**: Causes contribute independently. Each alone can produce the effect.

### Stopping Rules

Stop expanding a branch when you reach: an N+P cause, an NC cause, or a requirement that cannot be changed.

### Cause Exploration Categories

**Technical/engineering:** time, space, geometry, information, property, supersystem, materials, fields, energy.

**Business/management:** people, processes, information, resources, organization, technology, market, regulation, strategy, culture.

---

## 3. The 9 Steps of RCA+

**Step 1** — State the general negative effect (single sentence, one of four problem categories).

**Step 2** — Find the causes: "What causes this effect to occur?" Formulate as function, relative parameter value, change of property, or radical state change. Mark as factual or assumptive.

**Step 3** — Check AND / OR relationships. Is this the only cause, or do additional causes act together?

**Step 4** — Classify each cause: N (purely negative), N+P (contradiction cause), NC (non-changeable), P (positive effect of N+P).

**Step 5** — Continue top-down analysis for N-type causes. Stop at N+P, NC, or requirements.

**Step 6** — Check AND relationships for new causes. Continue Steps 5–6 iteratively until all branches end.

**Step 7** — Create summary table: ID | Cause | Type | Positive Effect | Negative Effect.

**Step 8** — Formulate problems. For N: elimination/prevention. For N+P: technical contradiction (TC) and physical contradiction (PC).

**Step 9** — Recommend problems for solving (prioritized list). Do not solve — solving uses other TRIZ methods.

---

## 4. Summary Table Format (Step 7)

| ID | Cause | Type | Positive Effect | Negative Effect |
|---|---|---|---|---|

- **Type**: N, N+P, NC, or P.
- For N+P: fill both Positive and Negative Effect columns.
- For N and NC: leave Positive Effect empty.
- For P: leave Negative Effect empty.

---

## 5. Contradiction Formulation Templates (Step 8)

### Technical Contradiction (TC)

"How to ensure [N+P-cause] to enable [positive effect] but to avoid [negative effect]?"

### Physical Contradiction (PC)

"[N+P-cause] should be present/high/strong to [positive effect] AND should be absent/low/weak to avoid [negative effect]."

### N-type Problem Statement

"How to eliminate / prevent [N-cause]?"

---

## 6. Selection Guidelines (Step 9)

- **AND causes**: solving any one contradiction cause eliminates the entire negative effect.
- **OR causes**: all must be solved to fully prevent the negative effect.
- **Closer to the top** is generally preferred — more ideal solutions.
- **Fewer components** involved → easier to resolve.
- **System-level** causes preferred over supersystem causes (easier to change).
- N-type causes without contradictions can be directly eliminated.

---

## 7. Solution Directions

### For N-type causes

Direct actions: elimination, mitigation, relocation, parameter adjustment, process correction, better measurement, control action, change of operating condition.

### For N+P-type causes (contradictions)

Inventive directions: separation in time, separation in space, separation by condition, separation by scale, separation by system level, dynamic adaptation, segmentation, feedback control, selective activation, local quality, transition to a higher system level, replacement of the harmful mechanism while preserving the useful effect.

### Recommended TRIZ solving methods

- Contradiction Matrix and 40 Inventive Principles (for TC)
- Separation Principles (for PC)
- 76 Standard Solutions and Substance-Field Analysis
- ARIZ
- Function-Oriented Search
- Feature Transfer

---

## 8. Worked Examples

### Technical: Toothbrush Damages Gums

**General negative effect:** "A toothbrush damages gums." (Negative effect)

**Causes (AND-related):** Bristle surface is too hard (N+P: plaque removal), Bristles move over gums (N), Pressure is too strong (N), Surface of gums is too soft (NC).

**Deeper:** Pressure → Bristles contact gums (N) AND Force is too strong (N+P: plaque removal). Bristles contact gums → Distance between teeth and gums is too small (NC). Bristles move over gums → Bristles move over teeth (N+P: all teeth cleaned).

| ID | Cause | Type | Positive Effect | Negative Effect |
|---|---|---|---|---|
| 1 | Bristle surface is too hard | N+P | Plaque is removed | Toothbrush damages gums |
| 2 | Pressure of bristles on gums is too strong | N | — | Toothbrush damages gums |
| 3 | Surface of gums is too soft | NC | — | Toothbrush damages gums |
| 4 | Bristles move over gums | N | — | Toothbrush damages gums |
| 5 | Bristles contact gums | N | — | Pressure on gums is too strong |
| 6 | Force on bristles is too strong | N+P | Plaque is removed | Pressure on gums is too strong |
| 7 | Distance between teeth and gums is too small | NC | — | Bristles contact gums |
| 8 | Bristles move over the teeth | N+P | All teeth are cleaned | Bristles move over gums |

**Recommended:** (1) Bristle hardness N+P — closest to top. (2) Force N+P — eliminates pressure path. (3) Movement N+P — prevents gum contact.

### Business: Sales Volume Is Low

**General negative effect:** "Sales volume is low." (Insufficient effect)

**Causes (mixed AND/OR):** Unexplored market segments (N, OR), Price too high (N+P: revenues, AND), Wrong price perception (N, AND).

**Deeper:** Wrong perception → Customers don't recognize value (N) AND Customers used to cheaper versions (N+P: happy customer). Don't recognize value → Communication too little (N) → Marketing team too small (N+P: cost effective).

| ID | Cause | Type | Positive Effect | Negative Effect |
|---|---|---|---|---|
| 1 | Unexplored market segments | N | — | Sales volume is low |
| 2 | Price of the product is too high | N+P | Higher revenues | Sales volume is low |
| 3 | Wrong perception of the price | N | — | Sales volume is low |
| 4 | Customers do not recognize new value | N | — | Wrong perception of the price |
| 5 | Customers used to much cheaper versions | N+P | Happy customer | Wrong perception of the price |
| 6 | Direct communication with potential buyers is too little | N | — | Customers do not recognize new value |
| 7 | Marketing team is too small | N+P | Cost effective | Direct communication is too little |

**Recommended:** (1) Price N+P — closest. (2) Marketing team N+P. (3) Unexplored segments N — direct elimination.

### Compact: Waste Bin

**General negative effect:** "A public waste bin creates odor problems."

**Contradiction causes:** Opening is large (N+P: easy disposal vs. odor), Emptying frequency is high (N+P: less odor vs. higher costs), Rain protection is present (N+P: dry waste vs. reduced access).

**Inventive directions:** Flap/sensor lid (separation in time), fill-level-dependent emptying (separation by condition), asymmetric hood (separation in space).

---

## 9. Quality Rules

- Each cause must be a sentence, not a single word.
- Always check for AND-related causes — breadth reveals more solution opportunities.
- Do not skip Step 4 — checking for positive effects is what makes RCA+ more powerful than plain RCA.
- Mark assumptive causes clearly; they require verification.
- Do not continue deeper analysis beyond N+P or NC causes.
- Keep the diagram top-down and readable.

---

## 10. Final RCA+ Report Structure

1. Executive Summary
2. System Description and Improvement Objective
3. General Negative Effect and Problem Category
4. RCA+ Diagram (top-down cause-effect structure with AND/OR relationships)
5. Summary Table (ID | Cause | Type | Positive Effect | Negative Effect)
6. Problem Formulations (TC and PC for each N+P cause; elimination problems for N causes)
7. Recommended Problems for Solving (prioritized list with rationale)
8. Assumptions, Open Questions, and Verification Needs
9. Suggested Next Steps (which TRIZ methods to apply)
