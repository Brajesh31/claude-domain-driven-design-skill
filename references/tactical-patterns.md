# Tactical DDD Patterns

## Entity
Use when identity and lifecycle matter. Define identity rules and lifecycle transitions explicitly.

## Value object
Use for concepts defined by attributes rather than identity. Prefer immutability and validate values at construction.

## Aggregate
Use as a consistency boundary. External code should normally reference the aggregate root, and invariants should be enforced within the boundary.

## Domain service
Use for domain behavior that does not naturally belong to one entity or value object. Keep it focused on domain rules, not infrastructure orchestration.

## Domain event
Represent a meaningful business fact that has already happened. Use past-tense names and include only data needed by consumers.

## Repository
Provide a collection-like persistence interface for aggregate roots when it clarifies the model. Avoid creating repositories for every table by default.

## Anti-patterns
- One aggregate containing the entire business.
- Database tables disguised as domain objects.
- Domain events used as generic notifications.
- Anemic models with all rules in application services.
- Pattern adoption without a concrete business problem.