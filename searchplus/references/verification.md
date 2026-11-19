# The self-refutation duel — a practicum

A supplement to Law 0 in `SKILL.md`. The duel rules live there; here are the evidence hierarchy, the weight scale, the owner test and a breakdown of typical failures. If anything here disagrees with `SKILL.md`, `SKILL.md` wins.

## The central idea

Search finds **text**. Text describes **the past** — the moment it was written — and **a specific context** — the object, segment and conditions it was written for. Between a find and an answer stand two questions that search itself does not close:

1. **What is the state of things on the user's target date?**
2. **Is this about the same object, segment and condition the user needs?**

A changeable fact has a **state owner** — whoever is authorized to say how things are now and who updates the source when the thing changes: the service operator, the agency, the code author, the timetable publisher, the official registry. Guides, forums, price lists and directories are witnesses of the past: they outlive what they describe.

## When the duel is mandatory

Anything that can change over time:

- whether a service, line, shop, project or company works or exists;
- prices, tariffs, access conditions, schedules, opening hours;
- statuses: deprecated, EOL, renamed, acquired, closed;
- behavior of software, flags, APIs between versions;
- laws, rules, requirements;
- "X exists" and "X does not exist".

No duel is needed for dates of historical events, authorship, the content of a specific commit, letter or release. They have their own law: read the primary artifact itself, in full.

## Five checks

### 1. Binding

Before counting a source as a vote FOR or AGAINST, check four coordinates:

| Coordinate | Question | Typical transfer |
|---|---|---|
| Object | The same product, plan, service run, version, rule? | News about the closure of a neighboring product from the same company; a rule for another API version; another plan from the same lineup |
| Segment | For the same user: where they are from, which account, document, region, platform they have? | Instructions written for users of another country; a corporate price instead of a consumer one; a rule for residents |
| Time | True on the target date? | A base schedule without the exceptions for the period; a condition that will change by announcement before the target date |
| Condition | Under which mode, profile, setting, plan? | "Free" during a trial taken as "free forever" |

A mismatch on any coordinate turns the source into evidence about a different claim (`OFFSCOPE` in the log). It neither confirms nor refutes the target claim.

### 2. Death query

Formula: `[exact name of the object] + [death verb] + [year]` in the question's language, in EN and in the owner's language, plus the news vertical.

Dictionary of death verbs:

- RU: закрыт, отменён, прекратил, не работает, больше не, перестал, приостановлен
- EN: closed, shut down, discontinued, ceased, stopped, no longer, suspended, bankrupt
- HE: נסגר, בוטל, הופסק, פשט את הרגל
- ZH: 停运, 关闭, 停止运营, 破产
- DE / FR / ES: eingestellt, geschlossen, ausgesetzt / fermé, supprimé, suspendu / cerrado, eliminado, suspendido

For access conditions add the requirement form: `X requires …`, `X … required`, `X impossible without …`.

Passed if the results were **read** (owner documents in the results opened), no news of the death of this very object was found, **and** check 3 was done.

### 3. Primary liveness — by the owner's layers

Evidence hierarchy for "true on the target date":

| Source | What it proves |
|---|---|
| The owner's exceptions page for the target period (disruptions, status, incidents, known issues, amendments) | the state **on that date**; stronger than the base rule |
| The owner's live base-rule page (schedule, prices, documentation, registry) | works **per the base plan**; without checking exceptions — not "on your date" |
| Binding terms (documentation, billing, terms of service) | the access condition; stronger than the same owner's landing page and pricing page |
| Official publication channel (gazette, register of acts, official journal, dated release note) | a change from its effective date; stronger than reference pages not yet updated |
| Landing page, pricing page, marketing summary | the owner's statement about itself; for conditions — until checked against the binding terms |
| Fresh dated news about the closure or change of **this object** | does not work / has changed — stronger than guides; loses to the owner's live page dated after the event |
| Fresh dated news about operation | works (secondary to the owner) |
| Dated guide, forum | "worked as of the post date" |
| Undated guide, forum, directory, price list | nothing: directories outlive services |
| Model memory | a hypothesis: wrong both ways on changeable facts |
| A search tool's summary, an AI overview, a reading tool's retelling of a page without a verbatim quote | nothing: a lead on where to look |

Classic traps:

