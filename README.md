# Mastering Taproot (Public Draft)

### About the Book

*Mastering Taproot* is a developer-focused, reproducible guide to Bitcoin’s most powerful upgrade — Taproot.

This manuscript emphasizes:

- full code samples
- real testnet transactions
- precise stack execution
- minimal abstractions

The goal is not to “explain concepts”, but to **engineer them** — from single-leaf script spends, to multi-path Merkle tree constructions, to privacy-preserving control blocks.

Foundational Bitcoin engineering knowledge should be reproducible, inspectable, and forkable — therefore this work is published open-access.

---

### Audience

This project is intended for:

- Bitcoin protocol engineers
- Script / Taproot developers
- Wallet and key management system designers
- Researchers studying Script, Merkle commitments, or Taproot privacy
- Contributors preparing for Bitcoin Core or protocol-level work

Beginners may also use it as a structured, hands-on learning path.

---

### Status

This is an active public draft.

Updates are pushed regularly as chapters and code samples reach reproducible stability.

---

### Repository Structure

All manuscript chapters are in:  
[`book/manuscript/`](./book/manuscript/)

The table of contents is maintained at:  
[`book/manuscript/SUMMARY.md`](./book/manuscript/SUMMARY.md)

---

### How to Use This Repository

1. **Read the Manuscript**

   All chapters:
   
   [`book/manuscript/`](./book/manuscript/)
   
   Start with `SUMMARY.md` for the full outline.

2. **Run the Code**

   Every chapter's runnable examples live in [`code/`](./code/).
   
   All scripts include:
   
   - deterministic key generation
   - raw transaction hex construction
   - witness stack building
   - sighash verification
   - control block validation (Taproot)
   
   Scripts target Bitcoin testnet and require only Python 3.

3. **Verify Against the Network**

   Most examples produce:
   
   - a real testnet transaction ID
   - a decodeable raw transaction
   - validation steps you can run in Core (`decoderawtransaction`, `testmempoolaccept`, etc.)

---

### How to Contribute

Pull requests are welcome.

Typical contribution areas:

- typo fixes / formatting
- improved explanations / diagrams
- corrections to code samples
- additional reproducible testnet transactions

If you open an Issue, please include:

- chapter + section
- reproduction steps (if code)
- expected vs actual behavior

This project values *precision and reproducibility* above abstraction or opinions.

---

## 🔄 Recent Public Updates

(auto-updated during evaluation period)

- **Dec 1, 2025** — Added full runnable Python examples for Chapters 1–3 (key generation, P2PKH, P2SH, SegWit witness execution).

- **Dec 2, 2025** — Corrected previous_txid in Chapter 6 script-path spend; verified with new testnet transaction.

- **Dec 3, 2025** — Preparing Taproot key-tweaking examples (BIP340/341 math + address construction).

- **This Week** — Uploading single-leaf Taproot spend + OP_CHECKSIG path.

- **Next Week** — Multi-leaf Merkle tree constructor + control-block generator (matching book Chapter 7).

- **Upcoming** — Full 4-leaf script-path spend (hashlock, multisig, CSV timelock, single-sig) with testnet-verified witness.

---

### License

- Text: **CC-BY-SA 4.0**
- Code: **MIT**

This repository is developed in the open to support reproducible Bitcoin Script engineering education.