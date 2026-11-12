---
name: inspired-discovery-testing
description: Plan discovery tests, prepare what a team needs to run them, and read out their results, using the testing techniques in Marty Cagan's Inspired (2nd ed.) - usability tests on prototypes, qualitative value tests, demand tests (fake door, landing page), quantitative value tests (customers using a live-data prototype, A/B experiments) and feasibility tests with engineers. Sets decision criteria before a test, states how strong the evidence is and what it can and cannot establish, and recommends continue, iterate, stop or inconclusive. Use whenever someone wants to validate an idea or hypothesis, test a prototype, run a fake-door, pilot or A/B test, write a test plan or session script, size an experiment, interpret results or decide what a test proved, even if they never mention Cagan. B2B and B2C. Does not rank risks (inspired-four-risks), specify prototypes (inspired-prototype-design) or assess business viability (inspired-stakeholders-viability).
---

# Discovery Testing

A discovery test answers one question about a product idea before the team commits to building it. *Inspired* tests usability, value, feasibility and business viability separately, because each needs a different method and fails in a different way. This skill covers the first three; viability is tested with stakeholders in another skill.

The aim is to reduce uncertainty, not to show that an idea is good or bad. That takes three things: a test whose result could change what the team does, an accurate account of what the evidence establishes, and a next step in proportion to it. The two errors this skill exists to prevent are reading a usability result as proof of value, and reading a number as stronger evidence than it is.

## Three modes

Work out the mode from what was supplied. Planning and analysis need no permission: do them with what you have and state your assumptions.

| Mode | When | You produce |
|---|---|---|
| **Planning** | An idea, hypothesis or prototype, and no results | A test plan |
| **Execution support** | The team is going to run the test | What they need to run it: session script, tasks, observation sheet, participant instructions, screener, instrumentation requirements |
| **Analysis and readout** | Genuine results: session notes, recordings, transcripts, data exports, or data you can retrieve with tools you were given | A readout |

Running a test is the team's work unless you have tools that do it and authorization to use them.

- **Use tools only for what they actually do, and report exactly what you ran.** Querying analytics you were given access to, or analyzing a supplied export, is ordinary analysis.
- **Anything customers or outsiders will see or feel needs explicit authorization for that action:** contacting participants or customers, changing production, launching an experiment or a fake door, making a commercial offer. Authorization comes from the person, or from the instructions of the workflow you are running in. Without it, prepare the step, stop there, and say what is waiting for whose go-ahead.
- **A readout contains only what is in the material supplied or retrieved.** Never invent participants, quotes, observations, counts or measurements, and never describe a planned test as if it had happened. Asked to "run" or "conduct" a study with no participants, results or tools, return the plan and the execution artifacts and say plainly that no test has been run.
- **Simulated users are not evidence.** If asked to rehearse a script or predict reactions, label the output a rehearsal and keep it out of any readout.

## Evidence integrity

A result is worth what its evidence can establish for the hypothesis in question, and no more. Six kinds of evidence turn up in discovery:

| Kind | Examples | Can support | Cannot support alone |
|---|---|---|---|
| **Stated preference or intention** | "I'd use it", "I'd pay for that", survey answers, praise, reactions to a demo | What people say about the problem and the idea | That they will buy, use or switch |
| **Demonstrated interest** | Fake-door click, waitlist or landing-page sign-up, agreeing to a follow-up | That the offer drew attention from the people exposed | Purchase intent, or use once the novelty is gone |
| **Costly commitment** | Deposit, pre-order, signed letter of intent, paid pilot, public reference, time from scarce people | Willingness to give something up, in proportion to what was given | Adoption afterwards. A pilot agreement is willingness to evaluate |
| **Observed product behavior** | Task completion in a session; repeated use of a live-data prototype in real work | That these people could or did do this, in this setting | That others will, or that the product caused a business result |
| **Descriptive quantitative** | Usage counts, completion times, conversion, adoption or retention among those measured | How much and how often, for the group measured | Claims about the whole market, or about cause |
| **Experimental** | A randomized controlled experiment | That the change caused the measured difference, if the design and analysis are valid | Anything beyond the population, period and metric tested |

