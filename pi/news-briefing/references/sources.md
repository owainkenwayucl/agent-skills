# Sources and search queries by section

Use these first. Prefer primary/official sources, then reputable specialist
outlets. Fetch the page to confirm dates and details.

## Steam Deck UK stock (on request only — not in the default briefing)

- Run `scripts/steamdeck_uk.sh` (Valve inventory API, `country_code=GB`).
- Store page: <https://store.steampowered.com/steamdeck>
- Known retail package IDs (new hardware):
  - 512GB OLED — `1202542`
  - 1TB OLED — `1202547`
  - 64GB LCD — `903905`
  - 256GB LCD — `903906`
  - 512GB LCD — `903907`
- Refurbished units are a separate program; only mention if the user asks.

## Video games — new on Steam

- New releases search (GB/English) — **primary**, parse titles and release dates
  from the `search_result_row` blocks:
  <https://store.steampowered.com/search/?sort_by=Released_DESC&category1=998&supportedlang=english&cc=GB&l=english>
- SteamDB upcoming (best for the next 7 days, filters out most shovelware):
  <https://steamdb.info/upcoming/>
- Store search API for a specific title (gives app ID / price):
  <https://store.steampowered.com/api/storesearch/?term=TERM&cc=GB&l=en>
- Steam "New & Trending": <https://store.steampowered.com/explore/new/>
- NOTE: do **not** rely on `https://store.steampowered.com/feeds/newreleases.xml`;
  it was observed stale (last real item ~3 months old) in Sep 2026.
- Suggested queries: `new Steam releases this week`, `Steam release <date>`,
  `upcoming PC game release date <month>`.
- Prefer notable/popular titles; skip shovelware.

## Warhammer 40k (books, videogames, tabletop)

- Warhammer Community (official): <https://www.warhammer-community.com/>
- Black Library (books): <https://www.blacklibrary.com/>
- Goonhammer (tabletop/competitive): <https://www.goonhammer.com/>
- Bell of Lost Souls: <https://www.belloflostsouls.net/>
- Wargamer 40k: <https://www.wargamer.com/warhammer-40000>
- Steam news for 40k titles (Space Marine 2, Darktide, Rogue Trader, Mechanicus):
  check each game's Steam news hub.
- Suggested queries: `Warhammer 40k news`, `Warhammer 40000 new release`,
  `Black Library new book <month>`, `Warhammer 40k balance dataslate`.

## BattleTech (books, videogames, tabletop)

- Catalyst Game Labs (official tabletop): <https://www.catalystgamelabs.com/>
- Sarna.net (wiki/news): <https://www.sarna.net/>
- BattleTech / MechWarrior news on Steam:
  MechWarrior 5: Mercenaries, MechWarrior 5: Clans, BattleTech (HBS).
- Suggested queries: `BattleTech news`, `MechWarrior 5 Clans update`,
  `Catalyst Game Labs BattleTech <month>`, `BattleTech novel release`.
- Note: "BattleTech" (tabletop/IP) frequently gets confused with "BattleTech"
  the HBS game and "MechWarrior". Keep them distinct.

## AI & HPC

- HPCwire: <https://www.hpcwire.com/>
- InsideHPC: <https://insidehpc.com/>
- The Register — HPC: <https://www.theregister.com/HPC/>
- TOP500: <https://www.top500.org/>
- NVIDIA newsroom: <https://nvidianews.nvidia.com/>
- Lab blogs: OpenAI, Anthropic, Google DeepMind, Meta AI, Hugging Face.
- arXiv (cs.AI / cs.LG new submissions): <https://arxiv.org/list/cs.AI/recent>
- Suggested queries: `AI news`, `HPC news`, `supercomputer <name>`,
  `GPU datacenter announcement`, `AI benchmark release`, `arXiv AI <topic>`.
- Focus on capability, product, funding, benchmarks, hardware/supercomputing.

## Pro wrestling (WWE, AAA, JCW)

- WWE official: <https://www.wwe.com/news/>
- PWInsider: <https://www.pwinsider.com/>
- Fightful: <https://www.fightful.com/>
- WrestleZone: <https://www.wrestlezone.com/>
- Cageside Seats: <https://www.cagesideseats.com/>
- AAA (Lucha Libre AAA Worldwide): <https://www.luchalibreaaa.com/> and
  <https://www.cagesideseats.com/lucha-libre-aaa>
- JCW = Juggalo Championship Wrestling (confirmed by the user). If you see
  Jersey Championship Wrestling in results, ignore it.
- Suggested queries: `WWE news`, `WWE <event> results`, `AAA Lucha Libre news`,
  `JCW wrestling news`.
- Mark show results as spoilers if the event is very recent.
