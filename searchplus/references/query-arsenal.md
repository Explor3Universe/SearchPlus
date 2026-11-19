# The reformulation arsenal

The point of reformulating is not cosmetics ("the same words in a different order") but lighting up **a different slice** of the information space. The people who have the answer to your topic phrase it differently than you do. Your job is to go through their phrasings.

---

## 1. Lexical axes

- **Synonyms and domain jargon:** error → crash → panic → traceback → segfault; "doesn't work" → broken → fails → не работает → 一直报错.
- **Hypernym / hyponym** (broader / narrower): "state management" ↔ "Redux store rehydration"; "CSS layout" ↔ "grid subgrid support".
- **Abbreviations and expansions:** K8s ↔ Kubernetes; JWT ↔ JSON Web Token.
- **Brand ↔ generic:** "Docker Desktop" ↔ "container runtime on macOS"; "ChatGPT" ↔ "LLM chat".
- **Transliterations and calques** — for non-EN axes: see `languages.md`.
- **The owner's words:** how the owner itself names the object, its plans and states (`Starter`, `EOL`, `maintenance window`, `errata`, `Übergangsregelung`). Its terms lead to its documents.
- **Words from the results:** the best phrasings come from other people's pages. Found one relevant result — write down how its author names the problem and re-query in their words. This is the fastest way out of the dead end of your own phrasings.

## 2. Structural forms

The same topic exists in the results in different grammatical forms:

- **Question form:** "how to X", "why Y", "почему Y", "怎么 X".
- **Symptom form:** a description of the observation without a guess about the cause ("after laptop sleep, docker build hangs on resolving").
- **Error form:** the exact error text in quotes ("dns probe finished noerr").
- **API/command form:** the exact name of a function, flag, event (`--dns-search`, `ENOSPC`, `EPERM`).
- **Goal form:** what you want in the end ("make container resolve corporate DNS").
- **Problem form:** "X doesn't work when Y".
- **Comparison:** "X vs Y", "X alternative to Y", "X replacement".

## 3. Operators and filters

- `"exact phrase"` — pins the wording.
- `site:github.com`, `site:stackoverflow.com`, `site:zhihu.com`, `site:habr.com`, `site:news.ycombinator.com` — targeted vertical search.
- `intitle:`, `inurl:` — when the term must be in the title/URL.
- `filetype:pdf` — documentation, papers, datasheets, standards.
- `-exclusion` — cut off a dominant irrelevant meaning (`-movie -wikipedia`).
- `OR` — combine variants in one query (`"dns fail" OR "dns timeout" docker`).
- Year/version as text: `2025`, `python 3.12`, `ubuntu 24.04`.
- `before:` / `after:` — where supported, for a historical slice.

## 4. Temporal and version slices

- Topic + year: `X 2024`, `X 2025` — radically different results.
- `X changelog`, `X release notes`, `X migration guide`, `X deprecation`.
- `X breaking change`, `X regression`.
- A specific version: "worked in X 2.3, broke in X 3.0" — two separate queries, one per version.

## 5. The refutation axis: death queries (Law 0)

A found answer is a claim, not a fact (see Law 0 and `verification.md`). Until a refutation search has been run for the claim and a verdict reached, the sub-question is not closed. A death query is the **first** query after a claim appears, not the last item on the list of variations.

**Formula:** `[exact name of the claim] + [death verb] + [year]`, at least in the question's language and in EN, plus the news vertical (`+ news`, `site:` of news domains).

Dictionary of death verbs:

- RU: закрыт, отменён, прекратил, не работает, больше не, перестал
- EN: closed, shut down, discontinued, ceased, stopped, no longer, gone, bankrupt
- HE: נסגר, בוטל, הופסק, פשט את הרגל
- ZH: 停运, 关闭, 停止运营, 破产
- DE / FR / ES: eingestellt, geschlossen / fermé, supprimé / cerrado, eliminado

Types of counter-queries by situation:

