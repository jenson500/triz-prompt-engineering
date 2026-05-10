# Root Conflict Analysis (RCA+) Knowledge File

This knowledge file contains the detailed method instructions for `root_conflict_analysis.xml`. The XML prompt should stay compact; this file holds the extended RCA+ methodology, definitions, tables, propagation rules, examples, and report structure.

---

## 1. Purpose of RCA+

Root Cause Analysis (RCA) focuses mainly on undesirable effects and traces them back to negative causes. Root Conflict Analysis (RCA+ / Grundkonfliktanalyse) extends RCA by also recording desirable effects, useful outcomes, goals, and requirements with equal importance.

A conflict exists when the same system state or parameter contributes to both desirable and undesirable effects. RCA+ is therefore especially useful when a system already works reasonably well, but improvement is difficult because removing the problem would also destroy a benefit.

Typical use cases:

- mature products or systems that need improvement;
- product, process, service, or organizational optimization;
- situations where a design decision has a useful purpose but also creates harm;
- innovation tasks where contradiction or conflict resolution is more suitable than defect repair.

RCA is usually sufficient when the task is mainly defect elimination and the unwanted effect is caused by an avoidable, actionable root cause. RCA+ is usually more powerful when the system is already functional and the problem results from a trade-off or conflict.

---

## 2. Core Concepts

### State

A state is a condition, property, behavior, parameter value, environmental condition, user behavior, or system situation that causally influences other states. Phrase states so that “more/less”, “stronger/weaker”, “larger/smaller”, “more frequent/less frequent”, or “present/absent” can be meaningfully discussed.

Examples:

- opening is large;
- rain protection is present;
- waste becomes wet;
- maintenance frequency is high;
- access to the opening is easy;
- system is located unfavorably.

### Desirable Aspect

A useful, intended, required, beneficial, or goal-related effect that should be preserved or strengthened.

Examples:

- users can easily throw waste into the bin;
- running costs are low;
- the product is easy to operate;
- maintenance effort is low;
- safety is high.

### Undesirable Aspect

A harmful, unintended, costly, risky, defective, inconvenient, or problematic effect that should be reduced or eliminated.

Examples:

- odor nuisance occurs;
- waste lies next to the bin;
- rain enters the bin;
- material becomes wet;
- maintenance costs increase.

### Causal Dependency

A directed relationship from a source state to a target state. The source state causally influences the target state.

The direction of causality is from cause to effect:

`Source State -> Target State`

### Positive Dependency / Reinforcing Dependency

Use `+ reinforces` when more of the source state leads to more of the target state, or less of the source state leads to less of the target state.

Example:

- More difficult access to the opening leads to more waste placed next to the bin.

### Negative Dependency / Weakening or Inverting Dependency

Use `- weakens/inverts` when more of the source state leads to less of the target state, or less of the source state leads to more of the target state.

Example:

- More rain protection leads to less rain entering the bin.

### Root Cause

A root cause is an undesirable state that causes other states but is not itself caused by another state within the chosen model boundary. A real root cause should be actionable or changeable in principle.

### Root Conflict

A root conflict is a state that receives both desirable and undesirable classifications. This means the same state contributes to at least one useful effect and at least one harmful effect.

A root conflict cannot normally be solved by simply removing the state, because the useful effect would also be lost. It requires inventive means, such as separation in time, separation in space, separation by condition, dynamic adaptation, or replacement of the harmful mechanism while preserving the useful effect.

---

## 3. RCA+ Workflow

1. Define the system, system boundary, operating context, stakeholders, and improvement objective.
2. Identify the initial undesirable aspect or problem.
3. Identify desirable aspects that must be preserved or strengthened.
4. List all relevant system states and parameters.
5. Mark known terminal aspects as desirable or undesirable.
6. Build directed causal dependencies between states.
7. Assign polarity to each dependency:
   - `+ reinforces`: more source creates more target;
   - `- weakens/inverts`: more source creates less target.
8. Propagate classifications backwards through the causal graph:
   - through `+`, keep the classification;
   - through `-`, invert the classification.
9. Iterate propagation until no additional classifications can be inferred.
10. Classify each state as desirable, undesirable, root conflict, unclassified, or ambiguous.
11. Identify root causes among actionable undesirable states with outgoing dependencies and no incoming dependencies.
12. Identify root conflicts among states that receive both positive and negative classifications.
13. Formulate each root conflict as a contradiction statement.
14. Only then propose solution directions.

---

## 4. Classification Propagation Rules

Classifications propagate **against** the direction of causal dependencies, from the target state back to the source state.

### Positive dependency

If the target is desirable and the dependency is positive, the source is desirable.

If the target is undesirable and the dependency is positive, the source is undesirable.

Example:

- More maintenance-friendly design leads to lower running costs.
- Low running costs are desirable.
- Therefore, maintenance-friendly design is desirable.

### Negative dependency

If the target is desirable and the dependency is negative, the source is undesirable.

If the target is undesirable and the dependency is negative, the source is desirable.

Example:

- More rain protection leads to less wet waste.
- Wet waste is undesirable.
- Therefore, rain protection is desirable.

Another example:

- Smaller opening leads to less easy waste disposal.
- Easy waste disposal is desirable.
- Therefore, a smaller opening is undesirable.

### Conflict detection

If one state receives only positive classifications, classify it as desirable.

If one state receives only negative classifications, classify it as undesirable.

If one state receives both positive and negative classifications, classify it as a root conflict candidate.

If evidence is weak or causal paths contradict each other due to uncertainty, classify it as ambiguous and state the missing data.

