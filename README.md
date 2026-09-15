# RevealLine archive 11

This repository preserves the original **v0.51.0** game at
`https://mekhovov.github.io/revealline-archive-11/releases/v0.51.0/site/game/`.
The frozen source is `5d4bd98718955fa471fe71d798715864af166d18`; `source-lock.json`
pins its original tag object, ZIP, manifest, release record and checksum.

The workflow downloads the original GitHub Release ZIP. It uses the existing
bounded extractor pinned to source commit `2b8521b0a118df8663f93de5500e14da11741407`,
verifies the whole ZIP and every member's CRC, size and SHA256, and preserves the
original worker and assets. No game source is rebuilt, no release/tag is moved,
and no previously allocated archive changes.

`expected-inventory.json` contains every canonical body, including hidden build
metadata, original manifest/checksum and release record. Two independent reads
must match all 620 files / 323,017,169 bytes before Pages upload. The artifact
stays below the existing 800,000,000-byte archive budget. The downloadable ZIP
remains on the original GitHub Release.

A successful workflow establishes extraction, artifact integrity and deployment;
public full-body verification and actual browser/offline acceptance are recorded
separately before the main publishing controller admits this route. This repository
does not select the main site's current game.

Focused local checks require Python 3.11 or newer:

```sh
python3 -m unittest discover -s tools -p 'test_*.py' -v
```
