# SOX ITGC (COSO)

**Project:** TRASHNET · **Category:** WASTE_MANAGEMENT · **Vendor:** Anticloud FZ LLE

## Model component (PAX L5 Narrow L2 General 27B — quoted with provenance)

| Module | Key Metric | Value |
|--------|-----------|-------|
| CRDT | lww_set_us | 0.51 |
| CRDT | merge_10k_ms | 0.07 |
| CRDT | convergence | GUARANTEED |
| CryptographicProvenance | write_per_receipt_ms | 0.059 |
| CryptographicProvenance | verify_1k_chain_ms | 2.53 |
| ZeroTrustLocalMesh | ca_gen_ms | 367.5 |
| ZeroTrustLocalMesh | cert_issue_ms | 333.8 |
| ZeroTrustLocalMesh | tls_version | 1.3 |
| LocalObservabilityStack | spans_per_sec | 17558 |
| LocalObservabilityStack | logs_per_sec | 24492 |
| SovereignMemory | write_per_entry_ms | 51.94 |
| SovereignMemory | encryption | AES-256-GCM |
| AIOSS_AuditChain | entries_per_sec | 232665 |
| AIOSS_AuditChain | hash_algo | SHA3-256 |

*Run ID loiskleinner/pax-benchmark-runner v3, 2026-10-02, Kaggle T4 x2 (2x 16GB VRAM), Ubuntu 22.04, Python 3.12. These are PAX L5 Narrow L2 General 27B model-level results — shared model component, not this project's verdict.*

## Project-level basis (this project's own measured checks)

| Basis check | Status | Observed |
|---|---|---|
| 05_git_health | PASS | head=7a5246b24e59cd1d51638fefc9044391f5ab1c90 commits=1 clea |
| 03_dependency_scan | PASS | pinned=6 hashed=6 problems=[] |

## Verdict

CONTROLS EVIDENCED — all basis checks PASS

Verdict derives only from the basis checks above (actual runs, register recorded). Nothing here is copied from another project's assessment.

## Cryptographic integrity

- BENCH.json sha3-256: `ba7fcda1d39601e84a4f16ed66b0fa3628620dca7ae95930c89dcdea396cea49`
- Result register sha3-256: `104eafb1884eb9e0f3298710ba2efd03c13c313447d72f7d000d53cbf0255c35`
- Generated: 2026-10-06T18:13:11Z

*Anticloud FZ LLE · AIOSS Ledger Genesis: 8b4a8a4f6312dfbe885de8280716985637c163fd2a4b5590341d56db1cc4e560*

> Self-assessment only. No external audit has been performed. A SOC 2 / NIST independent audit is committed post-funding.
