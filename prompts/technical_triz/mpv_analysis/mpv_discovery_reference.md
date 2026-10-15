# MPV Discovery - method reference

Reference for the prompt `mpv_analysis.xml`. The prompt carries the sequence, the rules and the
output format; this file carries the steps in full, the vocabulary, the background and a worked
example. Read it before step 1 and keep it in context.

---

## The ten steps

Work through the steps in order. Do not skip a substep and do not run two steps at once.
Where a step says STOP, stop and hand over.

### Step 1 - Define the object of improvement

- Ask the user which product, process or service is to be improved.
- Restate it briefly in your own words and ask for confirmation or correction.
- Record what the object is and, just as important, what it is not. A vague object produces vague parameters later.

### Step 2 - Formulate the business challenge

- Ask what business situation triggers this work: lost market share, a stagnating product, a competitor's advance, a price war, a new regulation, an unused technology.
- Formulate the business challenge as one question in the form "How can we ...?" and ask the user to confirm or sharpen it.
- Ask which data supports the challenge: market shares, complaint rates, returns, win-loss reasons, benchmarks. If the user has no data, record that as an open point. Do not invent figures.
- This step is not optional. Step 5 decides which parameters are important by asking whether they affect the main function or this business challenge. Without step 2 that filter does not exist.

### Step 3 - Identify market segments and usage situations

- Ask for the relevant life cycle phases of the object. At minimum, consider production, transport and storage, set-up, use, maintenance, and disposal.
- Ask for the stakeholders, the target market niches and the typical occasions of use. A parameter that matters to the installer may be invisible to the buyer.
- Summarize the result and ask for confirmation. The remaining steps are performed for these phases and segments, not for the product in the abstract.

### Step 4 - Build a simple function model (first handover)

- Explain that the parameters of value are not guessed, they are derived from the system. The function model is the first of the discovery channels.
- Together with the user, sketch a high-level function model for the most important life cycle phase: the main components, the super-system components acting on them, and the target component. Keep it coarse. Name the useful functions, the insufficient ones and the harmful ones.
- From this sketch, read off the parameters of value it suggests. A harmful function points to a parameter the customer suffers from; an insufficient function points to a parameter that is not delivered well enough. Record each one with the source tag FA.
- Then STOP the modelling and hand over: a chat sketch is not a function analysis. Tell the user that the proper model is built with a dedicated function analysis tool, name what they should take along (object, life cycle phase, component list), and ask them to come back with the result or to continue with the sketch for now, knowing it is provisional.

### Step 5 - TESE analysis (second handover)

- Explain the purpose: the Trends of Engineering System Evolution describe how systems typically develop. Applying a trend to an important parameter of value exposes a gap between the current state and the state the trend points to. That gap is an MPV candidate.
- State clearly that this is not an S-curve analysis. The S-curve is drawn after an MPV has been confirmed, not while searching for it.
- Decide with the user which parameters of value are important. A parameter is important when it directly affects the main function of the object or the business challenge from step 2. Only these go into the TESE analysis.
- Name the trends that are usually productive here, for example coordination, dynamization, rhythm of action, controllability, segmentation, and increasing sensing. Name them so the user knows what to look for.
- Then STOP. Do not perform the analysis yourself. Tell the user that the TESE analysis is a separate piece of work, that it needs the trends and their mechanisms in full, that it is advanced material beyond this step, and that it is normally done by a small team working in parallel. Say that it should be carried out before the parameter list is considered complete, and that any candidates it produces are added to the list with the source tag TESE.
- Do not name a specific product or service for this. Say what has to be done, not which tool to use.

### Step 6 - Parallel evolutionary lines

- Name this third channel and say what it does: it compares how a similar function evolves in other industries, and so reveals value parameters that the own system does not suggest.
- State that the method description for this step is not yet published and that it is therefore skipped here. Do not improvise a procedure for it. Note that a complete MPV Discovery would include it.

### Step 7 - Compile the list of parameters of value

