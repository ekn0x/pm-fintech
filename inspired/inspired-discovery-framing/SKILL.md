---
name: inspired-discovery-framing
description: Frame product work before discovery with the three framing techniques from Marty Cagan's Inspired (2nd ed.) - opportunity assessment for most work, customer letter for larger efforts with several goals, startup canvas for a new product or business. Turns a request that arrives as a solution ("build X") or as a bug report into the objective it serves, the measure of success, the customer problem and the target market, with every answer marked given, inferred or unknown and nothing invented, plus open questions, assumptions and their risks. Use whenever someone hands over a feature request, bug report, idea, stakeholder ask or roadmap item and wants to know whether or how to start, asks for an opportunity assessment, problem statement, working-backwards letter or lean canvas, or asks "what problem are we solving" or "how will we know it worked", even if they don't name Cagan. Not for ranking risks or choosing tests (inspired-four-risks), or for story maps and reference customers (inspired-discovery-planning).
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

- **Numbers are never inferred.** They follow their own rules under *Numbers and calculations*. You may name the *measure* for a key result as inferred ("time to first clean payment run") and leave its baseline and target unknown. An invented "from 18% to 23%" looks like data and gets repeated in the next meeting.
- **The tags say where a statement came from, not whether it is true.** "Given" means the requester said so; a stakeholder's claim is given and still unvalidated. Whether customers have the problem is what discovery finds out. If the person supplied actual evidence (interview notes, usage data, a churn reason on record), cite it in the source.
- **Do not write an objective to fit the work.** See step 2.

## Unknowns, assumptions and risks

These are three different things. Mixing them produces invented hypotheses and risk lists that repeat the open questions.

| | What it is | Example |
|---|---|---|
| **Unknown** | Missing information. A question, not a claim | "How many traders use the current RFQ workflow?" |
| **Assumption** | A proposition the work relies on as true without enough validation. It can be given (a stakeholder asserted it) or inferred (the request implies it) | "Traders would prefer automated RFQ execution to manual execution" |
| **Risk** | What goes wrong if an assumption is false | "If traders don't trust automated execution, adoption won't justify the build" |

- An unknown stays a question. It becomes an assumption only when the request or the frame relies on one particular answer to it.
- List an assumption only when it is material: the opportunity, or the solution named in the request, depends on it. Not every inference is one, and if nothing is relied on, list nothing.
- Write each assumption precisely enough to be checked later: who, does or wants what, under which condition. Give its source.
- Give a risk for an assumption when its being false would hurt in one of Cagan's four categories: **value** (will customers buy or choose to use it), **usability** (can users work out how to use it), **feasibility** (can we build it with the time, skills and technology we have), **viability** (does it work for our business: sales, legal, finance, support and so on).
- One assumption can carry several risks, and several unknowns can bear on one assumption.

## Numbers and calculations

Every number in the frame is one of four classes.

| Class | Meaning |
|---|---|
| **given** | Supplied by the person or by a source they pointed to |
| **calculated** | Derived by arithmetic from disclosed values, with the derivation shown |
| **proposed** | A target, scenario or estimate that is not established, labelled as such |
| **unknown** | Can't be determined from what was supplied. Leave it empty |

- A baseline is a fact, so it is given, calculated or unknown, never proposed.
- Don't volunteer proposed figures. The label is for a figure the person floats without agreement behind it, or one they ask you to suggest. A proposed target is never written as an agreed objective, and an estimate is never written as observed evidence.
- Calculate only when the result helps the frame. If the inputs are insufficient, the result is unknown.
- Write out every calculation you show, however simple, so anyone can reproduce it: the inputs with their source, any assumption used, the formula, the values substituted, the intermediate steps, the result with its unit, and the rounding if any. Keeping the frame short never shortens a derivation.
- Say percentage points for the difference between two percentages and percent for a relative change. Carry units through every step. Call an approximation an approximation.
- Recompute each result before returning, with a tool if one is available.

Layout, one block per calculation, in a *Calculations* section that exists only when there is one:

```
**Success rate** — calculated
Inputs: successful quotes = 15,000,000 (given); total quotes = 120,000,000 (given)
Assumptions: none
Formula: success rate = (successful quotes / total quotes) × 100
Substitution: (15,000,000 / 120,000,000) × 100
Steps: 15,000,000 / 120,000,000 = 0.125; 0.125 × 100 = 12.5
Result: 12.5% (exact)
```

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
   - Key results measure the outcome and say how the team will know it worked. Use the team's existing key results when they were supplied. "Ship by Q2" and "release three reports" measure activity; replace them.
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

The header and the four-question table are always present. Every other section appears only when it has something material in it.

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
| Key results | | |
| Customer problem | | |
| Target market | | |

## Open questions
| Question | Who can answer | Affects |
|---|---|---|

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

For *No framing needed*, return only the title, status and request lines. When corrective action is under way or needed, add one header line: `**Corrective action:** proceeds independently of this frame`.

## Checks before returning

- **A number with no class**, a proposed figure written as agreed, or a calculation with a step missing or an arithmetic error.
- **The objective restates the feature**, or appeared without being supplied.
- **Key results measure activity.**
- **The target market is everyone.**
- **The customer letter lists features**, or contains figures that are not in the key results.
- **The startup canvas has a detailed solution and a vague customer.**
- **An unknown written as an assumption**, an assumption with no source, or a risk invented to cover a category.
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
