# The language matrix

## Why it matters

The internet is not homogeneous. It consists of weakly connected language segments:

- **EN** — the widest layer, but not all of it: unique content lives outside EN.
- **ZH** — the largest separate segment: reverse engineering, hardware, cheap mass tutorials, local ecosystems. Much of it is not indexed by Western search engines and is not translated.
- **RU** — strong local ecosystems: system administration, reverse engineering, local markets, regional realities.
- **JP / KO / DE / ES / FR / PT / AR** — niche superpowers: JP — games, anime, electronics; KO — web technologies and gamedev; DE — mechanical engineering; ES/PT — huge audiences and local markets.

A fact known in one segment may be missing from another. Switching language is not "translating the same thing" — it is **a different map of the terrain**.

## Starting axes

- Base (always): the question's language **+ EN**.
- **The owner's or the place's language** if the subject is local: a local operator, agency or media outlet publishes news about repairs, closures, reforms and new rules in the local language earlier and in more detail. The cause query and the death query must be run in this language too.
- Extension (complex/niche topics, anything not found in the base): **+ ZH + RU**.
- By domain:

| Domain | Additional languages |
|---|---|
| Games, anime, consoles, retro | JP, KO, ZH |
| Electronics, components, hardware | ZH, JP, DE |
| Mechanical engineering, cars, machine tools | DE, ZH |
| Mobile development, Android mods | ZH, KO |
| Mathematics, algorithms, olympiads | ZH, RU |
| Local markets and country realities | The country's language + neighbors |

## The terminology loop (a mandatory mechanic)

The first translation of a query is almost always non-terminological: it conveys the meaning but not the words domain natives use.

1. Translate the query (yourself; with an MT tool if available, but check it). Back-translate and compare the meaning.
2. Go through Laws 1–2 with the translated query.
3. From the titles and first paragraphs of the results, write down the **native terminology**: what the concept is called, which calques/abbreviations are used.
4. Re-query with the native terms.
5. Repeat 3–4 until saturation.

Example: `load balancer` literally → 负载均衡器, but docs and blogs more often write `LB` / `均衡`. A query with the native term gives completely different results.

## Segment specifics

### ZH
- Write in simplified Chinese (simplified most often; traditional — for Taiwan/Hong Kong topics).
- Key platforms: Zhihu (知乎), CSDN, SegmentFault, Baidu Zhidao, JianShu, Bilibili (video tutorials), V2EX.
- Terms are often calques or transliterations: Docker → Docker (not translated), cloud → 云, cache → 缓存.
- Some Western services are unavailable from mainland China — local content solves the same problems with its own means, hence unique solutions.

### RU
- Habr, Russian-language Stack Overflow, vc.ru, specialized forums (e.g. forum.ubuntu.ru), Telegram communities.
- Strengths: sysadmin, networking, reverse engineering, hardware, local services and realities.

### JP
- Qiita, Zenn, teratail, 5ch. Technical blogs are very dense in detail.

### KO
- OKKY, Namuwiki (encyclopedic, surprisingly deep on pop culture and games).

### DE / ES / FR / PT / AR
- Bring them in by domain from the table above, or when the base axes are saturated and the answer is incomplete.

## Segment rules

- One language = **the full matrix** (Law 1 + Law 2), not one trial query.
- A unique fact from a segment → must be checked in other segments and in EN (segment isolation breeds myths).
- Don't know the language — read the results via translation (in your head or with a tool): slower, but no worse a check.
