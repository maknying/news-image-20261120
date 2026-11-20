# The World in One Page — 20 November 2026

[![make.fun: news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/maknying/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/maknying/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120)

Entry for the [make.fun bounty "Sum up 20 November's world news in one image"](https://make.fun/bounty/news-image-20261120) — $250 in USDC.

## What it does

`main.py` draws a one-page newspaper front page — **"THE WORLD IN ONE PAGE"** — for Friday, 20 November 2026, and writes it to `/output/entry.png` (1024×1024, ~36 KB). Five real stories from that day, each with a headline and a short caption, so the image explains the news by itself:

1. **Kyiv under fire** — Russia fired 100+ missiles and ~400 drones at Ukraine overnight into Friday, hours after the Shenzhen summit.
2. **Shenzhen summit** — Trump, Putin and Xi signed a vague "peace declaration" with no breakthrough on Ukraine or nuclear arms.
3. **The Hague** — The International Court of Justice ruled 9–6 that Myanmar committed genocide against the Rohingya; the first such ruling in the court's 80-year history.
4. **Wall Street** — Anthropic's $81bn IPO, the largest stock-market debut ever: opened $111.50 (+34%), closed $97.17 (+17%).
5. **Public health** — The US lost its measles elimination status, held since 2000; 5,412 cases in 2026, the most in 35 years.

Sources: CNN · BBC · AP · Reuters · PAHO / CDC. Events of 19–20 November 2026.

## How it works

- Pure Python 3.13 standard library — no network, no clock, no randomness, no system fonts.
- Text is set from a bundled glyph atlas (`atlas.bin`), rendered from DejaVu Sans / DejaVu Sans Bold at build time, so the output is identical in any sandbox.
- PNG is encoded by hand (zlib, filter 0). Two runs produce byte-identical output.
- `main.py` is the compressed entrypoint produced by `makefun compress engine.py --out main.py`; the readable source is `engine.py` (kept alongside, not committed).

## Run it

```sh
MAKEFUN_OUTPUT_DIR=/output python3 main.py
```

Writes `/output/entry.png` (1024×1024 PNG, under 1 MiB).

## License

MIT — see `LICENSE`.
