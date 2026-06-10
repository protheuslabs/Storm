# Subsystem Modularity

Storm will need powerful subsystems, but they should stay modular.

The product can begin as a simple application, even a monolith, but it should not become a tangled system where decomposition, value policy, rights enforcement, versioning, provenance, reputation, payments, applets, and InfRing adapters all reach directly into each other.

Modularity is what lets Storm start small, replace native mechanisms with InfRing primitives later, and add new project applets without making every subsystem understand every domain.

## Core Rule

Every major subsystem should have a clear contract.

A subsystem contract defines:

- What inputs it accepts.
- What outputs it returns.
- What events it emits.
- What state it owns.
- What policies govern it.
- What receipts or audit records it creates.
- What errors, disputes, or review states it can produce.
- Which parts are product-facing projections versus canonical authority.

## Modular Does Not Mean Microservices First

The first implementation can be a conventional monolith.

Modularity should start as code and data boundaries:

- Separate modules.
- Explicit interfaces.
- Clear ownership of records.
- No hidden cross-module writes.
- Events or service calls instead of ad hoc coupling.
- Tests around subsystem contracts.

Storm should not add network complexity before the core product loop works.

## Subsystems To Keep Modular

Likely subsystems include:

- Workflow orchestration.
- Project and task workflow.
- Applet framework.
- Identity, permissions, and roles.
- Artifact storage.
- Task decomposition.
- Review and dispute handling.
- Reputation.
- Value policy and contribution valuation.
- Value ledger.
- Payments.
- Fraud, risk, and anti-collusion.
- Search, discovery, and matching.
- Provenance and contribution graph.
- Versioning and forks.
- Originality and rights enforcement.
- AI training provenance.
- Notifications.
- Privacy, consent, and data access.
- API and integration layer.
- Audit/event bus.
- Policy engine.
- Governance and release switch.
- InfRing adapters.

Not every subsystem needs to exist in the MVP. The point is to avoid building early choices in a way that blocks later separation.

## Boundary Principles

### Own State Clearly

Each subsystem should own its canonical records.

Examples:

- Ledger owns economic entries.
- Value policy owns allocation rules and explanations.
- Rights enforcement owns originality checks, similarity matches, rights reviews, and enforcement actions.
- Versioning owns version nodes, fork records, and merge proposals.
- Applets own domain semantics.

Other subsystems can read through contracts or consume events, but they should not mutate another subsystem's records directly.

### Emit Events

Important actions should emit structured events.

Examples:

- Task approved.
- Contribution recorded.
- Value policy applied.
- Ledger entry created.
- Originality check flagged.
- Rights review decided.
- Merge proposal accepted.
- Receipt emitted.

Events make it easier to build audit trails, projections, notifications, reputation updates, and future InfRing receipt mapping.

### Keep UI Separate From Authority

UI should collect inputs, show state, and support review.

Authority should live in backend subsystems:

- Decomposition providers.
- Value calculation.
- Rights enforcement.
- Ledger allocation.
- Review state transitions.
- Merge decisions.

This keeps applet UI replaceable and prevents product screens from becoming hidden policy engines.

### Use Provider Interfaces

Subsystems that may later be replaced by InfRing should use providers or adapters from the beginning.

Examples:

- `DecompositionProvider`.
- `ReceiptProvider`.
- `VersionLineageProvider`.
- `RightsEvidenceProvider`.
- `ValuePolicyExecutor`.
- `NetworkValidationProvider`.

The first provider can be native Storm code. Later providers can call InfRing primitives.

### Keep Applets Thin Where Possible

Applets should define domain semantics and user workflow, not reimplement every platform primitive.

Story Forge can define what a canon merge means. It should not invent its own permanent version graph if a shared versioning subsystem can serve the need.

Code Forge can define code review rules. It should not bypass the value ledger, contribution graph, rights enforcement, or provenance model.

### Make Policy Versioned

Subsystems that affect money, rights, access, governance, or reputation should use versioned policy.

This includes:

- Value policies.
- Rights enforcement policies.
- Review rubrics.
- Applet merge rules.
- Reputation scoring rules.
- Governance rules.

Policy versioning protects users from invisible rule changes and supports later receipt-backed execution.

## Composition Pattern

The core product flow should compose subsystems without collapsing them into one another.

Example:

1. Applet creates or imports task candidates through a decomposition provider.
2. Project workflow opens a task.
3. Contributor submits work.
4. Rights enforcement checks originality and permissions.
5. Review subsystem validates against acceptance criteria.
6. Versioning or applet merge records accepted artifact state.
7. Value policy calculates allocation.
8. Ledger records economic events.
9. Reputation consumes outcomes.
10. Receipts or future InfRing adapters record verifiable evidence.

Each step can be native at first and stronger later.

## InfRing Migration

Modularity is required for the InfRing endgame.

If Storm-native mechanisms are behind contracts, Storm can replace them when InfRing provides mature primitives:

- Native decomposition -> InfRing task decomposition.
- Native receipts -> InfRing receipts.
- Native version lineage -> InfRing versioning/fork subsystem.
- Native rights evidence -> InfRing rights evidence receipts or validation.
- Native value execution -> deterministic policy execution where practical.
- Native network trust -> local validation and proof-carrying signals.

Without modularity, Storm will not be able to phase out native mechanisms cleanly.

## Anti-Patterns

Avoid:

- Applets writing directly to ledger tables.
- Rights enforcement directly changing payout records without a ledger event.
- Decomposition logic inside frontend UI.
- Value calculation hidden inside payment integration.
- Fork lineage stored only as display metadata.
- Reputation scores updated without source events.
- InfRing-specific assumptions leaking into every product component before InfRing is ready.
- A generic core that absorbs every applet-specific concept too early.

## MVP Implication

The MVP should implement only the modules needed for the core loop.

Minimum useful modules:

- Users and permissions.
- Projects and tasks.
- Claims and submissions.
- Review.
- Ledger.
- Basic reputation events.
- Story Forge metadata and templates.

Even inside a monolith, these should have visible boundaries so later subsystems can be added without rewriting the core.

## Open Questions

- What subsystem contracts should be defined before implementation starts?
- Which modules need provider interfaces on day one?
- What event format should subsystems emit?
- How strict should database ownership boundaries be in the first monolith?
- Which subsystem should own contribution events?
- Should applets call subsystems directly or through a project workflow orchestrator?
- How should future InfRing providers be tested against native providers?
- Which policies must be versioned before launch?
