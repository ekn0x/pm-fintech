# Verify: Inspired (2nd ed.) skill set

Built from my knowledge of *Inspired* (2nd edition, 2017), not from the text. For each skill: the claims I attribute to the book, my confidence, and where to check in your copy. Everything under "General practice" is mine or standard industry practice, not the book's. Chapter names are as I recall them; check the table of contents if one doesn't match.

Confidence: **High** = core, frequently restated concept. **Medium** = I'm confident of the idea, less of the exact framing or list. **Low** = check before relying on it.

---

## inspired-four-risks

Files: `SKILL.md`, `references/risk-definitions.md`, `references/risk-tests.md`. This skill now carries the most of my own construction in the set, mostly in the definitions file. Claims are grouped by where they sit.

### A. Taken from the book

| Claim | Confidence | Where to check |
|---|---|---|
| The four risks: value, usability, feasibility, business viability | High | Part I, "Beyond Lean and Agile"; Part IV, "Principles of Product Discovery" |
| Value: whether customers will buy it, or users will choose to use it | High | Same |
| Usability: whether users can figure out how to use it | High | Same |
| Feasibility: whether engineers can build it with the time, skills and technology available | High | Same |
| Viability: whether the solution works for the various parts of the business | High | Same |
| Owners: PM for value and viability, designer for usability, tech lead for feasibility | High | Part II, "The Product Manager", "The Product Designer", "The Engineers" |
| At least half of ideas won't work, and the ones that do usually need several iterations | High | Part I, "The Root Causes of Failed Product Efforts" |
| Business cases are unreliable before discovery: neither the revenue nor the cost is known | High | Same chapter |
| Customers don't know what's possible, so a request isn't proof of value | High | Part IV, "Principles of Product Discovery" |
| Users saying they like a prototype is not evidence of value | High | Part IV, "User Prototype Technique"; "Testing Value" |
| Engineers should get time to investigate feasibility, not answer in a meeting | Medium-High | Part IV, "Testing Feasibility" |
| Stakeholders should see the prototype one-on-one during discovery, not at launch | High | Part IV, "Testing Business Viability"; Part III/IV, "Managing Stakeholders" |
| Test types named in the catalog: concierge test, demand test, qualitative and quantitative value tests, usability test, feasibility prototype, live-data prototype, discovery program | High | Part IV, prototyping and testing chapters |

### B. Partly from the book: the idea is Cagan's, the wording or list is mine

| Claim | Confidence | What to check |
|---|---|---|
| Value signals: money, reputation, time, access | Medium | Whether "Testing Value" uses these four categories, and under these names |
| A new product must be clearly better than the alternative to make people switch | Medium-High | "Testing Value"; whether he puts it this strongly |
| Value usually ranks first because it's where most ideas fail | Medium | Whether he says value is usually the hardest or most important risk, or only that it is critical |
| B2B buyer vs user tested separately | Medium | "Testing Business Viability"; whether he treats the buyer under value or under viability |
| Feasibility questions (skills, time, architecture, dependencies, performance, infrastructure, cost) | Medium | "Testing Feasibility": compare the list |
| Viability functions (marketing, sales, finance, legal, business development, security, executives, customer success) | Medium-High | "Testing Business Viability": compare the list and whether customer success is in it |
| Restating the idea as a problem first | Medium | Echoes "fall in love with the problem, not the solution" (vision principles) and the opportunity assessment. The sentence template is mine |

### C. Mine, not the book's

From `risk-definitions.md`:
- The single question for each risk, and the "belongs here / belongs elsewhere" lists.
- Usability details: error recovery, efficiency for expert users, accessibility.
- The evidence ladders and rung numbers for all four risks. The *items* on the value ladder (requests, praise, costly signals, live-data behavior, reference customers) come from the book; the ordering into rungs is mine.
- The rating rule (High / Medium / Low from rung and consequence).
- All boundary rules, in particular:
  - **The customer's procurement, security review and internal compliance go under value (buyer side); only our own obligations go under viability.** The book doesn't draw boundaries between the risks (confirmed from your recollection), so this is a deliberate extension, not a contradiction. It is consistent with the book's definition of viability as working for *our* business.
  - The cost to run: estimated under feasibility, judged under viability.
  - "Can't vs won't" test separating usability from value.

- **Value sizing** (cost of the problem today, share removed by the solution, minus switching cost; compared with price and the current alternative; source tags per input; the sizing evidence ladder). Added at your request. *Inspired* asks whether the problem is real and whether the solution is better enough to switch, but it doesn't quantify what the problem is worth.
  - **One possible tension with the book:** Cagan is skeptical of business cases before discovery, because revenue and cost are guesses. The skill is designed to stay clear of that: it sizes the **customer's** current cost, which can be measured now, and explicitly forbids turning it into a revenue forecast for us. Check that this distinction matches your reading.

