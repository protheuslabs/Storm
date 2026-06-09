# Architecture Notes

This document captures early technical direction. It should evolve after product decisions become firmer.

## System Shape

Storm will likely need a conventional web application architecture first:

- Web frontend.
- Backend API.
- Relational database.
- Background jobs.
- Notification system.
- Payment provider integration.
- File or artifact storage.

## Early Design Preference

Start with a simple monolith or tightly integrated full-stack app. The domain is complex enough without adding distributed system complexity early.

The first implementation should optimize for:

- Fast product iteration.
- Clear domain modeling.
- Reliable workflow state transitions.
- Auditability for payments, reviews, and disputes.
- Testability around task and ledger behavior.

## Core Technical Concerns

### Workflow State

Task, submission, review, dispute, and payout states should be explicit. State transitions should be centralized enough to prevent invalid transitions.

### Auditability

Ledger entries, review decisions, dispute outcomes, and reputation events should be append-oriented where possible. Important economic events should not be silently overwritten.

### Permissions

Authorization should be designed early because the platform has multiple roles:

- Project owners.
- Contributors.
- Reviewers.
- Resolvers.
- Admins.

### Payments

Payments should be abstracted behind an internal ledger before integrating deeply with a payment provider. The product needs to represent value allocation even before real payouts are automated.

### Reputation

Reputation should be event-based rather than stored only as a mutable score. Aggregate scores can be derived from reputation events.

### Contribution Graph

Future Storm may need to connect ideas, decomposition work, submissions, reviews, research, and residual claims. The MVP does not need full residual compensation, but reputation and ledger events should be modeled so a contribution graph can be added later without rewriting every economic event.

### Project Applets

Storm core should stay generic. Applets should layer domain-specific metadata, task templates, artifact types, review rubrics, merge behavior, and export formats on top of the core project loop.

Story Forge can start as the first applet with static metadata and templates. A formal applet framework can come later after the first applet proves the model.

### AI Data Provenance

Future Storm may allow AI training on Storm data and approved Protheus Labs ecosystem data. Source records, artifacts, dataset membership, training runs, and downstream AI value events should be traceable. The MVP does not need model attribution, but it should avoid destroying source provenance in artifacts and contribution events.

### Future Protheus/InfRing Substrate

Storm may eventually use Protheus network and InfRing primitives once InfRing v2 is complete and individual instances can operate as network nodes. The relevant future primitives are receipt-backed execution, deterministic policy authority, Gateway boundaries, local validation, node identity, and federated proof-carrying signals.

The MVP should not depend on InfRing, but it should preserve event history and authority boundaries so future receipt emission is possible.

### Artifacts

Submissions may need files, links, Git commits, design files, documents, or other evidence. The first implementation can support links and notes, then expand by task type.

## Suggested Initial Stack

This is a placeholder recommendation, not a final decision.

- Full-stack TypeScript application.
- React or Next.js frontend.
- Postgres database.
- Prisma or Drizzle ORM.
- Background jobs with a simple queue.
- Stripe or similar provider for future payouts.

## Architecture Principles

- Keep economic state explicit.
- Keep workflow transitions testable.
- Prefer append-only records for payment and reputation history.
- Avoid early microservices.
- Do not make AI automation a hard dependency for MVP.
- Keep platform fee logic visible in code and UI.
- Preserve room for ideas, groups, and contribution events without making them MVP requirements.
- Preserve artifact provenance so future AI training compensation is possible.
- Keep authority and policy decisions separate from presentation so future InfRing integration is plausible.
- Keep applet-specific logic out of Storm core until multiple applets need the same concept.

## Future Capabilities

- AI-assisted project decomposition.
- Project applet framework.
- Skill-based contributor matching.
- Risk-based review assignment.
- Fraud and collusion detection.
- Public project pages.
- External reputation export.
- API for external project/task creation.
- Idea containers and recursive decomposition.
- Group and alliance governance.
- Residual contribution claims.
- AI training provenance and source compensation.
- Protheus/InfRing receipt-backed network transition.
- World Eye-style intelligence inputs.
- Bolt-style real-world bounties.
