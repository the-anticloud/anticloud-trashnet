# Educators — TRASHNET

**Project:** TRASHNET  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `6fa2b878c6c1b4304b91109070ce0edf9279bb31`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`  
**Date:** October 2026

## Teaching with TRASHNET

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
