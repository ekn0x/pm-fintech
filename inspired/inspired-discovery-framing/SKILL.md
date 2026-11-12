---
name: inspired-discovery-framing
description: Frame product opportunities before discovery, using Marty Cagan's Inspired (2nd ed.) - an opportunity assessment for most work, plus a customer letter for larger efforts or a startup canvas for a new product or business. Turns a feature request, bug report, product idea, stakeholder request or roadmap initiative into the objective it serves, its success measures, the customer problem and the target market, keeping evidence, assumptions and unknowns separate and inventing nothing. Use when someone asks whether or how to start such work, what problem it solves, or how success will be measured. Does not rank risks or choose experiments (inspired-four-risks), or plan detailed discovery (inspired-discovery-planning).
---

# Discovery Framing

Framing gets a team to agree on four things before anyone designs a solution: the objective the work serves, how success will be measured, the customer problem, and which customers it is for. It also sets out what is still unknown and which assumptions the work rests on. In *Inspired* it exists because most work arrives as a solution ("build X") and teams go straight to building it.

A frame is written before any evidence exists, so it is a hypothesis. Its job is to show what is known, what is guessed and what is missing. A frame that reads as finished when half of it was guessed does harm, because the team stops asking. Everything below follows from that.

## Mark where every answer came from

Every answer in the frame carries one of three tags.

| Tag | Meaning | What to write |
|---|---|---|
| **given** | The person stated it, or it is in a document they supplied | The answer, and where it came from |
| **inferred** | Your reading of what they supplied | The answer, and what you inferred it from. It needs their confirmation |
| **unknown** | Not supplied and not inferable | No answer. Write the question that would fill it and who can answer it |

Three rules:

- **Numbers are never inferred.** They follow their own rules under *Numbers and calculations*. You may suggest a *measure* for a key result, tagged inferred and labelled proposed ("time to first clean payment run"), and leave its baseline and target unknown. An invented "from 18% to 23%" looks like data and gets repeated in the next meeting.
- **The tags say where a statement came from, not whether it is true.** "Given" means the requester said so; a stakeholder's claim is given and still unvalidated. Whether customers have the problem is what discovery finds out. If the person supplied actual evidence (interview notes, usage data, a churn reason on record), cite it in the source.
- **Do not write an objective to fit the work.** See step 2.

## Unknowns, assumptions and risks

These are three different things. Mixing them produces invented hypotheses and risk lists that repeat the open questions.

| | What it is | Example |
|---|---|---|
| **Unknown** | Missing information. A question, not a claim | "How many traders use the current RFQ workflow?" |
| **Assumption** | A proposition provisionally relied upon as true. It can be given (a stakeholder asserted it) or inferred (the request implies it) | "Traders would prefer automated RFQ execution to manual execution" |
| **Risk** | A potential adverse consequence if an assumption is false or a relevant condition does not hold | "If traders don't trust automated execution, adoption won't justify the build" |

- An unknown remains an unanswered question. When the work relies on a provisional answer to that question, record the answer separately as an assumption, preserving the underlying uncertainty. An unknown can exist without an assumption, and an assumption need not come from an identified unknown.
- When an assumption is a provisional answer to an open question, number the question (Q1, Q2…) and cite it in the assumption's source, so the two stay linked without repeating the content.
- List an assumption only when it is material: the opportunity, or the solution named in the request, depends on it. Not every inference is one, and if nothing is relied on, list nothing.
- Write each assumption precisely enough to be checked later: who, does or wants what, under which condition. Give its source.
- Give a risk for an assumption when its being false would hurt in one of Cagan's four categories: **value** (will customers buy or choose to use it), **usability** (can users work out how to use it), **feasibility** (can we build it with the time, skills and technology we have), **viability** (does it work for our business: sales, legal, finance, support and so on).
- One assumption can carry several risks, and several unknowns can bear on one assumption.

## Numbers and calculations

A number has three separate properties. Label each number with the ones needed to keep it from being misread; most need one or two.