From `SKILL.md`:
- The value sizing step (step 4) and its output table.
- The sort step (each issue under exactly one risk), the separate rating passes, the optional subagent per risk, and the reconciliation step.
- The kill or change criterion written before each test.
- The decision options: stop / test first / build with the risk accepted / split.
- The output table format, including the rung column.
- The B2B and B2C notes, except reference customers and buyer/user, which come from the book.

From `risk-tests.md`:
- Every effort estimate (hours, days, weeks).
- The ordering of tests from cheap to expensive.
- Both worked examples (Ledgerline and Pantrypal are invented), including their value sizing figures.
- The problem-sizing test in the catalog.

### Questions to answer with your copy

1. Does "Testing Business Viability" discuss the B2B buyer at all? You recall no clear boundaries in the book, so the rule in C stands as an extension. Only revisit it if the chapter explicitly treats the customer's purchase approval as a viability matter.
2. Does "Testing Value" name money, reputation, time and access, or different signals?
3. Does Cagan say value is usually the riskiest of the four?
4. Does the viability chapter's list of stakeholders match the one in `risk-definitions.md`?

## inspired-discovery-framing

Files: `SKILL.md`, `references/framing-templates.md`, `evals/` (nine validation cases: your scenarios A–H plus a customer-letter case; not yet run). Rewritten 2026-11-11 (v2), then amended the same day from your six-point brief (v3): status separated from the discovery call, no risk ranking, unknowns / assumptions / risks kept distinct, number classes with full derivations, output scaled to the work, bugs in scope. Kept thin; the problem file and the interrogation procedure planned for the discovery loop are not in this skill.

### A. Taken from the book

| Claim | Confidence | Where to check |
|---|---|---|
| Three framing techniques: opportunity assessment, customer letter, startup canvas, by size of effort | High | Part IV, "Discovery Framing Techniques" |
| Framing has two purposes: align the team on the objective, the problem, the customer and the measure of success; and identify the big risks discovery must tackle | Medium-High | Same, overview |
| Opportunity assessment's four questions (business objective, key results, customer problem, target market) | High | "Opportunity Assessment Technique" |
| The objective and key results are the team's existing ones, not written for the feature | Medium | Same chapter: check that he ties the first two answers to the team's objectives |
| Opportunity assessment for most work; customer letter for larger efforts with several goals, such as a redesign; startup canvas for a new product line or business | Medium-High | Overview and each chapter: compare the size wording. v1's "multi-team initiative" was mine and is removed |
| Customer letter: from an imagined happy customer to the CEO after launch, with a congratulatory reply from the CEO to the team on the business result; a variant of Amazon's working-backwards press release | Medium | "Customer Letter Technique". The skill now treats the CEO reply as a standard part (v1 called it optional). I recall the variant credited to Walker Lockhart (Nordstrom, ex-Amazon); the skill doesn't name him |
| Startup canvas for new products or businesses; any canvas will do; the biggest risk is usually the value of the solution, which a canvas understates as one box among many | Medium | "Startup Canvas Technique" |
| Requests arrive as solutions and the team's job is to find the problem behind them | Medium | Framing overview (problems vs solutions). v1 listed this step as general practice |
| Teams gravitate to the risks they are comfortable with | Medium | Framing overview. The engineer and designer examples are mine if he gives none |
| Routine work needs no framing; I recall bug fixes among his examples | Medium | Framing overview. The skill departs from this, see C |

### B. Mine or yours, not the book's

- The source tags (given / inferred / unknown).
- **Answering the four questions at every size, with the letter or canvas added on top.** The book presents the three techniques as alternatives by size. I think the four answers are implied by framing's purpose, but the book doesn't say to combine them.
- The limit that figures in the letter come from the key results.
- Supplied key results are kept exactly as given, activity-based ones are flagged rather than replaced, and any suggested outcome measure sits on its own row labelled proposed. From your brief.
- The four statuses (No framing needed, Needs alignment, Draft, Ready for discovery), the separate discovery call (Proceed, Proceed conditionally, Requires a prior decision), and the rule that only an open decision holds discovery up. From your brief.
- The distinction between unknowns, assumptions and risks: an unknown stays an unanswered question, and a provisional answer the work relies on is recorded separately as an assumption, linked to the question by number. From your briefs.
- The three number properties (provenance, derivation, status), used only as far as needed to prevent misreading, and the full-derivation rule for calculations. From your briefs. The limit that the skill doesn't volunteer proposed figures, and that a baseline is never proposed, is my reading of your "never invent baselines or agreed targets".
- Tagging each risk with one of the four categories and the closing line for categories with nothing material.
- The open-questions, decisions-needed and out-of-scope sections, and "Updating a frame".
- The startup canvas field list and its order.
- All examples and the validation cases.

