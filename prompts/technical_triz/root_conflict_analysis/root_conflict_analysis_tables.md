# RCA+ Table and Output Requirements

Detailed output rules for `root_conflict_analysis.xml`.

---

## Lookup Map

- For the first analytical answer, use section 1.
- For the table `Relevant RCA+ Data`, use section 2.
- For the table `Causal Dependency Table`, use section 3.
- For the table `Classification and Propagation Table`, use section 4.
- For the table `Root Causes and Root Conflicts`, use section 5.

---

## 1. Required First Analytical Output

After the user provides a situation, the first analytical output must start with the relevant data in tabular form. Do not begin with a long conceptual explanation.

Always include:

1. `Relevant RCA+ Data`
2. `Causal Dependency Table`
3. `Classification and Propagation Table`
4. `Root Causes and Root Conflicts`
5. A direct statement beginning with `Root conflict(s) found:` or `No reliable root conflict identified yet:`

If the user has not provided enough information, extract what is available, mark assumptions clearly, and specify the missing data needed to identify reliable root conflicts.

---

## 2. Relevant RCA+ Data

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

---

## 3. Causal Dependency Table

| Dependency ID | Source State | Polarity | Target State | Causal Reading | Evidence / Assumption | Confidence |
|---|---|---|---|---|---|---|

Polarity must be one of:

- `+ reinforces`
- `- weakens/inverts`

Causal reading should be phrased as:

- More `[source]` leads to more `[target]`.
- More `[source]` leads to less `[target]`.

---

## 4. Classification and Propagation Table

| State | Direct Classification | Inferred Positive Paths | Inferred Negative Paths | Final RCA+ Classification | Interpretation |
|---|---|---|---|---|---|

Possible values for `Final RCA+ Classification`:

- Desirable
- Undesirable
- Root Conflict
- Root Conflict Candidate
- Unclassified
- Ambiguous

A state with both positive and negative propagated classifications is a root conflict candidate. If confidence is high enough, classify it as `Root Conflict`.

---

## 5. Root Causes and Root Conflicts

| ID | Finding Type | State / Parameter | Conflict or Cause Logic | Desirable Effect Preserved | Undesirable Effect Created | Actionability | Recommended Direction |
|---|---|---|---|---|---|---|---|

Possible values for `Finding Type`:

- Root Cause
- Candidate Root Cause
- Root Conflict
- Candidate Root Conflict
- Not Yet Decidable

Root causes should usually have an actionable elimination or mitigation direction. Root conflicts should usually have an inventive direction that preserves the desirable effect while reducing the harmful effect.
