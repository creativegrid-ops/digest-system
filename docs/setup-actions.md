# Setup Actions — Inoreader Wiring

*One sitting, ~20 minutes. Do in order. Everything here is the manual residue that can't live in the OPML.*

## Step 1 — Clean the slate

Your existing subscriptions will be superseded by the OPML subscription. To avoid duplicates:
- In Inoreader, select all current subscriptions and unsubscribe (Preferences → Folders & feeds makes bulk selection easiest), **except** Nature Briefing (it's an email feed — keep it; the OPML can't recreate it).
- Don't worry about losing anything: the master list now contains everything worth keeping, deduplicated and corrected.

## Step 2 — Subscribe to the master OPML

- Add subscription → **OPML subscription** → paste:
  `https://raw.githubusercontent.com/creativegrid-ops/digest-system/main/feeds/digest-feeds.opml`
- Inoreader will create the six folders and subscribe to every feed.
- **Check:** folder counts should be 01×14, 02×8, 03×9, 04×9, 05×4, 07×5. Aeon appears in both 02 and 05 — if Inoreader has instead created one Aeon subscription in a single folder, drag it so it sits in both.
- Flag any feed showing an error state to Claude (expected fragile: Arts Professional, History Today).

## Step 3 — File Nature Briefing

Drag the Nature Briefing email feed into **04 New Frontiers**.

## Step 4 — Create the thread monitoring feeds

Create folder **06 Threads**, then for each search below: run it in Inoreader search → save as **monitoring feed** → file in 06 Threads.

1. `"CMA" OR "Competition and Markets Authority" AND (music OR ticketing OR "Live Nation")` — name: *T1 CMA live music*
2. `Burnham AND (policy OR budget OR NHS OR housing OR devolution OR delivery)` — name: *T2 Burnham delivery*
3. `AI AND (jobs OR employment OR labour OR workforce)` — name: *T3a AI jobs*
4. `AI AND (energy OR "data centre" OR datacenter OR emissions OR water)` — name: *T3b AI environment*
5. `AI AND (music OR film OR art OR creative OR culture)` — name: *T3c AI culture*

(Adjust syntax to what Inoreader's query builder accepts — its AI search assistant can help convert these.)

## Step 5 — Filters (noise reduction, Pro allows 50)

Create these as content filters on the named feeds — hide matching articles:

| Feed(s) | Hide when title contains |
|---|---|
| Guardian UK news, Politics, World | `live updates`, `liveblog`, `as it happened`, `– live`, `latest updates` |
| Guardian UK news, Culture | `celebrity`, `royal family` (unless you want royals — your call) |
| Guardian Politics | `PMQs sketch`, `Westminster diary` |
| NYT World | `Trump` in combination with `reacts`, `mocks`, `slams`, `lashes` (horse-race noise; genuine state-change stories will use policy language) |
| Guardian Music, Film, Books | `review roundup` — keep individual reviews |
| All 03 State Changes feeds | `in pictures`, `photo essay` (visual galleries don't pipeline) |

Start with these; prune or extend at the monthly review based on what leaks through.

## Step 6 — Switch on output feeds

For each folder 01–07: folder settings (right-click or the ⋯ menu) → **create/enable RSS output feed** → copy the URL.

Send Claude the seven URLs (01, 02, 03, 04, 05, 06, 07). These become the pipeline endpoints in the scheduled-task prompts.

## Step 7 — Confirm

Reply to Claude with: the seven output URLs, any feed errors from Step 2, and any query-syntax adjustments made in Step 4. Tuning run 2 fires off the real pipeline immediately after.
