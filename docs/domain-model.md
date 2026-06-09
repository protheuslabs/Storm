# Domain Model

This document defines the initial product entities. It is not yet a database schema.

## User

A person using Storm.

Fields:

- id.
- name.
- email.
- handle.
- role flags.
- created at.

Relationships:

- May own projects.
- May contribute to tasks.
- May review submissions.
- May resolve disputes.

## Project

A container for coordinated work.

Fields:

- id.
- owner id.
- title.
- description.
- objective.
- budget.
- status.
- target outcome.
- created at.
- updated at.

Relationships:

- Has many tasks.
- Has many ledger entries.
- Has contributors through tasks.

## Idea

An early concept, problem, prompt, or goal that may become a project.

Fields:

- id.
- created by user id.
- title.
- description.
- status.
- visibility.
- created at.
- updated at.

Relationships:

- May become a project.
- May have contribution events.
- May belong to a group.

MVP status:

- Future concept. The first MVP can treat project creation as the starting point.

## Creative Seed

An early idea or creative input intended to grow into work and downstream value.

Fields:

- id.
- created by user id.
- title.
- description.
- source idea id.
- provenance notes.
- status.
- created at.
- updated at.

Relationships:

- May become an idea.
- May become a project.
- May have contribution events.
- May create future residual claims.

MVP status:

- Future concept. MVP can capture project descriptions without modeling creative seeds separately.

## Group

A persistent collaboration unit that can own ideas, projects, members, and governance rules.

Fields:

- id.
- name.
- description.
- visibility.
- member policy.
- governance model.
- created at.
- updated at.

Relationships:

- Has members.
- May own projects.
- May own ideas.
- May seed child groups.

MVP status:

- Future concept. The first MVP can support individual project owners before group ownership.

## Group Membership

A user's relationship to a group.

Fields:

- id.
- group id.
- user id.
- role.
- status.
- joined at.

MVP status:

- Future concept.

## Group Template

A reusable operating pattern for a group or alliance.

Fields:

- id.
- name.
- description.
- governance model.
- default roles.
- lifecycle rules.
- created at.
- updated at.

Relationships:

- May be used by many groups.

MVP status:

- Future concept.

## Group Relationship

A relationship between groups, such as parent, child, sponsor, or alliance member.

Fields:

- id.
- source group id.
- target group id.
- relationship type.
- residual rule id.
- status.
- created at.

MVP status:

- Future concept.

## Legal Wrapper

A legal entity, patent, license, contract, or business structure that represents Storm-created value in external legal systems while preserving contributor value rights.

Fields:

- id.
- wrapper type.
- project id.
- group id.
- legal owner id.
- contribution policy id.
- revenue routing policy id.
- status.
- created at.

MVP status:

- Future concept.

## Network Node

A future Protheus/InfRing node that can participate in Storm coordination with local authority and receipt-backed trust.

Fields:

- id.
- operator user id.
- group id.
- node identity.
- trust profile.
- status.
- created at.

MVP status:

- Future concept.

## Receipt

A future verifiable record of an event, decision, execution, validation, ledger entry, or provenance claim.

Fields:

- id.
- source event type.
- source event id.
- node id.
- receipt hash.
- policy version.
- created at.

MVP status:

- Future concept. MVP events should be structured so they can later emit receipts.

## Pledge

A pre-project signal of funding, preorder demand, volunteer interest, or support.

Fields:

- id.
- user id.
- idea id.
- group id.
- pledge type.
- amount.
- currency.
- notes.
- status.
- created at.

MVP status:

- Future concept.

## Task

A small executable unit of work.

Fields:

- id.
- project id.
- title.
- description.
- acceptance criteria.
- required skills.
- estimated effort.
- value.
- status.
- deadline.
- claimed by user id.
- created at.
- updated at.

Relationships:

- Belongs to project.
- May depend on other tasks.
- Has submissions.
- Has reviews.
- Has ledger entries.

## Task Dependency

A relationship between tasks.

Fields:

- id.
- task id.
- depends on task id.
- dependency type.

## Contribution Event

A record of a useful action that may create value or reputation.

Fields:

- id.
- user id.
- project id.
- task id.
- idea id.
- contribution type.
- source id.
- created at.

Contribution types:

- Idea creation.
- Problem clarification.
- Task decomposition.
- Task submission.
- Review.
- Research input.
- Dispute resolution.
- Funding.
- AI training source.

