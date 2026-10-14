# Ethics — TRASHNET

**Project:** TRASHNET  
**Category:** WASTE_MANAGEMENT  
**Upstream:** see BENCH.json  
**Pinned commit:** `6fa2b878c6c1b4304b91109070ce0edf9279bb31`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `07c0b6568db4f93c0ffecacc25e0191ac1352d7f918450bb31eb14472f919bbe`  
**Date:** October 2026

## Position

TRASHNET is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
