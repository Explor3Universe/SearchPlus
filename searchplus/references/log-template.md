# Research log template

The log is kept from the first minute and updated **immediately** after every query. Before every new query — a check against the log: am I repeating myself?

When to move it to a file: the "Deep research" level or more than ~15 expected queries → `research-log.md` in a temporary folder or one the user specifies (not in the project's working directory). For short tasks — an internal log of the same format.

Query statuses:

- `NEW` — gave a new source or fact;
- `DUP` — only repeats of what was already seen;
- `GARBAGE` — irrelevant results;
- `CONTRA` — contradicts what was already found (the most valuable status);
- `STALE` — the source is alive, but the fact in it is outdated;
- `OFFSCOPE` — the source is about a neighboring object, another segment, another date or condition: a vote neither FOR nor AGAINST the target claim;
- `BLOCKED` — the source was not read (captcha, 403, empty page, headings only). This is not "checked" and not GARBAGE: change the access method, not the address on the same domain.

---

```markdown
# Research Log — <topic> — <date, UTC>

## Task and target point
What we're looking for: <one line>
Object: <exact name, plan, version, service run, rule>
User's segment: <where from, which account/document/region/platform>
Target date: <when it will be needed>
Hard constraints: <list>

## Decomposition
- [ ] Q1: <atomic sub-question>
- [ ] Q2: ...

## Goal functions and mechanisms
| Function | Candidate mechanisms | Checked |
|---|---|---|
| <what must happen> | <solution classes, not vendors> | yes / no |

## Axis plan
Formulations: <draft list>
Languages: <question's language, EN, owner's/place's language, ...>
Verticals: <...>
Backends: <...>
Owners and their layers: <base / exceptions / terms / publication channel — where each lives>

## Query matrix
| # | Query | Language | Backend | Status | New |
|---|--------|------|--------|--------|-------|
| 1 | library X 4.2 migration breaking changes | EN | websearch | NEW | 2 sources; hypothesis A |
| 2 | "X 4.2" deprecated option removed | EN | websearch | CONTRA | option removed in 4.2 |

## Claim duels (Law 0)
| Claim (with target point) | Origin | Binding (object / segment / date / condition) | FOR: best (class, layer, date) | AGAINST: best (class, date; what the counter-query gave) | Which is stronger | Verdict |
|---|---|---|---|---|---|---|
| service D is available to consumers in country M on 2026-12-10 | search | matches | owner: base (prices, 2026) + exceptions (status, 2026-11) | counter-query read: empty; cause query: empty | FOR | claim wins |
| service E is free with no time limit | memory + reviews | FOR: reviews about the trial period — `OFFSCOPE` by condition | undated reviews (witnesses of the past) | owner's billing documentation: "paid after 30 days" | AGAINST (binding terms) | refuted |
| service F runs on the target date | search | AGAINST about the neighboring product F-Lite — `OFFSCOPE` | owner: base (schedule), exceptions **not checked** | news about the closure of F-Lite (a different object) | — | draw: check the owner's exceptions layer |
| schedule of D from memory "9:00–21:00" | memory | matches | matches other models' answers, not the owner | owner's site: 10:00–20:00 | AGAINST (owner) | refuted — echo confabulation |

The source class and the owner's layer in the FOR column are mandatory (`owner: base / exceptions / terms / publication` / `news` / `witness of the past`): without them a stack of witnesses of the past looks like a majority.

## Near misses
| Candidate | Which constraint it violates | Mechanism of the violation | Can it be neutralized | Checked with the owner |
|---|---|---|---|---|
| <candidate> | <constraint> | <why it violates it> | <workaround or "no"> | yes / no |

## Saturation
- Main query (variations 1–5): closed — 3×DUP ✅
- Language EN: closed ✅ / open
- Owner's language: open — terminology loop needed
- Vertical: not started

## Sources
| URL | What was taken | Date | Owner's layer | Independent? |
|-----|----------|------|----------------|--------------|
| https://... | facts F1, F2 | 2025-11-30 | base | yes |

## Contradictions
- A (src1, 2024) vs B (src2, 2025) — reason: version; binding: both about X 4.x; resolved in favor of B (owner, fresher).

## Value conflicts
| Attribute | Value A (source, date, effective date) | Value B (source, date, effective date) | Who applies the rule | Official channel checked | What goes into the answer |
|---|---|---|---|---|---|
| <price, term, limit, threshold> | <...> | <...> | <body / billing> | yes / no / unavailable | <new as in force / stricter with explanation / both with dates> |

## Inventory of the draft (phase 6)
| Statement in the draft | Source in the log | Does the quote confirm this value, object and date? | Load-bearing? | Status |
|---|---|---|---|---|
| <fact, number, instruction, command, assumption about the user> | <URL / none> | yes / no | yes / no | confirmed / labeled / removed |

## Sub-question status
- Q1: confirmed by the owner on the right layer ✅
- Q2: 1 source, counter-search needed ⏳
- Q3: did not win the duel — in the answer as "not confirmed" ⚠️

## Conclusion / what remains
<result, or "not found" with proof of exhaustion: which axes and mechanisms are closed, % new>
```

---

## The "not found" rule

The phrase "no information" or "no option exists" is allowed in the report only in this form:

> Not found. Checked: N formulations (list), languages X/Y/Z to saturation, verticals A/B/C, solution mechanisms (list), death queries per claim (list), primary sources and their layers reviewed (list). The last M queries gave 0% new.

Without this text, "not found" counts as unfinished work, not a result.
