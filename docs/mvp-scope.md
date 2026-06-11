# MVP Scope

## Goal

Prove that Storm can coordinate crowdsourced projects through small tasks with clear acceptance criteria, review, and transparent payout tracking, while also supporting individuals who start in private idea/workspace mode before inviting collaborators.

The MVP is not a generic freelancer marketplace. It is the first working version of a project model where distributed contributors can collectively execute meaningful work without a company acting as the central owner, manager, and value extractor.

The proposed first project applet is Story Forge: crowdsourced story creation. The MVP can focus on story projects while keeping the underlying Storm model generic.

## In Scope

### Projects

- Create a project.
- Define project objective, description, owner, budget, status, and target outcome.
- Start from a private idea capsule that can later become a full project.
- Add contributors manually by invite.
- View project progress by task status.
- For Story Forge, define story premise, format, genre, tone, audience, canon notes, and target artifact.

### Tasks

- Create tasks manually.
- Define title, description, acceptance criteria, required skills, estimated effort, value, status, dependencies, and deadline.
- Claim an available task.
- Submit work for review.
- Approve, reject, or request changes.
- For Story Forge, support task types such as scene draft, character profile, plot outline, dialogue pass, line edit, and continuity review.

### Contributors

- Create contributor profiles.
- Track claimed tasks, submitted tasks, approved tasks, rejected tasks, and earned value.
- Show basic reputation signals.
- Support owner-only solo workflows before opening collaboration.

### Review

- Assign or allow reviewer claim for submitted tasks.
- Review against acceptance criteria.
- Record reviewer decision and notes.
- Track reviewer accuracy over time.

### Value Ledger

- Record task value.
- Record contributor payout amount.
- Record reviewer reward amount if applicable.
- Record platform fee amount.
- Show transparent payout breakdown.
- Use a fixed visible task-value policy, not dynamic contribution scoring.

### Disputes

- Allow contributor to dispute a rejection.
- Allow project owner or designated resolver to make a final decision.
- Record dispute outcome.

## Out Of Scope For First MVP

- Fully automated AI task decomposition.
- Automated contributor matching.
- Advanced project planning, portfolio views, board management, and automation.
- Linear/Jira/Airtable-style PM workflows and native reporting.
- Complex legal contracting.
- Crypto payouts.
- Multi-currency payout flows.
- Enterprise permissions.
- Sophisticated fraud detection.
- Sophisticated bot or unauthorized-agent detection.
- Public API.
- Mobile apps.
- Advanced governance tokens or voting.
- Fully portable external reputation.
- Automated tax reporting.
- Residual lifetime compensation.
- Algorithmic contribution weighting.
- Idea ownership and downstream royalty calculations.
- Custom group or alliance governance.
- World Eye-style crowdsourced intelligence.
- Bolt-style real-world task bounties.
- Automated originality, IP, or plagiarism enforcement.
- Identity schemes requiring sensitive government identifiers.

## MVP Roles

- Project owner.
- Contributor.
- Reviewer.
- Admin or resolver.

## MVP Task States

- Draft.
- Open.
- Claimed.
- In progress.
- Submitted.
- Changes requested.
- Approved.
- Rejected.
- Disputed.
- Paid.
- Canceled.

## MVP Project States

- Draft.
- Open.
- In progress.
- Completed.
- Paused.
- Canceled.

## Initial Product Constraint

Start with manually created and manually reviewed tasks. Automation can assist later, but the first product must prove the workflow and incentives before relying on automation.

The MVP can allow simple AI assistance disclosure without enforcing advanced bot detection. Later Storm should distinguish human-only, human-assisted, agent-assisted, and authorized-agent task execution.

The MVP can still require contributors to attest that submitted work is original or properly licensed, and it should preserve enough submission provenance to support later originality checks.

The MVP should also use one-time task payout accounting before attempting residual compensation. Residual value is part of the long-term vision, but it depends on a trusted contribution graph, precise ownership rules, and dispute handling that does not exist yet.

The MVP should support crowdsourced projects deeply enough to prove the model, even if it only supports a narrow category of project at first.

Story Forge is the recommended first applet.
