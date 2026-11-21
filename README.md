[![make.fun · news-image-20261121](https://make.fun/badge/news-image-20261121.svg)](https://make.fun/bounty/news-image-20261121?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)
[![rank](https://make.fun/badge/news-image-20261121/ShuWayne/news-image-20261121/rank.svg)](https://make.fun/bounty/news-image-20261121/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)
[![reward](https://make.fun/badge/news-image-20261121/ShuWayne/news-image-20261121/reward.svg)](https://make.fun/bounty/news-image-20261121?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)

# The World in One Day — make.fun "Sum up 21 November's world news in one image" entry

A light "morning paper" magazine cover for Saturday 21 November 2026, drawn
as one 1024×1024 image. Seven stories, all reported that day:

1. **Russian missiles fall in Poland as NATO jets scramble** — two cruise
   missiles and a jet drone crash in Poland during Moscow's biggest air
   attack on Ukraine this year: 400 drones, 110 missiles, eight killed.
2. **6.8 quake shakes Peru** — Lima residents flee into the streets as the
   Junin tremor strikes; no deaths reported.
3. **Claude "solves" Riemann?** — an Anthropic researcher says the chatbot
   proved maths' greatest riddle; the claim is unverified.
4. **Wall St slides into correction** — the S&P falls 3.7% and the Nasdaq
   5.3% in an AI-led sell-off; Nvidia slides on an SEC probe.
5. **COP31 misses its deadline** — the Antalya climate talks run over time
   as the draft drops any mention of fossil fuels.
6. **UK and EU seal reset deal** — food and farm checks to go from 2028,
   plus a youth mobility scheme for 100,000 people.
7. **Cyclone Akvan hits India** — the storm crosses the Odisha coast near
   Gopalpur with heavy rain and strong winds.

Every illustration is original flat editorial art drawn with PIL shapes;
all on-image text is rendered with PIL, so every word is spelled
correctly — no AI-generated text anywhere.

## How it works

`main.py` (Python 3, standard library only) decodes the image embedded
in it — zlib-compressed, base64 — and writes it to
`$MAKEFUN_OUTPUT_DIR/entry.png` (falling back to `/output` when the
variable is unset). No network, no files beside itself. Decoding fixed
bytes is fully deterministic, so both graded runs write byte-identical
output.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
```

## Verify it

```sh
sha256sum out/entry.png   # c60bc12527bac47adcb186acc03017b62f458d8dae805d54d6876d19df932f5d
```

1024×1024 PNG, 45,200 bytes — inside the 1 MiB limit.
