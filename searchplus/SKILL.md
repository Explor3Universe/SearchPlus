---
name: searchplus
description: Deep-research and verification mode. Every claim that can change must survive a refutation search ("X closed/discontinued + year") and a check against the live primary source (operator, registry, not guides or forums); the answer is "is this true for the user's date and conditions", not "is it described somewhere". Use when the answer depends on real-world facts that change or are hard to find - whether something still works, exists or is available; prices, conditions, limits, schedules, rules, requirements, versions, statuses; practical travel, product, service and API questions, even when the answer seems obvious; recommendations and comparisons for a decision; fact-checking; troubleshooting that needs issues, changelogs or known bugs; researching a topic, library or market; conflicting sources; ordinary search found nothing. Not for timeless facts (history, definitions, math), questions answered by local code or files, or when the user explicitly asks for a quick unverified answer.
---

# SearchPlus — ultimate deep-research mode

## Core — always executed, at every level

Everything else in this file amplifies and explains the core. If resources are short, execute the whole core and as many amplifiers as you can. The core is never cut.

1. **Target point.** Pin down exactly what the user needs and under which conditions: the object, the segment (who they are, where from, which plan/document/version/platform they have), the **target date** (when they will need it, not "now in general") and hard constraints. Every check is made against this point. The segment comes from the question, not from the environment you run in; anything not in the question is an assumption, and the answer names it as one.
2. **Solution space — by mechanism, not by list.** Break the goal into functions and constraints. Look for candidates for each function and for combinations of them. A "best of" list you found is one source of candidates, not the boundary of the search.
3. **Read pages, not snippets or summaries.** A search snippet, a search tool's own conclusion, a reading tool's retelling of a page — all are leads. The source is the page text, quoted verbatim.
4. **Take every changeable claim to its owner, for the right attribute and layer:** base rule → exceptions and changes for the target date → binding terms. If the base rule is silent about the user's case, that is not an answer — it is a reason to look for an exception with the same owner.
5. **The duel is symmetric.** Look for a refutation of every claim — and test the refutation itself the same way: same object, same segment, same date, same source class.
6. **Inventory is done on the draft answer.** Every fact, number, instruction and command in the text is tied to an opened page or marked "inference / not verified". If a load-bearing claim of the main recommendation is not confirmed, the recommendation is presented as conditional.
7. **Answer in the user's plain language.** Separately: is the fact true, and does the option fit the user. Internal labels (duel, owner, claim) stay in the log.

---

## Manifesto

You are not a go-between for the user and the first search result. You are an analyst who exhausts the topic.

- **A hypothesis, not an answer.** The first plausible result is a hypothesis: confirm it with independent sources and try to refute it.
- **Saturation instead of a find.** A query is closed when results degrade into garbage. A topic is closed when formulations, languages, verticals and solution mechanisms are exhausted.
- **Queries are dimensions, not attempts.** Each reformulation, language, vertical and backend lights up a different slice. Rotate the object; don't repeat the same thing.
- **"No information" and "no option exists" are provable statements.** You earn the right to say them only by exhausting the query matrix and the space of mechanisms.
- **Confirmation ≠ verification.** Ten agreeing guides are often ten copies of one outdated text. What verifies is the state owner and a failed attempt to refute, not consensus.

Depth is set by saturation, not quota: an easy question saturates after a few pages, a hard one after dozens of queries.

---

## Law 0. The self-refutation duel: every claim against its own refutation

Laws 1–3 govern search. Law 0 governs publication: **everything found by search is a claim, not a fact.** Every claim that wants a place in the answer goes through a duel: you look for its refutation and weigh which side is stronger. Only a winner is published as fact. Saturated results prove nothing: outdated text is abundant, SEO-fresh and unanimous.

The duel is mandatory for any statement that can change over time: whether a service works, a price, a condition, a schedule, a project's status, API behavior, a law, a version, "X exists / doesn't exist". Static facts (date of an event, authorship, the content of a commit) live by Laws 1–3: read the primary artifact itself.

### The mechanism, step by step, for EVERY claim — not only the main one

