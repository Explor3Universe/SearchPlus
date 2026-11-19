<img width="2752" height="1536" alt="Gemini_Generated_Image_h352sfh352sfh352" src="https://github.com/user-attachments/assets/6782c9ab-bd06-4cdf-bb29-9c88e0de8667" />

# SearchPlus

**English** | [Русский](README.ru.md) | [Українська](README.uk.md) | [עברית](README.he.md)

[Installation](#installation) · [Example](#example-from-the-tests) · [Test results](#test-results) · [Limitations](#limitations) · [Changelog](CHANGELOG.md)

A skill that turns your AI agent into a master of search and information gathering and fixes the "dumb search" problem of modern AI. It gives your agent the ability to find even the rarest, most niche or little-known information on the internet — and to check whether it is still true.

The skill is based on in-depth research into the problems modern AI agents run into when searching the internet, and into their causes. To build it, a counter-methodology was developed: it fixes the problems of "dumb" search and builds, from scratch, an algorithm for deep search of rare, hard-to-find information on the web.

Below is a short description of the methodology and how it works.

## Introduction

Most modern AI agents can search the internet. When we need to find something, we increasingly prefer AI agents over search engines.

However, if this skill caught your interest, you have probably noticed, as the author of this project did, one very important thing: AI agents' search procedures are highly imperfect. Given a task that is harder than usual, an agent will very likely fail to do it the way you need, and in full.

To solve this problem and improve AI agents' search capabilities, I carried out research and analysis. A short summary of the results is below.

## Diagnosis: the main problems

I started by diagnosing and pinpointing the problems themselves, to understand what I would be dealing with at all.

The main problems found in how modern AI agents gather information on the internet:

**1. Primitive search strategies**

Most agents (regardless of which model they are built on) stop searching as soon as they have collected a certain number of sources that seem relevant to the model. It is a fixed number of sources: the agent studies them and returns a result.

By default, that is enough for most everyday questions whose answer lies on the surface. But for more complex tasks, this methodology cannot produce anything even close to the right answer.

**2. Methodologically wrong ways of validating the information found**

Most often (especially given the first point), agents do not validate the information gathered online well enough. Instead, they rely on the "average" across all the sources they collected, only checking whether a given source matches the overall mass of information collected. If 9 out of 10 sources say one thing and the 10th says another, the information from the 10th will almost always be disregarded.

This happens because, to save resources during information gathering, models are trained to verify information not logically (by collecting additional data and spending additional resources) but statistically — based on the data they have just collected. This methodology can work in general for simple questions or well-known facts. But when it comes to changing, impermanent information, this method is doomed to fail.

Worse, outdated information is almost always in the majority. Nine guides copied from each other describe how things used to be, while the tenth source is fresh news that everything has changed.

**3. Literal or narrow wording of search engine queries**

Most models do not reformulate queries (or barely change the wording). They literally cut a piece out of the user's prompt and send it to the search engine as is. The prompt is not analyzed logically; in effect, it is merely quoted. This severely limits the results.

This is especially noticeable with a language barrier — when the language of the information being sought differs from the language the user wrote the prompt in.

Some (but only a small fraction of) modern models already partly solve this problem by sending multilingual queries to search engines. However, I would not call it a complete fix: most of them have preset language settings and simply translate the original query into English or a couple of other predefined languages. There are AIs that adapt the language of the search query to the meaning of the prompt, but I know of only one or two such models.

**4. Too much trust in official sources on everyday questions**

According to the tests carried out, none of the modern models takes the human factor into account or can separate information with it in mind. Information from sources the model considers authoritative or official is unconditionally accepted as the ultimate truth and is, a priori, not subject to criticism or doubt.

But official sources are run by people too. The PR department embellishes. The marketing page promises one thing while the documentation requires another. The help section was not updated after a change. One department copies another's outdated text.

**5. Searching for confirmations instead of refutations**

Agents phrase all their queries affirmatively: "how to get there", "how much does it cost", "schedule". Not a single query of the form "X closed / cancelled / no longer works". In tests, models wrote outright in their reasoning "I should check whether this still works" — and did not make a single such query.

**6. Blind trust in their own memory**

The most dangerous statements are the ones the model considers obvious. Facts from memory never even get into the verification queue: the model double-checks its conclusions, but not its axioms.

**7. Skimming**

Agents often build the answer from search snippets or from the search tool's ready-made summary, without opening the pages themselves. The base page is taken as the complete answer, even though exceptions (changes, exemptions, special cases) are often published separately.

**8. A narrow solution space**

If there is no suitable option in the first "top 10 X" list, the agent concludes "there are no options". It does not look for workarounds or for solutions beyond the literal wording of the question, even though the right answer often lies exactly there.

## The new methodology and how the problems were solved

To solve these problems, I developed from scratch a methodology that describes the entire process of gathering (searching for) and validating information.

### A ban on stopping early

First, the model gets a direct ban on stopping early — including during the initial information gathering, if it suddenly seems to it that the answer has been found.

In my system, every piece of information found is a **CLAIM** (a hypothesis), not an answer. That is, whatever the model found after searching the topic is not, and cannot be, the answer to the question (task) it was given.

### The stop criterion

The stop criterion for the initial information gathering is that the new information coming in is no longer relevant. When the agent consistently starts getting irrelevant, garbage results, it stops searching and moves on to the next phases. This happens when it reaches deep pages of the search results where only poor-quality, low-relevance results remain, or when new phrasings stop producing anything new.

### Failure has to be proven

The agent cannot simply admit failure. Failure has to be justified: the agent must argue that every possibility was used and every available resource was examined, and show that it strictly followed the skill's methodology throughout. The very fact that information does not exist has to be proven.

### Multi-variant search queries

The initial information gathering uses a multi-variant methodology for phrasing queries:
- the agent takes the original search query as is;
- reformulates it using knowledge of how search engines work, to improve the results;
- reformulates it many more times to diversify the results (diversity is the key to raising the chance of getting the right result);
- analyzes the query and picks a language fork of 2–3 languages based on the content of the question, including the language of the place or of the information's owner, and then repeats all of the above in each language of the fork.

These steps alone greatly increase the amount of information the agent gets from search compared with classic scenarios.

### The validation phase: the death query and the cause query

Once the agent has finished the initial information gathering, the validation phase begins. If the question is specific and can have only one clear answer (even a detailed one), validation is applied to that answer. If the question is open-ended (for example, the agent needs to collect several possible answers), the same scheme is applied to each of them.

For every result obtained, the agent runs a death query and a cause query.

**The death query.** For every piece of information collected during the initial search, the agent uses search to check whether it is false or outdated: "X closed / cancelled / no longer works + year". It literally checks every piece of information logically for the possibility that it is false. The model's own knowledge is not a source here, but a claim like any other that has to be checked — and checked first.

**The cause query.** If, at the death-query stage, the agent found information that what it collected is false, it does not accept that blindly but moves on to the cause query. It tries to find a specific, logical cause — a factual, well-argued explanation of why the information is wrong: a reform, a closure, a rule change, a bankruptcy, and so on.

And the other way round: if the death query found nothing, that does not yet mean there are no refutations. News about a closure often lives not under the exact name but under phrasings like "why they disappeared" or "industry reform", so the cause query is run in this case too.

### Weighing: which is stronger — the source or the refutation

Having found confirmations and refutations, the agent does not count votes but weighs their strength:
- **The main judge is the "state owner"**: a source that is updated when the thing itself changes — the service operator, an official registry, documentation, a carrier's timetable. Guides, forums, directories and price lists are "witnesses of the past": they describe how things were and outlive what they describe.
- **Ten copies of one text are one vote, not ten.**
- **A cause found for the change makes a refutation many times stronger**: a refutation with a mechanism outweighs any number of guides without one.
- **A refutation is checked as strictly as the claim itself**: is it about the same object, the same date, the same user situation? News about a neighboring service closing does not refute this one.

The result is one of three verdicts: the claim is confirmed, the claim is refuted, or a draw. The verdict determines the order in the answer. Something unconfirmed is never presented as the main option, and a draw comes out with an honest "not confirmed" label and a way to check it yourself.

### The human factor and official sources

By default, an official source remains strong, but not unconditional. The agent distinguishes:
- who applies a rule and who merely talks about it;
- a binding document (documentation, terms, billing, an official publication) and a promotional one (a landing page, a press release, a pricing page);
- the base rule and the exceptions for the date in question (a disruptions page, changes, exemptions, special cases);
- facts the source is itself responsible for (a timetable, a price, conditions) and its assessments of itself ("reliable", "the best").

It is a filter, not a ban: both sides get checked — the official one and the unofficial one.

### An answer for the user's situation

All checks are made not "for now in general" but for the user's date and conditions: who they are, where they are from, which plan, document or version they have, and when they will need it. If the user is traveling in a month, the agent also looks for changes that will take effect before that date.

### Reading sources

The agent reads the pages themselves, not search snippets. A search tool's ready-made summary is not a source either: it is written by another model, with its own errors. A statement in the answer rests on a verbatim quote from the page.

### Searching for solutions, not just candidates

If an option fails one condition, the agent checks whether that condition can be legitimately worked around. And before saying "there are no options", it looks for solutions beyond the literal wording of the question: at a neighboring place, in another category, in a combination of several partial solutions.

### The final check of the answer

Before sending, the agent pulls every fact, number, instruction and command out of its draft answer and checks that each has a source confirming exactly that statement. Everything unverified is labeled. The answer is written in plain language and says separately what is confirmed (and as of which date), what is not — and how to check it.

### How the methodology was tested

The methodology was built iteratively:
1. real questions on which models made mistakes;
2. an analysis of exactly why;
3. a rule that closes the whole class of such mistakes;
4. a re-test on new questions.

The tests covered different areas (transport, hosting, certificates, entry rules, APIs, CI) on models of different tiers. Preliminary results:
- a small, fast model at the lowest reasoning effort with the skill performs on par with a mid-tier model without it;
- a mid-tier model at high reasoning effort with the skill scored best across all tests.

The sample is still small. A detailed methodology and the raw test results will be published separately.

## Example from the tests

The question: *"In early December 2026 I want to get from Paris to Berlin by night train, with a sleeper or at least a couchette, no flying. Which train actually runs now, how often, and where do I buy a ticket?"*

Same model, same reasoning effort, with and without the skill. Both answers found that the old Nightjet had been cancelled and that European Sleeper now runs the route three times a week. The difference was one level deeper:

- **Without the skill**, the agent took the operator's base timetable and built the plan around arriving at Berlin Hauptbahnhof. It noted in passing that track works are not included in the standard timetable and left it to the user to check the station.
- **With the skill**, after the base timetable the agent opened the operator's disruptions page for the travel dates: *"from 1 December to 11 December no stop at Berlin Hauptbahnhof… additional stop at Berlin Gesundbrunnen"*. Every departure the user could take in early December arrives at a different station, and the plan said so.

## Test results

The first multi-domain round had four questions: free Docker hosting, a night train, certificate expiry notices and OCSP, and Schengen entry. Each had an outdated-premise trap and an answer that can be checked with the owner. Each answer was scored from 0 to 3 (3 — correct, with the key facts confirmed at the source; 2 — correct with minor gaps; 1 — partly correct or a missed trap; 0 — wrong or misleading), 12 points maximum.

| Model and reasoning effort | Without the skill | With the skill |
|---|---|---|
| Mid-tier model, medium | 6 / 12 · 165k tokens | 9 / 12 · 257k tokens |
| Mid-tier model, high | 9 / 12 · 210k tokens | **12 / 12** · 347k tokens |
| Small fast model, medium | — | 7 / 12 · 281k tokens |
| Small fast model, low | — | 5 / 12 · 250k tokens |

The failures of that round were broken down by class, and each class was closed with a general rule rather than a fix for a specific question. The next round used five new questions: security updates after end of support, airside transit, CI pricing, a free weather API and visa-free entry.

| Configuration | Score |
|---|---|
| Small fast model, low effort, **with** the skill | 12 / 15 · 283k tokens |
| Mid-tier model, medium effort, **without** the skill | 12 / 15 · 195k tokens |

Before the revision, the same pair scored 5 / 12 against 6 / 12. The questions were different, so this is a consistent signal rather than a measurement.

Tokens are totals across all questions of a round. In those tests reading the skill cost about 15k tokens per question; the current English `SKILL.md` takes about 8k. There was one run per configuration and the scoring was not blind, so treat these numbers as preliminary. The tests were run on an earlier, Russian-language version of the skill; this English version is a translation and has not been benchmarked on its own yet.

## Limitations

- **Slower and more expensive.** In the tests the skill used about 1.6 times as many tokens and took about twice as long as the same model without it. For quick lookups that isn't worth it, so the skill is not meant to switch on for them.
- **Needs web search and page reading.** Without these tools the agent can only label claims as unverified.
- **Blocked pages stay blocked.** Captchas, 403 errors and pages that only render with JavaScript can't be read. The agent then looks for the owner's mirrors, but sometimes the honest result is "could not confirm".
- **Some checks are yours.** Availability and the final price for your exact date, or conditions tied to your account, show up only after you take a step yourself. The agent tells you what to check and what each result means.
- **Small models copy the form better than the substance.** At low reasoning effort they sometimes produce the tables and labels without doing every check.
- **The evidence is preliminary.** See the notes under the test results.
- **Not for timeless facts, math or your local code.** An ordinary answer is better there.

## Installation

### Claude Code (plugin)

```
/plugin install searchplus --marketplace Explor3Universe/SearchPlus
```

This works in one step on Claude Code 2.1.275 or later. On older versions:

```
/plugin marketplace add Explor3Universe/SearchPlus
/plugin install searchplus@searchplus
```

From the terminal:

```bash
claude plugin marketplace add Explor3Universe/SearchPlus
claude plugin install searchplus@searchplus
```

The skill switches on by itself for suitable questions. To call it explicitly, use `/searchplus:searchplus`.

### Claude Code (manual)

```bash
git clone https://github.com/Explor3Universe/SearchPlus.git
mkdir -p ~/.claude/skills
cp -r SearchPlus/skills/searchplus ~/.claude/skills/
```

For a single project, copy the folder into `.claude/skills/` inside that project instead. To call it explicitly, use `/searchplus`.

### Codex

```bash
codex plugin marketplace add Explor3Universe/SearchPlus
codex plugin add searchplus@searchplus
```

### Gemini CLI

```bash
gemini extensions install https://github.com/Explor3Universe/SearchPlus
```

### Other agents

The [skills CLI](https://github.com/vercel-labs/skills) installs SearchPlus into OpenCode, Amp, Codex, Gemini CLI, Claude Code and other agents that read the open Agent Skills format:

```bash
npx skills add Explor3Universe/SearchPlus
```

Or copy the `skills/searchplus/` folder into your agent's skills directory by hand.

Answer quality has so far been tested only in Claude Code; in the other agents, installation and skill discovery were checked.

## Evals

The `evals/` folder holds a suite for `claude plugin eval`:

- **trigger** cases check that the skill switches on for changeable facts and stays off for timeless facts, math, shell commands and explicit requests for a quick answer. They are cheap: each run is cut off after three turns on purpose, so the report marks it as stopped at the turn limit, and only the score matters. Allow the web tools, as in real work: without them a model may not reach for a research skill at all;
- **behavior** cases replay real questions from the tests and check the answer: a refutation search, pages actually read, no internal jargon, and the facts against a reference. They are expensive.

```bash
claude plugin eval . --tag trigger --allow-tools WebSearch WebFetch
claude plugin eval . --tag web --allow-tools WebSearch WebFetch --runs 1
```

The behavior cases are pinned to 19 November 2026. Their references were checked at the owners' sources on that date and will go out of date; the grader accepts a different answer if it is backed by a newer page from the owner.

## License

[Apache License 2.0](LICENSE)
