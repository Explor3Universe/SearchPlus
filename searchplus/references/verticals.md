# Vertical sources and snowballing

## Principle

Every domain has places where knowledge lives **locally**: issue trackers, documentation, forums, registries. General web search is a good start, but for expert topics a vertical is almost always more precise and deeper. Every vertical has an internal search — use it directly or via `site:`.

## Catalog by domain

### Programming and software
- Official documentation (a primary source — always the priority).
- **GitHub: issues, PRs, Discussions, SECURITY.md** — often the only place where bugs, regressions and workarounds live.
- Stack Overflow (English + Russian), MDN.
- Package registries: npm, PyPI, crates.io, Maven Central — changelogs and version metadata.
- HN (news.ycombinator.com), Reddit (r/programming, domain subs), Lobsters, dev.to.

### Security
- NVD, CVE.org, vendor advisories, GitHub Security Advisories, exploit-db, CISA KEV.
- Reports and write-ups: PortSwigger blog, Project Zero, closed mailing lists.

### Science and research
- arXiv, PubMed, Semantic Scholar, Google Scholar, dblp.
- Conference sites, supplementary materials, dissertation databases.

### Hardware and electronics
- Datasheet aggregators (alldatasheet, datasheetspdf), vendor application notes.
- EEVblog forum, r/AskElectronics, r/PrintedCircuitBoard.

### Chinese segment
- Zhihu, CSDN, SegmentFault, V2EX, 36kr (business/tech), Bilibili (tutorials), Baidu Zhidao.

### Russian segment
- Habr, vc.ru, Russian-language Stack Overflow, specialized forums, mailing lists.

### Japanese segment
- Qiita, Zenn, teratail, 5ch.

### Products, companies, markets
- Vendor docs, press releases, reports (get around paywalls by searching for document titles in open mirrors — legal and usually works).
- LinkedIn, company registries, court and regulatory databases, job postings (for dates and facts about companies).

### News and current events
- News aggregators with a date filter, the parties' official channels.
- Mandatory: at least two independent newsrooms per key fact.

## Snowballing (citation chaining)

As soon as you have found one strong document, it is not a result but **an entry into a network of links**:

1. **Forward:** bibliography, references, "see also", related links inside the document.
2. **Backward:** who links to this document — search `"<title or URL>"` + `reddit|HN|forum|评`.
3. **Discussions:** the material you found has almost always been discussed by someone — discussions contain criticism, refutations and practical experience that are not in the material itself.
4. **Author:** other materials on the topic by the same author/organization.

## Backends as an axis of variation

Different search tools — websearch, MCP search engines, a direct fetch to a search engine, verticals' internal searches — give **different results** for the same query.

- Run the key queries of a topic through at least **two different** backends.
- Switching the backend is a legitimate way to "open the next page" where there is no pagination.
