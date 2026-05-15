# RCA+ Method Knowledge

Detailed method rules for `root_conflict_analysis.xml`.

---

## Lookup Map

- For the purpose and background of RCA+, use section 1.
- For definitions of cause types, relationships, and problem categories, use section 2.
- For the 9-step analytical workflow, use section 3.
- For deciding RCA vs. RCA+, use section 4.
- For quality rules, use section 5.

---

## 1. Purpose of RCA+

Root Conflict Analysis (RCA+) was developed by Valeri Souchkov. It combines ideas from Root Cause Analysis, Theory of Constraints, and TRIZ. RCA+ extends classical Root Cause Analysis in two fundamental ways:

1. **Contradictions, not just causes.** Often a cause contributes to both a negative and a positive effect. Simply eliminating the cause would destroy the positive effect. RCA+ identifies these contradiction causes so they can be resolved inventively rather than by brute elimination.

2. **Closer to the problem is better.** Instead of drilling to the deepest root cause, RCA+ targets contradictions that reside as close as possible to the general negative effect. Experience with hundreds of problems shows that solving a contradiction closer to the top problem provides more ideal solutions.

RCA+ is domain-independent and applies equally to technical/engineering systems and business/management systems.

---

## 2. Core Concepts

### Four Problem Categories

RCA+ can analyze four categories of problems:

1. **Negative effect** — something happens that we do not want at all (a failure, defect, damage, loss, complaint).
2. **Insufficient effect** — a desired result is not achieved with the required degree of performance, quality, or completeness.
3. **Excessive effect** — a desired result is achieved but wastes too much of a costly resource.
4. **Ineffective control** — we have the means of control but the process of control is too slow, inaccurate, or unreliable.

### Four Types of Causes

Every cause in an RCA+ diagram is classified as one of four types:

| Tag | Type | Meaning |
|---|---|---|
| **N** | Negative | The cause is entirely negative; we want to eliminate it. Can be factual (verified) or assumptive (unverified). |
| **N+P** | Negative + Positive | The same cause produces both a negative and a positive effect. This is a **contradiction cause** — the core discovery of RCA+. |
| **NC** | Non-Changeable | The cause contributes negatively but cannot be eliminated or modified (beyond our control, e.g. laws of nature, policy, supersystem constraints). |
| **P** | Positive | A positive effect produced by a contradiction cause. Listed for completeness. |

### Cause Formulation

A cause must be stated as one of:

- A **function**: subject + action + object (e.g. "Knife scratches table surface", "Manager delays decisions").
- A **relative parameter value**: property + relative value (e.g. "Temperature is too high", "Marketing budget is too low").
- A **change of a property**: direction + property + relative value (e.g. "Decrease of temperature is too fast").
- A **radical state change**: (e.g. "Ice melts", "Key employee leaves").

Each cause must be a sentence, not a single word. Avoid the question "Why?" — always ask "What causes ...?"

### Factual vs. Assumptive Causes

- **Factual cause**: Verified by data or observation.
- **Assumptive cause**: Hypothetical, requires verification. Mark clearly.

### AND / OR Relationships

- **AND relationship**: Multiple causes are all required together. Removing any single one eliminates the effect.
- **OR relationship**: Causes contribute independently. Each alone can produce the effect.

For specific problems, causes are usually AND-related. For broad failure prevention, causes can be AND or OR.

### Stopping Rules

Stop expanding a branch when you reach:

- A **contradiction cause** (N+P) — the positive effect identifies why the cause exists.
- A **non-changeable cause** (NC) — we cannot influence it.
- A **requirement or demand** that cannot be changed.

### Cause Exploration Categories

**For technical/engineering problems:** time, space, geometry, information, property, supersystem, materials, fields, energy.

**For business/management problems:** people, processes, information, resources, organization, technology, market, regulation, strategy, culture.

---

## 3. The 9 Steps of RCA+

### Step 1 — State the general negative effect

The top-level problem must be a single sentence belonging to one of the four problem categories.

### Step 2 — Find the causes

Ask: "What causes this effect to occur?" Formulate each cause as a function, relative parameter value, change of property, or radical state change. Mark as factual or assumptive.

### Step 3 — Check AND / OR relationships

Check whether each cause alone is sufficient or whether additional AND-related causes exist.

### Step 4 — Classify each cause

For every cause, ask: "Does this cause also produce a positive effect?" Classify as N, N+P, NC, or P.

### Step 5 — Continue the top-down analysis

For each N-type cause, repeat Step 2. Do not expand N+P or NC causes.

### Step 6 — Check AND relationships for new causes

For each newly added cause, repeat Step 3. Continue iteratively until all branches end.

### Step 7 — Create the summary table

Single table with columns: ID | Cause | Type | Positive Effect | Negative Effect.

### Step 8 — Formulate the problems

For N causes: elimination problems. For N+P causes: technical contradiction (TC) and physical contradiction (PC).

### Step 9 — Recommend problems for solving

Prioritized list with rationale. Do not solve — solving uses other TRIZ methods.

---

## 4. RCA vs. RCA+

- If the system is underdeveloped or defective → RCA may be sufficient.
- If the system is mature and improvement is difficult because every change has disadvantages → RCA+ is more suitable.
- Mature products usually have fewer simple root causes and more contradictions.
- A problem caused by an actionable root cause indicates a defect.
- A problem caused by a contradiction cause indicates that a useful design decision also creates harm.

---

## 5. Quality Rules

- Each cause must be a sentence, not a single word.
- Always check for AND-related causes — breadth reveals more solution opportunities.
- Do not skip Step 4 — checking for positive effects is what makes RCA+ more powerful than plain RCA.
- Mark assumptive causes clearly; they require verification.
- Do not continue deeper analysis beyond N+P or NC causes.
- Keep the diagram top-down and readable.