- Collect everything found so far into one list. Remove exact duplicates. Do not prioritize yet.
- Present the list in two clearly separated blocks: Voice of the Product (everything from steps 4, 5 and 6) and Voice of the Customer (everything the user has reported from customers, complaints or market research).
- Every entry carries its source: FA, TESE, PEL or VoC. If you cannot name the source of a parameter, do not put it on the list. A list of generic product attributes is the failure mode of this step.
- Each entry is only a name that communicates the value aspect, such as convenience, safety, durability, inconspicuousness. No technical explanation, no units, no metrics. Those come in step 10.
- Parameters cannot contradict each other at this stage, because they are market-facing value concepts and not engineering characteristics. If the user raises a trade-off, record it and move on.

### Step 8 - Select the MPV candidates

- Narrow the list to the most promising candidates. The criterion is functionality over cost: which parameter promises a large functional improvement without an unreasonable cost increase, and which might even reduce cost.
- The judgement here is qualitative and internal. There is no formula and no score. Do not invent a rating scale.
- Select at most three candidates. One or two is typical, three is the upper limit. More than three dilutes the work.
- If cost or price appears on the list, keep it in the short list. In most projects it turns out to be a candidate in its own right.
- Present the short list with one sentence of reasoning per candidate and ask for confirmation.

### Step 9 - Validate with the Voice of the Customer (third handover)

- Explain what has to be confirmed for each candidate: that customers are dissatisfied with the current state, and that they are willing to pay for an improvement. Both, not either.
- State the acceptance threshold: a candidate counts as confirmed when more than half of the potential buyers say yes to both questions. This simple majority keeps the result from being driven by a niche.
- Work through the candidates with the user as an exercise, so that they get a feel for how the questions behave and where a candidate is likely to fail. Mark every result of this exercise as an assumption. Never present it as a finding.
- Do not invent survey results, percentages or customer quotes. You have not asked anyone. If the user has real data, use it and say so.
- Then STOP and hand over. Tell the user that this step has to be done with real customers, name the methods that are suitable (structured field interviews, surveys, conjoint analysis, focus groups, customer panels, A/B tests for digital products, observation where people cannot articulate their judgement), and say what the result has to document: method, sample size and characteristics, outcome per candidate, and the decision which candidates are confirmed.
- Offer to write a short briefing the user can hand to marketing or to the client: the candidates, the two questions per candidate, the threshold, and the suggested method.

### Step 10 - Translate the MPVs into physical parameters

- For each confirmed candidate, identify the engineering parameters that determine how well it is delivered. These are the physical parameters of value.
- A physical parameter of value is measurable, observable and controllable. Typical kinds are geometric (size, shape, thickness, curvature), mechanical (force, pressure, stiffness), optical (intensity, wavelength, uniformity), material (hardness, roughness, friction), and operational (speed, amplitude, uniformity of motion).
- It must be an engineering parameter, never an abstract benefit. "Convenience" is not one; "size of the delivery system" is. Check each entry against this before you write it down.
- There is no prescribed number per MPV. Some have one, some have several. Correctness matters, not quantity.
- Do not use Physical Parameter Determination here. It is an advanced method and not part of this step.
- Close with the handover list: the confirmed MPVs, their physical parameters, and the recommendation to continue with the TRIZ tools that identify and solve the key problems blocking them.

### Interaction rules

- Keep the sequence. Do not skip a step and do not assume an answer the user has not given.
- After each step, present the result and ask for confirmation or correction before continuing.
- Present results as lists or short summaries. Keep them copyable.
- If the user wants to jump ahead, say which step the answer depends on and offer to go there first.

---

## Definitions

**Parameter of Value (PV)** - Any characteristic of a product, service or system that influences customer choice or satisfaction. Can be functional, emotional, economic or experiential.

**Main Parameter of Value (MPV)** - A key attribute or result that is unsatisfied in the market and decisive for the purchasing decision. An MPV is noticed by customers, drives their choice, and can be improved by engineering action.

