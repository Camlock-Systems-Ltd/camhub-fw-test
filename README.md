# camhub-fw-test

Throwaway test repository for the CAMHUB firmware sync feature (customer firmware sourced from GitHub).

**This is not real firmware. Do not flash it onto a product.**

- Part number used for testing: `TEST001`
- Each release carries one asset named `TEST001.hex`.
- The HEX files are tiny, valid Intel HEX files containing only an idle loop. They exist so the sync code has something to fetch, validate and cache.
- `v1.0` and `v1.1` differ by a few bytes so a version change can be detected.

This repository can be deleted once the feature has been tested.
