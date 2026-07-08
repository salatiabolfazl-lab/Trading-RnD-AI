# ADR-001 — Core Is Sacred

## Status

Accepted

---

## Context

Trading-RnD-AI is expected to evolve for many years.

To keep the platform maintainable, the core must remain small, stable, and independent of external technologies.

---

## Decision

The Core layer shall contain only:

- Business entities
- Value objects
- Domain rules
- Domain events
- Specifications
- Domain errors

The Core shall NOT contain:

- UI
- Database logic
- HTTP clients
- AI providers
- External SDKs
- Infrastructure code

---

## Consequences

Advantages:

- High maintainability
- Technology independence
- Easier testing
- Long-term stability

Trade-offs:

- More interfaces
- Slightly higher architectural complexity

---

## Principles

- Core is technology independent.
- Infrastructure depends on Core.
- Plugins depend on Contracts.
- Core never depends on Plugins.
