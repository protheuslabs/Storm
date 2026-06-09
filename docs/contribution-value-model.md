# Contribution Value Model

Storm needs a system that calculates value based on contributions.

This is one of the core primitives. The system cannot simply say "everyone contributed" and split value equally. It also cannot recreate the corporate model where a hidden authority decides what everyone deserves. Storm needs transparent, versioned value policies that convert verified contribution records into explainable allocations.

## Core Thesis

Value should flow to the people whose contributions created, improved, validated, coordinated, or enabled the result.

The calculation should be:

- Visible before contribution when possible.
- Based on concrete records.
- Explainable after allocation.
- Versioned by policy.
- Contestable through disputes.
- Resistant to gaming.
- Conservative before provenance is mature.

## MVP Rule

The MVP should not use an opaque algorithm to calculate what contributors deserve.

The first version should use simple direct task value:

1. A task has a visible value before it can be claimed.
2. A contributor accepts that value by claiming the task.
3. Review determines whether the work satisfies the acceptance criteria.
4. Approval creates a contributor payout allocation.
5. Reviewer rewards, platform fees, and adjustments are shown separately.

This is less ambitious than the long-term Storm vision, but it is the right starting point. If contributors cannot trust simple task payouts, they will not trust residual value, AI data attribution, or network-governed allocation.

## Value Layers

Storm should eventually calculate value across several layers.

### Direct Task Value

Direct value is the amount attached to a task before work starts.

Examples:

- Write a scene draft for `$120`.
- Perform continuity review for `$40`.
- Create a character profile for `$75`.
- Fix a bug for `$150`.

Direct task value should be the MVP's primary economic mechanism.

### Review Value

Reviewers create value by validating quality and preventing bad work from entering the project.

Reviewer compensation should account for:

- Review difficulty.
- Required expertise.
- Speed.
- Accuracy over time.
- Dispute reversal history.
- Risk of the reviewed task.

Review should never become rubber-stamping. Reviewer rewards should depend on accountable review outcomes.

### Coordination Value

Coordination work can create real value.

Examples:

- Breaking a vague project into executable tasks.
- Clarifying acceptance criteria.
- Resolving dependency conflicts.
- Merging accepted work into a coherent artifact.
- Resolving disputes.

Coordination value should be introduced after Storm can distinguish useful coordination from vague management theater.

### Upstream Value

Some contributions matter before task execution begins.

Examples:

- A creative seed that becomes a project.
- Research that shapes the project.
- A decomposition plan that makes execution possible.
- A reusable template or rubric.

Upstream value must be handled carefully. Storm should reward useful origin work without letting vague ideas tax execution forever.

### Residual Value

Residual value routes downstream value back to earlier contributors when later success depends on their work.

Examples:

- A story becomes valuable after publication.
- A project spins out into a business.
- A patent uses crowd-created invention work.
- A software component becomes reused across projects.

Residual value should not ship until Storm has strong provenance, legal wrappers, dispute handling, and contribution weighting.

### AI Data Value

If AI systems train on Storm or Protheus Labs ecosystem data, value should remain traceable where possible.

AI data value may use:

- Direct attribution when source influence is knowable.
- Dataset pools when exact influence cannot be proven.
- Domain pools for broad capability value.
- Weighted pools when quality, uniqueness, or usage differs.

AI data value should connect to the same contribution records and value policies as non-AI value.

## Policy-Based Calculation

Storm should treat value calculation as a versioned policy, not as hidden product logic.

A value policy defines:

- Which contribution types are eligible.
- Which value event is being allocated.
- Which weights or caps apply.
- Which review or dispute outcomes affect allocation.
- Whether the allocation is direct, residual, pooled, or manual.
- Which explanation fields must be shown to users.

Policy versioning matters because contributors must know which rules governed their work.

## Candidate Weight Factors

Later value policies may consider:

- Contribution type.
- Accepted quality.
- Difficulty.
- Estimated effort.
- Actual usefulness.
- Originality.
- Scarcity of required skill.
- Dependency importance.
- Downstream usage.
- Reviewer confidence.
- Dispute outcome.
- Timeliness.
- Reliability history.
- Risk or liability.
- Degree of replacement difficulty.
- Whether the contribution became part of the accepted artifact.

These factors should be explicit and domain-specific where necessary. A Story Forge line edit should not be valued the same way as a Code Forge security fix or an Invention Forge prototype test.

