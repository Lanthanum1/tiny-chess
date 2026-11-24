# tiny-chess-01: a 4 KB Python chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Lanthanum1/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Lanthanum1/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 0x88-board negamax engine: alpha-beta with quiescence (captures,
promotions, check evasions), transposition table, killer moves, MVV-LVA
ordering, check extensions, null-move pruning and late-move reductions,
incremental evaluation (material + piece-square tables + bishop pair +
king middlegame/endgame interpolation). Searches to a fixed node budget
per move — no clock, no unseeded randomness, so a trial replays
identically.

`main.py` is the whole engine (4,025 bytes, Python 3.13 standard
library only). It was packed with the kit's own command (`node
cli/makefun.mjs compress src_min.py --out main.py`) from the readable
source `src.py` (sent with the entry's transcript bundle, not committed
here). The packed engine replays identically to the readable source
(verified: same perft, eval, hash and trial-0 Elo 1279).

Practice Elo (mean over trials 0-2): **1185** — above the 1154 floor,
below the ~1365 house baseline.

---

<sub>Entered on [make.fun](https://make.fun/?ref=3w2f5hhg&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
