# Risk test catalog

Ordered from cheapest to most expensive within each risk. Pick the cheapest test that would actually change the decision. If a cheap test cannot produce a result that would change the decision, it is not worth running.

## Value risk

| Test | Effort | What it tells you | Notes |
|---|---|---|---|
| Problem sizing: pull the customer's data or shadow their workflow to measure frequency, time and error cost | Days | What the problem costs them today, from measured inputs | Do this first when the sizing rests on assumptions. In B2B, ask the customer for their own numbers. |
| Customer interviews on the problem | Hours | Whether the problem exists, how they solve it now, what switching takes | Says nothing about this solution. |
| Concierge test | Days | Whether doing the job for them, by hand, produces value they notice | Good for B2B workflows and services. |
| Demand test (fake door, landing page) | Days | Whether people try to get it | Needs traffic. Use carefully with enterprise customers (see inspired-discovery-testing). |
| Qualitative value test on a user prototype | Days | Whether users would pay, recommend, spend time, or give access | Run after a usability check in the same session. |
| Live-data prototype + A/B or invite-only test | 1–3 weeks | Whether behavior actually changes | The strongest evidence short of shipping. |
| Reference customers (discovery program) | Weeks to months | Whether real customers will run it and vouch for it | B2B default for anything significant. |

### Value signals (stronger than "I like it")

When testing value with people, ask for something that costs them. The four kinds of cost:

- **Money:** will they pay, sign a letter of intent, pre-order, or move budget?
- **Reputation:** will they recommend it to a colleague or their boss, or share it publicly?
- **Time:** will they commit time to work with you on it, or schedule the next session?
- **Access:** will they give you their data, credentials, or system access so it can work for real?

A person who says it is great but gives none of these has not shown value.

## Usability risk

| Test | Effort | What it tells you |
|---|---|---|
| Walkthrough with the team on a low-fidelity prototype | Hours | Obvious flow problems |
| Usability test on a user prototype with target users | Days | Whether users complete the key tasks unaided |
| Usability test on a live-data prototype | 1–2 weeks | Behavior with real data and edge cases |

## Feasibility risk

| Test | Effort | What it tells you |
|---|---|---|
| Engineer review with time to investigate (not a meeting answer) | Hours to a day | Known vs unknown parts, rough options |
| Feasibility prototype (throwaway code on the risky part only) | A day to a few days | Whether the hard part works: performance, scale, algorithm, third-party or legacy integration |
| Spike against real data volumes | Days | Whether it holds at production load |

Common feasibility unknowns: a new technology to the team, performance or scale, an algorithm or model whose quality is uncertain, third-party or partner components, legacy system changes, dependent changes by other teams, infrastructure cost.

## Business viability risk

| Test | Effort | What it tells you |
|---|---|---|
| Show the prototype one-on-one to each relevant stakeholder | Hours each | Whether legal, finance, sales, security, marketing etc. can live with it |
| Buyer test (B2B), separate from the user test | Days | Whether the person who signs will pay, and through which budget |
| Pricing or packaging test | Days to weeks | Whether the monetization works |

See inspired-stakeholders-viability for the full stakeholder procedure.

---

## Worked example — B2B

**Idea:** Ledgerline, a procurement SaaS for mid-size companies, wants to auto-approve invoices under $500 when they match a purchase order. Source: three large customers asked for it in renewal calls.

**Problem statement:** Accounts-payable clerks at mid-size companies spend hours a week approving small invoices that almost always match, which delays payment and annoys suppliers.

| Risk | The question for this idea | Evidence today | Rung | Rating (confidence) | Owner |
|---|---|---|---|---|---|
| Value: users | Will AP clerks' time actually go down? How many small invoices are clean matches? | Three requests; no invoice data | 1 | High (medium) | PM |
| Value: buyer | Will controllers turn it on, and will their own auditors and internal controls allow automatic approval? | Unknown; no controller asked | 0 | High (low) | PM |
| Usability | Can a controller set rules and see what was auto-approved without support? | None | 0 | Medium (medium) | Designer |
| Feasibility | Is our PO matching accurate enough on messy line items? | Matching exists for exact matches only | 1 | Medium (low) | Tech lead |
| Viability | Does auto-approval shift liability for wrong payments onto us? Do our terms and our own security policy allow it? | Not yet discussed with legal | 0 | High (low) | PM |