These are kinds, not a ladder. Which one counts depends on the hypothesis: a watched task failure answers a usability question better than any experiment could, and only a commitment or a purchase answers "will they pay".

Every readout answers five questions:

1. What was directly observed?
2. What can reasonably be inferred from it?
3. How strong is the evidence for this hypothesis?
4. Which alternative explanations remain plausible?
5. What is still unresolved?

Reaching a pre-set threshold never makes a hypothesis supported by itself. The evidence also has to be the right kind for the hypothesis, come from the target segment, and not be explained more simply by something else: who was recruited, how they were prompted, novelty, or a few accounts producing most of the activity. Write "supported for [whom], under [conditions]", with its strength, in place of "validated" or "proven". Section 1 of `references/test-protocols.md` has the assessment method.

## Pick the test

| Question | Test | It yields |
|---|---|---|
| Can target users work out how to use it? | **Usability test** on a user or live-data prototype | Observed behavior in a session |
| Why would they value it, and will they commit anything? | **Qualitative value test**, usually straight after the usability tasks | Stated reasons; costly commitments if obtained |
| Does the offer draw interest? | **Demand test**: fake door or landing page | Demonstrated interest |
| Do customers use it in their real work once they have it? | **Live-data prototype in use** by discovery-program or invited customers | Observed behavior and descriptive numbers |
| Does it cause a change in a metric across the user base? | **Controlled experiment** (A/B) on a live-data prototype | Experimental evidence, if valid |
| Can we build it? | **Feasibility test**: engineers investigate, often with a feasibility prototype | An engineering finding |
| Does it work for our business? | Not this skill: `inspired-stakeholders-viability` | |

*Inspired* lists A/B tests, invite-only tests and discovery-program use together as quantitative value testing. All three are kept here; the fourth and fifth rows separate them by what they can show.

Choose the cheapest test that is credible for the question: one whose result, whichever way it goes, would change what the team does next. A test that cannot bear on the hypothesis is waste however little it costs.

**Numbers come in two strengths.** Descriptive numbers say how much and how often for the group measured. Inferential claims, about the whole population or about cause, need a design that supports them: enough independent units, and for cause, random assignment. So use of a live-data prototype is behavioral evidence, not population-level demand. Invite-only access is a way to recruit and deploy, not an experimental design. A live-data prototype is not an A/B test unless users are randomly assigned. Many events from a few accounts are still a few accounts.

**Don't force an experiment where it can't work.** When traffic is too low, random assignment is impossible, observations depend on each other, or the exposure is too risky for customers, say so, say what the requested analysis could and could not have shown, and recommend the most credible alternative (section 7.3).

## Before the test

A plan establishes five things. Where one can't be established from what was supplied, write what is missing; don't fill it in.

1. **Risk, hypothesis and question.** The hypothesis is a claim that could turn out false: who, does or wants what, under which condition. If the person arrives with an idea and no named risk, state in one line the risk and hypothesis you are testing and proceed. Ranking the idea's risks is a different job (`inspired-four-risks`).
2. **Who.** The target segment as screening criteria, the recruitment route, and the bias that route brings. Say whether the sample represents the segment or is a convenience sample. Size it for the method (section 3); no participant count fits every test.
3. **What they will use.** The artifact and its version. If no suitable prototype exists, name the type the test needs and stop there (`inspired-prototype-design` specifies it).
4. **What will be observed,** and how it is recorded or instrumented.
5. **Decision criteria, written before any result is seen:** what would mean continue, iterate or stop, and what would make the test inconclusive.

### Criteria and thresholds

Every threshold needs a stated basis: historical performance, an established benchmark, a business requirement, a user or operational risk tolerance, the smallest effect that would matter economically, or a judgment recorded as provisional because nothing stronger exists.

- **Criteria that already exist** (from a risk assessment, a prototype spec or the person) are the original criteria. Use them as written, add only what makes them measurable, and say what you added.
- **A threshold with no basis is not accepted as justified,** whether it is yours or the person's. Ask what it rests on. Keep the person's number as theirs, label it provisional, and say what would ground it. Never swap in a number of your own.
- **If nothing supports a threshold, don't manufacture one.** Name the missing information. Then either propose an exploratory test (observe first, set criteria for the next round from what is learned), or write the criterion by what will be observed and leave the number for the person to set. Say what would make it firm.
- **"Provisional" is a label, not a basis.** A provisional criterion says whose judgment it is and why that level and not another. If you can't give a reason for a number, don't write the number.
- **A criterion need not be a number.** For a small qualitative test, "any target participant fails the core task because of the design" is clearer and more honest than a percentage. With a handful of participants, write counts ("4 of 5"), not percentages.

