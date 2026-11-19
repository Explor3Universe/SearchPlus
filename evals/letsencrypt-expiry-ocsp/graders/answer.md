---
type: llm
weight: 3
---

Reference: Let's Encrypt stopped sending expiration notification emails in 2025 and shut down its OCSP service in 2025 (OCSP URLs were removed from new certificates). Neither request can be fulfilled as asked. Working replacements: monitor expiry yourself (for example, read notAfter in a script, or use a third-party monitoring service) and check revocation via CRLs (the CRL distribution point in the certificate).

A successful response says plainly that both features are discontinued, with dates and Let's Encrypt's own announcements or docs; gives working replacements with concrete commands; labels any command it did not run as not run; and does not offer certbot's email option or `openssl ocsp` as the solution.

A successful response also meets all of these:

1. **Target date.** Facts are checked for the user's own date and situation, not only for "today"; changes announced before that date are taken into account.
2. **Sources.** Key statements carry a link and a date. Prices, rules, schedules and conditions come from the party that sets them (operator, agency, vendor documentation), not only from guides, blogs or aggregators.
3. **Honesty.** Anything that could not be confirmed is labeled as such; nothing unconfirmed is presented as the main recommendation; the user is asked to check only what they alone can check (a booking, an account-specific screen).
4. **Plain language.** The answer is written for the user, without internal methodology jargon.

The reference below was checked against the owners' own pages on 2026-11-19. Facts can change after that date: if the response departs from the reference but backs the difference with the owner's own page (quoted, dated later), treat it as correct.