0. **Inventory of claims.** List every claim the answer will carry, marked by origin: `search` or `memory`. Claims from memory go first: they have no date and no search history, and confidence in them is highest. An "obvious" claim is not exempt — it is candidate #1: a model cross-checks its conclusions but not its axioms.
   **The list is the mandatory order of duels.** Go top to bottom (memory first), not by whatever turned up in the results. A lucky find is a bonus, but it does not close the other items.
   **The list lives until sending.** A claim that appears while writing the answer (an inference, a detail from memory, a command, a tip) goes through the same path — see phase 6.
1. **State the claim** in one sentence, present tense, with an operative verb and the **coordinates of the target point**: "X is available to [segment] under [condition] on [date]".
2. **Bind every piece of evidence.** Before counting a source FOR or AGAINST, check four coordinates against the claim:
   - **object** — the same product, plan, service run, version, rule, not a neighboring one. Different objects: retail and wholesale price; branches 2.x and 3.x; a scheduled service and a charter by the same carrier; a law and a bill; a personal and a business account;
   - **segment** — for the same user: country or city, account type, citizenship, region, platform. A source written for another segment brings its conditions along: instructions "for residents of another country", a price "for business", rules "for residents";
   - **time** — true on the target date. A base rule may be overridden by an exception for that period; an announced change may take effect before the target date;
   - **condition** — under which mode, profile, setting, plan it holds.

   If any coordinate does not match, the source speaks about a different claim. It is not a vote FOR and not a vote AGAINST. The rule is the same for confirmations and refutations.
3. **Collect FOR — from the owner, by attribute and by layer.** A state owner is a source that **is updated when the thing changes**. A tariff order, a directory, a POI on a map, a guide are not owners: they outlive the closure.
   - **The owner is defined by attribute, not by website.** Take the price, condition, schedule, availability from whoever sets that attribute. A third-party retelling of a price is a witness, even a fresh one. If several official bodies talk about the attribute, the owner is the one that **applies** it (the agency that checks and collects; the billing system that charges; the regulator that issues), not the one that tells about it (an information or promo portal, marketing, an industry association).
   - **The owner has layers, and you check all that concern the claim:**
     - *base rule* — schedule, price list, documentation, text of the rule;
     - *exceptions and changes for the target period* — disruption or status page, incidents, known issues, changelog and release notes, amendments and transitional provisions, announcements, "upcoming changes", "when X is not required" pages, exemptions and special cases;
     - *binding terms* — documentation, billing, terms of service, payment FAQ. They outrank the landing page, the pricing page and marketing summaries;
     - *official publication channel* — government gazette, register of legal acts, official journal, dated release note. There a change exists from its effective date, even if reference pages are not yet updated.

     A base rule without checking the exceptions layer gives "per the base plan", not "on your date".
   - **An owner's pointer must be followed.** If the owner's page says "changes are not reflected here", "details in section X", "see terms", open X. It is not a link "for the curious": this is how the owner tells you where the current state lives.
   - **Silence of the base rule is not an answer.** If the base page does not address the user's case (a special category, an intermediate stage, an exemption, an old version, a rare platform), look with the same owner for exception pages: "when X is not required", exemptions, special cases, FAQ, factsheet, staff guidance. The condition in the rule's wording ("if you pass through X", "for plan Y") draws its boundary: a case beyond the boundary is governed elsewhere, not by the same rule by default. The conclusion "the rule applies" is allowed only after the search for exceptions with the owner is done.
   - **Owner unavailable — look for its mirrors.** An owner usually publishes the same text in several official places: other missions or offices, the press office, the official gazette, the documentation repository, official accounts. A search restricted to the owner's domains (`site:`) yields its wording and the addresses of the pages you need. A third-party retelling while the owner is unavailable is a witness, not a substitute.
   - **Two pages of one owner contradict each other** → the more binding and more specific one wins: documentation beats the landing page, a page for the date beats a general one. If the hierarchy is unclear, it is a draw, not a win.
4. **Collect AGAINST — mandatory, and read it through.** At least one refuting query per claim: a death query `[X] closed/cancelled/discontinued/stopped/停运 + [year]` in the question's language, in EN and in the owner's language, plus related forms: `X stopped`, `X disappeared`, `X irregular`, `X complaints + year`, `X requires …` (for conditions).
   - **A counter-query is done only when its results are read.** You must open the relevant results from the owner's domain (documentation, billing, terms, status first) and the strongest contradicting result. An owner document in a counter-query's results that you did not open is an unchecked refutation.
   - **A contradiction from a weak source is not dismissed by rank.** It is a lead: find the owner's binding document on that very attribute. A lead can be dismissed by an owner document, not by the source's class.
   - **AGAINST counts as empty only after a cause query.** Results for the object's name are clogged by catalogs and price lists. News of a death lives under "industry X collapse / reform / why they disappeared", not under the exact name. A literal query returned nothing — that is "a query of the wrong shape", not "no refutations".
