# Core Workflows

## 1. Create Project

1. Project owner creates a project.
2. Project owner defines the goal, budget, context, and desired outcome.
3. Project enters draft state.
4. Project owner creates or imports tasks.
5. Project is opened when enough tasks are ready to claim.

For Story Forge, the project owner defines premise, genre, format, tone, target audience, canon notes, and target artifact.

## 1A. Solo Idea Workspace

1. The owner writes a structured idea capsule with goal, context, constraints, and desired outcome.
2. The owner refines the capsule in private draft mode and may create draft tasks.
3. The owner can complete early tasks themselves before any invitees join.
4. The project remains private until the owner explicitly opens it.

## 1B. Invite-Based Collaboration

1. The owner converts a private idea capsule into a draft project.
2. The owner chooses access mode: private, invite-only, or open.
3. Invitees join through explicit invitations only.
4. Owner can revoke access and pause contribution for the project.

## Future: Idea To Project

1. User records an idea, problem, suggestion, or goal.
2. The owner can choose to refine alone before sharing.
3. Other users clarify, decompose, research, or fund it after explicit access is enabled.
4. Storm tracks useful contribution events.
5. The idea becomes a project when it has enough clarity, ownership, funding, or invited contributors.
5. Any residual attribution rules are resolved before paid project work begins.

In MVP, this is staged:

- Idea capture and private refinement are in scope.
- Invite-based project launch is in scope.
- Broad contributor matching is future scope, after task quality and policy are stable.

## 2. Create Task

1. Project owner or coordinator creates a task.
2. Task receives title, description, acceptance criteria, value, estimated effort, skills, dependencies, and deadline.
3. Storm validates that the task has enough information to be claimed.
4. Task enters open state.

For Story Forge, tasks may include premise refinement, chapter outline, scene draft, character profile, dialogue pass, line edit, lore entry, or continuity review.

## Future: Decompose Project Into Task Candidates

1. User enters project goal and applet-specific constraints in the decomposition UI.
2. Backend temporary decomposition helper or future InfRing adapter generates task candidates.
3. UI displays candidates with title, description, acceptance criteria, dependencies, and rationale.
4. User edits, accepts, rejects, splits, merges, or reorders candidates.
5. Accepted candidates become draft tasks.

The UI owns review and interaction. The backend owns decomposition logic and candidate validation.

## 3. Claim Task

1. Contributor browses open tasks.
2. Contributor reviews scope, acceptance criteria, payout, and deadline.
3. Contributor claims the task.
4. Task moves to claimed or in progress.
5. Claim rules prevent indefinite task squatting.

## 4. Submit Work

1. Contributor completes the task.
2. Contributor submits work artifacts, notes, and evidence.
3. Task moves to submitted.
4. Review request is created.

## 5. Review Work

1. Reviewer inspects the submission against acceptance criteria.
2. Reviewer approves, rejects, or requests changes.
3. Reviewer must provide notes for rejection or requested changes.
4. Review decision updates task status.
5. Reviewer reputation is updated after final outcome.

## 6. Request Changes

1. Reviewer identifies specific gaps.
2. Contributor receives change request.
3. Contributor updates the submission.
4. Task returns to submitted for review.

## 7. Approve And Pay

1. Work is approved.
2. Task value is allocated to contributor, reviewer, and platform fee according to the task's payout rules.
3. Ledger records the allocation.
4. Task moves to approved, then paid once payout is complete.

## 8. Dispute Rejection

1. Contributor disputes a rejection.
2. Dispute references the task, submission, acceptance criteria, and review decision.
3. Resolver reviews the record.
4. Resolver upholds rejection, approves work, or requests changes.
5. Contributor and reviewer reputation are updated according to outcome.

## 9. Complete Project

1. Required tasks are approved or canceled.
2. Project owner marks project complete.
3. Final ledger summary is generated.
4. Contributors receive final reputation updates.

## Workflow Rules To Decide

- Can multiple contributors compete on the same task, or does a claim reserve it?
- Can reviewers be paid for rejected work reviews?
- Can a project owner override reviewer decisions?
- How long can a task stay claimed with no activity?
- How are partial completions handled?
- Can contributors propose new tasks?
- When should an idea become a project?
- Which contribution events deserve payout, reputation, or residual attribution?