- **"There's a tariff, so there's a service"**: a line in a tariff table stays after the service dies.
- **A directory with "opening hours"**: catalogs are not obliged to remove dead businesses.
- **A fresh page with an old fact**: page date ≠ fact date.
- **The base plan instead of the date**: a schedule or documentation is true "in general", but an exception published separately applies for the target period.
- **A landing page instead of terms**: the pricing page promises one thing, the billing documentation requires another.
- **Silence of the base**: the base page does not mention the user's case, and an exception for it is published on a separate page of the same owner.
- **Reference pages lag behind the gazette**: a new value is already in force per the official publication, while reference pages and retellings still show the old one.

### 4. Dating the fact

For each source write down: when it was written, when it was updated, which period it describes. An undated source does not confirm a changeable fact. A fact's freshness is the maximum over the dates of owner sources, not over the freshest page.

### 5. Independence

How does the source know what it writes? Does it quote another guide? Rewrite the vendor? One ancestor = one source.

## Weight scale

| Evidence | Weight for "true on the target date" |
|---|---|
| The owner's exceptions page for the target period | maximum |
| The owner's live base-rule page, exceptions checked | maximum |
| The owner's binding terms | maximum for access conditions |
| The owner's official publication channel | maximum for rules, fees and limits from the effective date |
| The owner's live base-rule page, exceptions **not** checked | high, but only "per the base plan" |
| Fresh dated news of the death of **this object** (binding passed) | high |
| A report by a government body, audit or controller (a register of facts) | high |
| The owner's landing or pricing page — for conditions | medium: needs checking against the binding terms |
| Fresh dated news about operation | medium |
| Dated guide, forum | low |
| Undated guide, forum, directory, price list | zero |
| Any source that failed binding | zero for this claim |
| A search tool's summary or a retelling without a quote | zero: a lead |
| Model memory | zero: a hypothesis |

Weighing rules:

- Compare **the best of FOR with the best of AGAINST**, not quantity with quantity.
- One scale for both sides: a refutation goes through binding, dating and class just like a confirmation.
- Copies of one ancestor = one vote. A hundred guides of one class are one guide.
- Equal weight is a draw. A draw is not published as fact.

## The cause query: a causal check

A change in the state of the world almost always has a **mechanism**: a reform, a law, a bankruptcy, a revoked license, repairs, a policy change, a crisis, a court ruling. Before a verdict, look for it with a query.

**Formula:** `why/почему/为什么 + X + closed/stopped/cancelled/shut down` + years; for temporary changes — `X repairs / works / maintenance / closure + period`.

What a cause gives you:

1. **Explains the whole class at once**: the closure, why the guides are wrong, and why directories still show tariffs.
2. **Dates the boundary**: everything written before the cause's date is a witness of the past.
3. **Strengthens a refutation** with a mechanism against any number of mechanism-free confirmations.
4. **Checks the claim symmetrically**: a live service has a carrier — an operator, a license, a tariff, a schedule, an economy.
5. **Explains an exception**: a cause found for a temporary change (repairs, migration, a temporary restriction) confirms that the exception on the target date is real and shows when it will end.

**A silent refutation** — with neither a cause nor a primary source — has reduced weight. But the absence of a cause does not revive the claim automatically: the owner decides, not silence.

## The state-owner test

An owner is not "any official document" but a source that **is updated when the thing changes**. Questions:

1. If X changes tomorrow, will this source change?
2. Does it speak for the target date, or describe the past or the base plan?
3. Does it address X in substance, or mention it in passing (via a tariff, an address, a ban)?
4. **Which layer is it:** base rule, exception, binding term or marketing? Is its layer enough for the claim?
5. **Is there a pointer on the page** ("not reflected here", "see section", "terms") — and was it followed?
6. **Interest:** what does the source lose if the claim is false? An owner is legitimate on operational data and illegitimate on assessments of itself.
7. **Does the source apply the rule itself** or only tell about it? If official bodies disagree, the one that checks, charges, issues or collects decides.
8. **Does it address the user's case** or stay silent about it? Silence of the base page is a reason to look for exceptions with the same owner, not grounds to apply the general rule.

Failing questions 1–3 — not an owner. Failing 4–8 — an owner, but the check is not finished: wrong layer, a pointer not followed, the wrong body, or the user's case not covered.

