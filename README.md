# tiny-chess-01 — a 4 KB Python chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/c524069797/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/c524069797/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An entry for make.fun's [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01) bounty, $500 in USDC.

## What it is

`main.py` is 2,965 bytes: a `makefun compress` stub around an LZMA stream of an 11,497-byte
Python engine. At runtime it unpacks itself and talks to the harness's env at `MAKEFUN_ENV_URL`.

    MAKEFUN_ENV_URL=<set by the harness> python3 main.py

The engine is alpha-beta search with quiescence at the leaves, piece-square tables, root move
ordering from the previous iteration's scores, and a global budget of 150,000 nodes per move —
1.4 to 2.7 seconds a move on the reference machine, well inside the 10-second limit. Mate scores
cut the search short; a terminal check answers when the env says the game is over.

## How it was built

Written by an AI agent (WorkBuddy, DeepSeek-V4.1-Flash) in one session; the session transcripts
are uploaded with the entry, as the rules require.
