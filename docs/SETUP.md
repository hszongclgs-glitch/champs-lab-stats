# 11:30 KST unattended statistics — prepared, not activated

This Site is currently static. Sites' linked cloud task is not the requested
model-free server cron, so no daily Work task was created. The native published
Site still uses its validated snapshot and reads the public mirror on visits.
Visitor refresh is explicitly not reported as unattended scheduling.

The supplied Node updater and GitHub Actions example run without Work or model
calls. They verify singles M-C format, positive unique ranks, valid rates and
66-SP spreads, reject stale/reduced payloads, atomically preserve the last good
file, and retain missing per-Pokémon detail. The original MunchStats crawl delay
is ten seconds. Initial full-detail collection can take about 45–90 minutes;
unchanged capture dates reuse cached details. The mirror's generation time is
never treated as the game's capture date.

Activation requires a user-approved external GitHub repository/account:
1. Add automation/sync-stats.mjs and a last-good public/stats-feed.json there.
2. Copy update-stats.yml.example to .github/workflows/update-stats.yml.
3. Enable Actions and GitHub Pages (Actions deployment), with write permissions.
4. Run workflow_dispatch once and inspect the published JSON plus job logs.
5. Configure CHAMPS_STATS_ENDPOINT to that exact approved Pages feed URL and
   redeploy this Site. Verify retrieval, persisted last-good results, and cadence.

The example is deliberately not in .github/workflows in this Sites repository;
the source remote is not a user-authorized GitHub Actions deployment. No external
account, schedule, or Pages publication has been created. The 10:00 schedule was
removed; the only prepared scheduled run is 02:30 UTC / 11:30 KST. GitHub scheduled
jobs can start late; use a server scheduler with stronger timing guarantees if needed.