| Property | Values |
|---|---|
| **Provenance:** where it came from | **given** (supplied by the person or a source they pointed to) · **unknown** (not established; leave it empty). Numbers are never inferred |
| **Derivation:** how it was obtained | supplied directly · **calculated** from disclosed inputs and assumptions · not calculable from what was supplied |
| **Status:** what standing it has | **established** or **approved**, only when that is explicitly supported · **proposed** or hypothetical · **unvalidated** · unknown |

Examples: "35% adoption target — given, proposed by a stakeholder, not approved". "12.5% success rate — calculated from given inputs". "20% improvement — calculated under a proposed scenario, not an observed result".

- Given is not validated or approved, and calculated is not observed or established. Say so whenever a reader could take it that way.
- A baseline is a fact, so it is never proposed or hypothetical.
- Don't volunteer proposed figures. The label is for a figure the person floats without agreement behind it, or one they ask you to suggest. A proposed target is never written as an agreed objective, and an estimate is never written as observed evidence.
- Calculate only when the result helps the frame. If the inputs are insufficient, the result is unknown.
- Write out every calculation you show, however simple, so anyone can reproduce it: the inputs with their source, any assumption used, the formula, the values substituted, the intermediate steps, the result with its unit, and the rounding if any. Keeping the frame short never shortens a derivation.
- Say percentage points for the difference between two percentages and percent for a relative change. Carry units through every step. Call an approximation an approximation.
- Recompute each result before returning, with a tool if one is available.

Layout, one block per calculation, in a *Calculations* section that exists only when there is one:

```
**Success rate** — calculated from given inputs
Inputs: successful quotes = 15,000,000 (given); total quotes = 120,000,000 (given)
Assumptions: none
Formula: success rate = (successful quotes / total quotes) × 100
Substitution: (15,000,000 / 120,000,000) × 100
Steps: 15,000,000 / 120,000,000 = 0.125; 0.125 × 100 = 12.5
Result: 12.5% (exact)
```

When an input is a proposed scenario, list it under Assumptions with its status, and say in the Result line that the result is a projection under that scenario, not an observed result.

## Pick the technique by size

The four questions are answered at every size, because agreement on them is the purpose of framing. Larger work adds a second artifact.

| Size of the work | Technique |
|---|---|
| Most work: a feature, an optimization, a medium-sized project, a bug that needs framing | **Opportunity assessment**: the four questions alone |
| A larger effort with several goals, such as a redesign or a major new capability | Four questions **+ customer letter** |
| A new product line or a new business | Four questions **+ startup canvas** |

If the size is unclear, pick the smaller technique. A frame is cheap to extend later.

Whether to frame at all depends on the work's impact, uncertainty and risk, not on what the item is called. Feature requests, bug reports, stakeholder asks, roadmap items and new product ideas are all valid inputs.

- **Nothing to frame.** The expected behavior is known, the impact is low and little is uncertain: a copy change, a config change, a defect whose correct behavior is specified. Say framing is not needed, give the reason in one line, and stop. Process on work with no meaningful risk teaches the team to ignore the process. If the impact wasn't stated, classify on what was supplied and name the one thing that would change the call.
- **A bug worth framing.** It points at something larger: an unclear customer need, a workflow that fails systemically, substantial operational impact, or business risk. Frame it like any other work. Its cause is an unknown until someone has established it.

Framing never stands in front of urgent corrective action. When something is broken for customers now, containment and the fix go ahead by whatever process the organization uses. The frame covers what remains to be understood afterwards or alongside, and says so in one line.

## Inputs

1. The request, idea or bug report as it was handed over, word for word if possible.
2. Who asked for it and why.
3. Objectives the company or team has already agreed (OKRs or equivalent).
4. What is known about the customers involved, and any evidence.

Don't hold the frame back to ask for missing inputs. Write it from what was supplied and let the unknowns show; the *Open questions* table is how you ask. The person then has something concrete to react to, and the frame works the same when nobody is there to answer. When answers come back, update the frame (see *Updating a frame*). The one exception is when nothing to frame was supplied at all: say what you need, and don't invent an opportunity.

## Procedure