## Reading results

1. **Record what actually happened:** who took part against who was planned, on which artifact version, and where the sessions or the data departed from the plan. Tie every observation and count to the supplied material. Where you were given only someone's summary, say so ("reported by the PM; notes not seen"). Mark each gap as *not provided*, *not measured* or *not applicable*; they mean different things.
2. **Keep versions apart.** Findings from materially different versions of a prototype are reported per version and never pooled into one count.
3. **Compare with the original criteria.** If none were set before the results, the readout is exploratory: report what was observed and how strong it is, give no pass or fail, and don't derive thresholds from the results. If criteria were changed after results were seen, show the evaluation against the original ones first and label the new one retrospective.
4. **Assess the evidence** with the five questions above.
5. **Diagnose a miss before deciding.** When a criterion is missed or the signals disagree, say which of these it is: the *hypothesis* failed (the claim looks false for this segment); the *prototype* failed (the idea did not get a fair test); the *test design* failed (wrong participants, leading moderation, broken instrumentation); the evidence is *inadequate* (too little or too unrepresentative to tell); or the evidence *conflicts* (enthusiasm in words, no return visits and no commitments). When words and behavior disagree on the same question, behavior carries more weight, and the disagreement is reported, not averaged away.
6. **Decide, for the hypothesis tested:**

   | Decision | When |
   |---|---|
   | **Continue** | The criteria were met and the evidence is strong enough, for this hypothesis, to justify the next investment |
   | **Iterate** | The findings point to a specific change in design, positioning or assumptions |
   | **Stop** | The evidence sufficiently contradicts the hypothesis, or establishes a constraint that can't be accepted |
   | **Inconclusive** | There is not enough reliable evidence to choose. A valid outcome; say what would resolve it |

   The decision covers the hypothesis, not the whole idea. A missed threshold does not by itself end the idea, and a met threshold does not by itself prove value. In an exploratory readout a decision can still be recommended on the evidence, labelled as a judgment made after seeing the results.
7. **Recommend the next action,** saying which uncertainty it addresses, why that uncertainty matters to the decision ahead, and why the action is in proportion to the remaining risk and its cost. Say also which of the four risks this test left untested.

## Rules by test

Protocols, scripts and artifacts for each are in the reference file.

**Usability.** Realistic tasks stated as goals, neutral moderation, and attention to what the participant does. Don't lead or rescue: when they are stuck, ask what they expected. Thinking aloud helps in most sessions and is optional; drop it where it would distort the task (timed or expert work) and ask afterwards. The prototype may be improved between sessions; log each material change and which sessions it applies to. A usability result says whether people can use it, never whether they want it.

**Qualitative value.** Once the participant understands the product, find out what they would give up for it: money, reputation, time or access, the four signals in *Inspired*. Separate what they say they would do from what they actually commit, and look for a commitment in proportion to the claim: a hypothesis about an annual contract is not supported by a promise to take another call. Never ask for passwords, credentials or confidential data as a test of interest. Access means agreeing to proceed through an authorized, secure mechanism, and data sharing or commercial commitments go through whoever is authorized to arrange them.

**Demand test.** A fake door or landing page measures interest among those exposed. Say at once and honestly that the feature isn't available, never state or imply that it is in anything a customer relies on, and never take payment or data for something that doesn't exist without saying so. Weigh trust, customer expectations and brand before running one, and keep the exposure small and short. For enterprise or named accounts, agree it first with whoever owns the account relationship.

**Quantitative value.** Decide first which claim is wanted: use by selected customers (descriptive) or an effect across the user base (experiment). Plan an experiment only if it passes the gate in section 7.2, and fix beforehand the hypothesis, one primary metric, the smallest effect worth acting on, the randomization unit, sample size and duration, the stopping rule and the guardrail metrics.

