# Independent Insurance — TRASHNET

**Project:** TRASHNET  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `6fa2b878c6c1b4304b91109070ce0edf9279bb31`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | TRASHNET with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
