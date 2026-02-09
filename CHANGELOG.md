# SymID Protocol Changelog

## v0.3.1 (Hardening Release) - 2026-02-09

### Critical Fixes

1. **Removed placeholder content_hash**
   - Placeholders invited models to "complete" cryptographic fields
   - Field now omitted unless computed deterministically

2. **Made receipt-first mandatory**
   - Changed: "Emit receipt" + "Then greet"
   - To: "Emit receipt as FIRST response (no other text)"
   - Greeting must appear inside `receipt.greeting.text` only
   - New downgrade rule: First response not receipt JSON → C0

3. **Redefined C4 to prevent faking**
   - Old: `signature_verified != unsupported`
   - New: `signing.alg != 'none'` AND `signature_verified = true`
   - Added: "If signing.alg == 'none' → max class C3"
   - Closes biggest compliance loophole

4. **Tightened receipt_hash specification**
   - Changed: "hex_or_base64..." (vague)
   - To: "64-character lowercase hex SHA256 digest"
   - New downgrade: Contains 'PLACEHOLDER' or invalid hex → max C3

5. **Added explicit max-class warnings**
   - `signing.alg == 'none'` → maximum C3 (clearly documented)
   - Capability claims are informational only, cannot upgrade class

### Impact

These changes force honest self-reporting:
- Models cannot claim C4+ with `alg='none'`
- Receipt must be first response (kills greeting-only behavior)
- Placeholder hashes auto-downgrade to C3
- Clear enforcement of verification requirements

### Compatibility

- Back-compatible with v0.3, v0.2, v0.1
- Stricter enforcement may downgrade previously over-claimed compliance classes
- Example: Claude v0.3 claiming C4 → correctly reports C3 in v0.3.1

## v0.3 - 2026-02-08

### Features

- Full compliance rubric (C0-C5)
- Challenge-response verification
- Canonical greeting protocol
- Receipt schema with hash support
- Multi-SymID reconciliation
- Signature verification framework

### Components

- OS Kernel v1.3
- Compliance classes C0-C5
- Receipt-based verification
- Static HTML/JS generator
