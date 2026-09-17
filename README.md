# RevealLine archive 11

This prepared append preserves original **v0.51.0** and **v0.60.1** games. The existing v0.51.0 route is
`https://mekhovov.github.io/revealline-archive-11/releases/v0.51.0/site/game/`.
The frozen source is `5d4bd98718955fa471fe71d798715864af166d18`; `source-lock.json`
pins its original tag object, ZIP, manifest, release record and checksum.

The workflow downloads the two original GitHub Release ZIPs. It uses the existing
bounded extractor pinned to source commit `2b8521b0a118df8663f93de5500e14da11741407`,
verifies the whole ZIP and every member's CRC, size and SHA256, and preserves the
original worker and assets. No game source is rebuilt, no release/tag is moved,
and no previously allocated archive changes.

`expected-inventory.json` contains every canonical body, including hidden build
metadata, original manifest/checksum and release record. Two independent reads
must match all 1,305 files / 636,098,834 bytes before Pages upload. The artifact
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

## Prepared v0.60.1 append — review pending

The v2 multi-release preparation/verifier comes from the accepted Archive16 contract. Archive11 keeps its 800,000,000-byte cap, the original pinned extractor and tooling commit, and every original v0.51.0 canonical row. `legacy/` preserves the exact v1 lock/inventory; the original Git predecessor preserves its implementation history. No historical game rebuild is used. The single original ZIP receipt becomes one receipt per edition, and the established 3 GiB v2 free-space guard is enforced both before preparation and in hosted CI. The existing main-only push workflow remains the publication route.

The resulting derived inventory has **1,305 files / 636,098,834 bytes**, leaving **163,901,166 bytes** headroom. All **618** original v0.51.0 canonical rows remain exact; only the shared root index changes among old public rows. The new main-Explorer bridge is additive. Original v0.60.1 metadata and qualification match published asset digests; `input-authority-v0601.json` binds the measured source, tag and release.

This is a prepared source candidate, not deployment or acceptance. The complete two-file synthetic cohort passed 20 tests without game payload or network access. A reviewed source PR, hosted extraction/reread, complete public-body audit and actual old/new play plus Explorer journeys remain required. No payload was downloaded by local preparation, and no physical-device, offline, enjoyment or full-phase completion is claimed.
