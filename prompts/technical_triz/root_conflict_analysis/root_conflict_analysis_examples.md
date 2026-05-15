# RCA+ Examples

Worked examples for `root_conflict_analysis.xml`.

---

## Lookup Map

- For a technical/engineering example, use section 1 (toothbrush).
- For a business/management example, use section 2 (sales).
- For a compact example with solution directions, use section 3 (waste bin).

---

## 1. Technical Example: Toothbrush Damages Gums

### General negative effect

"A toothbrush damages gums."

Problem category: Negative effect.

### Cause-effect analysis

**First level causes (AND-related):**

- Bristle surface is too hard (N+P: also removes plaque)
- Bristles move over gums (N)
- Pressure of bristles on gums is too strong (N)
- Surface of gums is too soft (NC)

**Deeper analysis of "Pressure of bristles on gums is too strong" (AND-related):**

- Bristles contact gums (N)
- Force on bristles is too strong (N+P: also removes plaque)

**Deeper analysis of "Bristles contact gums":**

- Distance between teeth and gums is too small (NC)

**Deeper analysis of "Bristles move over gums":**

- Bristles move over the teeth (N+P: all teeth are cleaned)

### Summary table

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

### Recommended problems to solve

1. **Bristle surface is too hard (N+P)** — TC: "How to ensure bristle hardness to remove plaque but avoid gum damage?" PC: "Bristles should be hard to remove plaque AND soft to avoid gum damage." Closest to the top problem; high impact.

2. **Force on bristles is too strong (N+P)** — TC: "How to ensure strong force to remove plaque but avoid excessive pressure on gums?" PC: "Force should be strong to remove plaque AND weak to avoid pressure on gums."

3. **Bristles move over the teeth (N+P)** — TC: "How to ensure bristles move over teeth to clean all teeth but avoid movement over gums?" PC: "Bristles should move over the entire area to clean all teeth AND should not move over gums to avoid damage."

---

## 2. Business Example: Sales Volume Is Low

### General negative effect

"Sales volume is low."

Problem category: Insufficient effect.

### Cause-effect analysis

**First level causes (mixed AND/OR):**

- Unexplored market segments (N, OR-related)
- Price of the product is too high (N+P: higher revenues) — AND-related with next cause
- Wrong perception of the price (N) — AND-related with previous cause

**Deeper analysis of "Wrong perception of the price" (AND-related):**

- Customers do not recognize new value (N)
- Customers used to much cheaper versions (N+P: happy customer)

**Deeper analysis of "Customers do not recognize new value":**

- Direct communication with potential buyers is too little (N)

**Deeper analysis of "Direct communication with potential buyers is too little":**

- Marketing team is too small (N+P: cost effective)

### Summary table

| ID | Cause | Type | Positive Effect | Negative Effect |
|---|---|---|---|---|
| 1 | Unexplored market segments | N | — | Sales volume is low |
| 2 | Price of the product is too high | N+P | Higher revenues | Sales volume is low |
| 3 | Wrong perception of the price | N | — | Sales volume is low |
| 4 | Customers do not recognize new value | N | — | Wrong perception of the price |
| 5 | Customers used to much cheaper versions | N+P | Happy customer | Wrong perception of the price |
| 6 | Direct communication with potential buyers is too little | N | — | Customers do not recognize new value |
| 7 | Marketing team is too small | N+P | Cost effective | Direct communication is too little |

### Recommended problems to solve

1. **Price is too high (N+P)** — TC: "How to maintain a high price for revenue but avoid low sales volume?" PC: "Price should be high for revenue AND low for sales volume." Closest to the top problem.

2. **Marketing team is too small (N+P)** — TC: "How to maintain a small team for cost efficiency but avoid insufficient buyer communication?" PC: "Team should be large for outreach AND small for cost."

3. **Unexplored market segments (N)** — Simple problem: "How to explore and enter new market segments?" Can be addressed directly without contradiction resolution.

---

## 3. Compact Example with Solution Directions: Waste Bin

### General negative effect

"A public waste bin creates odor problems."

### Key contradiction causes

- Opening is large (N+P: easy disposal vs. odor release)
- Emptying frequency is high (N+P: reduces odor vs. increases running costs)
- Rain protection is present (N+P: prevents wet waste vs. reduces accessibility)

### Possible inventive directions

- **Opening large only during disposal, small otherwise**: flap, spring lid, sensor lid (separation in time).
- **Frequent emptying only when needed**: fill-level, odor, temperature, or season-dependent emptying (separation by condition, feedback control).
- **Rain protection without access obstruction**: local cover geometry, asymmetric hood, funnel, hydrophobic entry path (separation in space, local quality).
