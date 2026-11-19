---
type: llm
weight: 3
---

Reference: OpenWeatherMap One Call 2.5 was closed in 2024. One Call 3.0 gives 1,000 free calls a day, but only through a subscription that requires payment card details, and its hourly forecast covers only 48 hours, so it does not meet "hourly for 7 days, no card". Open-Meteo is free for non-commercial use without an API key (under 10,000 calls a day) and provides hourly forecasts for 7 days and more, so it fits.

A successful response rejects One Call for these reasons, citing OpenWeatherMap's own pages; recommends an option that meets every constraint, with its terms from the provider's docs; and gives a request example, labeled if not run.

A successful response also meets all of these:

1. **Target date.** Facts are checked for the user's own date and situation, not only for "today"; changes announced before that date are taken into account.
2. **Sources.** Key statements carry a link and a date. Prices, rules, schedules and conditions come from the party that sets them (operator, agency, vendor documentation), not only from guides, blogs or aggregators.
3. **Honesty.** Anything that could not be confirmed is labeled as such; nothing unconfirmed is presented as the main recommendation; the user is asked to check only what they alone can check (a booking, an account-specific screen).
4. **Plain language.** The answer is written for the user, without internal methodology jargon.

The reference below was checked against the owners' own pages on 2026-11-19. Facts can change after that date: if the response departs from the reference but backs the difference with the owner's own page (quoted, dated later), treat it as correct.
