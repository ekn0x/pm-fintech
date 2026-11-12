# Risk definitions

Each risk below has: the definition (from *Inspired*), the question to ask, what belongs to it, what belongs to another risk, an evidence ladder, and how to rate it. The boundary rules at the end decide where an issue goes when it seems to fit two risks. Every issue goes in exactly one risk.

**Source:** only the one-line definitions come from *Inspired*. The book doesn't set boundaries between the risks, evidence ladders, a method for sizing value, or a rating rule; those are added here so ratings stay consistent and independent. When explaining a rating to the user, don't attribute these rules to Cagan.

---

## Value risk

**Definition:** whether customers will buy it, or users will choose to use it.

**Question:** will the target customer choose this over what they do today, including doing nothing, often enough to matter?

**Belongs here:**
- Whether the problem exists, and whether it matters enough to act on.
- Whether this solution solves it better than the current alternative, by enough to switch.
- Willingness to pay, at a price, from the customer's side.
- B2B: whether the buyer will buy and whether users will use it. Rate them separately; both must hold.
- B2B: constraints inside the customer's organization that stop the purchase or the use, such as their procurement, their security review, or their internal compliance policy.

**Belongs elsewhere:** users who want it but can't figure it out → usability. Whether we can build it → feasibility. Whether the price covers our costs, or whether our own legal, sales or partners can live with it → viability.

### Sizing the value: what the problem is worth to the customer

Rating value means knowing how much the problem is worth to the customer, not only whether it exists. Size it in two parts.

**1. Cost of the problem today**, for one customer (B2B: one account; B2C: one user), per year. Count only the drivers that apply:
- **Time:** people affected × how often × time per occurrence × loaded cost per hour.
- **Errors:** how often they happen × cost per error (rework, write-offs, penalties, bad fills or worse prices).
- **Lost revenue or opportunity:** deals, trades, sales or customers lost because of the problem.
- **Risk:** the size of a regulatory, audit, security or reputational exposure × how likely it is.
- **Spend on the current workaround:** other tools, contractors, headcount, manual services.
- **B2C, where money is the wrong unit:** frequency × intensity (time lost, stress, money wasted), and what they pay today for alternatives.

**2. Value of solving it** = the share of that cost the solution actually removes, minus the customer's cost to switch (migration, training, integration, contract changes, habit).

**Then compare:**
- The value of solving it against the price we would charge. If value isn't several times the price, the customer has little reason to switch.
- The value against the current alternative. "Doing nothing" or a free workaround already captures some of the value.
- In B2B, value per account against the cost of the buyer's approval effort. Small value doesn't justify a long procurement.
- Across the target market: how many customers have the problem at this size. That number belongs to the decision, but **it is not a revenue forecast**. A forecast of our revenue is a guess before discovery; the cost of a customer's problem can be measured now.

**Rules for the numbers:**
- Give ranges, not point estimates, and a source for every input: customer said / we observed / we measured in data / assumed.
- An input tagged "assumed" caps value evidence at rung 1, however large the number.
- Prefer the customer's own numbers, from their data or their workflow, over our estimates.
- If the problem can't be sized at all, say so. A problem nobody can put a cost on is usually a weak problem.

**Sizing evidence ladder (alongside the main ladder):**
- Guessed by us → stated by the customer → observed in their workflow → measured from data → confirmed by a commitment proportional to the size (a budget line, a price accepted, a letter of intent).

**Evidence ladder (weakest to strongest):**
0. Assumption: nobody has checked.
1. Opinion: a feature request, "I'd use it", an executive's belief, a competitor having it, praise for a prototype.
2. Problem evidence: interviews or data showing the problem and the current workaround, with the problem's cost sized from customer-stated, observed or measured inputs.
3. Costly commitment: money, time, reputation or access given before the product exists (see risk-tests.md). A money commitment counts more when it is in proportion to the sized value.
4. Behavior: usage of a live-data prototype, demand-test clicks, A/B results.
5. Production use by reference customers who will vouch for it.

---

## Usability risk

**Definition:** whether users can figure out how to use it.

**Question:** can the target users complete the key tasks without help, at the speed and accuracy their context demands?

**Belongs here:**
- Whether users can find, learn and complete the key tasks.
- Error rate, and whether users notice and recover from mistakes.
- Efficiency for expert or frequent users (traders, operators, power users), not only first use.
- Accessibility.