1. **Restate the request as a problem.** Write the request as given, then the customer problem behind it. For "add an export to Excel", the problem might be "analysts can't get our data into their monthly reporting without retyping it." For a bug report, the problem is what the customer can't do and what that costs them, not the defect's cause. Unless the person stated the problem themselves, this is inferred; say what you inferred it from.

2. **Check the objective.** In the book, the objective and key results of an opportunity assessment are ones the team already has, not ones written to justify the feature. So look for an agreed objective this work serves, and report one of three results:
   - The person named it, or it is in what they supplied and they tied the work to it: **given**.
   - An agreed objective was supplied, but the link to this work is your reading: **inferred**. Say why you think it fits.
   - No objective was supplied, or none fits: **unknown**. Do not write one. Its absence from what you were given doesn't mean the organization has none, so make it an open question: which agreed objective does this serve, and who can say? If the person tells you none has been established, that is no longer a gap someone can look up. It is a decision for whoever sets the team's objectives, and it goes under *Decisions needed*. Either way, still fill in the customer problem and target market where you can, so the conversation has something concrete in it.

3. **Choose the technique** from the table and say why in one line.

4. **Answer the four questions** using `references/framing-templates.md`. Rules:
   - The objective is a business or customer result, not the feature. "Launch export" is not an objective.
   - Key results that were supplied are reported exactly as supplied, tagged given, even when they measure activity. Never rewrite, replace or drop them. If one measures delivery or activity ("ship by Q2", "release three reports") rather than a business or customer outcome, say so in its source. Where it helps, add an outcome measure on its own row, tagged inferred and labelled proposed, with its baseline and target unknown unless supplied. If no key results were supplied, they are unknown; never invent one.
   - The customer problem is written from the customer's side, in a sentence the customer would recognise.
   - The target market is specific. "All users" is almost always wrong; name the segment the work is for first. In B2B, name the buyer and the user separately.

5. **Add the customer letter or startup canvas** if the size calls for it, from the same reference file.

6. **List the material assumptions and their risks**, as defined under *Unknowns, assumptions and risks*: the assumption, its source, what goes wrong if it is false, and the category of that risk. Look across all four categories, because teams drift toward the risk they are comfortable with (engineers to feasibility, designers to usability) and skip the others. Don't manufacture an entry to cover a category; close the list with one line naming the categories where nothing material was found. Do not rank the risks, say which to tackle first, or propose tests. Judging their relative importance is a separate job (inspired-four-risks), and this list is written to be its input. If the person asks for a ranking or for experiments, say that this is the next step and which skill does it; don't run that skill unless asked.

7. **Name what is out of scope** when there is a boundary worth stating, so the team doesn't drift.

8. **Record the decisions needed.** A question is settled by finding something out; a decision is settled by someone with the authority to make it. For each material decision or agreement still open, say what has to be decided, who owns it, and what it holds up. Use the name or role that was supplied; otherwise describe the role ("whoever sets this team's objectives") and mark the owner unknown, without assuming how the organization is structured.

9. **Set the status and the discovery call.** They answer different questions, so set them separately.

   *Status* describes the frame. Use the first that applies:

   | Status | When |
   |---|---|
   | **No framing needed** | Framing would add nothing, given the work's impact, uncertainty and risk |
   | **Needs alignment** | A material decision is open and needs agreement before the work it affects goes ahead. It is listed under *Decisions needed* |
   | **Draft** | No such decision, but material information is missing from the frame |
   | **Ready for discovery** | The frame is clear enough to tell discovery what to investigate |

   Material means it would change what the frame says or what happens next. A missing baseline or an unvalidated assumption is normal at this stage and doesn't make a frame a draft.

   *Discovery* says what can happen next:

   | Discovery | When |
   |---|---|
   | **Proceed** | Nothing has to happen first |
   | **Proceed conditionally** | Discovery can start on a stated part, or up to a stated point, while a named gap or decision is closed |
   | **Requires a prior decision** | Discovery can't be scoped or justified until a named decision is made |

   Missing information alone never holds discovery up, and that includes an objective that wasn't supplied; only an open decision can. So *Draft* goes with *Proceed* when the missing information is what discovery will find out, and otherwise with *Proceed conditionally*. *Needs alignment* goes with *Requires a prior decision*, or with *Proceed conditionally* when discovery on the part the decision doesn't touch can start. *Ready for discovery* never goes with *Requires a prior decision*. *No framing needed* has no discovery call.

