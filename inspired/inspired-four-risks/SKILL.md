---
name: inspired-four-risks
description: Assess a product idea, feature request or initiative against the four product risks from Marty Cagan's Inspired (value, usability, feasibility, business viability), rank them, and pick the cheapest test for each before anything is built. Use whenever someone proposes a feature or product, asks "should we build this", "what could go wrong", "is this worth doing", wants to de-risk an idea, or is about to commit engineering time to an exec, sales or customer request, even if they never mention Cagan or risk. Works for B2B and B2C. It plans what to learn; for running the tests use inspired-discovery-testing, for designing the prototype use inspired-prototype-design.
---

# Four Risks Assessment

In *Inspired*, discovery exists to resolve risk before the team writes production code. Most ideas fail, and the ones that work usually need several iterations, so the expensive mistake is building first and learning after. This skill turns an idea into a ranked risk map and a test plan. It does not judge whether the idea is good. It decides what has to be learned first, and the cheapest way to learn it.

## Inputs

Ask only for what is missing. If the person is not available to answer, state your assumptions at the top of the output and continue.

1. The idea in one sentence, and where it came from (executive, sales, a customer request, data, the team).
2. Who it is for: the user and, in B2B, the buyer if different.
3. The business result it is supposed to move.
4. What is already known: data, research, past attempts, competitor moves.
5. Hard constraints: dates, contracts, regulation, platform or partner dependencies.

## Procedure

1. **Restate the idea as a problem.** Write: "[target user] struggles to [problem], which costs them [consequence]." If you cannot write this sentence, say so. A solution without a clear problem is itself the biggest value risk.
2. **Read `references/risk-definitions.md` before rating anything.** Each risk has a definition, what belongs to it and what doesn't, an evidence ladder, and a rating rule. In short:
   - **Value:** will customers buy it, or users choose to use it, over what they do today?
   - **Usability:** can users figure out how to use it?
   - **Feasibility:** can engineers build it with the time, skills, technology and data available?
   - **Business viability:** does it work for the rest of our business (sales, marketing, finance, legal, compliance, security, partners, support, strategy)?
3. **Sort the issues.** List every concern about the idea, then put each one under exactly one risk using the boundary rules in the definitions file. An issue counted under two risks inflates both.
4. **Size the value.** Before rating value, estimate what the problem costs the customer today and how much of that cost the solution removes, using the method in the definitions file. Use ranges and tag the source of every input. If the inputs aren't available, size it with stated assumptions and make "measure the problem's cost" the first test.
5. **Rate each risk separately.** For each risk in turn, look only at the issues and evidence filed under it: write the specific question this idea raises, place the evidence on that risk's ladder (rung 0–5), and apply the rating rule. Don't let one risk's rating move another's. A strong value case doesn't make the build easier, and a hard build doesn't make customers want it less. If you can spawn subagents, you may give each risk to its own agent with only the idea, the inputs, the definitions file and that risk, so the ratings stay independent.
6. **Reconcile.** Only after all four are rated, note where one answer changes another's question. For example, a compliance condition (viability) may forbid sending data to an outside model, which changes the feasibility question. Record the dependency; re-rate only if the dependency changes the evidence.
7. **Assign an owner per risk.** The product manager owns value and viability, the designer owns usability, the tech lead owns feasibility. If one of those roles is missing from the team, say which risk is therefore probably under-assessed.
8. **Rank the risks.** Value usually comes first, because it is where most ideas die and because every other test is wasted if nobody wants the thing. Override that default only with a reason (for example, a regulated feature where viability decides everything). Do not leave all four at Medium; force an order.
9. **Pick the cheapest test that could change the decision** for each High or Medium risk. Use the catalog in `references/risk-tests.md`. Each test should aim to move its risk up at least one rung of the evidence ladder. For each test, write the kill or change criterion before the test runs, so the result cannot be rationalized afterward.
10. **Recommend a decision:**
   - Stop now (a High risk with strong negative evidence already).
   - Test before committing (the usual answer).
   - Build with the risk accepted (only when all risks are Low, or when the test costs more than building and undoing).
   - Split the idea (one part is low risk and can ship; another needs discovery).