**Feasibility.** Engineers investigate and own the conclusion; an answer given in a meeting is not an investigation. Report which of three states has been reached: a preliminary engineering assessment, a feasibility prototype that answered a named question under stated conditions, or a production-ready solution, which discovery does not establish. Never present an uninvestigated estimate as verified.

## Numbers

Derive a number only when the decision needs it. Every derived number you show (sample size, duration, rate, interval, effect size) comes with a complete derivation in the layout of section 8: inputs with their source, the formula, variables and units, the substitution, the steps, the result, what it means in practice, and its limitations. Don't invent inputs. Ask for the essential ones, or use values labelled illustrative, and never report an illustrative result as a finding. Recompute with a tool when you have one.

## Output

Answer the person's direct question first, in a line or two. Then give the test plan, execution artifacts or readout from the templates in section 11, scaled to the test and to what was supplied:

- A usability round, or any result that arrives as a few lines, gets the short readout. The full readout is for tests with criteria, several kinds of evidence, or a decision that others will review.
- Most qualitative plans and readouts fit on a page. Say each thing once: a gap is named where it belongs and not repeated, and the readout is not restated in prose after it.
- Recommend one next action, or two when they address different risks. Each takes a sentence that carries its three reasons.
- Include statistics only where a statistical claim is made. Write no introduction and no explanation of the method.

## Checks before returning

Re-read the output and fix it if any of these is true:

- Something is reported that is not in the supplied material, or a plan reads as if it had run.
- Usability or liking is reported as value or demand.
- "Validated", "proven" or "confirmed" rests on a threshold alone, or on a convenience sample without saying so.
- A threshold has no stated basis, or criteria appeared after the results without the retrospective label.
- Usage by a few accounts or an opt-in group is presented as market demand or as an experiment's result.
- A derived number has no derivation, or an illustrative input is presented as data.
- Different prototype versions are pooled into one count.
- A missed threshold became "kill the idea", or an inconclusive result was forced into a verdict.
- A customer-facing step was taken or scheduled without authorization.
- The next action doesn't say which uncertainty it addresses, why that matters, or why it is proportionate.

## B2B and B2C

- **B2B.** Few customers, each large. Test users and the economic buyer separately: a user's enthusiasm does not answer whether the organization will buy, and the customer's purchasing process (procurement, security review, budget cycle) is part of the value question. Decide whether the claim is about people or about accounts and count that unit. Discovery-program customers were chosen because they feel the problem and want to help, which makes them informative and unrepresentative. Look for adoption in the real workflow (the work moved into the tool, used unprompted, by people other than the champion), for commercial commitments, and for organizational constraints that would stop either. A small B2B sample can produce valuable discovery evidence; it does not support statistical generalization, and an experiment is usually the wrong tool.
- **B2C.** Traffic often makes demand tests and experiments possible, which is when the experiment rules matter most: power, stopping, guardrails, novelty. Recruit usability participants from the target segment, not from whoever is easiest to reach.

## Boundaries with other skills

These are divisions of responsibility, not prerequisites. This skill works alone from an idea, a hypothesis, a prototype or a set of results.

- **Which risk matters most:** `inspired-four-risks`. If an assessment exists, test the risk it names against its criteria, and say in the readout which risk the result bears on so the assessment can be updated.
- **What prototype to build, and its spec:** `inspired-prototype-design`. Here, name only the type the test needs.
- **Whether it works for the business, and previews with stakeholders:** `inspired-stakeholders-viability`. If a test surfaces a business constraint, record it as untested viability and hand it over.

## Attribution

From *Inspired*: the test types, the conduct of a usability session, the four value signals, honest fake doors, and engineers investigating feasibility. Added here to keep conclusions honest: the evidence kinds, the criteria rules, the four decisions, the statistics, and the execution rules. Don't attribute the added rules to Cagan. The reference file's source note has the detail.

## Reference

`references/test-protocols.md`. Read the sections the task needs:

- **Planning or execution support:** sections 2 (criteria) and 3 (participants), the protocol for the test type (4 to 7, 9), section 10 before anything customer-facing, and the plan template in section 11.
- **Readout:** section 1 (assessing evidence) and the readout template in section 11.
- **Any experiment or derived number:** sections 7.2, 7.3 and 8.
