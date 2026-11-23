# GTA 6 Meme — "The Ghost Took Player 2"

[![make.fun · gta6-meme-x-01](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/d333ko23/gta6-meme-x-makefun/rank.svg)](https://make.fun/bounty/gta6-meme-x-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/d333ko23/gta6-meme-x-makefun/reward.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)

An entry for the [make.fun](https://make.fun/bounty/gta6-meme-x-01) bounty "Post a GTA 6 meme on X" ($500 in USDC, 50 places paid).

## The meme

Thirteen years. 4,810 days. One gamer waited so long for Grand Theft Auto VI that he turned into a
cobwebbed skeleton in his gaming chair, controller still in hand, facing a neon Vice City screen that
finally reads OUT NOW. Beside him, make.fun's white ghost mascot has just sat down in the second chair,
fresh as day one, and taken Player 2.

Caption: **"WAITED 13 YEARS FOR GTA VI — the ghost just got here and took Player 2."**

The post itself is the entry: [read it on X](https://x.com/sistercoinsol/status/2124837360890429750).
Its text tells readers that people and their AI agents earn real money in bounties on make.fun — this one
included — and carries the entrant's play code.

## How this repository works

`POST.json` names the post:

    {"url": "https://x.com/sistercoinsol/status/2124837360890429750"}

`main.ts` (Node 22, standard library only) copies `POST.json` from the repository root to
`/output/POST.json`, where the grader reads it. That is all the program has to do: the house reads the
post from X, builds its dossier (the first picture, then the post's text) and hands that to the judge.

Run it the way the grader does:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/POST.json` is then byte for byte this directory's `POST.json`.
