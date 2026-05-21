# Path B — FA-Product Sustainability Analysis
## Utilization / Service / Support Phase

Use this reference for any assessment of a **product during its use phase**,
including normal operation, maintenance, and end-of-life transitions.
Follow Steps B1–B6 in order. Ask for missing information at each step before proceeding.

### Contents
- [B1 — Define the Use Case](#b1)
- [B2 — List System Components](#b2)
- [B3 — Build the Interaction Matrix](#b3)
- [B4 — Highlight Sustainability-Critical Interactions](#b4)
- [B5 — Structured Summary](#b5)
- [B6 — Recommended Next Steps](#b6)

---

## Step B1 — Define the Use Case

Ask the user to specify:
- The **product** being assessed (name and brief description).
- The **use case(s)** to analyse. Examples:
  - Normal operation (primary use)
  - Maintenance / servicing
  - Extreme conditions / edge cases
  - Cleaning / storage
- The **User** — identify the person or entity operating the product as the primary supersystem element.
- The **environment of use** (indoor, outdoor, temperature range, humidity, exposure to chemicals, etc.).

> Tip: Start with the normal operation use case. Add maintenance and extreme
> conditions only if the user wants a comprehensive picture.

---

## Step B2 — List System Components

Ask the user to list **all major components** of the product system,
organised into two groups:

**System components** (the product itself):
- Major sub-assemblies and functional units
- Consumables that need periodic replacement (filters, pads, lubricants, etc.)
- Components with moving or contacting surfaces

**Supersystem elements** (context the product operates within):
- People (e.g. user / operator / people interacting with the product)
- Infrastructure (e.g. road, power grid, internet, etc.)
- Environment (air, water, soil, UV radiation)
- Maintenance substances (lubricants, cleaning agents, fuels)
- Any other external elements that interact with the product

---

## Step B3 — Build the Interaction Matrix

For each pair of components (including supersystem elements), identify
the **interactions** that occur during the use case.

Classify each interaction using this taxonomy:

| Interaction Type | Symbol | Description |
|-----------------|--------|-------------|
| Useful Interaction | → (black) | Intentional function; positive contribution |
| Harmful Interaction | → (red) | Unintended negative effect between components |
| Harmful Interaction — sustainability-critical | → (bold red) | Harmful AND has significant environmental impact |
| Potential Wear between components | ⤍ (orange dashed) | Mechanical, chemical, or thermal degradation at interface |
| Potential Wear inside a component | ◻ (highlighted border) | Degradation within a component (fatigue, corrosion, aging) |

For each interaction, record:
- **Carrier** (what exerts the action)
- **Action** (single active verb that describes what is done to the object)
- **Object** (what receives the action, at least one measurable parameter or property of the object has to change or be maintained by the action)
- **Interaction type** (from table above)
- **Sustainability note** (what environmental harm results, if any)

---

## Step B4 — Highlight Sustainability-Critical Interactions

Focus attention on interactions and components where **wear, chemical harm, emissions, or other negative environmental impacts** occur during use.

### Systematic prompts to identify sustainability issues:

**Moving/contacting surfaces** (wear sources):
- Which components physically touch or slide against each other?
- What material is released as wear particles? (metal, rubber, polymer, ceramic)
- What is the aggregate state of the wear product? (usually fine dust or solid)
- Where do the wear particles end up? (landfill, water, air)

**Consumables** (replacement sources):
- What needs to be replaced periodically? (filters, pads, lubricants, seals)
- What happens to the replaced component? (landfill, recycling, hazardous waste?)
- What is its material composition? (metal, polymer, composite, chemical)

**Chemical emissions** (substance releases):
- Are any fluids or gases released during normal operation? (oil, refrigerant, exhaust)
- Do any materials degrade chemically during use? (UV degradation, hydrolysis, oxidation)
- Are any substances leached into the environment? (plasticisers, heavy metals, coatings)

**Energy emissions** (field effects):
- Does the product emit heat, radiation, noise, or electromagnetic fields?
- Are these harmful to the user, bystanders, or environment?

### Severity indicators (use to prioritise):

Rate each sustainability-critical interaction on two dimensions:
- **Frequency**: Continuous / Per use cycle / Periodic / Rare
- **Magnitude**: High (significant mass/energy release) / Medium / Low (trace amounts)

Interactions that are both **continuous** and **high magnitude** are top priorities.

---

## Step B5 — Structured Summary

Present findings in this format:

### High-Wear Components
List components with internal wear (highlighted border in FA model):
- Component name
- Wear mechanism (abrasion, fatigue, corrosion, UV degradation, etc.)
- Waste type released (fine dust, liquid, solid particles)
- State factor (1–5 from Harm Formula)
- Estimated toxicity (supporting / neutral / potentially toxic)

### Sustainability-Critical Interactions
List the most important harmful interactions (bold red arrows):
- Carrier → Object
- Interaction description
- Waste/emission type and state
- Environmental destination (where does it end up?)
- Severity (Continuous/Periodic × High/Medium/Low)

### Priority Issues Table
Present the top 3–5 sustainability issues using the template from SKILL.md,
ranking by: (1) Severity (frequency × magnitude), (2) Difficulty of mitigation,
(3) Strategic importance to the product's value proposition.

Include a one-sentence rationale for each ranked issue.

---

## Step B6 — Recommended Next Steps

### TRIZ-based follow-up tools

- **Cause-Effect Chain Analysis (CECA)**: For each top-ranked sustainability
  issue, trace the chain of causes upstream to find the root problem amenable
  to a TRIZ solution.
- **Nested Function Model**: Build a sub-system FA model for the most critical
  component (e.g., the brake unit, the drive train) to expose internal
  interactions not visible at the system level.
- **Contradiction Analysis**: When improving a sustainability-critical
  interaction creates a performance trade-off (e.g., better brake dust
  containment vs. braking performance), formulate a technical contradiction
  and apply Inventive Principles.
- **Trimming**: Ask whether any high-harm component can be eliminated
  entirely, with its function transferred elsewhere or removed.
- **Substance-Field (Su-Field) Analysis**: Model the most problematic
  interaction as a Su-Field problem and apply standard solutions to
  introduce a protective or corrective substance/field.

### Design / circular economy options

- **Material substitution**: Replace wear-generating materials with
  lower-impact alternatives (e.g., organic brake pads vs. metallic).
- **Repairability design**: Ensure high-wear components are easily
  replaceable to extend product life and keep materials in the
  technical cycle.
- **Lubrication strategy**: Closed-loop lubrication systems or
  biodegradable lubricants where fluid loss is unavoidable.
- **End-of-life routing**: Ensure consumables have a defined recycling
  or safe disposal pathway (not landfill).
- **7R hierarchy**: Apply Rethink → Refuse → Reduce → Repurpose →
  Reuse → Recycle → Rot to identified sustainability hotspots.

---

## Bicycle Use Phase Example (for reference)

### High-Wear Components

| Component        | Wear Mechanism         | Waste Type      | State | Toxicity     |
|------------------|------------------------|-----------------|-------|--------------|
| Rear / Front Tire | Abrasion on road       | Fine rubber dust | 3    | Potentially toxic (microplastics) |
| Drive Unit       | Metal-on-metal sliding | Metal particles  | 1–3  | Neutral       |
| Brake Unit       | Pad abrasion on rim/disc | Fine dust      | 3    | Potentially toxic (metallic/organic compounds) |
| Gear Unit        | Lubricant shear degradation | Liquid loss  | 2    | Neutral–Toxic |
| Seat Unit        | UV / sweat exposure    | Chemical release | 2–3  | Potentially toxic (plasticisers) |

### Sustainability-Critical Interactions

| Interaction                        | Type         | Destination  | Severity     |
|------------------------------------|--------------|--------------|--------------|
| Brake Unit → Road/Environment      | Dust emission | Landfill (road runoff) | Continuous, High |
| Tire Unit → Road/Environment       | Microplastic release | Landfill (road/water) | Continuous, High |
| Seat Unit ← UV/Sweat              | Chemical degradation | Landfill | Periodic, Low–Medium |

### Priority Issues Table

| # | Issue | Severity | Frequency | Magnitude | Mitigation Difficulty |
|---|-------|----------|-----------|-----------|-----------------------|
| 1 | Brake dust emission | High | Continuous | High | Medium — material substitution feasible |
| 2 | Tire microplastic release | High | Continuous | High | Hard — systemic; no drop-in fix |
| 3 | Drive unit lubrication loss | Medium | Periodic | Medium | Low — closed-loop lubrication available |

**Recommended first TRIZ step**: Cause-Effect Chain Analysis on brake dust
generation to find root contradictions amenable to Inventive Principles.