### C. Where the skill departs from the book, flagged

- **Bugs.** The book treats routine work, bug fixes included (as I recall), as not needing framing. The skill decides by impact, uncertainty and risk, so a bug can be framed. This keeps the book's intent (effort in proportion to risk) and drops its shortcut. From your brief.
- **Risk ranking.** The book says framing identifies the *big* risks, and that in a new product the biggest is usually the value of the solution. The skill lists material assumptions without ranking them, and leaves ranking to `inspired-four-risks`. The one exception kept from the book: a startup canvas frame must state that the value of the solution is unproven. That is a stated fact about new products, not a ranking of the listed risks.
- **A missing objective doesn't stop discovery.** The book assumes a team framing work against objectives it already has. The skill lets discovery start conditionally when the objective wasn't supplied, and never writes one in.

### Questions to answer with your copy

1. Is the CEO's reply a standard part of the customer letter, or optional?
2. Does the startup canvas chapter list boxes or show a figure? If so, replace my field list.
3. Does the framing overview discuss problems vs solutions?
4. Does he present the customer letter and startup canvas as replacing the opportunity assessment? If he says so explicitly, the "four questions at every size" rule is a departure and belongs under C.
5. Does the framing overview name bug fixes among work that needs no framing?

## inspired-discovery-planning

| Claim | Confidence | Where to check |
|---|---|---|
| Story map technique (credited to Jeff Patton) for large or complex scope | High | Part IV, "Story Map Technique" |
| Customer discovery program: about six reference customers in one target market | High | "Customer Discovery Program Technique" |
| Selection: in the target market, feel the pain, willing to be a public reference; avoid sales picking for deal size; not custom specials | Medium-High | Same chapter |
| Variants for platform/API, internal tools, consumer products | Medium | Same chapter. Check the consumer number (I used roughly 10–50; low confidence) |
| Program success = customers in production and willing to be references | High | Same chapter |

General practice: the story-map step wording and "first slice must cross the backbone", the agreement checklist, the candidate-screening table, both examples.

## inspired-customer-interviews

| Claim | Confidence | Where to check |
|---|---|---|
| Ideation techniques: customer interviews, concierge test, customer misbehavior, hack days | High | Part IV, "Discovery Ideation Techniques" |
| Interview's core questions: are they who we think, do they have the problem, how do they solve it today, what would make them switch | Medium-High | "Customer Interviews" |
| PM, designer and an engineer attend; interview regularly, every week; purpose is to understand, not to prove | Medium-High | Same chapter. Cadence detail (hours per week) not included; check if the book gives one |
| Customer misbehavior (users using the product in unintended ways) as a source of ideas, with eBay as an example | High | "The Power of Customer Misbehavior" |
| Directed vs undirected hack days | Medium | "Hack Days" |

General practice: question rules (past behavior, no hypotheticals), guide and synthesis templates, concierge plan and misbehavior log formats, examples.

## inspired-prototype-design

| Claim | Confidence | Where to check |
|---|---|---|
| Four prototype types: feasibility, user (low/high fidelity), live-data, hybrid (Wizard of Oz) | High | Part IV, "Discovery Prototyping Techniques" |
| A prototype should cost far less than building (the book gives an order-of-magnitude rule) | Medium | "Principles of Prototypes" |
| Feasibility prototype is throwaway, built by engineers, often a day or two | Medium | "Feasibility Prototype Technique" |
| User prototypes can't prove value; people say they love them | High | "User Prototype Technique" |
| Live-data prototype: real data and traffic, core use case only, far less than production effort; used for A/B tests | High (idea) / Low (any specific % of effort) | "Live-Data Prototype Technique". I deliberately gave no percentage |
| MVP should be a prototype, not a product | High | Part I, key concepts |

General practice: the spec template, time-box comparison with production estimate, the Wizard-of-Oz capacity cap, all examples.

## inspired-discovery-testing