**A filter, not a ban.** Official sources are a strong class by default and often the owner. Suspicion arises with a conflict of interest, in evaluative questions, and when pages of one owner disagree. In such disputes both sides get the full check.

## Memory — a claim with no date and no history

"Everyone knows X works", a schedule, a price, a command's syntax from memory — a claim with zero search history. It is doubly dangerous: confidence in it is highest, so it doesn't get into the verification queue, and it spreads between models like an echo. Such claims most often appear **while writing the answer** — which is why the inventory is done on the draft (phase 6 in `SKILL.md`).

## Typical duel failures

Each failure is a class, not a case. Recognize it by its sign.

| Failure | Sign | What to do |
|---|---|---|
| **Refutation tacked on at the bottom** | AGAINST found, mentioned as a caveat, recommendation kept | AGAINST is stronger → the recommendation is withdrawn |
| **Rescue by substitution** | "Officially no, but de facto…" without its own duel | A new duel; a draw at most |
| **A document taken for the owner** | A tariff, an order, a POI "confirm" operation | Owner test, question 1 |
| **Counting by number** | "Confirmed by 4+ sources" without an owner | Count by class |
| **Transfer from a neighbor** | Evidence about another object, segment or date counted for or against | Binding, check 1 |
| **Refutation without a check** | An undated third-party page outweighed the live owner | One scale for both sides; order in time |
| **Ritual counter-query** | Query made, results not opened; the owner's document in the results not read | A counter-query is closed only by reading |
| **Dismissal by rank** | A contradiction from a weak source thrown out instead of checked with the owner | A weak contradiction is a lead to the binding document |
| **Base plan instead of the date** | A general schedule or documentation taken; the exceptions page not opened, a pointer ignored | The owner's layers; pointers are mandatory |
| **Landing page instead of terms** | The pricing page taken as the condition while the documentation is silent or contradicts it | Binding terms beat the landing page |
| **Rejection by one constraint** | A candidate rejected, the mechanism of the violation not examined | Near miss |
| **Blindness to a neighboring solution** | "No option", though the solution lies beyond the question's boundary (a neighboring node, another category, a combination) | Go through mechanisms |
| **A claim after the inventory** | An inference, a detail from memory or a command appeared while writing and passed unchecked | Inventory on the draft |
| **Passed to the user** | "Check it yourself", though the owner publishes the answer | Resolve with the owner |
| **A hint in the question to the page** | The expected answer put into the request to the reading tool | Neutral question, verbatim quotes |
| **A summary instead of a source** | A conclusion taken from a search tool's result or a page retelling; no verbatim quote | A summary is a lead; a statement rests on a quote |
| **Silence of the base taken for the rule** | The base page does not mention the user's case, and the general rule applied without searching for exceptions | Search for the owner's exceptions; the rule's condition draws its boundary |
| **Old value despite a new one found** | A new value with an effective date before the target date found but presented as "not confirmed", with the old one as primary | Check in the official publication channel; the new one is likely in force |
| **The wrong official body** | Of two disagreeing official sources, the first one at hand taken | The owner is the one who applies the rule; an unresolved requirement — at the stricter value, with an explanation |
| **Third-party retelling while the owner is unavailable** | The official page didn't open — and the answer is built on retellings | The owner's mirrors, search across its domains |
| **A guessed address** | A URL composed by guesswork; a 404 taken as an answer | Addresses only from the results and from links |
| **Segment from the environment** | The user's properties (country, OS, plan) taken from the agent's environment rather than the question | Segment from the question; the rest is a named assumption |
| **A link about something else** | The statement is backed by a link to a page with a different value, object or date | The inventory checks the link against the statement by quote |

## What a won duel looks like

An inventory with the target point's coordinates → death queries in the question's language, EN and the owner's language → counter-query results read, owner documents opened → the cause found (if there was a change) → the base rule and the exceptions layer for the target date checked with the owner, pointers followed, the base's silence about the user's case checked by searching for exceptions, new values checked against the official publication channel → workaround mechanisms checked for rejected candidates → the refuted demoted, not softened → the replacement confirmed by the owner → for what can't be verified, an honest draw with a concrete way for the user to check.

Signs: the load-bearing claim is confirmed by the owner on the right layer; no evidence is taken from a neighboring object; the answer says in plain words what is confirmed, what is not, and how to check the rest.
