# CHAMPS LAB — Stats Automation Setup

This repository is a **staging area** for the proposed 11:30 KST statistics updater.

## Status: NOT ACTIVATED

The updater is stored in `automation/sync-stats.mjs`. The workflow under `automation/update-stats.yml.example` is **an example only** and does not run from that location. No automatic crawling, scheduled GitHub Actions, GitHub Pages publication, or CHAMPS LAB Site connection has been enabled.

Before activating: 

1. Verify the public API and MunchStats allow the intended automated collection and public redistribution. A scraper's MIT license does not itself grant rights to source data.
2. Review the collector's per-Pokémon crawling load, parser accuracy, possible long first run, and cache/last-good behavior.
3. Obtain a valid last-good `public/stats-feed.json` and test locally without publishing.
4. Only then place the workflow in `.github/workflows/update-stats.yml`, configure GitHub Actions/Pages permissions, and run a manual test.
5. The CHAMPS LAB site must separately point to the published endpoint and be redeployed.

See `docs/SETUP.md` and `docs/SOURCE-VERIFICATION.md` for the original Work-generated guidance.