## Output

Use this structure:

```
# Four risks: [idea]

**Problem statement:** [user] struggles to [problem], which costs [consequence].
**Source of idea:** [...]   **Business result targeted:** [...]
**Assumptions made:** [only if inputs were missing]

| Risk | The question for this idea | Evidence today | Rung (0–5) | Rating (confidence) | Owner |
|---|---|---|---|---|---|
| Value (B2B: buyer and user rows) | | | | | PM |
| Usability | | | | | Designer |
| Feasibility | | | | | Tech lead |
| Viability | | | | | PM |

## Value of solving it (per [account / user], per year)
| Driver | Input | Source (said / observed / measured / assumed) | Range |
|---|---|---|---|
| Cost of the problem today | | | |
| Share removed by the solution | | | |
| Switching cost | | | |
| **Net value of solving it** | | | |

**Compared with:** price we'd charge [...]; current alternative [...]; number of customers with the problem at this size [...] (not a revenue forecast).

**Dependencies between risks:** [from step 6, or "none"]

**Ranking:** 1. ... 2. ... 3. ... 4. ... — [one line on why]

## Tests, in order
| # | Risk | Test | Effort | Kill / change criterion (set before running) |
|---|---|---|---|---|

**Decision:** [stop / test first / build with risk accepted / split] — [two lines of reasoning]
**What would change this assessment:** [the one or two facts that would flip it]
```

## Checks before returning

Re-read the output and fix it if any of these are true:

- **A customer request is counted as proof of value.** Customers describe solutions; they rarely know what is possible. A request is evidence that a problem exists, not that this solution has value.
- **Feasibility is rated from a meeting.** "Engineering said it's doable" without giving engineers time to investigate is not evidence. Note it as an assumption.
- **Viability is pushed to the end** ("legal will review before launch"). Stakeholder constraints shape the solution, so they belong in discovery.
- **A test cannot fail.** Every test needs a criterion written before it runs.
- **Users liking a prototype is treated as value.** Liking a demo proves little; a value test asks for something of real cost (money, time, reputation, access). See `references/risk-tests.md`.
- **A business case with revenue projections is used as evidence.** Before discovery, both the revenue and the cost in a business case are guesses.
- **Value rated without sizing the problem**, or sized as a single number with no source per input.
- **The sizing turns into a revenue forecast for us.** Size the customer's problem; don't project our revenue.
- **A large problem cost is counted as value without checking how much the solution actually removes**, or without subtracting the switching cost.
- **Every risk is rated the same.** Rank them.
- **An issue appears under two risks.** Move it to one, using the boundary rules.
- **A rating doesn't match its rung.** A High or Low that the rating rule wouldn't give needs a stated reason, or it's wrong.
- **The B2B value row merges buyer and user.** Split it.

## B2B and B2C differences

- **B2B:** the buyer is often not the user, so value needs two answers: will users use it, and will the buyer pay for it. The customer's procurement, security review and internal compliance go under value (buyer side), since they decide whether the customer buys. Our contracts, our legal and regulatory obligations, and how our sales team gets paid go under viability. With few customers, tests are mostly qualitative and run with a small set of reference customers.
- **B2C:** traffic allows quantitative tests (demand tests, A/B tests). Viability includes brand, app-store policies, privacy law, and monetization. Value risk is mostly about switching from a current habit or a free alternative.

## Reference

- `references/risk-definitions.md`: definitions, what belongs to each risk, evidence ladders, boundary rules and the rating rule. Read it at step 2, every time.
- `references/risk-tests.md`: the test catalog by risk and cost, value signals, and two worked examples (one B2B, one B2C). Read it at step 9, or when the person wants an example.