MVP status:

- Partial. MVP reputation events and ledger entries cover task submissions and reviews. A broader contribution graph can come later.

## Dataset

A versioned collection of source records approved for AI training, fine-tuning, evaluation, retrieval, or analysis.

Fields:

- id.
- name.
- description.
- version.
- license policy.
- inclusion rules.
- created by user id.
- created at.

Relationships:

- Has many dataset source records.
- May be used by training runs.

MVP status:

- Future concept.

## Dataset Source Record

A link between a dataset and a source contribution, artifact, idea, task, submission, review, or external record.

Fields:

- id.
- dataset id.
- source type.
- source id.
- contributor user id.
- transformation notes.
- attribution weight.
- included at.

MVP status:

- Future concept.

## AI Training Run

A record that a model or AI system trained on, fine-tuned on, evaluated against, or otherwise learned from a dataset.

Fields:

- id.
- model id.
- dataset id.
- training purpose.
- usage scope.
- organization id.
- started at.
- completed at.

MVP status:

- Future concept.

## AI Value Event

A record that an AI system generated monetary or measurable value that may be attributable to source data.

Fields:

- id.
- model id.
- training run id.
- project id.
- value type.
- amount.
- currency.
- attribution method.
- created at.

MVP status:

- Future concept.

## AI Attribution Entry

A record linking an AI value event back to source contributors or source records.

Fields:

- id.
- ai value event id.
- source type.
- source id.
- beneficiary user id.
- attribution weight.
- confidence.
- created at.

MVP status:

- Future concept.

## Submission

Work submitted by a contributor for a task.

Fields:

- id.
- task id.
- contributor id.
- artifact links.
- notes.
- status.
- submitted at.

Relationships:

- Belongs to task.
- Has reviews.
- May have disputes.

## Review

A validation decision on a submission.

Fields:

- id.
- submission id.
- reviewer id.
- decision.
- notes.
- created at.

Decision values:

- Approved.
- Rejected.
- Changes requested.

## Dispute

A challenge to a review outcome.

Fields:

- id.
- task id.
- submission id.
- opened by user id.
- review id.
- reason.
- status.
- resolver id.
- outcome.
- created at.
- resolved at.

## Ledger Entry

A transparent record of value allocation.

Fields:

- id.
- project id.
- task id.
- user id.
- entry type.
- amount.
- currency.
- platform fee amount.
- source event.
- created at.

Entry types:

- Contributor payout.
- Reviewer payout.
- Platform fee.
- Refund.
- Adjustment.
- Residual allocation.
- AI data value allocation.

MVP status:

- MVP supports one-time task payouts, reviewer payouts, platform fees, refunds, and adjustments.
- Residual allocation is future scope.

## Reputation Event

A record that changes a user's reputation.

Fields:

- id.
- user id.
- source type.
- source id.
- dimension.
- value.
- reason.
- created at.

Dimensions:

- Quality.
- Reliability.
- Speed.
- Review accuracy.
- Dispute outcome.
- Domain skill.

## Residual Claim

A future record of continuing value rights from earlier contributions.

Fields:

- id.
- source contribution event id.
- beneficiary user id.
- project id.
- idea id.
- claim type.
- weight.
- dilution rule.
- status.
- created at.
- ended at.

MVP status:

- Future concept. This should not be implemented until contribution tracking, ownership rules, and disputes are mature.

## Notification

A message generated by workflow events.

Fields:

- id.
- user id.
- type.
- title.
- body.
- read at.
- created at.

## Open Modeling Questions

- Should project ownership support teams from the start?
- Should task value be fixed, variable, or milestone-based?
- Should review be single-reviewer, multi-reviewer, or risk-based?
- Should submissions support structured artifacts per task type?
- Should reputation be global, skill-specific, project-specific, or all three?
- Should ideas and projects be separate entities from the start?
- Should creative seeds be separate from ideas, or are they the earliest idea state?
- Should every useful action become a contribution event?
- How should residual claims be calculated, diluted, challenged, and ended?
- What is the minimum viable group model?
- How should training datasets preserve source provenance?
- How should AI value events map back to source contributors?
- What legal wrapper structures preserve contributor value rights?
- Which MVP events should be designed to become receipts later?
- How should Storm users, groups, and projects map to Protheus network nodes?
