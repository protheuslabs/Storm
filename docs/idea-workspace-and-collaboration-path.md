# Idea Workspace And Collaboration Path

Storm should work for people before it works for any marketplace. The first value
is making ideas usable.

This document defines the minimum practical path for moving from raw idea to
collaborative execution.

## Core Principle

Every project starts as a structured idea and can remain solo until the owner
chooses to expand it.

- Start with structure, not hype.
- Start private by default, then share by design.
- Start with manual collaboration (owner-controlled invites), then add
  algorithmic matching only where project/task decomposition is clear.

## Phase 0: Idea Workspace (MVP)

The owner records an idea capsule with enough structure to reduce drift.

1. Create an idea capsule with title, summary, constraints, and target outcome.
2. Track optional tags, assumptions, and notes.
3. Add initial task hints or a rough plan.
4. Work in a private drafting mode where the owner can contribute and iterate
   alone.

This phase is not a marketplace yet. It is idea capture, clarification, and
personal execution infrastructure.

## Phase 1: Invite-Based Collaboration

Collaboration scales up without opening a public matching surface first.

1. Create a project from the idea capsule (or keep it in draft form).
2. Set access policy:

   - private (owner only),
   - invite-only, or
   - open (future phase).

3. Send explicit invite links/approvals to collaborators.
4. Decompose work into tasks manually.
5. Contributors claim and complete tasks in normal Storm workflow.

This keeps trust boundaries simple and prevents accidental crowding-in until the
project is ready.

## Phase 2: Matching-Based Collaboration (Later)

Matching is introduced only after projects can provide stable task contracts.

1. Tasks have clear acceptance criteria and fixed expected value.
2. The project has stable decomposition structure and audit trail.
3. Matching logic can suggest candidates.
4. Owners still retain opt-in controls.

Without these conditions, matching is likely to produce low-quality claims,
disputes, and avoidable review overhead.

## Applet Coupling

This model should apply across applets.

- Story Forge starts with idea capsules (story concepts, premise, setting,
  constraints).
- The same source structure feeds Story Forge-specific task templates.
- The applet can stay narrow: it does not need to solve matching policy; it
  needs good decomposition support and review flows.

## MVP Implication

- Idea scaffolding is in-scope for early UX.
- Invite-only collaboration and project/private visibility are in-scope for initial
  trust design.
- Automatic matching is explicitly future phase, outside the first manual proof
  loop.

## Open Questions

- Should every idea automatically start private, or can users choose defaults by
  applet?
- What minimum fields are required before an idea can be converted to a project?
- What is the owner-side workflow for declining, re-inviting, or removing invitees?
- What event records are required to prove contribution quality when an invitee
  later brings on further collaborators?
- When should matching become visible at applet level?
