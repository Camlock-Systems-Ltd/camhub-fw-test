# camhub-fw-test

Throwaway test repository for the CAMHUB firmware sync feature (customer firmware sourced from GitHub).

**This is not real firmware. Do not flash it onto a product.**

- Part number used for testing: `TEST001`
- Each release carries one asset named `TEST001.hex`.
- The HEX files are tiny, valid Intel HEX files containing only an idle loop. They exist so the sync code has something to fetch, validate and cache.
- `v1.0` and `v1.1` differ by a few bytes so a version change can be detected.

This repository can be deleted once the feature has been tested.

## Release naming rule under test

Only a `.hex` asset whose name ends in `release` is published to CAMHUB, for example `TEST001_release.hex`.
Any other asset on a release is ignored.

| Release | Assets | Expected in CAMHUB |
|---|---|---|
| v1.0, v1.1 | `TEST001.hex` | nothing published |
| v1.2 | `TEST001.hex`, `TEST001_debug.hex`, `TEST001_release.hex` | `TEST001_release.hex` |