**Dependencies between risks:** if legal requires customers to own the rules (viability), the rules screen must make ownership explicit (usability).

**Value of solving it (per customer, per year; all inputs assumed until test 2):**
| Driver | Input | Source | Range |
|---|---|---|---|
| Clerk time on small invoices | 1,000–1,500 invoices/month × 2–4 min × $45/h loaded | Assumed | $18k–$54k |
| Late-payment penalties and lost early-pay discounts | | Assumed | $5k–$20k |
| Share removed by auto-approval | 50–80% of clean matches | Assumed | |
| Switching cost | Rule setup, audit sign-off | Assumed | ~1 week of controller time |
| **Net value** | | | **~$10k–$55k** |

Compared with a planned add-on price of $12k a year, the low end barely covers the price, so sizing from real invoice data comes first.

**Ranking:** 1. Value, buyer side (an audit objection inside the customer kills it regardless of anything else), 2. Viability (liability), 3. Value, users, 4. Feasibility, 5. Usability.

| # | Risk | Test | Effort | Kill / change criterion |
|---|---|---|---|---|
| 1 | Value (buyer) | Two customer controllers and their audit teams review a mock audit log | 1 week | Kill if auditors require human approval at any amount |
| 1b | Viability | Legal reviews liability and terms, in parallel | 1 week | Change the design if legal requires customer-owned rules |
| 2 | Value (users) | Pull 3 months of invoice data from 6 customers; count clean small matches | 3 days | Change scope if fewer than 30% of invoices qualify |
| 3 | Feasibility | Feasibility prototype on fuzzy line-item matching against that data | 1 week | Change approach if false matches exceed an agreed threshold |
| 4 | Usability | Usability test of the rules screen with 5 controllers | 1 week | Iterate the design until most complete setup unaided |

**Decision:** Test first. The buyer side of value and our liability are both at rung 0, and either could make the rest moot.

## Worked example — B2C

**Idea:** Pantrypal, a meal-planning app, wants to add one-tap grocery ordering of the week's ingredients through a delivery partner. Source: CEO, after a competitor launched it.

**Problem statement:** Users who plan meals still spend 30+ minutes building a grocery order by hand, and some abandon the plan.

| Risk | The question for this idea | Evidence today | Rung | Rating (confidence) | Owner |
|---|---|---|---|---|---|
| Value | Will users order groceries through us instead of their usual store or app? | Competitor launch (says nothing about our users) | 1 | High (medium) | PM |
| Usability | Can users fix substitutions and quantities quickly? | None | 0 | Medium | Designer |
| Feasibility | Can the partner API map our ingredients to store products reliably? | Partner docs only | 1 | Medium (low) | Tech lead |
| Viability | Does the partner's revenue share cover our costs? Brand risk from bad deliveries? | Draft term sheet | 1 | Medium | PM |

**Dependencies between risks:** none significant.

**Value of solving it (per user, per year):** 30–45 minutes a week building an order × 50 weeks ≈ 25–37 hours, plus food wasted from abandoned plans. Users already get free ordering from their grocery app, so the value is only the time saved over that free alternative: maybe 10–20 minutes a week. All inputs assumed. That small margin is why value ranks first.

**Ranking:** 1. Value, 2. Feasibility, 3. Viability, 4. Usability.

| # | Risk | Test | Effort | Kill / change criterion |
|---|---|---|---|---|
| 1 | Value | Fake-door "Order these ingredients" button shown to 5% of weekly planners | 1 week | Stop if click-through is below the threshold the team agrees on beforehand |
| 2 | Feasibility | Feasibility prototype mapping 200 recipes' ingredients through the partner API | 3 days | Change approach if the mapping is not usable without manual fixes for most recipes |
| 3 | Viability | Finance models the term sheet on test click-through; partner contract reviewed by legal | 1 week | Renegotiate or stop if unit economics are negative |
| 4 | Usability | Usability test of the substitution screen with 6 users | 1 week | Iterate until users complete an order unaided |

**Decision:** Test first. A competitor launching it is not evidence that our users want it.
