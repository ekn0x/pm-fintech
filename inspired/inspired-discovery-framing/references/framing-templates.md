# Framing templates

Contents: 1. The four questions (every frame), with examples including two bugs · 2. Customer letter (larger efforts) · 3. Startup canvas (new product or business)

The examples show the tags in use. Their figures are invented for illustration; in a real frame every figure is given, calculated, proposed or left empty under the skill's number rules.

## 1. The four questions

This is the opportunity assessment. On its own it frames most work; it also opens every larger frame.

| Question | What a good answer looks like |
|---|---|
| **Business objective:** which objective is this work meant to serve? | An objective the company or team has already agreed. A result, not the feature. |
| **Key results:** how will we know we succeeded? | The measure of the outcome, with baseline and target when they were supplied. The team's existing key results if it has them. |
| **Customer problem:** what problem does this solve for customers? | Written from the customer's side, in a sentence a customer would recognise. |
| **Target market:** which customers is this for? | A specific segment. In B2B, buyer and user named separately. |

### B2B example: objective given, numbers missing

Supplied: "CS wants a bulk-edit screen for vendor records. One mid-market account churned and cited data clean-up. Our company objective this year is to reduce churn in mid-market."

```
# Frame: vendor record clean-up
**Status:** Ready for discovery — objective given; the open items are for discovery to find out
**Discovery:** Proceed
**Request as received:** "Add a bulk-edit screen for vendor records" — from Customer Success
**Technique:** opportunity assessment — a feature in an existing product

## The four questions
| | Answer | Source |
|---|---|---|
| Business objective | Reduce churn in mid-market accounts | given: company objective this year, tied to the request by the requester |
| Key results | Measure: time for a new customer to get its vendor records clean enough to run payments. Baseline: —. Target: —. | measure inferred from the churn reason; numbers unknown |
| Customer problem | People onboarding a new account fix duplicate and outdated vendor records one at a time before they can trust a payment run | inferred from one churned account's stated reason |
| Target market | User: whoever cleans vendor records in a mid-market account's first months. Buyer: — | user inferred; buyer unknown |

## Open questions
| Question | Who can answer | Affects |
|---|---|---|
| How long does vendor clean-up take a new account today, and who does it, by role? | Onboarding team | Key result baseline; target market (user) |
| Who decides on renewal in these accounts? | Account managers | Target market (buyer) |

## Assumptions and risks
| Assumption | Source | Risk if false | Category |
|---|---|---|---|
| Slow vendor clean-up is a cause of mid-market churn beyond the one account that cited it | given: CS, from one churned account | The work doesn't move churn | Value |
| A bulk-edit screen removes the pain better than cleaner import or deduplication on the way in | inferred: the request names this solution | Users keep fixing records one at a time | Value |
| Users can change many payment records at once without errors they can't undo | inferred: bulk edit depends on it | Wrong payments; users avoid the screen | Usability |
| Bulk changes to vendor bank details are acceptable under our own audit and fraud controls | inferred: bulk edit depends on it | The screen can't ship as designed | Viability |

Nothing material identified for feasibility from what was supplied.

## Out of scope
Vendor records after onboarding. Enterprise accounts.
```

Whether clean-up really drives churn is not listed as an open question. The request relies on the answer being yes, so it is an assumption and appears once, in that table.

### B2C example: objective and numbers given

Supplied: "The CEO wants streaks. Team objective this quarter: week-4 retention of new users from 18% to 23%."

| | Answer | Source |
|---|---|---|
| Business objective | Improve retention of new users | given: team objective this quarter |
| Key results | Week-4 retention of new users from 18% to 23% | given |
| Customer problem | New users who want a daily habit lose momentum after the first days and don't return | inferred from the request; no evidence supplied |
| Target market | New users in their first four weeks. A narrower segment (for example those who said they want to practise daily) is — | inferred; narrower segment unknown |

Status: **Ready for discovery**. Discovery: **Proceed**. One assumption: new users leave because they lose momentum (inferred from the request). If it is false, streaks won't move week-4 retention (value).

### Example: objective not supplied

Supplied: "A board member wants a Slack integration."

| | Answer | Source |
|---|---|---|
| Business objective | — | unknown: none supplied |
| Key results | — | unknown |
| Customer problem | — | unknown: the request names a solution and no customer |
| Target market | — | unknown |

Status: **Draft**. Discovery: **Proceed conditionally**: finding out who asked for it and what they would do with it can start now; confirm the objective before anything is prototyped. Open questions: which agreed objective would this serve, and which customers asked for it or would use it? The frame does not supply "increase engagement" to fill the box, and it lists no assumptions, because nothing has been asserted yet.

If the answer comes back that no objective covers it, the frame changes: status **Needs alignment**, and under *Decisions needed*, "Which objective this serves, or whether to pursue it without one | owner: whoever sets the team's objectives (unknown) | holds up everything past initial problem discovery".

### Example: a bug worth framing

Supplied: "Several accounts say their scheduled reports sometimes arrive empty. Support thinks it only affects scheduled reports. We don't know why it happens."