## Basic Allocation Shape

A future generic calculation can look like this:

```text
allocatable_value = value_event.amount - reserved_fees - required_reserves

contribution_score =
  base_weight
  * quality_multiplier
  * difficulty_multiplier
  * usefulness_multiplier
  * policy_adjustments

contributor_allocation =
  allocatable_value
  * normalized_contribution_score
```

This is not a final formula. It is a placeholder shape that keeps the model understandable:

1. Define the value being allocated.
2. Identify eligible contributions.
3. Score those contributions under a visible policy.
4. Normalize scores into allocations.
5. Record explanations in the ledger.

## Explanation Requirement

Every calculated allocation should produce an explanation.

An explanation should answer:

- What value event was allocated?
- Which policy version was used?
- Which contribution records were considered?
- Which contribution records were excluded?
- What weights, caps, or multipliers applied?
- What dispute or review outcomes affected the result?
- What amount was allocated and why?

If Storm cannot explain an allocation, it should not automate it.

## Guardrails

Contribution value calculation must avoid several failure modes.

### Avoid Black-Box Scores

Users should not see unexplained "value scores." They should see the rules, inputs, and outcomes that produced an allocation.

### Avoid Idea Rent-Seeking

Storm should not let a vague idea capture most of the value from people who did the hard execution work.

Early upstream claims should be capped, time-limited, disputable, or heavily dependent on concrete downstream use.

### Avoid Execution Erasure

Storm should not over-romanticize origin work. Execution, review, coordination, and refinement often create most of the practical value.

### Avoid Equal Split By Default

Equal splits can be fair in small groups that explicitly choose them. They are not a general model for a large project marketplace.

### Avoid Retroactive Rule Changes

Policy changes should not retroactively alter allocations unless the old policy explicitly allowed that governance path.

### Avoid Hidden Manual Overrides

Manual adjustments may be necessary, especially for disputes, but they must create ledger entries with explanations and authority records.

### Avoid Perverse Optimization

If a metric becomes valuable, people will optimize for it. Value policies should be audited for gaming, collusion, fake work, inflated difficulty, and circular review.

## Story Forge Example

Story Forge can start with direct task value:

- Scene draft task: fixed contributor payout after approval.
- Line edit task: fixed contributor payout after approval.
- Continuity review: fixed reviewer or contributor payout.
- Character profile: fixed payout if accepted into project materials.

Later Story Forge can test limited upstream and residual value:

- A creative seed receives a small capped upstream allocation if it becomes a funded project.
- A worldbuilding entry receives future value only if it becomes accepted canon or is reused by downstream story tasks.
- A plot outline receives downstream weight if later scenes explicitly depend on it.
- Reviewers earn value and reputation when their decisions survive later audit or dispute.

The first Story Forge version should keep this conservative. It should prove that contributors trust visible task payouts before attempting story royalties.

## Relationship To The Ledger

The contribution value model decides how value should be allocated.

The value ledger records what allocation actually happened.

The ledger should reference:

- Value event.
- Value policy version.
- Contribution records.
- Calculation result.
- Explanation.
- Dispute or manual adjustment records.

The ledger is the economic history. The value policy is the rule that produced part of that history.

The value policy engine should remain a separate subsystem from review, ledger recording, and external payments. Other systems should request allocation results and consume explanations; they should not embed hidden payout formulas inside workflow or payment code.

## Relationship To InfRing

In the endgame, value calculation may rely on InfRing primitives for:

- Receipt-backed contribution records.
- Deterministic policy execution.
- Task decomposition provenance.
- Local validation of incoming claims.
- Network-verifiable ledger events.

Storm should not wait for InfRing to begin value modeling. It should start with explicit task values and structured events, then migrate calculation and verification to stronger primitives later.

If InfRing later provides deterministic policy execution or stronger receipt-backed value verification, Storm's native value calculation should become a product-facing policy layer over that primitive rather than a competing authority mechanism.

## Open Design Questions

- What is the first formal value policy version?
- Should the MVP store value policy records even if the rule is simple?
- Which contribution types can receive value before residual compensation exists?
- When should coordination work be paid directly versus rewarded through reputation?
- How should Story Forge cap creative seed value?
- How should downstream value dilute across dependency chains?
- How should rejected or partially used contributions be valued?
- How much value should reviewers receive relative to executors?
- When should value policies be applet-specific?
- What authority can change a value policy before and after the release switch?
