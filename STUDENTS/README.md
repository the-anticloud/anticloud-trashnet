# Students — TRASHNET

**Project:** TRASHNET  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `6fa2b878c6c1b4304b91109070ce0edf9279bb31`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `6fa2b878c6c1b4304b91109070ce0edf9279bb31`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
