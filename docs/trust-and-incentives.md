# Trust And Incentives

Storm's core product risk is trust. The platform only works if project owners trust contributors, contributors trust review and payout, and reviewers are accountable for decisions.

## Trust Goals

- Contributors should know what is expected before they claim work.
- Project owners should know why work was approved or rejected.
- Reviewers should be rewarded for accurate review, not arbitrary gatekeeping.
- Reputation should reflect verified behavior, not popularity.
- Bad actors should become more expensive to the system over time.
- Upstream contributors should not be erased when later work builds on their useful input.
- AI systems should not be able to absorb contributor work while stripping source attribution.
- Legal owners should not be able to withhold network-created value from contributors.
- Contributors should not be able to pass off another user's work or externally owned work as their own.
- Bots and agents should not be able to impersonate human contributors or reviewers.

## Incentive Problems

### Contributor Squatting

A contributor may claim a task and block others without doing the work.

Possible controls:

- Claim expiration.
- Activity checkpoints.
- Contributor claim limits.
- Reliability penalties for abandonment.

### Low-Quality Submissions

A contributor may submit incomplete or careless work to force review labor.

Possible controls:

- Submission requirements.
- Rejection penalties for repeated low-quality work.
- Minimum reputation for higher-value tasks.
- Review fees charged against task bounty only after basic completeness checks.

### Reviewer Rubber-Stamping

A reviewer may approve low-quality work to earn reviewer rewards quickly.

Possible controls:

- Reviewer accuracy score.
- Random audit of approved work.
- Penalties when later disputes overturn approvals.
- Higher review rewards for higher-risk reviews.

### Reviewer Gatekeeping

A reviewer may reject valid work unfairly.

Possible controls:

- Required rejection notes tied to acceptance criteria.
- Contributor dispute path.
- Reviewer accuracy penalties for overturned rejections.
- Multi-review for high-value tasks.

### Collusion

Contributors and reviewers may coordinate to approve fake or low-quality work.

Possible controls:

- Relationship and repeat-review detection.
- Random second review.
- Risk scoring.
- Delayed payouts for new accounts or high-risk patterns.

### Project Owner Abuse

A project owner may reject acceptable work to avoid payment.

Possible controls:

- Acceptance criteria locked when task is claimed.
- Independent review.
- Escrow or funded task balances.
- Dispute process based on the original task record.

### Upstream Claim Abuse

A user may try to claim residual value from vague, obvious, copied, or low-effort ideas.

Possible controls:

- Require concrete contribution artifacts.
- Limit residual claims for legacy or obvious ideas.
- Weight execution and validation more heavily than vague ideation.
- Require provenance links between upstream work and downstream work.
- Let disputed claims be reduced, capped, or removed.

### Value Calculation Gaming

A user may try to inflate contribution value by exaggerating difficulty, splitting work into unnecessary tasks, creating fake dependencies, coordinating circular reviews, or optimizing for whatever factors the value policy rewards.

Possible controls:

- Start with fixed task values before complex dynamic scoring.
- Make value policies visible before contribution.
- Record allocation explanations.
- Cap upstream and coordination allocations until provenance is mature.
- Audit unusual task splitting, repeated reviewer relationships, and sudden weight changes.
- Version policies so rule changes cannot silently rewrite past allocations.

### Identity And Duplicate Accounts

The old source suggests making duplicate accounts difficult. This matters for fraud and collusion, but sensitive identity requirements create privacy and onboarding risks.

Possible controls:

- Start with email, payment, and device-risk checks.
- Add stronger verification only for high-risk or high-value actions.
- Avoid collecting highly sensitive government identifiers unless legally necessary and operationally justified.

### Unauthorized Bots And Undisclosed Agents

A user may use automation, scripts, or AI agents to claim, complete, review, or influence tasks while pretending the work was done by a human.

Possible controls:

- Task-level execution-mode policy.
- Contributor attestation at claim or submission.
- Authorized agent registration.
- Scoped agent credentials.
- Session, device, API, and behavior risk signals.
- Human-only checks for high-risk task categories.
- Payout holds for suspicious undisclosed automation.
- Separate reputation treatment for human-only, agent-assisted, and agent-executed work.
- Penalties for repeated deception.

### AI Attribution Abuse

A user or organization may try to use Storm data for AI training while avoiding source compensation, or may falsely claim that a valuable AI output depended on their work.

Possible controls:

- Version every training dataset.
- Preserve source records inside dataset manifests.
- Require explicit data-use terms.
- Log training runs and usage scopes.
- Use attribution confidence scores.
- Support disputes over AI attribution.
- Penalize unauthorized dataset exports or provenance stripping.

### Plagiarism And Rights Abuse

A contributor may submit work copied from another Storm user, copied from an external source, generated by AI from a protected source, or incompatible with the project's license and rights rules.

Possible controls:

- Contributor originality and permission attestations.
- AI-assisted similarity search against Storm-native work.
- External corpus, license, and prior-art checks where feasible.
- Applet-specific rights checks for stories, code, designs, datasets, and inventions.
- Rights review workflow with explainable evidence.
- Payout holds or merge blocks for high-risk submissions.
- Appeals for false positives.
- Reputation penalties for repeated bad-faith copying.

### Legal Wrapper Capture

A patent holder, business entity, or project owner may try to use legal title to capture value while ignoring the contribution graph.

Possible controls:

- Require non-withholding legal terms for Storm-created assets.
- Bind legal wrappers to ledger and contribution records.
- Record revenue events against the value ledger.
- Preserve upstream provenance during forks and spinouts.
- Support disputes when legal wrappers fail to route value.

### Fork Provenance Stripping

A user or group may fork a project, dataset, story world, codebase, or invention record and then attempt to remove upstream attribution or value obligations.

Possible controls:

- Preserve parent lineage on forks.
- Require fork receipts or audit records.
- Carry applicable value policies, licenses, and legal-wrapper obligations into fork metadata.
- Show upstream dependency and contribution history in forked projects.
- Dispute or quarantine forks that strip provenance.

### Network Trust Failure

When Storm eventually uses Protheus/InfRing primitives, a node may publish false receipts, unsafe signals, bad provenance, or value claims that other nodes should not trust blindly.

Possible controls:

- Require local validation before adopting network signals.
- Track node reputation by domain and claim type.
- Quarantine suspicious receipts or signals.
- Preserve rollback paths.
- Prefer proof-carrying signals over authority-based trust.

### Release Switch Capture

A release switch can fail if it releases too early, releases too late, or preserves hidden control under another name.

Possible controls:

- Define public release criteria before activation.
- Make Protheus Labs origin allocation explicit and immutable or tightly governed.
- Remove hidden unilateral admin powers after release.
- Require transparent governance for protocol changes.
- Preserve emergency handling without recreating secret central control.
- Audit whether origin value is compensation or extraction.

## Reputation Dimensions

Contributor reputation should not be one score. Useful dimensions include:

- Completion quality.
- On-time delivery.
- Claim reliability.
- Communication clarity.
- Dispute history.
- Skill-specific performance.

Reviewer reputation should include:

- Review accuracy.
- Review speed.
- Decision consistency.
- Quality of notes.
- Dispute reversal rate.

Project owner reputation should include:

- Task clarity.
- Payment reliability.
- Dispute rate.
- Contributor feedback.
- Change request quality.

## Incentive Principle

Every paid or reputation-bearing action should make the system more trustworthy. If an action can extract value without improving work quality, coordination, or validation, it should be redesigned.
