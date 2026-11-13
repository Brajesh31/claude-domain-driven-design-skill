# Context Mapping Patterns

Choose a relationship based on ownership, leverage, and integration constraints.

- Shared Kernel: contexts deliberately share a small model and coordinate changes.
- Customer-Supplier: a downstream context depends on an upstream provider that can prioritize its needs.
- Conformist: downstream adopts the upstream model because it cannot influence it.
- Anti-Corruption Layer: downstream translates an external model into its own language.
- Open Host Service: upstream exposes a stable integration contract.
- Published Language: shared, documented interchange model.
- Separate Ways: contexts remain independent when integration cost exceeds value.

## Mapping questions
For each relationship, record:
- Upstream and downstream context.
- Data and behavior exchanged.
- Contract owner.
- Translation or compatibility layer.
- Failure and retry behavior.
- Change coordination.
- Security and privacy boundary.

Do not label a relationship without describing the actual dependency.