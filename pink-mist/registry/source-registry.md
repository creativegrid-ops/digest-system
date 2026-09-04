# Pink Mist — Source Registry

Lane assignments are **verified empirically on first runs**, never assumed (World Digest build finding: the Cowork sandbox egress proxy blocks major commercial publishers; feed URLs rot and lie). Status values: `untested` · `lane1-ok` · `lane2-only` · `lane3` · `dead`.

## Digest 3 — Agents & Pitching (PM3)

| Source | Intended lane | Status | Notes |
|---|---|---|---|
| usedigest.com "Ross's Digest" (Reddit: r/Emo, r/midwestemo, r/Hardcore, r/Screamo, r/postrock, r/mathrock) | 1 (daily email → label:feeds) | **trial live 4 Sep 2026** (~$6/mo) | First issue yielded 3 real signals (BRUIT≤/Cult of Luna UK routing, Engine Down reactivation, Caspian date tease). Recurrence computed across the week's dailies; dedupe multi-builds/day. Keep/cancel at monthly review |
| usedigest.com "Boutique Agency Digest" (IG: Toutpartout, Swamp, Atonal, Odyssey, Upsurge + others) | 1 (daily email → label:feeds) | **trial live 4 Sep 2026** | Interim signal, never system of record (server-side scraping under the hood — fragility risk, not safety risk). Captions truncate ~50 chars → pointers only. Windowing = only new-since-last-build posts (suspected, confirming). Official Make business-discovery build remains the reliable replacement |
| ~~Direct Reddit RSS (`feeds/reddit.opml`)~~ | — | **retired** — 403 all six on www AND old.reddit (runs 1–2); generic web search also failed twice pre-build | OPML kept in repo for reference only |
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

## Scene newsletters (lane 3, label:scene — subscribed free tier 3 Sep 2026)

| Newsletter | Author | Status | Notes |
|---|---|---|---|
| IDIOTEQ (idioteq.substack.com) | Karol Kaminski | subscribed, accumulating | Best genre fit: screamo/skramz, post-hardcore, blackgaze, math rock, post-rock at demo/first-EP stage. Weekly + monthly round-ups |
| Liner Notes (chorus.substack.com) | Jason Tate | subscribed, accumulating | Weekly emo/pop-punk/alt scene curation. Supporter tier $3/mo if it earns it |
| Bandcamp Notes (bandcamp.substack.com) | Bandcamp Daily | subscribed, accumulating | Broad discovery, 1–2×/week |
| Washed Up Emo (washedupemo.substack.com) | Tom Mullen | subscribed, accumulating | Authoritative but archival lean — watch yield |
| Unhappy Place (andrewsacher.substack.com) | Andrew Sacher (ex-BrooklynVegan) | subscribed, accumulating | Emo/post-hardcore; Emo Revival book Sep 2026 |
| Everything Is Noise | — | **parked** | Perfect genre fit but email signup disabled ("in maintenance") — recheck quarterly, promote if it reopens |

## Industry/signings stack (lane 3, label:trade + page-watches — from newsletter research 3 Sep 2026)

| Source | Status | Notes |
|---|---|---|
| ROSTR Signings Tracker (hq.rostr.cc) | Ross signing up | Free account + Insider email alerts → trade label. Caveat: 75–80% agency self-reporting — high recall, not gospel. First-login check: search recent Atonal/Runway signings to test sub-500-cap coverage |
| CelebrityAccess VitalSigns | recommended, not yet subscribed | Weekly "Agency Signings" email, free |
| CMU Daily | recommended, not yet subscribed | Free weekday UK deals round-up ("One Liners") |
| Record of the Day | trial candidate | Paid after 2-week trial; carried ATC/ROAM releases verbatim |
| primarytalent.com/new-signings/ + runwayartists.com/new-signings/ | page-watch (prompt v1.5, Step 4) | Dated structured pages — replaces roster diffs for these two |
| Boutique EU agency IG/FB (Toutpartout, Swamp, Atonal, Odyssey) | staged → Digest 1 Make lane | Signings announced ONLY on social, parseable boilerplate ("NEW ROSTER ADDITION!", "welcome to the roster") — add agency handles to business-discovery watch list |

## Change log
- 2 Sep 2026 — registry created; all web sources untested pending first on-demand runs. Trade newsletters confirmed by Ross: IQ Index + Bob Lefsetz long-subscribed (populated), Music Week added today — all auto-labelled `trade`.

- 2 Sep 2026 — agency list confirmed, three tiers (majors scene-filtered / independents / growth); One Fiinix dropped.
- 2 Sep 2026 — run 1 debrief: Reddit www dead (403×6); Gmail label query quirk (sender-search fallback codified); Earth JS-rendered partial; ATC Live → ROAM (merger verified via IQ/Music Week/Billboard, Sep 2025); pitch-integrity rules added to prompt v1.3 after fabricated internal history (CASEY) caught in review.
- 2 Sep 2026 — Solo roster URL confirmed by Ross: soloagency.com (snapshot + prompt updated).
- 2 Sep 2026 — run 2 debrief: CASEY correction — claims were TRUE pre-Airtable history (Ross confirmed), not fabrication; integrity rule recalibrated to verify-or-label (prompt v1.4). old.reddit also 403 → lane 1 dead. UTA roster JS-rendered/empty (press-first applies). Duplicate-window addendum behaviour codified. Schedule live: first scheduled issue Fri 4 Sep.
- 2 Sep 2026 — Reddit lane fix staged (in Digest 1 build task): official Reddit API via Make → Airtable staging; Digest 3 lane 1 to read staging once live. redditapis.com evaluated and rejected (unofficial, rule #2). browser-use.com parked as Phase-2 candidate for JS-rendered roster pages — revisit at 4-week review.
- 3 Sep 2026 — prompt v1.5: Digest Library archive write added (shared cross-stream Notion archive `collection://e54a3f19-b99a-4fe0-8b28-b771bd5bf98c`); permitted writes now four. Digest 1/2 build tasks updated to include Library write from birth.
- 3 Sep 2026 — newsletter research adopted: 5 scene Substacks subscribed (label:scene), industry stack defined (ROSTR pending sign-in), page-watches added, prompt v1.5 (two-label lane 3, per-newsletter yield line). Corrections: Odyssey = Antwerp not UK; Upsurge disambiguation required.
- 3 Sep 2026 — agent-signings use case shipped with current stack; revisit later (likely path = better website viewing; browser-use remains the parked candidate). ROSTR Pro not purchased (no email/API/export on any tier). ROSTR RSS feed-index = curated Insider editorial archive, insufficient (occasionally scene-relevant, e.g. Static Dress x Gold Theory — cheap-fetch candidate at revisit). CelebrityAccess rejected (too US/mainstream). Data licensing not pursued. Prompt v1.6 consolidates Digest Library write (sibling-project commit) + newsletter lanes. NOTE: repo write convention agreed — pink-mist/ commits from the Pink Mist project only.
- 4 Sep 2026 — prompt v1.7: feeds lane live (usedigest trial), per-band links line (Bandcamp · IG · booking), buzz board widened to all-lane sourcing, candidate target 8–12. Ross verdict on week 1: both surfaced bands bang on — principle working, upweighting coverage.
