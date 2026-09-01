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
| Agency rosters: ATC Live · Primary Talent · Solo · One Fiinix Live · Runway Artists | 2 (direct page fetch, diffed vs Notion snapshot) | untested | List pending final confirmation by Ross. Blocked pages → press-based check |
| Festivals: ArcTangent · 2000trees · Portals · Outbreak | 2 | untested | Lineup announcements |
| Viberate MCP | connector | validated 21 Aug 2026 | Free tier; ~20 lookups/run cap; `graph_mode: 'total'` only; audience top-5 cities only |
| Airtable / Notion / Gmail | connectors | validated (chat client) | **Cowork scheduled-task environment: unconfirmed — blocking check** |

## Change log
- 2 Sep 2026 — registry created; all web sources untested pending first on-demand runs. Trade newsletter subscriptions (IQ Index, Music Week → `label:trade`) initiated by Ross for accumulation.