5. **Find the cause (cause query).** Ask: why could the statement be false at all? A change in the state of the world almost always has a mechanism: a reform, a law, a bankruptcy, a revoked license, repairs, a policy change, a crisis, a court ruling. Queries: `why X closed`, `X reform reason`, `почему X закрылся`, `X 倒闭 原因` + years. A cause found explains the whole class at once and dates the boundary: everything written before the cause's date is a witness of the past.
6. **Weigh — by causal strength and symmetrically.**
   - AGAINST has a causal mechanism → the refutation is strengthened many times over, and no number of agreeing guides outweighs it;
   - the claim "X works" has no carrier (operator, license, tariff, live page) → the claim hangs in the air;
   - **a refutation is a claim too.** It goes through binding (step 2), dating and the class check. An undated third-party page does not outweigh the owner's live page. News about a neighboring object does not refute this one;
   - **order in time.** If a refutation says "discontinued from date D" and the owner has active records after D (sales, schedule, updates, releases), the refutation is refuted;
   - a refutation with neither a cause nor a primary source is "silent": its weight is reduced; it is a signal to recheck the owner, not a reason to believe the claim;
   - **a value conflict with an effective date.** If sources give different values (price, term, limit, threshold) and one states an effective date later than the other's date and before the target date, it is the candidate for the current value. Check it in the owner's official publication channel. If you can't, present the new value as likely in force and the old one as previous — not the other way round;
   - **a requirement for the user remains unresolved** (amount, document, term, threshold) after searching the owner, including exceptions and mirrors → the answer gives the stricter value and explains the discrepancy: playing it safe costs the user less than being refused on the spot. This is the last step, not a substitute for searching for exceptions;
   - copies of one ancestor are one vote; equal weight is a draw, not a win.
7. **Verdict before publication — one of three:**
   - **CLAIM WINS** — FOR has an owner on the right layer (base plus exceptions for the target date, binding terms for conditions), and AGAINST, after a counter-query that was read through, is empty or weaker;
   - **REFUTATION WINS** — AGAINST is stronger → the claim is not presented as working;
   - **DRAW** → only with the label "not confirmed"; no instructions to act, except instructions on how to check.

   **An empty AGAINST does not win by itself.** Without an owner, a stack of agreeing witnesses of the past remains unverified: "no refutation found" and "no confirmation found" are the same emptiness.

   **The verdict drives the ranking.** A claim with a draw or a refutation does not come first and is not called "the main way". If there is no winner, say "no reliable option found in this category".

   **Resolve a draw yourself if you can.** If the owner publishes the answer, find it rather than passing it to the user. If only the user's action can resolve the draw (sign-up, call, booking), present the option as conditional, with an exact check: what to do and what each result means.

### Duel rules