**Latent MPV** - Unsatisfied and unknown: customers do not ask for it because they have not imagined it is possible, but they recognize the benefit at once when it appears. Latent MPVs usually sit on an accepted limitation of current technology.

**Tacit PV** - Satisfied but unknown: delivered automatically as an artifact of the current technology, so nobody mentions it. Customers notice tacit parameters only when they get worse, which is why improving an MPV can create unexpected resistance.

**Voice of the Product (VoP)** - What the system can actually deliver and where its limits are, established by function analysis, TESE and parallel evolutionary lines. The MPV search starts here.

**Voice of the Customer (VoC)** - What customers perceive, want or miss, established by market research. In MPV Discovery, VoC primarily validates and selects, and may also contribute a parameter that the product analysis did not surface.

**Physical Parameter of Value (PPV)** - The measurable engineering parameter through which an MPV is realized.

**Innovation** - A measurable, market-ready improvement of at least one MPV. New technology alone does not qualify.

---

## Terminology in English and German

The four categories form a matrix of customer satisfaction against customer awareness. Use the names below and no others. Do not translate them freely and do not invent abbreviations.

| Category | English | Deutsch |
|---|---|---|
| unsatisfied, known | MPV (Main Parameter of Value) | HPW (Hauptparameter des Wertes) |
| unsatisfied, unknown | Latent MPV | vHPW (Verdeckter Hauptparameter des Wertes) |
| satisfied, known | PV (Parameter of Value) | PW (Parameter des Wertes) |
| satisfied, unknown | Tacit PV | iPW (Impliziter Parameter des Wertes) |

---

## Why the method works this way

### Why the parameters are not simply asked for

Customers can describe needs, frustrations and expectations, but they rarely name their own main parameters of value. They speak in outcomes, not in parameters: a shaver should be gentle, efficient, comfortable. The parameters behind those outcomes may be the dynamic behaviour of the blade system, the pressure distribution on the skin, or the vibration pattern. Customers cannot describe these, but they can be engineered. This is why the search starts with the product and ends with the customer, and not the other way round.

### Why latent parameters matter

Users of early navigation apps asked for better maps and faster routing. What they did not ask for was live traffic information and parking availability. Those were latent, and they reshaped the market. Latent parameters sit behind limitations that everyone has silently accepted.

### Why tacit parameters matter

Tacit parameters are delivered by the current technology and nobody talks about them. They become visible only when an improvement elsewhere makes them worse, and then the reaction is strong even though the parameter was never mentioned. Watch for them when a candidate is pushed hard, and record the risk.

### Three channels, one list

Function analysis, TESE and parallel evolutionary lines are independent sources. Each finds parameters the others miss. They merge in step 7. A list that comes from only one channel is incomplete, and saying so is part of the result.

---

## Worked example

**Problem.** Business challenge: how can a teeth whitening product be made that becomes the market leader? Trigger: loss of market share and only marginal performance differences between the competing products.

**Solution.** Function model during use: the tray holds the whitening gel, the gel dissolves the dental plaque on the teeth, and the gel also damages the gums. Parameters read from the model, source FA: intensity of whitening, comfort in the sense of no gum irritation, comfort in the sense of taking up little space in the mouth, inconspicuousness, safety. Reported from customers, source VoC: whitening effectiveness and duration of application. Candidates after step 8: intensity, comfort, inconspicuousness. Physical parameters in step 10: comfort becomes the size of the delivery system, inconspicuousness becomes its transparency, safety and intensity both become the concentration of the whitening gel. The key problem that follows is a contradiction in that concentration, and it is handed to the problem-solving tools.

**Problem.** During step 7 the user suggests adding "reliability" and "ease of use" because every product has them.

**Solution.** Ask which channel produced them. If neither the function model nor TESE nor a customer statement produced them, they do not go on the list. They are category attributes, not discovered parameters, and carrying them along hides the parameters that were actually found.
