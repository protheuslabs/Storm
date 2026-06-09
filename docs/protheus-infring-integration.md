# Protheus And InfRing Integration

Storm may eventually transition from a conventional web platform into an application layer on the Protheus network, using primitives from the InfRing operating system once InfRing v2 is complete and a single instance can become a network node.

Reference:

- InfRing repository: `https://github.com/protheuslabs/InfRing`

## Migration Goal

Storm can build native mechanisms early, but they should be treated as bootstrap scaffolding when they overlap with future InfRing primitives.

The long-term goal is:

> use InfRing primitives wherever they are mature enough, and phase out Storm-native mechanisms that would otherwise duplicate those primitives.

This keeps Storm from becoming a second operating substrate. Storm should own the product layer: project semantics, applets, contributor experience, review workflows, value policies, legal wrappers, marketplace behavior, and release-switch governance. InfRing should increasingly own the lower-level trust, execution, receipt, validation, node, and policy primitives when those primitives are ready.

Versioning and forks are part of this future substrate. GitHub's open-source model is an inspiration, but Storm needs those mechanics generalized beyond code. InfRing may need a versioning/fork subsystem so Storm can rely on shared primitives for lineage, merge, fork, and provenance instead of creating a permanent Storm-only implementation.

## Native Mechanisms As Scaffolding

Storm-native mechanisms are acceptable when they help reach product-market proof before InfRing is ready.

Examples:

- Native task decomposition can bootstrap Story Forge, then converge with InfRing task decomposition.
- Native action receipts can provide auditability, then map to InfRing receipts.
- Native ledger records can model economics, then emit or reconcile with economic receipts.
- Native value-policy execution can start in application code, then move toward deterministic policy execution when available.
- Native contribution and dataset provenance can preserve history, then map to InfRing provenance receipts.
- Native originality and rights evidence can support early review, then map to receipt-backed evidence bundles and validation signals.
- Native project versioning and fork records can bootstrap collaboration, then converge with an InfRing versioning/fork subsystem if one exists.
- Native trust and moderation can support the MVP, then shift toward local validation and proof-carrying network signals.

The rule is not "wait for InfRing." The rule is "build Storm so native mechanisms can be replaced when InfRing has the stronger primitive."

## Primitive Replacement Criteria

Storm should phase out a native mechanism when the corresponding InfRing primitive is:

- Stable enough to depend on.
- Receipt-backed or otherwise verifiable.
- Compatible with Storm's user, project, task, value, and applet semantics.
- Testable against existing Storm event history.
- Migratable without losing contributor provenance.
- Capable of local validation or clear trust-boundary enforcement.
- Better than the native mechanism at reducing platform authority.

Until those criteria are met, Storm can keep the native mechanism behind an interface.

Subsystem modularity is the condition that makes this possible. Native mechanisms should sit behind explicit contracts so an InfRing-backed provider can replace the native provider without rewriting every applet or workflow.

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
- Task decomposition.
- Contribution receipts.
- Task execution receipts.
- Review receipts.
- Ledger event receipts.
- Dataset provenance receipts.
- Rights evidence receipts.
- Governance policy enforcement.
- Project state replication.
- Peer validation.
- Versioning and fork lineage.
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
| Task | Bounded work request or decomposed micro-task |
| Submission | Artifact plus execution receipt |
| Review | Validation receipt |
| Ledger entry | Economic receipt |
| Contribution event | Provenance receipt |
| Action receipt | Project-scoped receipt with later InfRing receipt mapping |
| Dispute | Evidence bundle plus governance process |
| Dataset source record | Data provenance receipt |
| AI value event | Value event receipt |
| Originality check | Rights evidence or validation receipt |
| Rights review | Evidence bundle plus governance decision |
| Group or alliance | Governed network collective |
| Project fork or branch | Version/fork lineage primitive |
| Merge proposal | Receipt-backed merge decision |

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

## Task Decomposition Integration

Storm should eventually use InfRing's task decomposition primitives.

Current InfRing repository signals include:

- `execution:task-decompose` and `execution:task-decompose:status` commands.
- `V3-TASK-001`: Task Decomposition Primitive + Parallel Micro-Task Execution.
- `V3-TASK-002`: Task Decomposition Live Execution Handoff.
- Rust execution code for composing micro-tasks with success criteria, routing, provenance, governance, and attribution fields.

