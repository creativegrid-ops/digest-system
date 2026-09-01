# Pink Mist — Source Registry

Lane assignments are **verified empirically on first runs**, never assumed (World Digest build finding: the Cowork sandbox egress proxy blocks major commercial publishers; feed URLs rot and lie). Status values: `untested` · `lane1-ok` · `lane2-only` · `lane3` · `dead`.

## Digest 3 — Agents & Pitching (PM3)

| Source | Intended lane | Status | Notes |
|---|---|---|---|
| r/Emo, r/Mathrock, r/postrock, r/screamo, r/Hardcore, r/indieheads | 1 (RSS via `feeds/reddit.opml`) | **dead (www)** — 403 all six, run 1 (2 Sep) | Next: old.reddit.com variant, then named lane-2 queries. General web search for Reddit threads failed twice pre-build — do not regress to generic queries. |
| DIY | 2 | untested | Query rule: named source + subject + date anchor |
| Kerrang! | 2 | untested | Commercial masthead — expect proxy block on direct fetch |
| Distorted Sound | 2 | **lane2-ok** (run 1, both buzz items) | |
| The Quietus | 2 | untested | |
| Stereogum | 2 | untested | US crossover only |
| IQ Magazine | **3** (IQ Index newsletter, Gmail `label:trade`) | **lane3-ok** (7 issues in window, run 1) | Site feed known-broken (redirects to shop) — never rely on it |
| Music Week | **3** (bulletins, Gmail `label:trade`) | pending accumulation (subscribed 2 Sep) | Partial paywall on site |
| Majors rosters (scene-relevant only): The Team (formerly Wasserman) · UTA · ROAM (formerly ATC Live, merged w/ Arrival Sep 2025) · Primary Talent · Earth · Solo · Runway Artists | press-first + 1 roster/week rotation | partial (run 1: Primary too large to crawl in budget; Solo domain now confirmed: soloagency.com) | Signings via lane 3 + named lane-2 searches |
| Independents (diff in full): Atonal (atonal.agency) · Just Another (just-another.co) · Northern Music Company (northernmusicgroup.co.uk) | 2 | partial (run 1: Atonal JS-rendered; Just Another DNS/robots error; Northern site = placeholder) | Warm paths exist in Airtable (e.g. haydn@northernmusic.co.uk) — relationship intel doesn't depend on their websites |
| Growth tier (diff in full): Odyssey Booking (odysseybooking.com) · Toutpartout (toutpartout.be) · Upsurge Artists (upsurgeartists.com) | 2 | partial (run 1: Odyssey robots-blocked → press-based; others ok) | Relationship-maintenance rotation weighted here |
| Festivals: ArcTangent · 2000trees · Portals · Outbreak | 2 | untested | Lineup announcements |
| Viberate MCP | connector | validated 21 Aug 2026 | Free tier; ~20 lookups/run cap; `graph_mode: 'total'` only; audience top-5 cities only |
| Airtable / Notion / Gmail | connectors | validated (chat client) | **Cowork scheduled-task environment: unconfirmed — blocking check** |

## Change log
- 2 Sep 2026 — registry created; all web sources untested pending first on-demand runs. Trade newsletters confirmed by Ross: IQ Index + Bob Lefsetz long-subscribed (populated), Music Week added today — all auto-labelled `trade`.

- 2 Sep 2026 — agency list confirmed, three tiers (majors scene-filtered / independents / growth); One Fiinix dropped.
- 2 Sep 2026 — run 1 debrief: Reddit www dead (403×6); Gmail label query quirk (sender-search fallback codified); Earth JS-rendered partial; ATC Live → ROAM (merger verified via IQ/Music Week/Billboard, Sep 2025); pitch-integrity rules added to prompt v1.3 after fabricated internal history (CASEY) caught in review.
- 2 Sep 2026 — Solo roster URL confirmed by Ross: soloagency.com (snapshot + prompt updated).