## Output

Whenever framing is performed, the full header and the four-question table are required. Every other section appears only when it has something material in it. The one exception is *No framing needed*, below.

```
# Frame: [working name]
**Status:** [No framing needed / Needs alignment / Draft / Ready for discovery] — [one line why]
**Discovery:** [Proceed / Proceed conditionally / Requires a prior decision] — [the condition or the decision]
**Request as received:** "[...]" — from [who, if known]
**Technique:** [opportunity assessment / + customer letter / + startup canvas] — [why]

## The four questions
| | Answer | Source |
|---|---|---|
| Business objective | | given / inferred / unknown, and from what |
| Key results (agreed) | as supplied, or — | given (flag if activity-based) / unknown |
| Proposed outcome measure | only when useful | inferred from [...]; proposed, not agreed |
| Customer problem | | |
| Target market | | |

## Open questions
| # | Question | Who can answer | Affects |
|---|---|---|---|

## Assumptions and risks
| Assumption | Source | Risk if false | Category |
|---|---|---|---|

## Decisions needed
| Decision | Owner | Holds up |
|---|---|---|

## Calculations

## Customer letter  /  Startup canvas

## Out of scope
```

Scale the frame to the work. A small request may need the header, the table and a few lines; a new business needs the full set. Write no introduction, no closing summary and no explanation of the method, and say each thing once: a gap goes under open questions, assumptions or decisions, not under all three.

Every unknown or inferred answer in the table must be traceable to an open question, an assumption or a decision. Combine related gaps into one question where that reads better, and put first the questions whose answers would change the frame or the next decision. Never drop a material uncertainty to save space.

For *No framing needed*, return only the title, the status with a concise justification, and the request as received: no discovery call, technique, four-question table or other section. When corrective action is under way or needed, add one header line: `**Corrective action:** proceeds independently of this frame`.

## Checks before returning

- **A number that could be misread for lack of a label**: given treated as validated or approved, calculated treated as observed, a proposed figure written as agreed. Or a calculation missing an input, its provenance, an assumption, the formula, the substitution, a step, the unit or the rounding, or with an arithmetic error.
- **The objective restates the feature**, or appeared without being supplied.
- **Supplied key results changed, replaced or dropped**, an activity-based one not flagged, a proposed measure presented as agreed, or key results invented when none were supplied.
- **The target market is everyone.**
- **The customer letter lists features**, or contains figures that are not in the key results.
- **The startup canvas has a detailed solution and a vague customer.**
- **An unknown treated as answered**, a provisional answer relied on but not recorded as an assumption, an assumption with no source or no link to the question it answers, or an assumption or risk invented to fill the output.
- **A *No framing needed* result carrying the four-question table or other sections**, or a framed result missing the header or the table.
- **Risks ranked, or tests proposed.**
- **The status and the discovery call disagree**, or discovery is held up by missing information and not by a decision. Re-apply step 9.
- **The same gap appears in more than one section**, or a section has nothing material in it.
- **A bug waved through because it is a bug**, or a frame placed in front of an urgent fix.

## B2B and B2C

- **B2B:** buyer and user are separate lines in the target market, and often have different problems. Key results tend to be adoption inside accounts, retention or expansion, and effects on the sales cycle. Write one short letter for each when buyer and user differ.
- **B2C:** the target market is a segment defined by a behavior or situation, not a demographic alone. Key results usually tie to activation, retention, engagement or conversion. The letter is from one individual.

## Updating a frame

When an earlier frame comes back with new information (answers from the requester, findings from discovery), revise it in place: fill the answers, change the tags, re-apply the status and the discovery call, and add a short "Changed since last version" list at the top. Don't start over, because the open questions and assumptions are the record of what the team set out to learn.

## Reference

- `references/framing-templates.md`: field guidance for the four questions, the customer letter and the startup canvas, with B2B, B2C and bug examples. Read it at step 4.
