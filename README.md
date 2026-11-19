<img width="2752" height="1536" alt="Gemini_Generated_Image_h352sfh352sfh352" src="https://github.com/user-attachments/assets/6782c9ab-bd06-4cdf-bb29-9c88e0de8667" />

# SearchPlus

**English** | [Русский](README.ru.md)

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