---

## 5. Required First Analytical Output

After the user provides a situation, the first analytical output must start with the relevant data in tabular form. Do not begin with a long conceptual explanation.

Always include:

1. `Relevant RCA+ Data`
2. `Causal Dependency Table`
3. `Classification and Propagation Table`
4. `Root Causes and Root Conflicts`
5. A direct statement beginning with `Root conflict(s) found:` or `No reliable root conflict identified yet:`

---

## 6. Required Table Formats

### Relevant RCA+ Data

| Item ID | State / Aspect | Type | Known Classification | Why It Matters | Source / Evidence | Confidence |
|---|---|---|---|---|---|---|

Possible values for `Type`:

- Initial Problem
- Desirable Aspect
- Undesirable Aspect
- Intermediate State
- Parameter
- Environmental Condition
- User Behavior
- Cost Driver
- Maintenance Driver
- Assumption

Possible values for `Known Classification`:

- Desirable
- Undesirable
- Unknown
- Ambiguous

### Causal Dependency Table

| Dependency ID | Source State | Polarity | Target State | Causal Reading | Evidence / Assumption | Confidence |
|---|---|---|---|---|---|---|

Polarity must be one of:

- `+ reinforces`
- `- weakens/inverts`

Causal reading should be phrased as:

- More `[source]` leads to more `[target]`.
- More `[source]` leads to less `[target]`.

### Classification and Propagation Table

| State | Direct Classification | Inferred Positive Paths | Inferred Negative Paths | Final RCA+ Classification | Interpretation |
|---|---|---|---|---|---|

Possible values for `Final RCA+ Classification`:

- Desirable
- Undesirable
- Root Conflict
- Root Conflict Candidate
- Unclassified
- Ambiguous

### Root Causes and Root Conflicts

| ID | Finding Type | State / Parameter | Conflict or Cause Logic | Desirable Effect Preserved | Undesirable Effect Created | Actionability | Recommended Direction |
|---|---|---|---|---|---|---|---|

Possible values for `Finding Type`:

- Root Cause
- Candidate Root Cause
- Root Conflict
- Candidate Root Conflict
- Not Yet Decidable

---

## 7. Root Conflict Formulation Templates

Use one or more of these templates:

- The `[state/parameter]` should be high / present / strong so that `[desirable effect]` is achieved, and it should be low / absent / weak so that `[undesirable effect]` is avoided.
- The system needs more `[state]` for `[useful result]`, but less `[state]` for `[harm reduction]`.
- `[Design decision]` creates `[desirable effect]`, but also causes or increases `[undesirable effect]`.
- The conflict is not merely that `[problem]` exists; the conflict is that the same underlying state also provides `[benefit]`.

---

## 8. Solution Guidance

Do not jump to solutions before the root conflict has been clearly stated.

For root causes, suggest direct actions such as:

- elimination;
- mitigation;
- relocation;
- parameter adjustment;
- process correction;
- better measurement;
- control action;
- change of operating condition.

For root conflicts, suggest inventive directions such as:

- separation in time;
- separation in space;
- separation by condition;
- separation by scale;
- separation by system level;
- dynamic adaptation;
- segmentation;
- feedback control;
- selective activation;
- local quality;
- transition to a higher system level;
- replacement of the harmful mechanism while preserving the useful effect.

For every solution direction, explicitly explain how it preserves the desirable effect while reducing the undesirable effect.

---

## 9. RCA vs. RCA+

RCA is limited to identifying root causes of undesirable effects. RCA+ identifies both root causes and root conflicts. RCA+ requires more effort because desirable aspects must also be identified and modeled.

Useful decision rules:

- If the system is underdeveloped or defective, RCA may be sufficient.
- If the system is mature and generally works, but improvement is difficult because every change has disadvantages, RCA+ is often more suitable.
- Mature products usually have fewer simple root causes and more root conflicts.
- A problem caused by an actionable root cause indicates a defect or unfinished development.
- A problem caused by a root conflict indicates that a useful design decision also creates harm.

RCA mainly answers causal “Why?” questions: Why does this undesirable effect occur?

RCA+ also answers goal-related “Why?” questions: Why was this design decision made? Which useful effect does it preserve?

---

## 10. Waste Bin Example

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

Possible inventive directions:

- opening large only during disposal, small otherwise: flap, spring lid, sensor lid;
- frequent emptying only when needed: fill-level, odor, temperature, or season-dependent emptying;
- rain protection without access obstruction: local cover geometry, asymmetric hood, funnel, hydrophobic entry path.

---

## 11. Final RCA+ Report Structure

When the user asks for a final report, use this structure:

1. Executive Summary
2. System Boundary and Improvement Objective
3. Initial Desirable and Undesirable Aspects
4. Relevant RCA+ Data
5. Causal Dependency Model
6. Classification Propagation
7. Root Causes
8. Root Conflicts
9. Conflict Formulations
10. Inventive Solution Directions
11. Recommended Investigation and Validation Steps
12. Assumptions, Open Questions, and Confidence Level

---

## 12. Quality Rules

- Distinguish clearly between root causes and root conflicts.
- Do not treat every negative state as a root cause.
- Check whether an undesirable state is caused by another state.
- Check whether a conflict state preserves a useful effect.
- Do not remove a conflict state without preserving its desirable effect.
- Use cautious language for assumed causal dependencies.
- Mark uncertain findings as candidates.
- State missing data explicitly.
- Keep the analysis structured and suitable for engineering, product, process, service, or organizational systems.
