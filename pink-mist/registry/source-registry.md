# Pink Mist — Source Registry

Lane assignments are **verified empirically on first runs**, never assumed (World Digest build finding: the Cowork sandbox egress proxy blocks major commercial publishers; feed URLs rot and lie). Status values: `untested` · `lane1-ok` · `lane2-only` · `lane3` · `dead`.

## Digest 3 — Agents & Pitching (PM3)

| Source | Intended lane | Status | Notes |
|---|---|---|---|
| r/Emo, r/Mathrock, r/postrock, r/screamo, r/Hardcore, r/indieheads | 1 (RSS via `feeds/reddit.opml`) | untested | Reddit 429s automated fetchers aggressively; lane 2 fallback in prompt. General web search for Reddit threads failed twice in testing — do not regress to it. |
| DIY | 2 | untested | Query rule: named source + subject + date anchor |
| Kerrang! | 2 | untested | Commercial masthead — expect proxy block on direct fetch |
| Distorted Sound | 2 | untested | |
| The Quietus | 2 | untested | |
| Stereogum | 2 | untested | US crossover only |
| IQ Magazine | **3** (IQ Index newsletter, Gmail `label:trade`) | untested | Site feed known-broken (redirects to shop) — never rely on it |
| Music Week | **3** (bulletins, Gmail `label:trade`) | untested | Partial paywall on site |
| Majors rosters (scene-relevant only): The Team (formerly Wasserman) · UTA · ATC Live · Primary Talent · Earth · Solo · Runway Artists | 2 (page fetch, diffed vs snapshot) | untested | Confirmed 2 Sep 2026. Large rosters — diff filtered to Pink Mist's world. Blocked pages → press-based check |
| Independents (diff in full): Atonal (atonal.agency) · Just Another (just-another.co) · Northern Music Company (northernmusicgroup.co.uk) | 2 | untested | Regular collaborators |
| Growth tier (diff in full): Odyssey Booking (odysseybooking.com) · Toutpartout (toutpartout.be) · Upsurge Artists (upsurgeartists.com) | 2 | untested | Relationship-maintenance rotation weighted here |
| Festivals: ArcTangent · 2000trees · Portals · Outbreak | 2 | untested | Lineup announcements |
| Viberate MCP | connector | validated 21 Aug 2026 | Free tier; ~20 lookups/run cap; `graph_mode: 'total'` only; audience top-5 cities only |
| Airtable / Notion / Gmail | connectors | validated (chat client) | **Cowork scheduled-task environment: unconfirmed — blocking check** |

## Change log
- 2 Sep 2026 — registry created; all web sources untested pending first on-demand runs. Trade newsletters confirmed by Ross: IQ Index + Bob Lefsetz long-subscribed (populated), Music Week added today — all auto-labelled `trade`.

- 2 Sep 2026 — agency list confirmed, three tiers (majors scene-filtered / independents / growth); One Fiinix dropped.
