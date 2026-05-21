# Path A — FA-Process Sustainability Analysis
## Production / Realization / Implementation Phase

Use this reference for any assessment of a **manufacturing, assembly, or production process**.
Follow Steps A1–A8 in order. Ask for missing information at each step before proceeding.

### Contents
- [A1 — Process Scoping](#a1)
- [A2 — Sub-Steps and Function Categories](#a2)
- [A3 — Substance Inputs per Sub-Step](#a3)
- [A4 — Losses and Waste Streams](#a4)
- [A5 — Harm Evaluation](#a5)
- [A6 — Aggregate and Normalize Harm](#a6)
- [A7 — Portfolio Analysis](#a7)
- [A8 — Recommended Next Steps](#a8)

---

## Step A1 — Process Scoping

Ask the user to define:
- The **start point** and **end point** of the process being analysed.
- The **main process Steps (Operations)** — typically 3–8 high-level stages
  (e.g., Cutting, Welding, Painting, Assembly).
- The **primary substance input categories** present. Typical categories:
  - Raw Materials
  - Semi-Finished Products
  - Purchased Parts
  - Auxiliary Substances (lubricants, solvents, gases, coolants, etc.)

> Tip: If the user lists more than 10 steps, suggest grouping related
> operations to keep the analysis manageable.

---

## Step A2 — Sub-Steps and Function Categories

For each main Step (Operation), ask the user to list the individual
**Sub-Steps (Functions)** performed. Then assign each sub-step a
**Function Category** and **Function Rank**:

| Category | Label | Rank | Description |
|----------|-------|------|-------------|
| Productive  | P | 5 | Directly contributes to the desired output of the process, changes/effects are visible in the final output of the process |
| Supportive  | S | 4 | Enables productive steps, changes/effects are not visible in the output of the process|
| Transport   | T | 3 | Moves, holds, stores, repositions or redirects materials or information |
| Measure     | M | 2 | Monitors, measures or checks |
| Corrective  | C | 1 | Repairs defects that have been created by previous process Sub-Steps or compensates for problems created during previous Sub-Steps |

**Functionality Score per Step** = sum of all Function Ranks within that Step.

**Normalized Functionality** = (Step's Functionality Score) ÷ (maximum Functionality Score across all Steps) × 100 %

Record these in the Detailed Function Model Table (template in SKILL.md).

---

## Step A3 — Substance Inputs per Sub-Step

For each Sub-Step, ask the user to list **all substance inputs** and classify each into one of the four substance categories:
- Raw Materials
- Semi-Finished Products
- Purchased Parts
- Auxiliary Substances

This establishes what enters each sub-step and therefore what could potentially become waste.

---

## Step A4 — Losses and Waste Streams

For each Sub-Step and each input substance, ask the user to identify all
**outputs that leave the process as waste or loss** (i.e., not incorporated into the desired product or intermediate).

For each loss/waste stream, ask the user to estimate:
- **Amount** as a percentage of the input (0–100 %).

> If Amount = 0 %, no further evaluation needed for that loss stream.
> Move to the next.

Common waste/loss types to prompt for:
- Offcuts, trim waste, reject parts (solids)
- Spent coolants, rinse water, process fluids (liquids)
- Solvent vapours, exhaust gases, fumes (gases)
- Fine dust, mist, spray overspray (fine dust / nebulised)
- Heat, radiation, noise (fields — assess State as 5)

---

## Step A5 — Harm Evaluation

For each loss stream identified in A4, determine the four Harm factors.
Refer to the **Harm Formula** and factor tables in `SKILL.md`.

For each loss stream, ask the user (or estimate with stated assumptions):

1. **Source** of the input substance: Reused / Recycled / Virgin?
2. **Destination** of the waste: Reuse / Recycling / Energy / Landfill?
   → Look up **Cyclicity** from the matrix in SKILL.md.
3. **State** of the waste: Solid / Liquid / Fine dust / Gas / Field?
   → Assign **State** factor (1–5).
4. **Toxicity** of the waste: Supporting / Neutral / Potentially toxic?
   → Assign **Impact** factor (0.5 / 1 / 2).

Calculate: `Harm = (Amount + Cyclicity) × State × Impact`

Record all values in the Detailed Function Model Table.

### Guidance on common ambiguous cases

| Situation | Guidance |
|-----------|----------|
| Waste goes to municipal landfill with no sorting | Destination = Landfill |
| Waste incinerated for district heating | Destination = Energy |
| Metal scrap sold to scrap dealer | Destination = Recycling |
| Solvent recovered and returned to supplier | Destination = Reuse |
| Material composted on-site | Destination = Energy (biological conversion) |
| "We don't know where it goes" | Default to Landfill; note assumption |
| Input is tap water from mains | Source = Virgin |
| Input is recycled process water | Source = Recycled |

---

## Step A6 — Aggregate and Normalize Harm

For each Step:
1. **Sum all Harm values** across all sub-steps and all loss streams within
   that Step → `Sum Harm per Step`
2. **Normalized Harm** = (Step's Sum Harm) ÷ (maximum Sum Harm across all Steps) × 100 %

Add these values to the Summary Portfolio Table (template in SKILL.md).

---

## Step A7 — Portfolio Analysis

Present the Summary Portfolio Table and describe the portfolio diagram:

```
Normalized Functionality %
        ^
   100% |  ●Step B        ← High value, high harm: TOP PRIORITY
        |
    50% |           ●Step A  ← High value, low harm: monitor only
        |
     0% |  ●Step C        ← Low value, high harm: candidate for trimming
        +-------------------------> Normalized Harm %
              0%        50%       100%
```

**Quadrant interpretation:**
- **Upper right** (high functionality, high harm): Most important targets —
  valuable steps with significant environmental impact. Focus innovation here.
- **Upper left** (high functionality, low harm): Performing well; maintain.
- **Lower right** (low functionality, high harm): Strong trimming candidates —
  ask whether this step is necessary at all (7R: Rethink / Refuse).
- **Lower left** (low functionality, low harm): Low priority.

List the top 3 sub-steps by absolute Harm value and explain what drives
each high score (Amount? State? Destination?).

---

## Step A8 — Recommended Next Steps

Based on the portfolio, suggest targeted follow-up actions:

### TRIZ-based options
- **Trimming**: Eliminate high-harm sub-steps entirely if their function can
  be transferred to another component or step.
- **Contradiction Analysis**: If eliminating a sub-step creates a performance
  trade-off (e.g., removing solvent reduces adhesion), formulate a technical
  contradiction and apply TRIZ Inventive Principles.
- **Cause-Effect Chain Analysis**: For the highest-harm loss streams, trace
  root causes upstream in the process.
- **Ideality**: Ask — what would the ideal sub-step look like? (100 % input →
  desired output, zero waste, zero auxiliary substances.)

### Engineering / circular economy options
- Shift **Source** from Virgin to Recycled or Reused (reduces Cyclicity).
- Shift **Destination** from Landfill/Energy to Recycling/Reuse (reduces Cyclicity).
- Substitute high-State waste streams (gas, fine dust) with solid equivalents.
- Substitute potentially toxic materials with neutral or supporting alternatives.
- Apply the **7R hierarchy**: Rethink → Refuse → Reduce → Repurpose →
  Reuse → Recycle → Rot.

---

## Bicycle Production Example (for reference)

| Step                        | Norm. Functionality | Norm. Harm |
|-----------------------------|---------------------|------------|
| Manufacturing Frame/Handlebar |       94 %        |    55 %    |
| Painting                    |       100 %         |   100 %    |
| Manufacturing of Tires      |        59 %         |     0 %    |
| Final Assembly              |        88 %         |     0 %    |

Key findings:
- **Painting** = top priority (upper-right quadrant). Main culprits:
  exhaust gas from burn-in (Harm 992), burnt solvent (Harm 592), cleaning
  agent (Harm 424). All involve virgin inputs going to landfill as toxic
  gases or liquids.
- **Frame/Handlebar** = secondary priority; focus on soldering exhaust gases.
- **Tires and Assembly** = no waste identified; no action needed at this stage.