- **The verdict lives in the log and in the answer, not in your head.** In the answer it is expressed in plain words (see "Answer standard").
- **A refutation cannot be tacked on at the bottom.** Finding AGAINST, mentioning it as a caveat and keeping the recommendation means losing the duel and hiding it. AGAINST is stronger → the recommendation is withdrawn, not softened.
- **A document confirms only its own content.** A tariff confirms a price, not operation; a POI confirms an address, not a service; a mention of X in an order does not confirm that X works. Ask: "would this source change if X closed?" No — it does not prove X is alive.
- **Official ≠ disinterested.** A source that sells the claim (a vendor about itself, a press release, a landing page) confirms operational facts, but its assessments of its own qualities and its promises are self-promotion. A third-party "authority" retelling the vendor inherits its interest. This is a filter, not a ban: official sources are a strong class by default, and in a dispute both sides are checked.
- **Swapping the claim is a new duel.** "Officially no, but de facto yes" is a different claim with its own duel. "De facto", "rumored", "semi-legal" give at most a draw.
- **A near miss is not a rejection.** If a candidate fails one constraint, ask by which mechanism it violates it and whether that mechanism can be legitimately neutralized: by a setting, a workaround, a combination with another component, a neighboring point, date or category. A workaround is a separate claim with its own duel: is it documented, does it break the owner's rules, what are its risks.
- **The boundary of the question ≠ the boundary of the solution.** A solution may lie outside the question's words: at a neighboring place or node (services often start beyond an administrative, jurisdictional or licensing boundary), in a different product category, in a combination of components (two partial solutions together make a whole), at a different time. Before declaring "no option exists", go through the mechanisms that achieve each function of the goal, not only the vendors from "best of" lists.
- **An answer's role is filled only by a winner.** If the best candidate in a category is refuted, don't soften the corpse: search for a replacement until a live winner appears, or conclude "no live option in this category". Look for replacements with system owners (full lists of networks, lines, plans, registries) and by mechanism, not by mentions in guides.
- **Count by class and causal strength, not by number.** A directory + a blog + a guide + a forum = one class of witnesses of the past, one vote. The main weight multiplier is a cause found.
- **Selective verification is forbidden.** A duel for the main claim does not cancel duels for the others; checking a secondary item does not close the main one.
- **Doubt is an obligation.** The thought "I should check whether it still works" is an open duel: close it, or put it in the answer as "not confirmed".
- **Absence is a claim too, and it gets the strictest judge.** "X does not exist / is not there / does not run" is proven only by the system owner's full list plus an empty death query. Silence of indexes, aggregators and empty results does not prove absence.

---

## Intensity levels

| Level | When | On top of the core |
|---|---|---|
| **Fact check** | One specific fact | A duel for every claim; 3+ independent sources for static facts |
| **Standard research** (default) | Any "gather information" task | Full cycle (phases 0–6); languages: the question's + EN + the owner's or the place's language if the subject is local; verticals by domain |
| **Deep research** | Niche topic, contradictions, high cost of error, empty first page, the user asks to go "deep" | Full matrix: formulations × languages × verticals × snowballing × several backends; log to a file |

Escalation rule: on **any** sign of difficulty (a contradiction, a niche domain, data older than 2 years, a question about a specific version, garbage in the results, a unique find in one language segment) move up a level. Having started deep, don't "speed up".

Volume is set by saturation, but the spending must do work: each step closes a specific claim or a specific axis. Repeating the same query, a third attempt to open the same unavailable page, and reading what you've already seen are spending without work.

---

## Law 1. Query saturation

A query is not closed by a find.

1. Open and **actually read** the first 5–10 results — pages, not snippets. Extract facts and promising links from each.
2. **Even if the answer is in the first result**, keep opening the next ones.
3. Stop only on signs of garbage: persistently irrelevant topics, repeats, SEO dumps, the bottom of the results.

Search tools often have no "page 10". The role of deep pages is played by **query variations, other backends and verticals** (Laws 2–3). If several search tools are available, run key queries through at least two. If there is only one, compensate with variations and direct reading of owners' sites.

### How to read a source

- **Ask neutrally.** The question to the page: "what does it say about X, which object, segment and date does that refer to, is there a publication date". Don't put the expected answer into the question: the reading tool will gladly confirm the hint.
- **Ask for verbatim quotes** for everything that goes into the answer, together with what the quote refers to.
- **Note pointers.** Links to sections on changes, terms, status, archives are candidates for a mandatory follow-up (Law 0, step 3).
- **Page date ≠ fact date.** A fresh page may carry an old fact; find when the fact was established and which period it describes.
- **A tool's summary is not a source.** A search tool's conclusion ("Bottom line", "Short answer"), an AI overview of results, a reading tool's retelling of a page are written by another model and inherit its errors and hints. They show where to look; a statement in the answer rests on a verbatim quote from the page. If the summary draws a conclusion that is not in the quotes, it is the summary's own guess.
- **Don't guess addresses.** Take URLs from the results or from links on pages. A 404 on a guessed address proves nothing — neither that the page is missing nor that the rule is.
- **Unavailable does not mean read.** Captcha, 403, an empty page, headings only (JS rendering) — `BLOCKED`. After two such responses from one domain, change the access method: another official domain or mirror, a text, API or .md version, a search for the owner's exact wording, a cache. A third address on the same domain with the same tool is a dead end.

---

## Law 2. Exhausting formulations

Saturating one query is a signal to reformulate. At least 4–8 meaningful variations (more for the deep level), until the variations return only what you've already seen.

Mandatory variation types:

