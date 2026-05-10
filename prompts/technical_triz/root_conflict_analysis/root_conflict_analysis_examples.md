# RCA+ Examples

Worked example for `root_conflict_analysis.xml`.

---

## Lookup Map

- For a compact demonstration of the required tables and conflict statements, use section 1.
- For typical solution directions after conflict identification, use section 2.

---

## 1. Waste Bin Example

Situation:

A public waste bin creates odor problems. It should also be easy for passers-by to use, and running costs should stay low. Opening size, rain protection, maintenance frequency, and placement influence both useful and harmful effects.

### Relevant RCA+ Data

| Item ID | State / Aspect | Type | Known Classification | Why It Matters | Source / Evidence | Confidence |
|---|---|---|---|---|---|---|
| A1 | Odor nuisance occurs near the bin | Undesirable Aspect | Undesirable | Creates discomfort and complaints | Given problem | High |
| A2 | Waste is easy to throw into the bin | Desirable Aspect | Desirable | Ensures user adoption | Requirement | High |
| A3 | Running costs are low | Desirable Aspect | Desirable | Keeps operation economical | Requirement | High |
| S1 | Opening is large | Parameter / State | Unknown | Affects both usability and odor/rain ingress | Assumption | Medium |
| S2 | Rain protection is present | Parameter / State | Unknown | Reduces wet waste but may reduce access | Assumption | Medium |
| S3 | Emptying frequency is high | Maintenance Driver | Unknown | Reduces odor but increases cost | Assumption | Medium |

### Causal Dependency Table

| Dependency ID | Source State | Polarity | Target State | Causal Reading | Evidence / Assumption | Confidence |
|---|---|---|---|---|---|---|
| D1 | Opening is large | + reinforces | Waste is easy to throw into the bin | More opening size leads to easier disposal | Plausible dependency | High |
| D2 | Opening is large | + reinforces | Odor nuisance occurs near the bin | More opening size can lead to more odor release | Plausible dependency | Medium |
| D3 | Rain protection is present | - weakens/inverts | Waste becomes wet | More rain protection leads to less wet waste | Plausible dependency | High |
| D4 | Rain protection is present | - weakens/inverts | Waste is easy to throw into the bin | More rain protection may reduce accessibility | Plausible dependency | Medium |
| D5 | Emptying frequency is high | - weakens/inverts | Odor nuisance occurs near the bin | More emptying leads to less odor nuisance | Plausible dependency | High |
| D6 | Emptying frequency is high | - weakens/inverts | Running costs are low | More emptying leads to lower cost efficiency | Plausible dependency | High |

### Classification and Propagation Table

| State | Direct Classification | Inferred Positive Paths | Inferred Negative Paths | Final RCA+ Classification | Interpretation |
|---|---|---|---|---|---|
| Opening is large | None | From easy disposal via D1 | From odor nuisance via D2 | Root Conflict | Large opening is both useful and harmful |
| Rain protection is present | None | From less wet waste via D3 | From reduced accessibility via D4 | Root Conflict Candidate | Rain protection may be useful and harmful |
| Emptying frequency is high | None | From reduced odor via D5 | From increased operating costs via D6 | Root Conflict | Frequent emptying reduces odor but increases cost |

### Root conflict(s) found

1. The waste bin opening should be large so that waste can be thrown in easily, and it should be small so that odor release and rain ingress are reduced.
2. The emptying frequency should be high so that odor nuisance is reduced, and it should be low so that running costs remain low.
3. Rain protection should be present so that rain does not enter the bin, and it should be absent or non-obstructive so that users can easily access the opening.

---

## 2. Possible Inventive Directions

- Opening large only during disposal, small otherwise: flap, spring lid, sensor lid.
- Frequent emptying only when needed: fill-level, odor, temperature, or season-dependent emptying.
- Rain protection without access obstruction: local cover geometry, asymmetric hood, funnel, hydrophobic entry path.
