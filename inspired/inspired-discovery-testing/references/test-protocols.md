# Test protocols

Contents: 1. Assessing evidence · 2. Decision criteria · 3. Participants and samples · 4. Usability test · 5. Qualitative value test · 6. Demand test · 7. Quantitative value tests · 8. Calculations · 9. Feasibility test · 10. Customer-facing safeguards · 11. Templates · 12. Examples

**Source.** From *Inspired*: testing usability, value, feasibility and viability separately; how a usability session is conducted (it is a prototype, realistic tasks, don't help, record easy / struggled / failed, fix problems between sessions); the value test in the same session; the four value signals; fake-door and landing-page demand tests with an honest page behind them; A/B tests, invite-only tests and discovery-program use as quantitative techniques; the feasibility questions; the analytics categories. Added here, and not the book's: sections 1, 2, 3, 8 and 10; the experiment gate and checklists in section 7; the three feasibility states; the version log; the decision vocabulary; the limits on the access signal. The book advises protecting customers, revenue and reputation while testing; the specific rules in section 10 are added. Every figure in the examples is invented for illustration.

## 1. Assessing evidence

Used for every readout. It answers the five questions in the skill.

### Three classes of result

| Class | What it is | Claims it supports | How to word it |
|---|---|---|---|
| **Qualitative** | Observations, motivations, explanations, context | Why and how; what gets in the way; that something happened | "3 of the 5 participants…", "one buyer said…" |
| **Descriptive quantitative** | Measured usage, completion times, frequency, conversion, adoption | How much and how often, among those measured | "Across the 3 pilot accounts…" |
| **Inferential or causal** | Estimates meant to hold for a population, or to show cause | Population-level or causal statements, subject to sampling, design and statistical assumptions | "Among [population] during [period], the change moved X by Y (interval …)" |

The class is set by the design, not by how many numbers the result contains. A dashboard of usage from three accounts is descriptive however many events it holds.

### What common results do and don't establish

- "I would pay" is a stated intention. A purchase, a deposit or a signed order is a commitment.
- A waitlist or landing-page sign-up shows interest in a description. It does not show intent to buy.
- A pilot agreement shows willingness to evaluate. It is not adoption and not renewal.
- Repeated use in production is strong evidence that the product is useful to those users. It does not show that the product caused a change in a business result; other things changed over the same period.
- A randomized experiment can show cause, provided assignment was random, the sample-ratio and data checks pass, and the analysis was fixed beforehand.
- Completing tasks in a moderated session shows the design can be used. It does not show they would choose to use it.
- Reactions to a demo or a walkthrough are stated preferences at best: the participant used nothing.

### Quality checks

| Check | Ask | Strength drops when |
|---|---|---|
| Relevance | Is this the kind of evidence the hypothesis needs? | Stated intent offered for a purchase claim; a usability result offered for value |
| Participants | Are they in the target segment? How were they recruited? | Convenience sample, friends, staff, fans, or discovery-program customers treated as the market |
| Independence | What is the unit: event, user or account? How concentrated is the activity? | Most activity comes from one account or one champion; several participants share a team |
| Cost | What did they give up? | Nothing, or something trivial next to the claim |
| Prompting | Was it volunteered, asked for, or led? | The signal followed a leading question, a scheduled session, or an obligation to use the product |
| Same stimulus | Did everyone meet the same version under the same conditions? | The prototype changed mid-round; fake data made the task easier than real work |
| Measurement | Was the metric defined beforehand and fully captured? | The definition was chosen after seeing the data; events are missing; the period is partial |
| Duration | Did it outlast novelty and cover a normal cycle? | A few days of use; one unusual week |

### Stating strength

State strength for the hypothesis, in one of four words, with the reason:

- **Strong:** the right kind of evidence for the hypothesis, from the target segment, consistent, with no likely alternative explanation.
- **Moderate:** the right kind, limited by sample, selection, or one alternative explanation that hasn't been ruled out.
- **Weak:** the wrong kind for the hypothesis, or badly compromised on the checks above.
- **None:** the test did not bear on the hypothesis.

The same result can be strong for one hypothesis and none for another. Say both when a reader might confuse them: "strong for usability of the setup flow; none for willingness to pay."

### Alternative explanations to consider

Politeness, or wanting to please the moderator. Who was recruited. Novelty that decays. Use that happened because we asked, scheduled it, or the pilot terms require it. One account or champion producing most of the activity. An incentive. A prototype that was easier, or more broken, than the real thing. Something else that changed in the period: season, marketing, price. A metric that measured curiosity about a label and not interest in the product.

### Traceability

Every observation, quote and count in a readout comes from the material supplied or retrieved. Name the source in the readout header: session notes, recordings, an export, or a summary reported by someone. When only a summary was supplied, the readout repeats it as reported and cannot vouch for it. Three markers keep gaps honest:

- **not provided:** it may exist, but it wasn't in what you were given.
- **not measured:** the test didn't capture it.
- **n/a:** it doesn't apply to this test.

## 2. Decision criteria

Written before any result is seen, and kept with the plan.

```
Continue if: [observable result] — basis: [type]: [the fact or reasoning] — [agreed by whom / provisional]
Iterate if: [...]
Stop if: [...]
Inconclusive if: [conditions under which the test cannot be read]
Set on [date] by [who], before results.
```

### The basis for a threshold

| Basis | What it looks like |
|---|---|
| Historical performance | "The current flow is completed by [x]% of new accounts ([source], [period]); the redesign has to beat that." |
| Established benchmark | A published or internal standard that applies to this product and segment, named. |
| Business requirement | "Support can absorb [n] setup calls a week, so no more than [share] of accounts can need help." |
| User or operational risk tolerance | "An error in this step sends a wrong payment, so one unrecovered error in the round is enough to iterate." |
| Smallest economically meaningful effect | "Below [x] points of conversion the feature doesn't cover its running cost." With the derivation. |
| Provisional judgment | "No baseline exists. [Who] judges that [level] is enough to move on, because [reason]. Provisional; to be replaced once a round shows what failure looks like." |

When nothing supports a threshold:

1. Name the missing information: the baseline, the capacity, the cost, the tolerance.
2. Propose an exploratory test where that fits: observe first, then set criteria for the next round from what was learned.
3. If a criterion is still wanted, write it as a provisional judgment: whose it is, and why that level and not another. A number nobody can give a reason for is left open for the person to set; state the criterion by what will be observed.
4. Say what would make it firm: which measurement or decision, and from whom.

### Small samples

A percentage threshold on a handful of participants reads as a measurement and isn't one. "80% of 5" is 4 of 5; one participant is 20 points, and the interval around 4 of 5 runs from about 38% to 96% (section 8, block C). Such a threshold can serve as a rule of thumb for moving on. It cannot stand for the rate in the segment. Criteria about what was seen usually work better: which task, what kind of failure, and whether the design or the prototype caused it.

### Inconclusive, set in advance

Decide beforehand what would make the test unreadable: fewer qualified participants than the plan needs, a prototype defect that blocked the task, lost instrumentation, exposure too small to reach the planned sample, or participants who turn out to be outside the segment. State these against the plan's own figures. A new cut-off needs a basis like any other threshold.

### Criteria from more than one place

A risk assessment, a prototype spec and the person may each have written criteria. If they agree, use them. If they differ, show both, evaluate against each, and say which one the decision rests on and why.

### Changes after the results

```
Against the original criteria (set [date]): [result]
Retrospective criterion (added [date], after results; reason: [...]): [result]
```

The decision cites the original evaluation. A retrospective criterion is input to the next test's criteria.

## 3. Participants and samples

**Define the segment as screening criteria:** the situation or behavior that puts someone in the target market, their role, and in B2B the type of account and whether they are a user or the economic buyer. Confirm the criteria at the start of each session. A participant who turns out to be outside the segment is reported separately and left out of the counts.

**Name the recruitment route and its bias:**

| Route | Usual bias |
|---|---|
| Discovery-program or design-partner customers | Chosen for feeling the problem and wanting to help; more engaged and more forgiving than the market |
| Existing active users | Already chose the product; silent on non-users and those who left |
| Customers nominated by sales or account teams | Friendly, often larger accounts |
| Panels, ads, community groups | Self-selected and incentive-motivated; check they are really in the segment |
| Colleagues, friends, investors | Not the segment. Use them to debug the script, not as participants |

A sample is **representative** only if it was recruited in a way that gives the segment's main variations a fair chance of appearing. Otherwise it is a **convenience sample**; say so in the readout header and limit the claims to the people seen.

**How many depends on the method:**

| Method | Sizing logic |
|---|---|
| Formative usability | Small rounds per segment, continued until sessions stop revealing new material problems. Count per prototype version |
| Qualitative value | Enough different participants to see whether signals repeat; in B2B, across different accounts and roles, buyers included. Say how many accounts they come from |
| Demand test | Exposure large enough that the expected number of clicks can be read; computed (section 8) if a population-level claim is wanted |
| Use by selected customers | Every account with access, each reported |
| Experiment | Computed from the baseline, the smallest effect worth acting on, α and power (section 8) |

Note any thank-you or incentive in the readout. It bears on how to read time and interest signals.

## 4. Usability test

**Preparation**

- Recruit per section 3. Label the prototype version.
- Write the few tasks that matter as goals ("You need to pay supplier X before Friday"), not instructions ("Click Payments").
- Their own setting, or a screen share, shows context a lab hides.
- One person moderates and one takes notes. In *Inspired* the product manager and designer attend each session and an engineer joins when possible.
- Decide whether to use think-aloud. It shows what participants expect and where they look. It also slows them and changes how they work, so skip it for timed tasks and for experts doing speed-critical work; watch silently and ask them to walk back through what they did.

**Session script**

1. Introduce: this is a prototype, some things won't work, we are testing the product and not you, honest reactions help. Ask permission to record.
2. Screen: confirm they are in the segment and have the problem. Ask briefly how they handle it today.
3. Give tasks one at a time. Stay neutral: no explaining, no praise, no hints.
4. When they are stuck: "What would you expect to happen?", "Where would you look?", or repeat their question back. If they cannot continue, record the failure, then help them past it so later tasks can be seen, and mark those tasks as started with help.
5. Then run the qualitative value test (section 5), while they understand the product.

**Observation sheet**

```
Participant: [id] · In segment: [yes / no, why] · Recruited via: [...] · Prototype version: [v]
| Task | Outcome (easy / struggled / failed) | What they did | Moderator stepped in? | Their words |
```

Write what was seen and heard. Interpretation goes in the debrief.

**Version log**

```
| Version | Sessions | Material change from the previous version | Prompted by |
```

Fix clear problems between sessions; waiting for the round to end wastes participants on a known flaw. A change is material when it alters what a participant sees or does on a tested task: flow, labels, layout, content, data. Log anything doubtful.

**Reporting across versions.** Give outcomes per version. A later version doing better is consistent with the change helping. It is not a controlled comparison: the participants differ, and the team already knew what to fix. To say the fix worked, run a further round on the stable version.

**Afterward.** Debrief the same day, keep observations apart from interpretations, decide the changes, update the log.

## 5. Qualitative value test

Run it once the participant understands the product. For each of the four signals, keep what was said apart from what was given:

| Signal | Said (stated preference) | Given (commitment) |
|---|---|---|
| Money | An answer to "what would this be worth?" or "would you pay [price]?" | B2C: a pre-order or deposit at the real price, through a real and refundable payment flow. B2B: a signed letter of intent, a budget line confirmed by the budget holder, a paid pilot |
| Reputation | "I'd recommend it" | Introduced it to their manager or a peer; agreed to be a named reference; brought a senior colleague to the next session |
| Time | "Let's keep in touch" | Booked and attended a working session; assigned scarce people; used it daily for an agreed period |
| Access | "You could have our data" | Started their own data-sharing or security approval; connected an account through an authorized integration; signed a data agreement |

Rules:

- **Count only what was given as commitment.** Record the stated answers too; they explain motivation.
- **Match the commitment to the claim.** "Will pay a subscription" needs a payment or pre-order at that price. "The organization will buy" needs something from the budget holder, not from a user. "Will switch from the current tool" needs steps toward switching.
- **Don't press.** A commitment won by pressure or a large incentive says little. Record whether it was volunteered or asked for.
- **No credentials, no confidential data in the session.** Never collect a password or have a participant enter real credentials into a prototype. If a later test needs real data, it moves under the customer's and your organization's approved process, and the signal is that they start that process.
- **Commercial offers need an owner.** A price shown, pilot terms or a letter of intent come from, or with the agreement of, whoever is authorized to make offers. If that isn't confirmed, the script asks about budget and current spend and shows no price.
- **B2B: buyers get their own session.** Ask about budget, who else approves, how purchases like this get made, and what it would replace.

```
| Participant (role, account) | Said | Did or committed | Volunteered or asked? | In proportion to the claim? |
```

Read across participants: do commitments repeat across different accounts and roles, unprompted? One enthusiastic account is one data point.

## 6. Demand test

- **Fake door:** an entry point (button, menu item, tile) for something that doesn't exist yet. Clicking leads straight to an honest page: this is being considered, it isn't available, would you like to hear when it is or join early access.
- **Landing page:** a page describing the offer, reached from an ad or a link. It says before asking for anything that the offer isn't available yet.

**What it measures.** Interest in a label or description among those exposed. Instrument who saw the entry point, not only who clicked; the rate needs that denominator. Placement and wording move the rate, and some clicks are curiosity. Leaving contact details after the disclosure is a somewhat stronger signal than the click.

**Before it runs**

- *Honesty.* Disclosure is immediate. Nothing a customer relies on (sales material, contracts, documentation, support answers) says or implies the feature exists. No payment or data is taken for something that doesn't exist unless the page says so, and any deposit is refundable and described as such.
- *Trust and brand.* Who will see it, and how will a customer who needed the feature feel on learning it isn't there? Tell support and sales so they can answer questions. Where showing an unavailable function could mislead in a contractual or regulated setting, don't use a fake door; use an explicit "register interest" framing.
- *Enterprise or named accounts.* Agree it with whoever owns the account relationship, or exclude those accounts.
- *Exposure.* Share of users and duration fixed in advance, small and short.
- *Authorization.* Section 10.

**Criteria.** A first fake door rarely has a baseline, so a click-rate threshold is usually a guess. Compare with an existing entry point of known click rate on the same surface, or run it as exploratory.

**Reading it.** People who clicked are not buyers. Describe who clicked, and recruit from them for value tests.

## 7. Quantitative value tests

*Inspired* names three techniques: A/B tests, invite-only tests, and discovery-program customers using the product. They answer two different questions, and the design decides which one a result can speak to.

### 7.1 Use by selected customers

A live-data prototype used in real work by discovery-program customers or by users invited or opted in. "Invite-only" describes who gets access. There is no control group, so the result is observed behavior and descriptive numbers.

Capture, per account in B2B or per cohort in B2C:

- **Access and use:** who was given access, who used it, how often, over how long.
- **Real work:** which real tasks went through it, and whether the old way stopped.
- **Unprompted use:** use outside scheduled sessions and without reminders.
- **Spread:** people other than the champion.
- **Failure handling:** what they did when it failed them.
- **Commercial steps:** pilot terms signed, budget requested, security review started, reference agreed.
- **Organizational constraints:** what inside the customer would stop wider adoption or a purchase.
- **Concentration:** the share of all activity that comes from the most active account and the most active user.

Report each account first, then the total, with units: "3 accounts, 14 users, 212 sessions". A before-and-after comparison within the same accounts is descriptive; label it and list what else changed.

It supports: "these customers adopted it in their workflow", which is strong behavioral evidence of value to them. In *Inspired* the discovery program has succeeded when its customers run the product in production and will act as references. It does not support market-wide demand, the product having caused a change in their results, or the behavior of customers unlike them.

### 7.2 Controlled experiment

**Gate.** Check these before designing anything. If one fails, go to 7.3.

1. *Enough independent units.* Compute the sample needed for the smallest effect worth acting on (section 8) and compare it with the eligible units over a duration the team accepts. If the smallest effect the available traffic can detect is larger than the effect worth acting on, the test is underpowered: "no significant difference" will not mean no effect, and a significant result will tend to overstate the effect.
2. *Random assignment at the right unit,* without contamination: users in one account sharing screens, one user meeting both variants, effects that spread between users.
3. *Independence.* Where outcomes cluster (users within accounts, sessions within users), randomize and analyze at the cluster, or allow for it with the design effect.
4. *Acceptable risk.* The treatment cannot expose customers to operational, financial, contractual or regulatory harm. Exposure is bounded and can be rolled back.
5. *The design supports the claim wanted.* An opt-in, invite-only or before-and-after comparison cannot support a causal claim, however large the numbers.

**Design, fixed before the start**

| Item | What to fix |
|---|---|
| Hypothesis | The change, the metric, the direction, the population |
| Primary metric | One, defined exactly, including the time window |
| Baseline | Measured on the same population, with its source and period |
| Smallest effect worth acting on | From a business basis (section 2), not from what the traffic can detect. A test sized on it (section 8) can tell an effect of that size from zero. It is not sized to show the effect is at least that large; if the decision needs that, say so beforehand and size for it |
| Randomization unit | User, account, session; the unit of analysis matches it |
| Inferential framework | Significance level and power, or another framework with its justification |
| Sample size | Per arm, derived (section 8) |
| Duration | Whole weeks, covering the normal cycle and long enough to see past novelty |
| Stopping rule | Stop at the planned sample or date. Stopping at the first significant look inflates false positives; early stopping needs a sequential method chosen beforehand. A pre-set harm limit on a guardrail can stop the test at any time |
| Guardrail metrics | What must not get worse (retention, complaints, revenue, performance), each with a limit |
| Other metrics and segments | Declared in advance. Treated as exploratory, or corrected for multiple comparisons (Bonferroni: α divided by the number of confirmatory comparisons) |
| Valid data | Exclusions defined in advance: bots, staff, duplicates, partial exposures |

**Analysis**

1. *Sample-ratio mismatch first.* If the arms' sizes differ from the planned split by more than chance allows (section 8), don't interpret the result. Find the cause: assignment, logging, or filtering that differs by arm.
2. *Missing and invalid data.* Report exclusions per arm; unequal loss between arms is a warning.
3. *Effect size with its interval,* not a p-value alone. Read the interval against the smallest effect worth acting on:

   | The interval for the effect | Reading |
   |---|---|
   | Lies wholly above the smallest effect worth acting on | The effect is at least that large |
   | Lies above zero and contains the smallest effect worth acting on | There is an effect, and it may or may not be large enough. A test sized by section 8 can show no more than this when the true effect is near that size |
   | Lies above zero and wholly below the smallest effect worth acting on | A real effect, too small to act on |
   | Contains both zero and the smallest effect worth acting on | Inconclusive: the test could not tell |
   | Contains zero and lies wholly below the smallest effect worth acting on | Any effect is smaller than what was worth acting on |
   | Lies wholly below zero | The change made the metric worse |

   Which of the first two readings counts as Continue is a criterion to set before the test.

4. *Guardrails* against their limits.
5. *Novelty.* Look at the effect by week since first exposure, and for new against existing users.
6. *Selection and contamination.* Assignment independent of user choice; no unit in both arms.
7. *Scope.* The result holds for the population, period and metric tested.

Not every experiment needs every item. Use what the design calls for, and say in one line which material ones were left out and why.

### 7.3 When an experiment can't work

Say which limit applies, what the requested analysis could and could not have shown, and offer the alternative.

| Limit | Consequence | Credible alternatives |
|---|---|---|
| Too little traffic | An underpowered test can't separate an effect worth acting on from none | Test a bolder change with a larger expected effect. Measure a nearer step in the funnel with a higher base rate, stated as a proxy. Run longer if conditions are stable. Or rely on use by selected customers plus qualitative value tests, and say the question of scale stays open |
| Random assignment impossible | No causal claim | Use by selected customers with their own before-and-after, labelled descriptive. A phased rollout across comparable groups, with the reasons the groups may differ |
| Dependent observations | Events overstate the sample | Analyze at the account or user level. Report per account |
| Exposure too risky | The harm outweighs the learning | Invite-only use with consent. A Wizard-of-Oz or concierge version for a few customers. A sandbox |
| The design can't support the claim | A causal reading would be wrong | Restate the claim descriptively, for the group measured |

### 7.4 What to measure

Pick metrics from the categories that fit the question; don't default to clicks.

- User behavior: paths, feature use, engagement.
- Business: active users, conversion, retention, lifetime value.
- Financial: price, billings, time to close.
- Performance: load time, uptime.
- Operational and go-to-market cost: support load, cost to acquire.
- Sentiment: satisfaction or NPS surveys. These are stated preferences.

## 8. Calculations

This applies to every derived number, however simple: a rate, a sample size, a duration, an interval, an effect size. A reader must be able to reproduce it without asking anything.

One block per result:

```
**[Quantity]** — [calculated from given inputs / under illustrative assumptions]
Inputs: [name = value and unit (source: given by…, measured in…, illustrative)]
Assumptions: [conventions used, and anything not supplied]
Formula: [...]
Variables: [symbol = meaning, unit]
Substitution: [...]
Steps: [...]
Result: [value, unit, rounding]
Meaning: [what it implies for the decision]
Limits: [what could make it wrong]
```

Rules:

- **Inputs come from the person or their data.** If an essential input is missing (the baseline, the traffic, the smallest effect worth acting on), ask for it. When nobody can answer, compute with values labelled illustrative and say that the result is an illustration: not a plan, and not a finding.
- **The smallest effect worth acting on is a business input** (section 2). Never work it backwards from the traffic available.
- **α = 0.05 two-sided and power = 0.80 are conventions.** List them under Assumptions. Change them when the cost of a wrong call justifies it, and say why.
- **Percentage points** for the difference between two percentages; **percent** for a relative change.
- **Round sample sizes up,** and durations up to whole weeks.
- **A plain rate or ratio may go on one line:** name = substitution = result with its unit. State the source of the counts, the meaning and the limits once for the group. Anything that uses a statistical formula takes the full block.
- **Recompute before returning,** with a code tool when one is available. A short script may accompany a block that runs to more than a few steps.
- **These are normal-approximation formulas for planning.** They are unreliable when a group has few expected successes or failures (a common rule of thumb is fewer than about 10). The final analysis of a real experiment follows the team's analytics tooling or a statistician.

Standard normal values: two-sided α = 0.05 → 1.960; two-sided α = 0.01 → 2.576; power 0.80 → 0.842; power 0.90 → 1.282.

| Purpose | Formula | Notes |
|---|---|---|
| Sample size per arm, two proportions | n = (z_α/2 + z_β)² × [p₁(1 − p₁) + p₂(1 − p₂)] / (p₂ − p₁)² | p₁ = baseline rate; p₂ = p₁ + smallest effect worth acting on (absolute) |
| Sample size per arm, two means | n = 2 × (z_α/2 + z_β)² × σ² / δ² | σ = standard deviation of the metric per unit; δ = smallest difference worth acting on, same unit |
| Duration | days = arms × n / eligible units entering per day | Round up to whole weeks |
| Smallest detectable effect on the sample available | δ ≈ (z_α/2 + z_β) × √(2 × p₁(1 − p₁) / n) | Approximate; n = units available per arm |
| Interval for a difference in proportions | (p̂₂ − p̂₁) ± z_α/2 × √(p̂₁(1 − p̂₁)/n₁ + p̂₂(1 − p̂₂)/n₂) | |
| Interval for one proportion, small sample (Wilson) | centre = (p̂ + z²/2n) / (1 + z²/n); half-width = z × √(p̂(1 − p̂)/n + z²/4n²) / (1 + z²/n) | Use for counts such as "4 of 5" |
| Sample-ratio mismatch | χ² = Σ (observed − expected)² / expected, with arms − 1 degrees of freedom | Investigate when p < 0.001 (a common convention) |
| Clustered units | design effect = 1 + (m − 1) × ICC; effective n = n / design effect | m = average units per cluster; ICC = intraclass correlation. If the ICC is unknown, count clusters |

### Block A: sample size and duration

```
**Sample size per arm** — under illustrative assumptions
Inputs: baseline conversion p₁ = 4.0% (illustrative); smallest effect worth acting on = 0.5 percentage points, so p₂ = 4.5% (illustrative)
Assumptions: two-sided α = 0.05 (z = 1.960); power = 0.80 (z = 0.842); equal arms; users independent
Formula: n = (z_α/2 + z_β)² × [p₁(1 − p₁) + p₂(1 − p₂)] / (p₂ − p₁)²
Variables: n = users per arm; p = conversion rate as a proportion; z = standard normal value, no unit
Substitution: n = (1.960 + 0.842)² × [0.040 × 0.960 + 0.045 × 0.955] / (0.045 − 0.040)²
Steps: 2.802² = 7.851204; 0.0384 + 0.042975 = 0.081375; 0.005² = 0.000025; 7.851204 × 0.081375 = 0.638892; 0.638892 / 0.000025 = 25,555.7
Result: 25,556 users per arm (rounded up); 51,112 in total
Meaning: with fewer users, a true lift of 0.5 points would be missed more than 1 time in 5
Limits: normal approximation; assumes the baseline holds during the test; says nothing about novelty

**Duration** — under illustrative assumptions
Inputs: total sample = 51,112 users (block above); eligible users entering per day = 1,500 (illustrative)
Assumptions: every eligible user is enrolled; traffic is steady
Formula: days = total sample / eligible users per day, rounded up to whole weeks
Substitution and steps: 51,112 / 1,500 = 34.07 days; next whole week = 35 days
Result: 5 weeks
Meaning: the test occupies this traffic for 5 weeks; a shorter run is underpowered
Limits: holidays, campaigns or releases in the window change the baseline
```

### Block B: what the available traffic can detect

```
**Smallest detectable effect** — under illustrative assumptions
Inputs: eligible users per day = 400 (illustrative); longest acceptable duration = 28 days (illustrative); baseline p₁ = 4.0% (illustrative)
Assumptions: two-sided α = 0.05 (z = 1.960); power = 0.80 (z = 0.842); equal arms; users independent
Formula: n = users per day × days / 2;  δ ≈ (z_α/2 + z_β) × √(2 × p₁(1 − p₁) / n)
Variables: n = users per arm; δ = detectable difference as a proportion
Substitution: n = 400 × 28 / 2 = 5,600; δ ≈ 2.802 × √(2 × 0.040 × 0.960 / 5,600)
Steps: 2 × 0.0384 = 0.0768; 0.0768 / 5,600 = 0.000013714; √0.000013714 = 0.0037033; 2.802 × 0.0037033 = 0.010377
Result: about 1.04 percentage points (approximate: uses the baseline variance for both arms)
Meaning: in 28 days the test can reliably detect a move from 4.0% to about 5.0%, a relative lift of about 26% (0.010377 / 0.040 = 0.259). If the smallest effect worth acting on is 0.5 points, the test is underpowered. The sample that effect needs (block A: 51,112) would take 51,112 / 400 = 127.8 days, about 19 weeks
Limits: normal approximation; a 19-week test would also run into seasonality and product changes
```

### Block C: a count from a small round

```
**Interval for "4 of 5 completed"** — calculated from given counts
Inputs: completed x = 4; participants n = 5 (session notes)
Assumptions: 95% level (z = 1.960); participants treated as an independent random sample of the segment, which a convenience sample is not
Formula (Wilson): p̂ = x / n; centre = (p̂ + z²/2n) / (1 + z²/n); half-width = z × √(p̂(1 − p̂)/n + z²/4n²) / (1 + z²/n)
Variables: p̂ = observed proportion; n = participants
Substitution: p̂ = 4 / 5 = 0.8; z² = 3.8416; 1 + 3.8416 / 5 = 1.76832
Steps: centre = (0.8 + 0.38416) / 1.76832 = 0.6697; inside the root = 0.16 / 5 + 3.8416 / 100 = 0.032 + 0.038416 = 0.070416; √0.070416 = 0.26536; half-width = 1.960 × 0.26536 / 1.76832 = 0.2941; 0.6697 − 0.2941 = 0.3756; 0.6697 + 0.2941 = 0.9638
Result: about 38% to 96%
Meaning: five sessions cannot tell a completion rate of 80% from one of 40% or 95%. Small rounds find problems; they don't measure rates
Limits: the random-sample assumption rarely holds in discovery, so the real uncertainty is wider
```

## 9. Feasibility test

**Who.** Engineers investigate and own the conclusion; in *Inspired* that is the tech lead's risk. The product manager supplies the question and what depends on it. If you are asked to help with the investigation using code tools, report what you ran and under which conditions, and leave the conclusion to the engineers responsible.

**Give them time.** A day or two is typical, sometimes with a feasibility prototype: throwaway code that answers the hardest technical question.

**Questions**, as far as each is relevant:

- Do we know how to build it, and does the team have the skills?
- Architecture: does it need changes?
- Dependencies: components, third parties, other teams, legacy systems, and whether the data exists at the quality needed.
- Performance and scale at the quality the product needs.
- Security and privacy.
- Operational constraints: infrastructure, deployment, monitoring, support.
- Effort: how long, given other commitments.
- Cost to build and to run. Feasibility supplies the number; whether the business accepts it is a viability question.

**Say which state was reached:**

| State | What was done | What can be said |
|---|---|---|
| Preliminary engineering assessment | Engineers considered it, perhaps read code or documentation. Nothing was built | "Engineers expect it to be feasible. Unverified. Open questions: …" |
| Feasibility prototype result | Throwaway code answered a named question under stated conditions: data, volume, environment | "Question X answered under conditions Y. Not covered: …" |
| Production-ready solution | Built, hardened and tested under production conditions | Not an outcome of discovery. Never claimed from a prototype |

**Output:** feasible, feasible with conditions, or not feasible as specified, with the alternatives. Always give the state and the conditions next to it. An estimate carries the state it came from; an estimate from a meeting is a preliminary assessment.

**Criteria** for a feasibility prototype usually rest on a business requirement or an operating tolerance (the response time the workflow needs, the accuracy below which users stop trusting the output) and need a stated basis like any other.

## 10. Customer-facing safeguards

Preparing any of these is ordinary planning. Doing them needs authorization for that action from the person or the workflow's instructions (see the skill), and the conditions below.

| Action | Before it happens |
|---|---|
| Contacting customers or prospects to recruit | Where an account has a relationship owner, their agreement. An honest description of the session. Consent to record |
| Sessions that show customer data | Fake or approved data only, under the customer's and your organization's rules for confidential data |
| Collecting real customer data or account access | An approved, secure mechanism and an agreement. Never passwords. The least data that answers the question |
| Showing a price, pilot terms or a letter of intent | Agreement from whoever is authorized to make commercial offers |
| Fake door or landing page | The checks in section 6 |
| Experiment or live-data prototype on production | Bounded exposure, a rollback, guardrails with stop limits, and someone watching them. No operational, financial, contractual or regulatory harm to customers |
| Incentives | Fair, and allowed by the participant's employer's rules in B2B |

## 11. Templates

Drop a field that doesn't apply to the test. Where a field applies and has no answer, write one of the three markers from section 1.

**Test plan**

```
# Test plan: [name]
**Status:** plan only; no test has been run
**Risk:** [value / usability / feasibility]   **Hypothesis:** [who, does or wants what, under which condition]
**Question:** [the one question this test answers]
**Method:** [test type] — [why it is the cheapest credible test for the question]
**Evidence it can yield:** [kind(s)]. It cannot show: [...]
**Participants or population:** [segment and screening criteria; route; how many and why; representative or convenience]
**Artifact:** [prototype type and version, or "needed: [type]"]
**Procedure:** [tasks, treatment or exposure; who runs it; dates if supplied]
**Observed and recorded:** [what is captured, by whom, with what instrumentation]

**Criteria** (set [date] by [who], before results)
| Outcome | Criterion | Basis | Agreed or provisional |
|---|---|---|---|
| Continue | | | |
| Iterate | | | |
| Stop | | | |
| Inconclusive | | | |

**Risks, biases and limits:** [selection, prompting, sample, customer or brand risk]
**Needs authorization before it runs:** [each customer-facing step and whose go-ahead], or n/a
**Missing information:** [what would firm up the plan, and who has it]
```

For an experiment, add:

```
**Experiment design:** primary metric · baseline (source) · smallest effect worth acting on (basis) · randomization unit · α and power · sample per arm · duration · stopping rule · guardrails (limits) · exclusions · checks left out and why
**Calculations:** [blocks in the section 8 layout]
```

**Execution artifacts**, by test:

| Test | Artifacts |
|---|---|
| Usability | Screener, session script, task cards, observation sheet, version log |
| Qualitative value | Question guide (users; buyers), commitment record |
| Demand | Entry-point and disclosure-page copy, instrumentation requirements, exposure plan, note for support and sales |
| Use by selected customers | Access list, instrumentation requirements, check-in guide, per-account record |
| Experiment | Design, logging requirements, guardrail and monitoring plan, analysis plan |
| Feasibility | Question list for the engineers, findings record with the state reached |

**Readout**

```
# Readout: [name], [dates]
**Type:** confirmatory (criteria set [date], before results) / exploratory (no criteria set beforehand)
**Risk:** [...]   **Hypothesis:** [...]
**Original criteria:** [as written, with basis] / none set before the test
**What was done:** [method; who took part against the plan; how recruited; representative or convenience; artifact version(s); departures from the plan]
**Source:** [session notes / recordings / data export / summary reported by ...]

## Observed
[facts, counts and quotes; per version or per account where that applies]

## Evidence
| Kind | Strength for this hypothesis | Why |
|---|---|---|
**Inferred:** [what reasonably follows, as interpretation]
**Alternative explanations and limits:** [...]

## Against the criteria
[each criterion: met / not met / cannot be judged — or "exploratory: no pass or fail"]
[if missed or conflicting: hypothesis / prototype / test design / inadequate evidence / conflicting evidence, and why]

**Decision:** [Continue / Iterate / Stop / Inconclusive] for this hypothesis — [rationale]
**Still uncertain:** [what is unresolved; which of the four risks remain untested]
**Next action:** [what] — addresses [uncertainty]; matters because [...]; proportionate because [...]
```

Add a **Calculations** section only when a number was derived, and experiment analysis (section 7.2) only for an experiment.

**Short readout**, for a usability round or any result supplied in a few lines

```
# [Test]: [name], [dates] — [n] participants ([recruited how; representative or convenience]), prototype [version(s)]
**Type:** confirmatory (criteria: [...]) / exploratory (no criteria set beforehand)   **Source:** [...]
| Task or measure | [v1, sessions 1–3] | [v2, sessions 4–7] | What was seen |
|---|---|---|---|
**Changed between versions:** [...]
**Evidence:** [kind and strength for the hypothesis tested; the main alternative explanation]
**Decision:** [...] — [one line: against the criteria, or a judgment made after the results]
**Not shown:** [what this result does not bear on; for a usability round, value and demand]
**Next action:** [what] — addresses [...]; matters because [...]; proportionate because [...]
```

## 12. Examples

### B2B: usability and value sessions, criteria set beforehand

```
# Readout: auto-approval rules, 3–12 March
**Type:** confirmatory (criteria set 28 February, before results)
**Risk:** usability; value (user side)
**Hypothesis:** controllers at mid-market accounts can set up an auto-approval rule unaided, and want it enough to commit time or reputation
**Original criteria:** Usability: iterate if any controller cannot finish setup unaided because of the design (basis: risk tolerance; a wrong rule approves payments automatically). Value: at least 3 of 6 make a commitment beyond words (provisional: the PM's judgment that fewer than half would not justify a live-data prototype; no benchmark)
**What was done:** usability tasks, then value questions. 6 controllers from 4 discovery-program accounts (convenience sample). Prototype v2 throughout. As planned
**Source:** session notes

## Observed
- 4 of 6 completed rule setup unaided. 2 failed at the amount threshold: both typed a currency symbol and saw no error message.
- 2 of 6 booked a follow-up session and brought their head of internal audit, without being asked.
- 4 of 6 said they would share invoice data. None started their own approval to do so.
- Price: not measured. Buyers: not included.

## Evidence
| Kind | Strength for this hypothesis | Why |
|---|---|---|
| Observed behavior | Strong, for "the threshold field blocks setup" | Same failure and same cause in 2 participants |
| Costly commitment (time, reputation) | Moderate, for user-side value | Unprompted, but 2 of 6, from accounts chosen for their interest |
| Stated intention (data sharing) | Weak | Words only |
**Inferred:** apart from one field, the setup flow can be used. Some controllers want it enough to involve audit.
**Alternative explanations and limits:** discovery-program accounts are more engaged than the market. 6 people are 4 accounts. The audit leads may be coming to object.

## Against the criteria
- Usability: not met. A prototype failure (one field), not a failure of the hypothesis.
- Value (provisional): not met, 2 against 3. Inadequate evidence, not contradiction: the criterion was a judgment and the sample is small.

**Decision:** Iterate on usability. Inconclusive on value.
**Still uncertain:** whether the budget holder will pay; whether audit will accept it. Feasibility and viability untested.
**Next action:** fix the threshold field and rerun setup with 3 new controllers — addresses whether that field was the only blocker; matters because a wrong rule moves money; proportionate because it costs a day of design and three sessions. Separately, sessions with the budget holder at 3 accounts, for the buyer-side question.
```

### B2C: fake door, no criteria set beforehand

```
# Readout: one-tap grocery ordering, fake door, 7 days
**Type:** exploratory (no criteria set beforehand)
**Risk:** value   **Hypothesis:** weekly meal planners want to order their plan's groceries in one tap
**Original criteria:** none set before the test
**What was done:** a tile shown to 5% of weekly planners, with a disclosure page behind it. Assignment method: not provided
**Source:** analytics export

## Observed
- 8,420 users saw the tile. 505 clicked. 312 left an email address after reading that the feature isn't available.

## Calculations
**Click rate** — calculated from given counts
Inputs: clicked = 505 users; saw the tile = 8,420 users (analytics export)
Assumptions: none
Formula: click rate = clicked / saw the tile × 100
Substitution and steps: 505 / 8,420 = 0.05998; 0.05998 × 100 = 5.998
Result: 6.0% (rounded to one decimal)
Meaning: about 1 in 17 people who saw the tile clicked it
Limits: describes these users in this week. There is no reference rate for this placement

## Evidence
| Kind | Strength for this hypothesis | Why |
|---|---|---|
| Demonstrated interest (clicks, emails) | Moderate, for "the offer draws interest among weekly planners" | Behavior, at no cost to the user. Placement and novelty not controlled |
| The same | None, for "they will complete orders or pay" | Not measured |
**Inferred:** the description appeals to some weekly planners.
**Alternative explanations and limits:** curiosity about a new tile; a prominent placement; one week.

## Against the criteria
Exploratory: no pass or fail. A click-rate threshold chosen now would be fitted to the result.

**Decision:** Continue to the next test. A judgment made after seeing the results, not a verdict against criteria.
**Still uncertain:** whether they place orders, and repeat them. Usability, feasibility and viability untested.
**Next action:** invite the 312 to a live-data prototype, with criteria written first — addresses whether interest turns into orders; matters because the partner integration is the main cost; proportionate because it reuses people who already raised their hand. Also measure the click rate of an existing tile in the same position, to give the next demand test a baseline.
```