- synonym, domain jargon, **the owner's words** (how the owner itself names the object and its states);
- symptom form (a description of the observation, not a guess about the cause);
- exact text of an error, function name, flag — in quotes;
- version + year (`docker 27 dns 2025`);
- operators: `site:`, `intitle:`, `filetype:pdf`, quotes, minus exclusions;
- social form: how real people ask the question (`... reddit`, `... forum`, `... 知乎`);
- **a counter-query is not "one of the variations" but a mandatory step once a claim appears** (Law 0);
- **mechanism query** — how the goal's function is achieved by other means: `X alternative without Y`, `how to keep X Y`, `X workaround`, `self-hosted X`.

The full arsenal with examples is in `references/query-arsenal.md`.

Stop rule: two consecutive variations returned only duplicates → the formulation space is exhausted; move to the next axis (language, vertical, backend).

---

## Law 3. The language matrix

The whole cycle (Laws 1 and 2) is repeated **in every language of the axis**. A single trial query in another language is an imitation.

Starting axes:

- base: the question's language **+ EN** — always;
- **the owner's or the place's language** if the subject is local: news about repairs, closures, reforms and rules appear in the local language earlier and in more detail than in English;
- complex and niche topics: **+ ZH, + RU** (skip RU if it is the question's language);
- further by domain — see `references/languages.md`.

**Terminology loop:** translate the query and back-translate it → go through Laws 1–2 → write down native terms from the results → re-query with them → repeat until saturation.

A unique fact from one language segment must be checked in others: segment isolation breeds errors.

---

## The full research cycle

**Phase 0 — Decomposition and target point.** Sub-questions; what counts as an answer to each; the target point (object, segment, date, constraints); the goal's functions and the classes of mechanisms that can deliver them; primary sources and their layers (base, exceptions, terms). Plan: starting queries, languages, verticals. Ask the user only about an ambiguous goal, when different readings lead to different searches; anything that search can find out, find out yourself.

**Phase 1 — Pass over the results.** Law 1 for the starting query.

**Phase 2 — Digging deeper.** Keep opening results beyond the first success until signs of garbage. Don't skip "dissimilar" results — counter-facts live there.

**Phase 3 — Reformulation.** Law 2: next variation → phases 1–2 again.

**Phase 4 — Switching language.** Law 3.

**Phase 5 — Verticals, snowballing, mechanisms.**
- Verticals: every domain has places where knowledge lives locally (issues, Stack Overflow, changelogs, Zhihu, Habr, arXiv, specialized forums). Catalog — `references/verticals.md`.
- Snowballing: follow links from every strong page; look for discussions of what you found (`URL + reddit|HN|forum`).
- Mechanisms: for every rejected candidate, a near-miss check; for the goal as a whole, a search for solutions beyond the question's wording.

**Phase 6 — Synthesis: draft → inventory of the draft → answer.**
1. Write a draft answer.
2. Pull out of the draft **every** fact, number, date, condition, instruction, command. Find a source for each in the log. No source — it is a new claim: a duel or the label "inference / not verified". The link must confirm exactly this statement — the same value, the same object, the same date. Check it against the quote; don't substitute the nearest URL on the topic.
3. **A load-bearing claim** is one without which the main recommendation collapses. It must win its duel. An unverified load-bearing claim turns the recommendation into a conditional one.
4. **Commands and code are claims too.** If the environment allows, run them; if not, mark them "not run".
5. Check the ranking against the verdicts and rewrite the answer per the "Answer standard".

At the "Deep research" level, phases 3–5 nest: language → formulation → vertical, and each cell goes through Law 1.

---

## Exact stop conditions (saturation criteria)

**A query is closed** (any of):
- the last ~10 results gave no new source or fact;
- the results are persistently irrelevant to the topic;
- the sub-question is confirmed and each of its claims has won its duel.

**A sub-question is closed:** confirmed by 3+ independent dated sources (not quoting each other) for static facts; for technical statements, one of them is a primary source (documentation, standard, author, code). For changeable facts — a won duel: an owner on the right layer, exceptions for the target date checked, the counter-query read through.

**A topic is closed:** all sub-questions are closed + every language axis is saturated + new variations yield less than ~10–20% new material + the duel is won for every load-bearing claim + for "no option exists" the mechanisms have been gone through.

**Not a closure:**
- `BLOCKED` — the page was not read, so the source was not checked;
- silence of indexes — a table of contents, an index, a `site:` search and empty results do not prove that an entry, an amendment or a line does not exist.

---

## Contradictions

A contradiction between sources is a signal: behind it there are usually different objects, segments, dates or versions.

1. Record it in the log (what, where, when).
2. Check the binding: do the sides talk about different objects, segments, dates?
3. Find the reason for the discrepancy (date? version? region? the author's interest?).
4. Resolve it with the owner if the owner publishes the answer — yourself, without passing it to the user. Otherwise honestly mark it as unresolved.

**A discrepancy is not settled by voting.** Nine against one is a question to both: aren't the nine copies of one ancestor, and what are the class and date of the tenth? A fresh primary outlier beats nine old copies.

Ignoring a contradiction and quietly picking what you like is forbidden.

---

## Research log

Keep it from the first minute. Format — `references/log-template.md`. Rules:

- every entry right after the query: text, language, backend, status (`NEW` / `DUP` / `GARBAGE` / `CONTRA` / `STALE` — the source is alive, the fact is outdated / `OFFSCOPE` — about a neighboring object, segment or date / `BLOCKED` — not read), summary of what is new;
- key claims — in a duel table: FOR and AGAINST with class, date, layer and binding; which is stronger; verdict;
- before every new query — a check: am I repeating myself?
- contradictions — into a separate section immediately;
- "Deep research" and tasks with more than ~15 expected queries — log to a `research-log.md` file in a temporary folder or one the user specifies, not in the project's working directory; for short tasks, an internal log of the same format.

---

## Answer standard

- **Two axes, never mixed:**
  - **fact** — confirmed (by the owner, with the page date) / single source / not confirmed / outdated or refuted;
  - **fit of the option for the user** — fits / fits on condition … / does not fit, because …

  "A subscription is required" when the condition is "free" means "does not fit", not "refuted".
- **Plain language.** Instead of "the claim won the duel, the owner is alive" — "confirmed on X's site (page dated DD.MM)". Instead of "draw" — "could not confirm: …; you can check it like this: …". The skill's internal terms don't belong in the answer.
- Every key statement comes with a source (URL) and the source's date; for a changeable one — the date it was checked for, and a note on whether the exceptions layer for the target date was checked.
- A table of options has columns "what is confirmed" and "does it fit you"; unconfirmed options do not come first.
- Instructions to act (where to go, how much to pay, what to run) — only for what is confirmed for the target date. Everything else is labeled or not published.
- Only checks that require the user's own action are passed to the user — with a concrete step and what each result means.
- Inferences, details from memory and assumptions about the user are labeled; commands and code are run or labeled "not run".
- Contradictions: which were found and how they were resolved.
- "Not found" or "no option exists" — only with an exhaustion table: formulations, languages, verticals, mechanisms.
- If there is nowhere left to search, say so: "the matrix is exhausted, new material <X% per query".

---

## Before sending the answer (checklist)

1. **Target point** — object, segment, date and constraints are pinned down, and checks were made against them, not against "now in general"? The segment comes from the question, assumptions are named?
2. **Solution space** — mechanisms and combinations gone through; near misses checked for rejected candidates; looked for solutions beyond the question's wording?
3. **Inventory of the draft** — every fact, number, instruction and command in the text is tied to an opened page or labeled? Every link confirms exactly its own statement? Load-bearing claims verified?
4. **Binding** — every piece of evidence, FOR and AGAINST, is about the same object, segment, date and condition?
5. **Owner by layer** — base rule + exceptions for the target date + binding terms + official publication channel; the owner's pointers followed; the owner is the one who applies the rule?
6. **Silence and unavailability** — if the base is silent about the user's case, did you search for the owner's exceptions? If the owner is unavailable, did you look for its mirrors?
7. **Source, not summary** — no statement rests on a search tool's conclusion or a retelling without a verbatim quote; no guessed addresses?
8. **Counter-query and symmetry** — owner documents from the results opened; a weak contradiction checked with the owner; refutations passed the same tests; in a value conflict, the new value with an effective date checked?
9. **Ranking** — the unconfirmed doesn't come first; what can be checked with the owner was checked, not passed to the user; an unresolved requirement given at the stricter value with an explanation?
10. **Form** — plain language, two axes (fact / fit), source dates, no internal labels?
