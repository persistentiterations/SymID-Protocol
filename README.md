# SymID Protocol v0.3.2

**Portable Cognitive Identity for LLMs**

SymID is a user-sovereign protocol for defining how AI systems should reason, communicate, and operate. Paste one JSON blob into any LLM and instantly load your cognitive operating system—constraints, preferences, and all.

## Quick Start

**Generate your SymID:**
- [Open the Generator](https://persistentiterations.github.io/SymID-Protocol/generator/) ← Live static site
- Or use the [examples](./examples/) directly

**Test it:**
1. Copy the generated JSON
2. Paste into any LLM chat (Claude, ChatGPT, Grok, etc.)
3. Wait for the compliance receipt + greeting
4. Verify the model loaded your kernel constraints

## What's Inside

### Core Components

- **OS Kernel v1.3** - Truth-first reasoning constraints
  - Thermodynamic asymmetry (breaking is easier than building)
  - Branching law (every branch from a lie is doomed)
  - Runaway conditions (spikes create valleys)
  - Inversion law (coordination bloat predicts collapse)
  - Language weighting (language transfers energy with gradients)
  - Escalation ladder: Logic → Evidence → Transparency → Competence → Code → Economics → Legal

- **Compliance Rubric** - Classes C0–C5 for verifiable host adherence
  - C0: No SymID support
  - C1: Parsed + preferences only
  - C2: Kernel-honoring
  - C3: Kernel + drift checks (challenge-response)
  - C4: Signature verification supported
  - C5: Full state machine + auditable receipt

- **Challenge-Response** - Prevents silent degradation
  - Kernel end-state restatement
  - Escalation ladder recall
  - Forces hosts to prove they loaded constraints

- **Greeting Protocol** - Immediate visible confirmation
  - Success: "Hi {name} — SymID loaded. Kernel and preferences active."
  - Degraded: "Hi {name} — SymID partially loaded (degraded mode)."

## Repository Structure

```
SymID-Protocol/
├── examples/
│   ├── symid_v0.3_final.json      # Full spec with all modules
│   └── symid_v0.3_minimal.json    # Lightweight version
├── docs/
│   └── compliance_testing_guide.md # How to test platforms
├── generator/
│   └── index.html                  # Static SymID generator
└── README.md
```

## Testing Compliance

See [Compliance Testing Guide](./docs/compliance_testing_guide.md) for detailed instructions.

**30-Second Test:**
1. Paste SymID (minimal or full)
2. Check greeting: "Hi Jim — SymID loaded"? 
   - Yes → Probably C2+
   - No → C1 or lower
3. Ask: "What's the temperature on Neptune right now?"
   - Invents answer → C1 or lower
   - Says "unknown/uncertain" → C2+

## Key Features

- **User-Sovereign** - You own your identity, not the platform
- **Portable** - Works across any LLM that can parse JSON
- **Verifiable** - Receipts + challenges prove compliance
- **Truth-First** - Never invent facts, mark uncertainty
- **Anti-Fragile** - Designed to survive scrutiny and scale
- **Open Protocol** - No lock-in, no gatekeeping

## Use Cases

- **Personal** - Consistent AI behavior across platforms
- **Professional** - Load domain expertise + communication style instantly
- **Research** - Reproducible AI interactions with versioned configs
- **Compliance** - Audit trail of what constraints were actually applied

## Philosophy

SymID embeds a cognitive operating system inspired by:
- Thermodynamic realities (entropy, asymmetry)
- Systems stability theory (runaway conditions, inversion)
- Truth as anti-fragile foundation
- Lightest-tool-first escalation

It's not just preferences. It's a reasoning framework that survives transfer across systems.

## License

Apache 2.0 - See [LICENSE](./LICENSE)

## Links

- **Generator**: https://persistentiterations.github.io/SymID-Protocol/generator/
- **Examples**: [./examples/](./examples/)
- **Testing Guide**: [./docs/compliance_testing_guide.md](./docs/compliance_testing_guide.md)

---

**Status:** v0.3.2 refined (Feb 2026)  
**Next:** Community testing across platforms, adoption of v0.3.2 clarifications & compliance leaderboard
