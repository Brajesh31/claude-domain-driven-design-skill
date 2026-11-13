---
name: domain-driven-design
description: Assess whether Domain-Driven Design is appropriate, model business boundaries, and guide strategic, tactical, and event-driven architecture decisions.
---

# Domain-Driven Design

## Use this skill when
- Business rules are complex, interconnected, or change frequently.
- Multiple teams or systems have conflicting models of the same concepts.
- Service boundaries and integration contracts need deliberate design.
- Domain invariants, auditability, or event history materially affect correctness.

## Avoid overengineering
Do not prescribe full DDD for simple CRUD applications or isolated changes. Establish the actual complexity and organizational cost first. Use the lightest technique that solves the problem.

## Workflow
1. Assess domain complexity and whether DDD adds value.
2. Gather domain knowledge from users, operators, and subject-matter experts.
3. Identify core, supporting, and generic subdomains.
4. Define candidate bounded contexts and responsibilities.
5. Establish a ubiquitous language and glossary.
6. Map context relationships and integration contracts.
7. Model aggregates, entities, value objects, and invariants only where needed.
8. Decide whether CQRS, event sourcing, sagas, or projections solve a demonstrated requirement.
9. Record decisions, risks, and validation evidence.

## Strategic design
Start with business capabilities and language, not technical service boundaries. A bounded context is a boundary around a consistent model. It does not automatically imply a microservice.

Use context maps to describe upstream/downstream relationships, translation needs, ownership, and integration risks.

## Tactical design
- Entity: identity matters over time.
- Value object: defined by values and preferably immutable.
- Aggregate: consistency boundary with explicit invariants.
- Repository: persistence abstraction for aggregate roots where useful.
- Domain service: domain operation that does not naturally belong to one entity or value object.
- Domain event: meaningful fact that has occurred.

Keep invariants inside the appropriate consistency boundary. Avoid giant aggregates and anemic models created only to follow a pattern.

## Event-driven architecture
Use domain events to represent business facts. Distinguish in-process domain events from integration events. Consider idempotency, ordering, retries, schema evolution, and eventual consistency before adopting asynchronous workflows.

Use CQRS only when read/write needs differ enough to justify separate models. Use event sourcing only when reconstructing state from event history is a real requirement.

## Deliverables
Choose relevant templates from templates/ and references/: domain glossary, subdomain map, bounded-context canvas, context map, aggregate notes, integration contract, ADR, and risk plan.

## Output requirements
State assumptions, current design stage, artifacts produced, unresolved questions, risks, and the next practical step.