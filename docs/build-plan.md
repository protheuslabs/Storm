# Build Plan

This is the first engineering-oriented plan. It should change as product decisions become sharper.

## Build Objective

Create the smallest useful Storm product loop:

Project -> Task -> Claim -> Submit -> Review -> Ledger -> Reputation.

The first build should prove crowdsourced projects, not a generic task board. It should show that distributed contributors can collectively move a project forward through claimable work, accountable review, and transparent value allocation.

The first build should not implement residual compensation, AI training provenance, automated originality and rights enforcement, sophisticated bot or unauthorized-agent detection, Protheus/InfRing networking, InfRing task decomposition, groups, alliances, World Eye, or Bolt. It may include simple Storm-owned or applet-owned task templates/decomposition helpers, but those should stay behind an interface that can later merge with InfRing's task decomposition primitive.

When a Storm-native mechanism overlaps with an eventual InfRing primitive, the first implementation should treat it as scaffolding: useful now, interface-backed, auditable, and replaceable later.

## Definition-First Build Rule

The build plan should not advance until the core definition package is stable and agreed:

- Core thesis and public wedge positioning.
- Primitive contract and authoritative workflow states.
- Governance contract including steward roles, origin allocation, and stewardship decay.
- MVP economics and ledger transparency requirements.
- Storm core vs applet boundary.
- InfRing migration boundary and what is intentionally scaffolded.

If any of the above is unresolved, implementation should pause to avoid rework.

Major subsystems should stay modular even inside a monolith. Start with code boundaries, provider interfaces, and contract tests before considering separate services.

## Implementation Gate From Definition-First

- Before Milestone 1 begins, mark the [Storm Definition Gate](docs/storm-definition-gate.md) as complete.
- If the gate is not complete, implementation work should remain at design and definition tasks only.
- If the gate is complete and stable, we proceed into Milestone 1 and the minimum MVP loop.

## Milestone 1: Repo And App Foundation

Deliverables:

- Initialize application structure.
- Add linting, formatting, and test setup.
- Add basic local development instructions.
- Add database schema migration setup.
- Add seed data for demo projects and tasks.
- Establish initial module boundaries for users, projects, tasks, review, ledger, reputation, and applets.
- Establish workflow orchestration and audit/event module boundaries.
- Add contract-test pattern for subsystem interfaces.

## Milestone 2: Identity And Roles

Deliverables:

- User accounts.
- Basic profiles.
- Role support for project owner, contributor, reviewer, and admin.
- Authorization checks for project and task actions.
- Separate public contributor identity from private account/payment identity where possible.

## Milestone 3: Projects And Tasks

Deliverables:

- Create and edit projects.
- Create and edit tasks.
- Define whether a task expects human-only work or allows disclosed AI assistance.
- Backend task candidate generation interface for applet templates or temporary decomposition helpers.
- Decomposition UI for reviewing and accepting task candidates.
- Task status model.
- Task dependency model.
- Project progress view.

## Milestone 4: Claim And Submission Flow

Deliverables:

- Browse open tasks.
- Claim task.
- Release or expire claim.
- Submit work artifacts and notes.
- Include simple automation or AI-assistance disclosure on submission.
- Artifact storage for submission links/files and source references.
- View contributor task dashboard.

## Milestone 5: Review Flow

Deliverables:

- Review queue.
- Approve, reject, or request changes.
- Required review notes for rejection and changes.
- Submission history.
- Reviewer dashboard.

## Milestone 6: Ledger And Reputation Events

Deliverables:

- Internal ledger entries.
- Task payout breakdown.
- Platform fee display.
- Fixed-task-value policy record or constant.
- Allocation explanations for contributor payouts, reviewer rewards, platform fees, and adjustments.
- Reputation event creation.
- Basic contributor and reviewer metrics.

## Milestone 7: Disputes

Deliverables:

- Contributor dispute creation.
- Resolver queue.
- Dispute outcome recording.
- Ledger and reputation adjustments.

## Milestone 8: MVP Hardening

Deliverables:

- End-to-end workflow tests.
- Subsystem contract tests.
- Permission tests.
- Ledger correctness tests.
- Workflow transition tests.
- Audit/event emission tests.
- Seeded demo scenario.
- Basic admin visibility.
- Native mechanism inventory with likely future InfRing replacement targets.

## First Implementation Bias

Build the workflow manually before adding AI decomposition, marketplace matching, or payment automation. The manual workflow is the proof that the incentives and domain model work.

If temporary decomposition is added in the MVP, keep it backend-owned and interface-backed. The frontend should only collect inputs and let users review candidate tasks.

Do the same for other future InfRing overlaps: receipts, audit logging, provenance, rights evidence, value-policy execution, and network trust should be designed so Storm can phase out native authority as InfRing primitives become ready.
