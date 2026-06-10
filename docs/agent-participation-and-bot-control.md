# Agent Participation And Bot Control

Storm should eventually support AI agents and automated tools through authorized channels.

The problem is not that agents exist. Agents can help people decompose work, draft, research, test, review, and execute tasks. The problem is undisclosed automation pretending to be a human contributor, reviewer, or project participant.

Storm needs a subsystem that distinguishes:

- Human work.
- Human work with ordinary tools.
- Human-directed AI assistance.
- Authorized agent execution.
- Unauthorized bots pretending to be humans.

## Core Principle

Agents can participate, but they must not lie about what they are.

Storm should allow automation when:

- The task permits it.
- The agent is identified.
- The responsible user or organization is known.
- The execution mode is disclosed.
- The work can be reviewed under the right standard.
- Receipts or logs preserve enough evidence.

Storm should treat undisclosed automation as a trust violation when it affects payout, reputation, review, rights, or governance.

## Why This Matters

Storm's value model depends on knowing who or what did the work.

If unauthorized bots can pose as humans:

- Reputation becomes fake.
- Review quality can be gamed.
- Payouts can be farmed.
- Human-only tasks become meaningless.
- Project owners cannot set real expectations.
- Rights and originality checks become harder.
- AI-generated work may enter projects without provenance.
- Network governance can be attacked by fake participants.

Storm should not become anti-agent. It should become anti-deception.

## Execution Modes

Every task can eventually declare allowed execution modes.

Suggested modes:

- Human-only.
- Human with tools.
- Human-directed AI assistance.
- Authorized agent execution.
- Mixed human and agent team.
- Agent-only allowed.

The execution mode should be visible before claim and recorded on submission.

## Authorized Agent Channel

An authorized agent should have:

- Agent id.
- Responsible user id.
- Owning organization or project if applicable.
- Allowed scopes.
- Allowed project or task types.
- Tool permissions.
- Data access permissions.
- Execution receipts or logs.
- Revocation status.

An agent should not be able to silently inherit all authority from a human account. Delegation should be explicit and scoped.

## Human Accountability

Even when an agent executes work, a responsible human or organization should be accountable for:

- Claiming or authorizing the task.
- Data the agent accessed.
- Licenses and source material used.
- Submission quality.
- Rights and originality violations.
- Disputes or reversals.
- Payout destination.

Storm can recognize agent work without pretending the agent has human legal responsibility.

## Detection And Controls

Possible controls:

- Execution-mode attestation at claim or submission.
- Task-level automation policy.
- Agent registration and scoped tokens.
- Device, session, and behavior risk signals.
- Rate limits.
- Browser or API channel distinction.
- Review of suspicious activity.
- Watermark or metadata checks where useful.
- Similarity checks for AI-generated or templated submissions.
- Proof-of-human checks only for high-risk human-only tasks.
- Delayed payouts for suspicious automation patterns.

Detection should be risk-based. Storm should avoid turning every contributor into a surveillance target.

## Review Implications

Reviewers should know when automation was used if it affects evaluation.

Examples:

- A story task may allow AI drafting only if the contributor substantially edits and discloses it.
- A code task may allow an agent to generate a patch, but tests and review still matter.
- A research task may allow AI summarization but require cited sources.
- A governance task may require human-only participation.
- A rights review may need to know whether an agent used external source material.

Execution mode should become part of the review record when relevant.

## Reputation Implications

Storm should not let users farm human reputation by secretly delegating everything to bots.

Possible reputation handling:

- Human-only reputation for verified human work.
- Agent-assisted reputation for disclosed assisted work.
- Agent performance metrics tied to an agent id.
- Responsible-user reliability affected by agent outcomes.
- Penalties for undisclosed automation on restricted tasks.

This lets Storm reward good use of agents without corrupting human trust signals.

## Payment Implications

Task payment rules should specify whether agent work is eligible.

Possible policies:

- Human-only tasks reject undisclosed or agent-submitted work.
- Agent-assisted tasks pay the responsible user or organization.
- Agent-only tasks pay according to project policy.
- Unauthorized automation can hold or void payout.
- Repeated deception can affect reputation and access.

The ledger should record payout effects through explicit entries, not hidden flags.

## Relationship To Rights And Provenance

Agent work still needs provenance.

Storm should record:

- Which agent participated.
- Which human or organization authorized it.
- Which sources or datasets it used when known.
- Which model or tool family was used when relevant.
- Whether the task allowed that execution mode.
- Whether originality or rights checks were triggered.

Agents can be powerful laundering tools if provenance is weak. Bot control, rights enforcement, AI provenance, and audit receipts should reinforce each other.

## Relationship To InfRing

Long term, InfRing may help with:

- Agent identity.
- Scoped delegation.
- Tool permissions.
- Execution receipts.
- Local validation of agent claims.
- Proof-carrying task execution.
- Revocation and trust signals.
- Node-level policy enforcement.

Storm can start with native agent authorization records, then map mature pieces to InfRing primitives when available.

## MVP Implication

The first MVP does not need sophisticated bot detection.

It should still prepare by:

- Defining task terms around automation disclosure.
- Recording contributor attestations.
- Preserving submission metadata.
- Keeping review and dispute records explicit.
- Avoiding reputation language that assumes all approved work was purely human.

Advanced bot detection, registered agents, and execution receipts should come later.

## Open Questions

- Which tasks should be human-only by default?
- Which tasks should allow AI assistance by default?
- What level of AI disclosure is required at submission?
- How should Storm distinguish normal tools from agent execution?
- Should agents have their own public profiles?
- Can an agent earn reputation, or only the responsible user?
- How should payout work for agent-executed tasks?
- What proof is required before accusing a user of unauthorized bot use?
- Which agent execution records should become InfRing receipts?
- How should Storm avoid over-surveilling honest contributors?
