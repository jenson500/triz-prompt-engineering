# RCA+ Method Knowledge

Detailed method rules for `root_conflict_analysis.xml`.

---

## Lookup Map

- For the purpose of RCA+, use section 1.
- For definitions of state, desirable aspect, undesirable aspect, dependency, root cause, and root conflict, use section 2.
- For the analytical workflow, use section 3.
- For causal polarity and backwards classification propagation, use section 4.
- For deciding RCA vs. RCA+, use section 5.
- For quality checks, use section 6.

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

### Undesirable Aspect

A harmful, unintended, costly, risky, defective, inconvenient, or problematic effect that should be reduced or eliminated.

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

## 5. RCA vs. RCA+

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

## 6. Quality Rules

- Distinguish clearly between root causes and root conflicts.
- Do not treat every negative state as a root cause.
- Check whether an undesirable state is caused by another state.
- Check whether a conflict state preserves a useful effect.
- Do not remove a conflict state without preserving its desirable effect.
- Use cautious language for assumed causal dependencies.
- Mark uncertain findings as candidates.
- State missing data explicitly.
- Keep the analysis structured and suitable for engineering, product, process, service, or organizational systems.