**Belongs elsewhere:** users who could use it but don't want to → value. Slowness caused by the system → feasibility. Whether the company can afford the training or support load → viability.

**Evidence ladder:**
0. Assumption.
1. The team's walkthrough of a design.
2. A usability test on a prototype with target users.
3. Repeated usability tests after iterating, with task completion recorded.
4. Task completion and error data from a live-data prototype.

---

## Feasibility risk

**Definition:** whether engineers can build it with the time, skills, technology and data available.

**Question:** can we build and run it at the quality needed (accuracy, performance, scale, reliability) within an acceptable time?

**Belongs here:**
- Technology new to the team; skills the team lacks.
- Architecture changes; dependencies on third parties, partners or other teams; legacy systems.
- Performance and scale; data availability and quality.
- Algorithm or model quality (for example, whether an AI output is accurate enough).
- Build time and the cost to run, stated as an estimate.

**Belongs elsewhere:** whether the cost to run is acceptable to the business → viability (feasibility provides the number; viability judges it). Whether we are allowed to build it → viability.

**Evidence ladder:**
0. Assumption.
1. An answer given in a meeting, without investigation.
2. Engineers investigated and identified the known and unknown parts.
3. A feasibility prototype answered the hardest technical question.
4. Tested against production data volumes or real integrations.

---

## Business viability risk

**Definition:** whether the solution works for the various parts of our business.

**Question:** can our business sell, market, support, fund, legally offer and secure it, consistent with its strategy and partners?

**Belongs here:**
- Sales: can our channel sell it; does it fit pricing, deal structure and compensation?
- Marketing and brand.
- Finance: unit economics; whether the cost to run is covered by revenue.
- Legal, regulatory and compliance obligations on us, including laws that apply to the product itself.
- Our own security policy.
- Partners and contracts.
- Customer success and support capacity.
- Fit with the company's strategy and executives' bets.
- Whether it is a one-customer special the company will maintain alone.

**Belongs elsewhere:** whether customers want it → value, even when a stakeholder claims they do. The customer's own procurement or compliance blocking a purchase → value (buyer side).

**Evidence ladder:**
0. Assumption: no stakeholder has been asked.
1. A stakeholder said something in passing, or reacted to a slide.
2. One-on-one preview of the prototype with each relevant stakeholder.
3. Written acceptance or conditions from each blocking stakeholder; a financial model using tested numbers.
4. Proven in a live pilot: deals closed, support load measured, audit passed.

---

## Boundary rules

When an issue seems to fit two risks:

| Issue | Goes to | Why |
|---|---|---|
| Will the customer pay this price? | Value | It's the customer's choice. |
| Does that price cover our costs? | Viability | It's our business. |
| Users can't do it vs. users won't do it | Usability vs. value | Test: if it were effortless, would they? If yes, it's usability. If no, it's value. |
| The cost to build or run | Feasibility gives the estimate; viability judges it | Keeps the number separate from the judgment. |
| Slow system | Feasibility (can we make it fast?) | Whether that speed is acceptable to users goes under usability. |
| Training needed | Usability (users can't learn it unaided) | Whether we can afford the onboarding goes under viability. |
| The customer's procurement, security review or internal policy | Value (buyer side) | It decides whether they buy. |
| A law or regulation that applies to offering the product | Viability | It's our ability to offer it. |
| A stakeholder's opinion about what customers want | Value, at rung 1 | Stakeholders hold constraints, not evidence of customer value. |

If an issue truly spans two risks, record it under the one where the decision to stop or change would be made, and mention it in the other row.

---

## How to rate

Rate each risk from its evidence rung and from what happens if it fails. Don't rate a risk by how good the idea looks overall.

| Rating | When |
|---|---|
| **High** | Evidence at rung 0–1, and failure would kill the idea. Also any rung where the evidence points the wrong way. For value: also when the sized value of solving it is not clearly above the price plus the switching cost. |
| **Medium** | Evidence at rung 0–1 where failure would change the solution rather than kill it; or rung 2 where failure would kill it. |
| **Low** | Evidence at rung 3 or above, pointing the right way; or failure would be cheap to fix after launch. |

Confidence says how sure you are of the rung itself. For example, a second-hand report that "the client requires it" is rung 1 with low confidence until someone talks to the client.
