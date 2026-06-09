# AI Training Provenance

AI makes Storm's value thesis more urgent.

If AI systems are trained on people's work and the resulting systems create value, the original contributors usually receive no compensation. Storm should take the opposite position: AI may be allowed to train on Storm data, and later on approved data from the broader Protheus Labs ecosystem, but source provenance should remain traceable enough for contributors to receive a share of value when their work materially contributes to downstream value.

## Core Principle

Training access should not erase attribution.

Storm can allow data to be used for AI training while still preserving:

- Who created the source work.
- What project, task, idea, or contribution it came from.
- Which dataset included it.
- Which model or AI system trained on it.
- Which downstream AI product, output, or value event used it.
- How compensation was calculated when value can be attributed.

## Why This Matters

AI can turn millions of people's labor, writing, designs, code, research, reviews, and judgments into model capability. Without provenance and compensation, this becomes another form of value extraction.

Storm's model can be different:

- Contributors create work.
- Storm records provenance.
- AI systems can train on approved data.
- Training and usage events are logged.
- Downstream value is connected back to source contributions where possible.
- Contributors receive compensation when their data creates attributable value.

## Traceability Levels

Perfect attribution from a trained neural model back to a specific source may not always be technically possible. Storm should still preserve traceability at multiple levels.

### Source Traceability

The system knows the original contribution:

- User.
- Project.
- Task.
- Submission.
- Review.
- Idea.
- Creative seed.
- Research input.

### Dataset Traceability

The system knows which data was included in a training or fine-tuning dataset:

- Dataset id.
- Source records.
- Inclusion rules.
- License terms.
- Data transformations.
- Time included.

### Training Traceability

The system knows which model training or fine-tuning run used which dataset:

- Model id.
- Training run id.
- Dataset version.
- Training purpose.
- Owning organization.
- Allowed usage scope.

### Output Traceability

When possible, the system connects outputs to sources through:

- Retrieval citations.
- Source-grounded generation.
- Similarity or influence scoring.
- Tool-use logs.
- Prompt and context records.
- Human-labeled attribution.

### Value Traceability

The system records when an AI system creates monetary or measurable value:

- Product revenue.
- Licensing revenue.
- Project value.
- Bounty completion.
- Paid AI output.
- Internal cost savings if treated as compensable.

## Compensation Models To Explore

Storm may need more than one model because AI influence is not always directly traceable.

### Direct Attribution

Use when an AI output clearly references, retrieves, adapts, or depends on specific source records.

### Dataset Pool Allocation

Use when a model trained on a dataset creates value, but exact source-level influence cannot be proven. A portion of value is distributed across the dataset according to contribution weight, quality, uniqueness, or usage.

### Domain Pool Allocation

Use when value comes from a model capability trained on a domain-specific body of work. Value is distributed across contributors to that domain.

### Contribution-Weighted Allocation

Use when some source contributions are more valuable than others based on review quality, downstream usage, uniqueness, or expert validation.

## Protheus Labs Ecosystem

Storm should eventually support provenance for approved data across the broader Protheus Labs ecosystem.

This means Storm's provenance model should not assume that all source data originates inside Storm. It should be able to represent:

- Storm-native contributions.
- External project artifacts.
- Research records.
- Simulation outputs.
- Lab notes.
- Dataset imports.
- AI-generated artifacts with known upstream sources.

## Required Safeguards

- Contributors must understand when their work can be used for AI training.
- Data licenses must preserve attribution and compensation rules.
- Sensitive or private data must not be included without explicit permission.
- Training datasets must be versioned.
- Source records must not be silently stripped from datasets.
- Training datasets should pass originality and rights checks before use.
- AI outputs submitted back into Storm should be checked for source laundering or close similarity to protected works.
- Revenue allocation rules must be visible before data is used.
- Disputes over source attribution must be supported.

## MVP Implication

The first Storm MVP does not need AI training compensation.

It should, however, record contribution events and artifact provenance cleanly enough that future AI training provenance can be added without rebuilding the platform's economic history.

## Open Problems

- How should Storm measure model value generated from training data?
- What percentage of AI-generated value should flow back to source contributors?
- How should attribution work when many sources influence a model generally?
- How should opt-in, opt-out, or tiered data licenses work?
- How should AI-generated work inherit upstream provenance?
- How should disputes over AI attribution be resolved?
- How should private, confidential, or sensitive project data be excluded?
