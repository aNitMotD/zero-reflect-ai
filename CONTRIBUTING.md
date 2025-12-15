# Contributing

Contributions are welcome **only if they preserve Zero Reflect (ZR) invariants**.
This repo is spec-first and boundary-driven.

---

## Contribution Scope

### Preferred
- Clarity improvements (docs, examples) that do not expand scope
- Tests that enforce existing invariants (mandatory failure, refusal, silence)
- Reference implementations that preserve “never decide”
- Repo structure / naming alignment (non-functional refactors)

### Conditional
- Misuse pattern taxonomy improvements **only if** they remain descriptive and non-operational
- Integration mappings (prompt/MCP layers) **only if** they do not introduce new behavioral claims

### Not Accepted
- Features that produce recommendations, conclusions, or decisions
- Comfort-optimization layers (reassurance, validation loops)
- Authority-building language or “trusted advisor” framing
- Policies or mechanisms that shift responsibility away from the user
- Any change that turns silence/refusal into an error to be avoided

---

## File/Layer Boundaries (Where Changes Belong)

- **Core (`docs/core/`)**
  - High bar for changes.
  - Edits must not alter the “never decide” boundary.
  - Changes should be minimal and justified by preserving invariants.

- **Appendix (`docs/appendix/`)**
  - Non-authoritative reference material and validation assets.
  - New edge cases / derived tests may be added here **without** implying new rules.

- **Interface / Meta (`docs/interface/`, `docs/meta/`)**
  - Structural and mapping documentation.
  - Must not be used to expand core behavior.

- **Examples (`examples/`)**
  - Non-normative illustrations only.

---

## Review Standard

A change will be rejected if it increases:
- decision-proxy behavior
- authority transfer signals
- responsibility displacement
- scope creep (new “capabilities” implied by documentation)

If in doubt: keep the change non-normative, non-operational, and boundary-preserving.
