# Stage 3 source verification — 2026-10-13

- Public singles API: https://eurekaffeine.github.io/pokemon-champions-scraper/singles/battle_meta.json
- Source repository: https://github.com/eurekaffeine/pokemon-champions-scraper
- Original game-data pages: https://munchstats.com/champions/singles/

The singles scraper reads MunchStats' Champions in-game Battle Data for M-C.
The repository's root/doubles Showdown feed is intentionally excluded. The checked
singles response contains 257 ordinal ranks and numerical-ID move, item and
ability rates. Its Pokemon usage_rate=0 is a compatibility placeholder, not a
measured percentage. No Pokemon percentage or invented rank is shown.

All 257 records map to existing app species. Escaped apostrophes are decoded for
name matching; Vivillon-Fancy maps to Vivillon's cosmetic-form aggregate, in line
with the source's documented aggregation. Mega forms share base/regional-form
ranks; separate Mega ranks are not inferred. Other eligible app species remain
unreported. No Pokemon ID, saved team value or calculation formula was changed.

The checked mirror was generated 2026-10-13T09:45:53.422121Z, with season data_date
2026-10. Those values are not the game's capture date. The original Garchomp
page reports October 06, 2026 at 12:07 UTC. Its actual nature percentages and
SP spreads were parsed separately; the initial deployed enrichment covers only
Garchomp. Other existing nature/SP data remain a separately attributed legacy
snapshot, not a fabricated extension of the API. Missing fields stay unavailable.

The checked upstream workflow runs daily at 02:00 UTC. The README's older
Monday-only table is inconsistent with that workflow. Actual new game capture
availability is controlled upstream; daily mirror runs do not prove daily new
game data. The updater compares generation/capture dates and retains prior data.

The repository documents public API consumption and an MIT-licensed scraper.
This does not establish ownership of underlying game content or grant additional
rights beyond the public feed. The original crawler uses a ten-second delay,
which the prepared detail updater preserves. No authenticated endpoint is used.

Display-only Korean corrections were verified separately:
- Aura Guard → 파동의방호: https://pokemonkorea.co.kr/pokedex/view/573
- Eelevate → 천정부지: https://pokemonkorea.co.kr/pokedex/view/770
- Fire Mane → 불꽃의갈기: https://pokemonkorea.co.kr/pokedex/view/850
- Roseli Berry → 로셀열매; Leek → 대파 (retained Korean naming references).

Scheduling is NOT activated. The external example is 02:30 UTC / 11:30 KST,
without a Work/model invocation. Approval and a user-owned GitHub Actions/Pages
repository are required before its creation and Site endpoint configuration.
