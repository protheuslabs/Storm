# Storm Definition Gate

This is the practical go/no-go document for entering implementation work.  
Storm should not move from Phase 0 to Phase 1 until every required item is marked `Ready`.

## Gate Format

For each area, list owner, required evidence, current state, and blockers.

## 1) Core Thesis and Positioning

- [ ] Core thesis is defined in one sentence.
  - Evidence: link to [Vision](vision.md) and [Positioning And First Wedge](positioning-and-wedge.md).
- [ ] Public wedge is Story Forge with concrete scope and MVP promise.
  - Evidence: explicit in [Story Forge Vertical](story-forge-vertical.md).
- [ ] Internal thesis is distinct from public messaging and documented.
  - Evidence: [Protheus Ecosystem Thesis](protheus-ecosystem-thesis.md).
- [ ] A single public promise exists that avoids over-abstracted ecosystem framing.
  - Evidence: [README](../README.md) first-pitch sections and docs consensus.

## 2) Core Platform Contract

- [ ] Non-negotiable core surfaces are fixed.
  - Expected: Projects, Tasks, Claims, Submissions, Reviews, Disputes, Reputation, Ledger, Provenance.
- [ ] State transitions for core surfaces are defined with validation expectations.
  - Evidence: [Core Workflows](core-workflows.md), [Domain Model](domain-model.md), [Architecture Notes](architecture-notes.md).
- [ ] The minimum event set is defined for auditable workflow history.
  - Evidence: [Value Ledger](value-ledger.md), [Architecture Notes](architecture-notes.md), [ID And Receipt Strategy](id-and-receipt-strategy.md).
- [ ] It is clear what is authoritative truth at each transition in implementation.
  - Evidence: explicit contract language in linked docs and no contradictory assumptions.

## 3) Governance Contract

- [ ] Protheus stewardship and control boundaries are explicit.
  - Evidence: [Release Switch](release-switch.md), [Ownership And Governance](ownership-and-governance.md), [Protheus Ecosystem Thesis](protheus-ecosystem-thesis.md).
- [ ] Origin allocation is separate from day-to-day control.
  - Evidence: documented in [Release Switch](release-switch.md) and [Ownership And Governance](ownership-and-governance.md).
- [ ] Stewardship decay conditions are defined and tracked.
  - Evidence: criteria section in [Release Switch](release-switch.md).
- [ ] Anti-capture constraints are explicit.
  - Evidence: [Trust And Incentives](trust-and-incentives.md), [Agent Participation And Bot Control](agent-participation-and-bot-control.md), [Platform Concepts](platform-concepts.md).

## 4) Economics Contract

- [ ] Fixed visible task payout policy is defined for MVP.
  - Evidence: [Contribution Value Model](contribution-value-model.md), [MVP Scope](mvp-scope.md), [Build Plan](build-plan.md).
- [ ] Dispute and correction behavior is defined.
  - Evidence: [Core Workflows](core-workflows.md), [Value Ledger](value-ledger.md), [Release Switch](release-switch.md).
- [ ] Ledger visibility requirements are defined.
  - Evidence: [Product Brief](product-brief.md), [Value Ledger](value-ledger.md).
- [ ] Residual/upstream value is explicitly deferred and scoped to later phases.
  - Evidence: [MVP Scope](mvp-scope.md), [Roadmap](roadmap.md).

## 5) Applet Contract

- [ ] First applet boundary is locked as Story Forge.
  - Evidence: [Project Applets](project-applets.md) and [Story Forge Vertical](story-forge-vertical.md).
- [ ] Core vs applet responsibilities are explicit.
  - Evidence: [Project Applets](project-applets.md), [Core Workflows](core-workflows.md), [Subsystem Modularity](subsystem-modularity.md).
- [ ] Applet onboarding path to the next applet is defined.
  - Evidence: [Project Applets](project-applets.md), [Roadmap](roadmap.md).
- [ ] Applet-specific decomposition/review/export boundaries are defined.
  - Evidence: [Story Forge Vertical](story-forge-vertical.md), [Subsystem Modularity](subsystem-modularity.md).

## 6) Integration and Network Contract

- [ ] Native scaffolding vs durable primitive boundaries are defined.
  - Evidence: [Architecture Notes](architecture-notes.md), [Protheus And InfRing Integration](protheus-infring-integration.md).
- [ ] InfRing migration targets are explicitly scoped with replacement order.
  - Evidence: [Protheus And InfRing Integration](protheus-infring-integration.md), [Roadmap](roadmap.md).
- [ ] Data-sharing boundaries across products are defined.
  - Evidence: [Protheus Ecosystem Thesis](protheus-ecosystem-thesis.md), [Open Questions](open-questions.md).
- [ ] Bot/agent trust boundaries are documented without enforcing full fraud system in MVP.
  - Evidence: [Agent Participation And Bot Control](agent-participation-and-bot-control.md), [Roadmap](roadmap.md), [Build Plan](build-plan.md).

## 8) Legal Completion Gate

- [ ] Legal-document and filing requirements are defined for non-MVP and release phases.
  - Evidence: [Legal Documentation And Filing](legal-documentation-and-filing.md), [Roadmap](roadmap.md), [Platform Concepts](platform-concepts.md).
- [ ] Legal-state gates are modeled as policy rules, not hardcoded checks.
  - Evidence: [Architecture Notes](architecture-notes.md), [Subsystem Inventory](subsystem-inventory.md).

## 7) Security, Trust, and Compliance Readiness

- [ ] Identity, access, and role model are defined.
  - Evidence: [Architecture Notes](architecture-notes.md), [Open Questions](open-questions.md) - legal and compliance section.
- [ ] Rights and originality assumptions are constrained to future phases where needed.
  - Evidence: [Originality And Rights Enforcement](originality-and-rights-enforcement.md), [AI Training Provenance](ai-training-provenance.md).
- [ ] Privacy and consent posture is documented before cross-product data paths.
  - Evidence: [Protheus Ecosystem Thesis](protheus-ecosystem-thesis.md), [Open Questions](open-questions.md).
- [ ] Legal documentation and filing workflows are identified, with clear user responsibility boundaries.
  - Evidence: [Legal Documentation And Filing](legal-documentation-and-filing.md), [Ownership And Governance](ownership-and-governance.md).

## Definition Gate Decision

Status: `Blocked` until all required items are satisfied.

Go condition:

- All required items above are marked `Ready`.
- No unresolved core contract questions remain in [Open Questions](open-questions.md).
- Remaining items are implementation detail, and each has a visible owner and expected milestone.

No-Go condition:

- Ambiguous governance and value-routing rules.
- Core contract ambiguity between core vs applet ownership.
- Missing anti-capture constraints.
- Unclear release-switch transition triggers.

## Owners and Review Rhythm

Owners for this gate should be assigned before any engineering milestone begins.

- Governance and anti-capture owner: to be assigned.
- Economics and payout policy owner: to be assigned.
- Product scope and applet boundaries owner: to be assigned.
- Technical and integration owner: to be assigned.
- Network and InfRing migration owner: to be assigned.

Suggested review rhythm:

- Weekly gate check until Phase 1 is unlocked.
- Monthly re-evaluation of unresolved questions.

## Log

- Added from the current definition-first planning sequence in this repository.