Files: `SKILL.md`, `references/test-protocols.md`, `evals/` (eight validation cases: your scenarios A–H). Revised 2026-11-12 (v2) from your brief: six kinds of evidence and a strength rating for every readout, three operating modes, thresholds that need a stated basis, four decisions, descriptive numbers kept apart from inferential claims, an experiment gate with design and analysis checklists, full derivations, safeguards for customer-facing tests. Run on 2026-11-12 on claude-opus-5-5 and graded by me by hand against the case graders: 52 of 52 with the skill on its final text; 42 to 45 of 52 without it, depending on how three borderline graders are read. Not run through the eval harness and not graded independently. Three fixes came out of the runs: the provisional-label rule, the interval-reading table for experiments, and the short readout as the default for small results.

### A. Taken from the book

| Claim | Confidence | Where to check |
|---|---|---|
| Usability, value, feasibility and viability are tested separately | High | Part IV, "Discovery Testing Techniques" |
| Usability session: tell them it is a prototype, give realistic tasks, don't help, turn their questions back, record easy / struggled / failed per task | Medium-High | "Testing Usability" |
| Fix problems between sessions; don't wait for the round to end | Medium-High | Same |
| The product manager and designer attend every session; an engineer when possible | Medium-High | Same |
| Testing in the participant's own setting shows context | Medium | Same |
| Value test straight after the usability tasks, in the same session | Medium-High | "Testing Value" / qualitative chapter |
| Value signals: money, reputation, time, access | Medium | Qualitative value testing chapter |
| Demand tests: fake door and landing page, with an honest page behind them | Medium-High | "Demand Testing Techniques" |
| Quantitative value testing: A/B tests, invite-only tests, discovery-program customers | Medium-High | "Quantitative Value Testing Techniques" |
| The discovery program has succeeded when its customers run the product in production and act as references | High | "Customer Discovery Program Technique" |
| Feasibility: engineers need time to investigate; the question list (know-how, skills, time, architecture, components and dependencies, performance, scale, infrastructure, cost) | Medium | "Testing Feasibility" |
| Feasibility is the tech lead's risk | High | Part II, "The Engineers" |
| Analytics categories (behavior, business, financial, performance, operational and go-to-market cost, sentiment) | Low-Medium | Quantitative testing chapter or the analytics material. Check the exact list |
| Protect customers, revenue and reputation while testing | Medium | I recall a section on testing responsibly in risk-averse companies. Only the general advice is attributed; the rules in section 10 are mine |

### B. Mine or yours, not the book's

- The six kinds of evidence, the three classes of result (qualitative, descriptive quantitative, inferential or causal) and the five readout questions. From your brief. The quality-check table, the four strength words (strong, moderate, weak, none) and the list of alternative explanations are mine.
- The three modes, the authorization rule for customer-facing actions, and the ban on invented results. From your brief. "Simulated users are not evidence" is mine.
- Thresholds need a stated basis; the six bases; exploratory readouts when no criteria were set; the retrospective label. From your brief. Two rules are mine: "provisional is a label, not a basis" (added after the first test round, where the model wrote "5 of 7" and called it provisional), and "criteria from more than one place: show both".
- The four decisions and the five-way diagnosis of a miss. From your brief. Scoping the decision to the hypothesis and not the idea is my reading of it.
- The experiment gate, the design table, the analysis steps and the alternatives table. The checklist items are from your brief; the gate, the interval-reading table and the alternatives are mine.
- Every formula, the three worked blocks, α = 0.05 and power = 0.80 as conventions, the sample-ratio threshold of p < 0.001, and the "fewer than about 10" rule of thumb for normal approximations. Standard statistics.
- The three feasibility states. From your brief. Security and operational constraints are added to the book's question list.
- The version log, the definition of a material change, and per-version reporting. From your brief.
- The recruitment-route bias table and sizing by method.
- Section 10 (customer-facing safeguards).
- The templates, the execution-artifact list, both examples (invented) and the validation cases.

### C. Where the skill departs from the book, flagged

- **The access signal.** As I recall, the book's example of access is asking for the login credentials of the product the user would switch from. The skill forbids collecting credentials and redefines access as the customer starting an authorized, secure process. From your brief.
- **Quantitative techniques are split.** The book groups A/B tests, invite-only tests and discovery-program use as quantitative value testing. The skill keeps all three and says only a randomized experiment supports a causal claim; use by selected customers is behavioral and descriptive. v1's "treat their production use as the quantitative evidence" is removed.
- **Think-aloud is optional.** v1 made it part of the protocol and attributed it to the book.
- **No participant count.** v1's "5–8 per round" (general practice, never the book's) is removed. Sizing follows the method.
- **Cheapest credible test.** v1 said "as cheaply as possible".
- **Demand tests carry more checks** than the book's treatment: trust and brand, account-owner agreement, nothing a customer relies on implying availability.

### Not carried over from my earlier review