```
# Frame: empty scheduled reports
**Status:** Draft — impact and extent are not established
**Discovery:** Proceed conditionally — finding the extent, impact and cause starts now; confirm the objective before scoping work beyond the fix
**Corrective action:** proceeds independently of this frame
**Request as received:** "Scheduled reports sometimes arrive empty" — from Support, relaying several accounts
**Technique:** opportunity assessment — a defect with unknown cause and unknown impact

## The four questions
| | Answer | Source |
|---|---|---|
| Business objective | — | unknown: none supplied |
| Key results | — | unknown |
| Customer problem | Customers who rely on scheduled reports sometimes receive an empty one | given: reported by several accounts |
| Target market | Accounts using scheduled reports; how many are affected is — | given (segment); unknown (extent) |

## Open questions
| Question | Who can answer | Affects |
|---|---|---|
| How often does it happen, to which accounts, and since when? | Support, engineering | Target market; key results |
| What do customers do when a report arrives empty, and has anyone acted on one? | Affected accounts | Customer problem |
| What causes it? | Engineering | Everything downstream of the fix |
| Which agreed objective does this fall under? | The requester | Business objective |

## Assumptions and risks
| Assumption | Source | Risk if false | Category |
|---|---|---|---|
| The failure is confined to scheduled reports | given: Support's belief, not verified | Customers are also acting on incomplete on-demand reports without knowing | Value |

The cause is not established, so no feasibility assumption can be stated. Nothing material identified for usability or viability from what was supplied.
```

### Example: a bug with nothing to frame

Supplied: "The date picker on the invoice form starts the week on Sunday. The spec says Monday."

```
# Frame: date picker week start
**Status:** No framing needed — the correct behavior is specified, the impact is low, and there is nothing to find out
**Request as received:** "The date picker on the invoice form starts the week on Sunday" — from (not stated)
```

## 2. Customer letter

For a larger effort with several goals. The letter is from one specific, realistic customer to the company's CEO, dated after launch, saying how the product changed their work or life. It is followed by a short reply from the CEO to the team, saying what the product did for the business.

The letter is imagined by design, so it carries no tags. That makes two limits necessary:

- Any figure in the letter or the reply is one of the frame's key results. Where the key result's numbers are unknown, write `[x]`.
- The customer, their role and their situation match the target market in the four questions.

Guidance:

- Use the customer's voice and words. No feature lists, no marketing language.
- Name the before and the after concretely: time saved, mistakes avoided, money made, stress removed.
- One customer per letter. If buyer and user differ, write two short letters.
- The letter tests the idea. If the team can't write one that sounds true, the value isn't clear yet; say so instead of forcing the letter.

Skeleton:

```
Dear [CEO],
I'm [name], [role] at [company or life situation]. Before [product], I [painful situation, concrete].
Since we started using it, [what changed, concrete]. The part that surprised me was [...].
[What it means for them: confidence with their boss, time back, a risk gone.]
Thank you, [name]

Team,
[Product] has [business result, in the terms of the key results]. It worked because [...].
[CEO]
```

### B2B example (key results given: month-end close two days earlier)

"Dear Dana, I run accounts payable at a logistics firm. Every month-end my team approved small invoices by hand, mostly from the same suppliers, and we were always the last thing holding up the close. Since auto-approval went live my team only looks at the invoices that don't match, and we closed last quarter two days early. Our auditor read the approval log and asked for nothing more..."

"Team, mid-market customers on auto-approval now close two days earlier, which is what we set out to do. It worked because we solved for the auditor as well as the AP lead."

### B2C example (numbers unknown)

"Dear Sam, I've tried to learn Portuguese three times and quit within a week each time. This time I'm on day [x]. What kept me going wasn't a streak count. When I missed a day, the app gave me a three-minute lesson instead of a twenty-minute one..."

## 3. Startup canvas

For a new product line or business, where the whole business has to work and not only the product. Any one-page canvas does the job. If the team already uses one (lean canvas, business model canvas), use theirs. Otherwise use the fields below, in this order, because the first ones are the ones most often skipped.

| Field | Prompt |
|---|---|
| Target customer | Who exactly, and who pays if different? |
| Problem | The top one to three problems, as the customer would say them |
| Current alternatives | What they do today, including nothing |
| Value proposition | Why someone would switch, in one sentence |
| Solution | The product idea, kept short |
| Channels | How customers find and buy it |
| Revenue model | Who pays, and how |
| Cost structure | Main costs to build, run, sell and support |
| Key metrics | The few numbers that would show it is working |
| Assumptions | What the business relies on. Each one goes in the frame's *Assumptions and risks* table with its risk and category |

Guidance:

- Every field carries a source tag, as in the four questions. Prices, market sizes, acquisition costs and margins follow the skill's number rules; when none was supplied they stay empty.
- In a new product, the biggest risk is usually whether the team can discover a solution customers want enough to switch for. A canvas gives the solution one box among ten and makes the business-model boxes look just as uncertain. So the frame says plainly that the value of the solution is unproven. That is the book's point about canvases, not a ranking of the other risks, which stay unranked.
- Keep the solution box to a few lines. Detail there is false precision before discovery.

### B2B example (headlines)

| Field | Answer | Source |
|---|---|---|
| Target customer | User: heads of trading at mid-size asset managers. Buyer: — | given (user); unknown (buyer) |
| Problem | Can't show best execution on illiquid bonds without days of manual work | given: stated by the requester from client conversations |
| Current alternatives | Spreadsheets, broker reports | given |
| Value proposition | An evidence pack for compliance without the manual work | inferred |
| Revenue model | Subscription; price — | inferred (model); unknown (price) |
| Assumptions | Their compliance teams will accept the evidence (value; unproven). We can meet our own obligations when a client relies on it in a regulatory review (viability) | inferred |

### B2C example (headlines)

| Field | Answer | Source |
|---|---|---|
| Target customer | New parents tracking feeding and sleep; both parents use it | given |
| Problem | Tired parents lose track of who did what and when | given |
| Current alternatives | Notes app, paper, a competitor app with ads | inferred |
| Value proposition | Both parents see the same log, entered in one tap | inferred |
| Revenue model | — | unknown |
| Assumptions | A one-tap log beats a notes app at 3 a.m. (value; unproven) | inferred |
