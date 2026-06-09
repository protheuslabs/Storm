# Protheus And InfRing Integration

Storm may eventually transition from a conventional web platform into an application layer on the Protheus network, using primitives from the InfRing operating system once InfRing v2 is complete and a single instance can become a network node.

Reference:

- InfRing repository: `https://github.com/protheuslabs/InfRing`

## Why InfRing Matters To Storm

Storm requires a trustworthy substrate for:

- Provenance.
- Receipts.
- Contribution records.
- Value ledger events.
- Policy enforcement.
- Dispute evidence.
- AI training data lineage.
- Federated project execution.
- Local authority with network participation.

InfRing is a plausible future substrate because its public docs describe it as a deterministic, receipt-first runtime designed for verifiable execution, fail-closed safety, and reproducible workflows.

## Relevant InfRing Concepts

Based on the current InfRing repository and vision docs, the relevant concepts are:

- Deterministic Kernel authority.
- Orchestration Control Plane for coordination.
- Gateway boundary membrane for external ingress and policy boundaries.
- Thin Shell presentation.
- Receipts and reproducible evidence.
- Validation and observability.
- Fail-closed safety.
- Local-first adaptive intelligence under user authority.
- Federated user-owned nodes.
- Proof-carrying signals exchanged between nodes.
- Local validation before adoption.

## Storm On Protheus Network

In the long term, Storm should be able to use Protheus/InfRing primitives for:

- Node identity.
- Contributor identity.
- Contribution receipts.
- Task execution receipts.
- Review receipts.
- Ledger event receipts.
- Dataset provenance receipts.
- Governance policy enforcement.
- Project state replication.
- Peer validation.
- Local-first contributor workspaces.
- Federated discovery of tasks, projects, models, and contributors.

## Single Instance To Network Node

The key technical transition is when an InfRing instance can become a network node.

At that point, Storm can move from:

> centralized app with database-backed trust

to:

> federated project network with receipt-backed trust

This does not mean Storm should abandon conventional infrastructure immediately. The MVP should remain a normal web app. But the data model should avoid assumptions that make later network transition impossible.

## Suggested Primitive Mapping

| Storm Concept | Future InfRing/Protheus Primitive |
| --- | --- |
| User | Node identity or contributor identity |
| Project | Network-visible project state |
| Task | Bounded work request |
| Submission | Artifact plus execution receipt |
| Review | Validation receipt |
| Ledger entry | Economic receipt |
| Contribution event | Provenance receipt |
| Dispute | Evidence bundle plus governance process |
| Dataset source record | Data provenance receipt |
| AI value event | Value event receipt |
| Group or alliance | Governed network collective |

## Trust Model

Storm should eventually rely on proof rather than platform authority.

Future trust should come from:

- Receipts.
- Local validation.
- Transparent policy.
- Reproducible evidence.
- Contributor reputation.
- Node reputation.
- Governance decisions.
- Audit trails.

No node should blindly accept another node's work, model, policy, or value claim. Incoming network claims should be validated locally or accepted only within explicit trust boundaries.

## MVP Implication

The first Storm implementation should not depend on InfRing.

It should, however:

- Keep contribution records append-oriented.
- Keep ledger events explicit.
- Keep provenance attached to artifacts.
- Make state transitions auditable.
- Separate policy decisions from UI presentation.
- Avoid hiding critical authority in frontend code.
- Preserve enough event history to later emit receipts.

## Open Questions

- What InfRing v2 primitives will be stable enough for Storm to depend on?
- What is the minimal Storm receipt format?
- Which Storm events must be receipt-backed first?
- How should Storm map users to network nodes?
- Can one user operate multiple nodes?
- Can one node represent a group?
- How should ledger events reconcile across nodes?
- What data remains local by default?
- What data can be shared across the Protheus network?
- How should Storm handle offline contribution and later network reconciliation?
