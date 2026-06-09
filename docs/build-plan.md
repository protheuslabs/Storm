# Build Plan

This is the first engineering-oriented plan. It should change as product decisions become sharper.

## Build Objective

Create the smallest useful Storm product loop:

Project -> Task -> Claim -> Submit -> Review -> Ledger -> Reputation.

The first build should prove crowdsourced projects, not a generic task board. It should show that distributed contributors can collectively move a project forward through claimable work, accountable review, and transparent value allocation.

The first build should not implement residual compensation, AI training provenance, Protheus/InfRing networking, InfRing task decomposition, groups, alliances, World Eye, or Bolt. It should model economic and reputation events cleanly enough that those layers can be explored later.

## Milestone 1: Repo And App Foundation

Deliverables:

- Initialize application structure.
- Add linting, formatting, and test setup.
- Add basic local development instructions.
- Add database schema migration setup.
- Add seed data for demo projects and tasks.

## Milestone 2: Identity And Roles

Deliverables:

- User accounts.
- Basic profiles.
- Role support for project owner, contributor, reviewer, and admin.
- Authorization checks for project and task actions.

## Milestone 3: Projects And Tasks

Deliverables:

- Create and edit projects.
- Create and edit tasks.
- Task status model.
- Task dependency model.
- Project progress view.

## Milestone 4: Claim And Submission Flow

Deliverables:

- Browse open tasks.
- Claim task.
- Release or expire claim.
- Submit work artifacts and notes.
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
- Permission tests.
- Ledger correctness tests.
- Seeded demo scenario.
- Basic admin visibility.

## First Implementation Bias

Build the workflow manually before adding AI decomposition, marketplace matching, or payment automation. The manual workflow is the proof that the incentives and domain model work.