Storm may have its own decomposition logic early, especially inside applets like Story Forge. That is acceptable as a bootstrap path. It should not become a permanent competing substrate.

Near-term Storm can create tasks manually, from applet templates, or from lightweight Storm-owned decomposition helpers. Later, Storm decomposition should converge with InfRing's task decomposition primitive.

The long-term path should be:

1. Manual tasks and applet templates.
2. Storm-owned applet decomposition helpers.
3. Storm-to-InfRing compatibility contract.
4. InfRing-backed task candidate generation.
5. Full convergence where Storm accesses InfRing's task decomposition primitive for canonical decomposed task candidates.

Storm's decomposition UI should survive this migration. The backend decomposition provider can change from temporary Storm logic to InfRing without changing the core user interaction model.

For example:

- Story Forge passes premise, format, genre, canon notes, and target artifact.
- InfRing decomposes the goal into proposed story tasks.
- Story Forge filters those tasks through story-specific templates and review rules.
- Storm records accepted tasks, provenance, and value rules.

The boundary should be:

- InfRing decomposes, routes, receipts, and validates execution primitives.
- Storm owns project economics, applet semantics, contributor marketplace, review, ledger, and value routing.
- Storm may shape decomposition with applet constraints, but InfRing becomes the canonical primitive for decomposition when the network substrate is mature.

## Native-To-InfRing Replacement Targets

The first likely replacement targets are:

| Storm-native mechanism | Long-term direction |
| --- | --- |
| Decomposition helper | InfRing task decomposition primitive |
| Action receipt table | InfRing-compatible receipt emission and verification |
| Audit log | Receipt-backed event history |
| Value policy execution | Deterministic policy execution where practical |
| Contribution provenance records | Provenance receipts |
| Originality and rights checks | Rights evidence receipts and validation signals |
| Ledger event records | Economic receipts and reconciled ledger state |
| Dataset source records | Data provenance receipts |
| Project version and fork records | InfRing versioning/fork subsystem |
| Trust scoring for incoming network data | Local validation plus node and contributor reputation |

Storm may still keep product-facing projections of these records for UI and reporting. The phased-out part is the native authority mechanism, not the product's ability to show useful state.

## MVP Implication

The first Storm implementation should not depend on InfRing.

It should, however:

- Keep contribution records append-oriented.
- Keep ledger events explicit.
- Keep provenance attached to artifacts.
- Keep originality, similarity, and rights-review evidence structured enough to emit receipts later.
- Make state transitions auditable.
- Separate policy decisions from UI presentation.
- Keep subsystem contracts explicit so native providers can later be replaced by InfRing providers.
- Avoid hiding critical authority in frontend code.
- Preserve enough event history to later emit receipts.
- Keep project and task structures compatible with future InfRing task decomposition receipts.
- Keep project lineage, forks, and exported versions structured enough to map into a future InfRing versioning/fork subsystem.
- Keep any Storm-owned decomposition helper behind an adapter boundary so it can be replaced or merged with InfRing.
- Keep action receipt IDs readable while preserving structured fields and hashes for later InfRing mapping.
- Track which native mechanisms have future InfRing replacements and avoid hard-coding them as permanent authority.

## Open Questions

- What InfRing v2 primitives will be stable enough for Storm to depend on?
- What is the minimal Storm receipt format?
- Which Storm events must be receipt-backed first?
- Which Storm-native mechanisms should be phased out first?
- What interface boundaries make native-to-InfRing replacement safe?
- Does InfRing need a generic versioning/fork subsystem, and what is its minimal primitive set?
- Does InfRing need rights evidence receipts or a rights validation primitive?
- What Storm task fields must map to InfRing task decomposition outputs?
- How should applet constraints be passed into InfRing decomposition?
- What is the migration path from Storm-owned decomposition helpers to InfRing-backed decomposition?
- How should Storm map users to network nodes?
- Can one user operate multiple nodes?
- Can one node represent a group?
- How should ledger events reconcile across nodes?
- What data remains local by default?
- What data can be shared across the Protheus network?
- How should Storm handle offline contribution and later network reconciliation?