- User test vs product demo vs walkthrough (I recall this from "Testing Business Viability"). The skill has one line: reactions to a demo are stated preference at best.
- "Ask how they solve it today before showing the prototype" is in the session script. Low-Medium that the book puts it there.

### Questions to answer with your copy

1. Does the qualitative value chapter's access example involve login credentials? If it does, the departure in C stands as written. If not, drop the first bullet of C.
2. Does "Testing Usability" ask participants to think aloud, or only tell the moderator to keep quiet?
3. Does the book call discovery-program use quantitative evidence, or only list it among the techniques?
4. Is there a section on testing responsibly, and what does it list?
5. Where is the analytics category list, and does mine match?
6. Does the feasibility question list match?

## inspired-stakeholders-viability

| Claim | Confidence | Where to check |
|---|---|---|
| PM responsible for knowing stakeholder constraints (business viability) | High | Part II, PM role; Part IV, "Testing Business Viability" |
| Functions covered: marketing, sales, customer success, finance, legal, business development, security, executives | Medium-High | "Testing Business Viability" |
| Preview prototypes one-on-one with stakeholders before building; not group reviews, not specs | High | "Managing Stakeholders" |
| User test vs buyer test in B2B | Medium | "Testing Business Viability" |
| Communicate learnings (not features) in a short regular update | Medium | "Communicating Product Learnings" |

General practice: the blocking/shaping/info rating, the per-function question table wording, the update template fields, examples.

## inspired-outcome-roadmap

| Claim | Confidence | Where to check |
|---|---|---|
| Problems with feature roadmaps rooted in the two inconvenient truths | High | Part III, "Problems with Product Roadmaps" |
| Alternative: give teams business problems and outcome-based objectives | High | "The Alternative to Roadmaps" |
| High-integrity commitments: only after discovery, for the few items that need dates | High | Same chapter |
| OKRs for product teams: qualitative objectives, measurable results, few, team-level, tracked openly | High (idea) / Medium (exact rules) | "Product Objectives", "Product Objectives @ Scale" |
| Weaning an organization off feature roadmaps | Medium-High | Part IV, transformation techniques |

General practice: the conversion tables, the "how to answer 'when will X ship'" scripts, examples.

## inspired-vision-principles

| Claim | Confidence | Where to check |
|---|---|---|
| Vision horizon roughly 2–10 years; visiontype and storyboard as formats | High | Part III, "Product Vision and Product Strategy" |
| The ten vision principles (start with why … evangelize continuously) | Medium | "Principles of Product Vision". My order and wording may differ |
| Strategy as a sequence of product/market fits; pick target markets by size, go-to-market, time to market | Medium-High | "Product Strategy" chapters |
| Five strategy principles (one market at a time, align with business and sales strategy, customers not competitors, communicate it) | Medium | "Principles of Product Strategy" |
| Product principles settle trade-offs (the book uses eBay buyers vs sellers) | Medium-High | "Product Principles" |
| Evangelism tips | Medium | "Product Evangelism". My list is partial |

General practice: horizon defaults (3–5 B2B, 2–5 B2C), the trade-off finding procedure, examples.

## inspired-team-diagnostic

| Claim | Confidence | Where to check |
|---|---|---|
| The failed-effort pattern (stakeholder ideas → business case → roadmap → requirements → design late → engineering late → agile only in delivery → validation at launch) | High | Part I, "The Root Causes of Failed Product Efforts" |
| Team principles (missionaries vs mercenaries, cross-functional, empowered, durable, flat reporting, colocated, scope, autonomy) | Medium-High | Part II, "Principles of Strong Product Teams" |
| PM needs deep knowledge of customer, data, business, market and industry; smart, creative, persistent | High | "The Product Manager" |
| Ten causes of lost innovation | Medium | Part V, "Top Reasons for Loss of Innovation". Check order and wording |
| Ten causes of lost velocity | Medium | Part V, "Top Reasons for Loss of Velocity". Check order and wording |
| Good team / bad team contrasts | High (idea) | Part V. Not reproduced as a list in the skill |
| Team structuring considerations at scale | Medium | Part II, "Principles of Structuring Product Teams" |
| Discovery sprint (one week) and pilot team as transformation techniques | High | Part IV, transformation techniques |

General practice: the scoring method (present / partly / absent / unknown), ranking by symptom, the output format.

---

## Deliberately left out
- Profiles of individual product leaders (Part II and IV sidebars).
- Product marketing detail: belongs to *Loved*.
- Coaching PMs and empowered-team leadership: belongs to *Empowered*.
- Operating-model transformation: belongs to *Transformed*.