- **operation of a service/line/company:** `[X] closed 2026`, `[X] больше не работает`, `[X] suspended`;
- **access condition:** `[X] requires …`, `[X] … required`, `[X] impossible without …` — plus going straight to the owner's documentation, billing and terms (`site:[owner domain] docs …`);
- **cause query (causal check):** `why X closed`, `X reform reason`, `почему X закрылся`, `למה X נסגר` + years — a change in the state of the world should have a causal mechanism (details — `verification.md`, "The cause query");
- **technical:** `X deprecated`, `X broken`, `X security issue`, `X known issue`, `X gotcha`, `X regression`;
- **live complaints:** `X reddit`, `X HN`, `X критика` (RU axis);
- **comparison:** `X vs Y` — how the candidate is worse than the alternatives.

Counts as passed when:

1. the results are **read**: all documents from the owner's domain in the results and the strongest contradicting result are opened;
2. each refutation found has passed **binding** (same object, segment, date, condition) and dating;
3. the owner confirms the claim on the right layer: base rule + exceptions for the target date, and for conditions — the binding terms.

News of the death of **this object**, dated after the owner's last live evidence, is stronger than any number of agreeing guides. News about a neighboring object or an undated page is a lead for checking with the owner, not a verdict.

## 5a. The owner's exceptions axis

A base rule (schedule, prices, documentation) is true "in general". The owner often publishes the state for a specific date separately. Queries and entry points:

- `site:[owner domain] disruptions OR status OR incidents OR "known issues" OR changelog OR "release notes" OR notices`;
- `[X] [target month/date] changes`, `[X] works / maintenance / travaux / Wartung + period`;
- `[X] upcoming changes`, `[X] from [date]`, `[X] will change`, `[X] transitional provisions`, `[X] amendments take effect`;
- pointer pages that the owner's page itself points to ("changes are not reflected here", "see section …");
- **special cases, when the base page is silent about the user's case:** `site:[owner domain] [X] exemption OR exempt OR "does not apply" OR "not required" OR "special cases"`, `site:[owner domain] "when you do not need"`, `[X] except / not required / exempt / exemption`; plus the owner's FAQ, factsheets, staff guidance;
- **official publication channel:** `[X] Federal Register / Official Journal / Bundesgesetzblatt / Journal officiel / official publication + year`, `[X] effective [date]`, `[X] fee adjustment [year]`, `[X] takes effect`;
- **the owner's mirrors, if its page is unavailable:** the owner's exact phrase in quotes, the same document on the sites of other missions, the press office, in the documentation repository (`site:[other official domain]`).

## 5b. The mechanism axis: solutions beyond the list of candidates

"Best of X" lists set the candidates, not the boundaries of the solution. For each function of the goal and for each near miss:

- `how to [function] without [constraint]` — `how to receive parcels without a home address`, `how to sign a PDF without a paid account`;
- `[candidate] workaround [violated constraint]`, `keep [candidate] [desired property]`;
- `[function] self-hosted`, `[function] alternative`, `[solution class] vs [solution class]`;
- neighboring nodes and categories: `[X] near [place]`, `[X] from [neighboring point]`, `[function] via another product category`.

A workaround is a separate claim: check with the owner whether it is allowed and what its risks are.

## 6. Social platforms as a separate slice

Phrase questions in the words people use to ask them: "docker dns hell", "почему отваливается", "求助 X 报错". Platforms: Reddit, HN, Stack Overflow, GitHub Discussions, specialized forums, Zhihu, Habr, Telegram channels (via site search).

## 7. Example formulation matrix

Topic: "why a Docker container loses DNS after the laptop sleeps".

| # | Type | Query |
|---|---|---|
| 1 | Symptom EN | `docker dns resolution fails after sleep` |
| 2 | Error | `"dns probe finished noerr" docker` |
| 3 | Jargon | `systemd-resolved docker dns break ubuntu` |
| 4 | Version | `docker 27 dns timeout ubuntu 24.04` |
| 5 | Vertical | `site:github.com docker dns sleep regression` |
| 6 | Social form | `docker dns after sleep reddit` |
| 7 | Death query (Law 0) | `docker dns fix removed deprecated 2026` |
| 8 | ZH (after the loop) | `docker 容器 DNS 解析失败 休眠 唤醒` |
| 9 | RU | `docker dns не работает после сна ubuntu` |

Nine queries — nine different slices of one topic. Each is run per Law 1 (down to garbage), all together — until exhaustion (Law 2).

## Stop rule

A variation is meaningful while it changes the slice. Two consecutive variations returned only duplicates → the formulation space is exhausted → next axis: language, vertical or backend.
