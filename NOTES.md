# SUPER RUN 21 (g_run21_hd)

Status: **runs (smoke-tested)** — Unity family; reaches its menu/tutorial/board headless; not yet played by hand. Scaffolded 2026-10-07. Facts: [notes/scaffold.md](notes/scaffold.md).

## Checklist
- [ ] Starts: `make run GAME=g_run21_hd` (player log on stdout)
- [ ] Graphics and text look right; window size
- [ ] Sound and music (FMOD → PulseAudio through libmega_unity.so)
- [ ] Settings it can't find: `make run GAME=g_run21_hd 2>&1 | grep "Couldn't pull"` — add them to scripts/launch.sh
- [ ] A full game plays through
- [ ] Launcher messaging (FIFO/TCP to the cabinet) failing doesn't break play

## Log
<!-- dated notes: what broke, what fixed it -->
- 2026-10-07 — smoke test: 20 s with screenshots (build/smoke/g_run21_hd); no crash. Launcher settings now follow the cabinet's own launcher.xml format (per-player keys are player.<n>.player.*, 1-based).
