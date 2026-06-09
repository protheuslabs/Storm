# Value Ledger

The value ledger is Storm's economic record. It should make value allocation transparent before and after work is completed.

## Purpose

The ledger answers four questions:

- What value was attached to the task?
- Who created, reviewed, or adjusted that value?
- How was the value split?
- Why did the split happen?

Longer term, the ledger may also answer whether later value depends on earlier ideas, research, decomposition, group seeding, or AI systems trained on traceable source work.

## Ledger Principles

- Economic events should be explicit.
- Contributors should see expected payout before claiming work.
- Platform fees should be visible.
- Reviewer rewards should be visible.
- Adjustments should be explained.
- Important ledger events should be append-only.

## Example Allocation

For a task worth `$100.00`:

- Contributor payout: `$92.00`.
- Reviewer reward: `$3.00`.
- Platform fee: `$5.00`.

This is only an example. Actual allocations need product and business decisions.

## Ledger Event Types

- Task funded.
- Task claimed.
- Submission approved.
- Value event recorded.
- Contribution valuation recorded.
- Allocation explanation recorded.
- Contributor payout allocated.
- Reviewer payout allocated.
- Platform fee allocated.
- Upstream contribution allocated.
- Residual claim created.
- Residual payout allocated.
- Dataset value allocated.
- AI training value allocated.
- AI attribution adjustment.
- Protocol origin allocation.
- Release switch allocation.
- Refund issued.
- Dispute adjustment.
- Manual adjustment.
- Payout completed.
- Payout failed.

## Required Ledger Fields

- Ledger entry id.
- Project id.
- Task id.
- User id when applicable.
- Entry type.
- Amount.
- Currency.
- Direction.
- Source event.
- Explanation.
- Created at.

## Internal Ledger Before External Payments

Storm should model value allocation internally before automating real payouts. This keeps product logic clear and testable.

Payment provider events should reconcile with the internal ledger, not replace it.

## Contribution Value Calculation

Storm needs a contribution value model, but the ledger should not hide that model inside payment plumbing.

The value policy calculates what should happen. The ledger records what did happen.

For the MVP, contribution value should be simple:

- Task value is visible before claim.
- Approved work receives the task's defined contributor allocation.
- Reviewer rewards and platform fees are shown separately.
- Disputes or manual adjustments create explicit ledger entries.

Later versions can introduce policy-based contribution valuation:

- Direct task value.
- Reviewer value.
- Coordination value.
- Upstream creative seed or research value.
- Residual downstream value.
- AI data value.

Every calculated allocation should store the value policy version, eligible contribution records, excluded contribution records, applied weights or caps, and an explanation visible to affected users.

## Residual Value

The old Storm vision includes residual compensation when later work builds on earlier contributions.

This should be modeled as future scope because it requires:

- Creative seed and idea provenance.
- A contribution graph.
- Rules for contribution weights.
- Rules for downstream dilution.
- Legal clarity around ownership and licensing.
- Strong dispute handling.
- Protection against fake upstream claims.

The MVP should use direct task-based allocation first.

## AI Training Value

Storm may allow AI systems to train on Storm data and later approved data from the Protheus Labs ecosystem. If that data contributes to downstream value, the ledger should be able to record compensation back to traceable sources.

AI training value requires:

- Dataset versioning.
- Source-level provenance.
- Training-run records.
- AI value events.
- Attribution methods.
- Dispute handling for source claims.

When exact source attribution is impossible, Storm may need pool-based allocation across a dataset or domain.

## Open Ledger Decisions

- Should task funds be held upfront?
- Should reviewer rewards come from the task value, project owner budget, or platform fee?
- Should the 95% value target include reviewer rewards or only contributor payouts?
- Should platform fees be flat, percentage-based, capped, or variable by risk?
- How should failed payouts be represented?
- How should chargebacks or refunds affect reputation?
- What value policy should govern the first public release?
- Should fixed task payouts still reference a value policy version?
- Which contribution types can receive direct value before residual compensation exists?
- How should coordination work be valued without recreating opaque management?
- When should a contribution create residual value?
- When should a creative seed create residual value?
- How should downstream dilution be calculated?
- How are legacy ideas handled?
- What counts as value generated from AI training?
- Should AI training value use direct attribution, dataset pools, domain pools, or a hybrid?
- What compensation share should source contributors receive from AI-generated value?
- Should Protheus Labs receive a permanent protocol-origin allocation?
- How large should an origin allocation be before it becomes extraction?
- Can an origin allocation be changed after the release switch?
