# Source Registry — World & Culture Digests

*Master record of every source feeding the reflection-stream digests. The OPML file (`feeds/digest-feeds.opml`) is the machine master; this document is the human-readable map and the record of decisions. Changes to sources happen here first, at the monthly review.*

## How the pipeline works

1. This repo's OPML is the master list. Inoreader follows it via **OPML subscription** — edits to the file sync automatically to Inoreader.
2. Inoreader folders mirror digest sections. Each folder exposes an **output feed** (RSS URL) that the Saturday/Sunday Cowork scheduled tasks read.
3. Filters (noise reduction) and **monitoring feeds** (thread searches) live natively in Inoreader — they cannot be expressed in OPML. See `docs/setup-actions.md`.
4. Newsletter-based sources (e.g. Nature Briefing) are Inoreader-native email feeds and also live outside the OPML.

## Sections → folders

| Folder | Digest section | Feeds |
|---|---|---|
| 01 Hinterland | World Digest ① | Guardian UK news, Politics, Business, Education, Energy, Advertising; On London; Dave Hill; IQ Magazine; Arts Professional; Guardian EU; Politico Europe; Notes from Poland; Le Monde in English |
| 02 Understanding | World Digest ② | Guardian Long Read; Aeon; Psyche; Rest of World; The Dial; New Lines; The New Humanitarian; NYT Magazine |
| 03 State Changes | World Digest ③ | Verfassungsblog; International Crisis Group; Guardian World, Ukraine, MENA, Iran, China, US; NYT World |
| 04 New Frontiers | World Digest ⑥ | Quanta; Works in Progress; Guardian Science, Environment, Technology, AI, Psychology, Datablog; NYT Science |
| 05 Illuminating the Past | World Digest ⑦ | Public Domain Review; Aeon (dual); Smithsonian; History Today |
| 07 Culture (Sunday) | Culture Digest | Guardian Culture, Music, Film, Books; Time Out London |
| (Inoreader-native) 06 Threads | Thread ledger | Monitoring feeds — see setup actions |
| (Inoreader-native) Newsletters | New Frontiers | Nature Briefing (email feed); The Browser when subscribed |

## Changes enacted from the 31 Aug 2026 export

**Deduplicated:** Guardian Technology (3 copies → 1), Guardian World (2 → 1, International edition dropped), Guardian Business/Economy (2 → 1), Public Domain Review Mastodon mirror dropped.

**Replaced (wrong feed type):** International Crisis Group and Politico Europe were YouTube channel feeds — swapped for their website RSS.

**Swapped:** NYT HomePage → NYT World + NYT Science (homepage is noise-heavy; sections match this system's use of the NYT).

**Added:** IQ Magazine, Arts Professional, Le Monde in English, Smithsonian, History Today, NYT Science/World.

**Left out (recommend confirming):** Guardian Food & Drink industry, Guardian Health & Wellbeing — lifestyle-adjacent, no digest section claims them. Say the word to restore either.

## Access map (current)

| Tier | Sources | Status |
|---|---|---|
| Free core | Everything in the OPML except below | Live |
| Subscribed | NYT (full text via login; pipeline reads headlines) | Live |
| Pending decision | FT, LRB, The Browser, On London supporter, Ground News, Economist, Music Week, History Today full access | Review after tuning runs |

## Verification status

Feed URLs for additions follow each publisher's standard pattern but are unverified until first Inoreader sync — check the folder counts after subscribing and flag any feed showing errors. Known-fragile: Arts Professional, History Today (paywalled site; RSS may be partial).
