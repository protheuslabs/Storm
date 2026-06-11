# Open Questions

## Product

- What is the minimum applet contract every project type must implement?
- Which applet concepts belong in Storm core only after multiple applets need them?
- How many applets can exist before the core project loop is proven?
- Should Story Forge be limited to one initial format, such as short stories or serialized fiction?
- Which story task types should ship first?
- How should Story Forge represent canon in the MVP?
- How much planning metadata should be in MVP versus a future Delivery Forge applet?
- What is the first project category Storm should support?
- Should Storm start with software projects, creative projects, operational tasks, research tasks, or another niche?
- Who creates tasks in the first version: project owners, Storm staff, AI assistance, or the crowd?
- Can contributors propose tasks that a project owner funds later?
- Should tasks be exclusive claims or open competitions?
- Should contributors be allowed to claim multiple tasks at once?
- Should ideas exist before projects, or should all early ideas become draft projects?
- What is the minimum idea capsule schema needed for solo-first work?
- What access states are required for MVP (private, invite-only, open)?
- When should a project transition from private to invite-only to broader matching?
- Should creative seeds be modeled separately from ideas?
- What is the first useful version of a recursive container model?
- Should microtasks be a real MVP feature or a later optimization?
- How small can tasks become before review overhead destroys the economics?

## Versioning And Forks

- How much GitHub-like workflow should Storm expose directly?
- Should project forks exist before groups and residual value are mature?
- What is the first useful version of project lineage in the MVP?
- How should merge proposals work for non-code artifacts?
- How should applets define their own merge semantics over shared version primitives?
- Does InfRing need a generic versioning/fork subsystem?
- What should a version node, fork record, lineage edge, and merge decision contain?
- How should upstream value policies propagate through forks?
- Can a fork reject future parent governance while preserving past obligations?
- Should private forks be allowed, and what provenance becomes public if they later create value?

## Groups And Alliances

- When should Storm introduce persistent groups?
- Can groups own projects and ledger balances?
- What governance models should groups support first?
- Should groups be able to seed child groups or projects?
- Should parent groups receive residual value from child groups?
- How should group leaders be selected, challenged, or removed?
- Should Storm provide preset group templates?
- What lifecycle stages should adaptive groups support?
- Should groups automatically add internal divisions as they grow?
- How should public pledge demand convert into a group, alliance, or project?
- What checks and balances are required before group funds or residuals exist?

## Review

- Who can become a reviewer?
- Are reviewers paid, reputation rewarded, or both?
- Should high-value tasks require multiple reviewers?
- Should project owners be allowed to review their own tasks?
- What happens when reviewer and project owner disagree?
- What review evidence is required for rejection?

## Payments

- Is task value funded upfront, after approval, or by project milestones?
- Should Storm hold funds in escrow?
- What platform fee is required to operate sustainably?
- How are payment processing fees shown?
- How are refunds handled?
- How are partial payouts handled?
- Should residual compensation exist at all in the first public product?
- How should contribution weight be calculated?
- How should residual value decay or dilute downstream?
- How are legacy ideas defined?

## Contribution Value

- What is the first formal value policy version?
- Should the MVP persist value policy records even if payouts are fixed by task?
- Which value factors should be visible before a contributor claims a task?
- How should Storm value coordination work without rewarding vague management?
- How should Story Forge cap creative seed value?
- What contribution types are eligible for direct payment, reputation only, residual value, or no value?
- When should value policies be platform-wide versus applet-specific?
- How should contributors dispute a calculated allocation?
- What evidence is required to increase or reduce a contribution's weight?
- How should Storm prevent task splitting, circular review, and fake dependencies from gaming the value model?

## Reputation

- What reputation dimensions matter most at launch?
- Should reputation decay over time?
- Should reputation be task-category specific?
- How are abandoned claims penalized?
- How are successful disputes reflected?
- How does Storm prevent review rings and fake work?
- How should human-only, agent-assisted, and agent-executed work affect reputation differently?
- Should idea origination affect reputation?
- Should research accuracy affect reputation separately from execution quality?

## Agent Participation And Bot Control

- Which tasks should be human-only by default?
- Which tasks should allow disclosed AI assistance by default?
- What disclosure is required when a user uses an AI agent?
- What counts as an unauthorized bot pretending to be human?
- Should authorized agents have public profiles?
- Can agents earn reputation, or only responsible users?
- How should payouts work for agent-executed tasks?
- What evidence is required before penalizing suspected bot use?
- How can Storm detect automation without over-surveilling contributors?
- Which agent authorization or session records should become InfRing receipts?
- How should invite-only projects expose agent participation in policy and audit records?

## Intellectual Property

- How should Storm represent idea provenance without overclaiming legal ownership?
- How should Storm represent creative seed provenance?
- How should contributors license or assign work?
- Can a project fork an idea while preserving upstream credit?
- What counts as plagiarism inside Storm?
- Should AI concept matching be used for discovery, IP protection, or both?
- What external corpora should originality checks compare against first?
- How should rights checks handle private submissions without exposing them?
- When should a similarity match hold payout, block merge, or only require reviewer attention?
- How should Storm distinguish inspiration, permitted derivative work, fair use, and infringement risk?
- What evidence is required before penalizing a contributor for plagiarism?
- How should repeated plagiarism affect reputation?
- What identity checks are justified for preventing duplicate accounts?

## AI Training And Data Provenance

- Should Storm data be AI-trainable by default, opt-in, or licensed by project?
- How should Protheus Labs ecosystem data connect to Storm provenance?
- What source metadata must be preserved in every training dataset?
- How should AI training runs be logged?
- What counts as value generated from AI training?
- How should value be attributed when exact source influence cannot be proven?
- Should compensation use direct attribution, dataset pools, domain pools, or a hybrid?
- How should AI-generated artifacts inherit upstream provenance?
- What percentage of AI-generated value should flow to source contributors?
- How should contributors dispute missing or incorrect AI attribution?
- What data should be excluded from training even if it exists inside Storm?

## Governance And Disputes

- Who resolves disputes at launch?
- What evidence is required for a dispute?
- Can a contributor appeal a dispute outcome?
- Can a reviewer appeal reputation penalties?
- Should dispute outcomes be public, private, or partially visible?

## Ownership And Legal Structure

- What does it mean for everyone who contributes to have rights without creating collective deadlock?
- Which rights should contributors receive automatically?
- What legal structures can prevent patents or businesses from withholding value?
- How should a Storm-created business route revenue back to contributors?
- How should forks, mergers, and spinouts preserve upstream value rights?
- How should Storm handle contributors who want attribution but not legal ownership?
- How should Storm handle contributors who want payment but no ongoing rights?
- Should Protheus Labs receive a permanent protocol-origin allocation?
- How can Protheus Labs collect origin value without retaining control?
- What legal wrapper is needed before a release switch?

## Release Switch

- What critical mass threshold should trigger release-switch planning?
- What criteria must be met before Storm can grow beyond direct organizational control?
- Which powers should Protheus Labs have before release?
- Which powers must Protheus Labs lose after release?
- How should emergency intervention work without recreating hidden control?
- How should protocol changes be approved after release?
- How should the system handle hostile capture attempts?

## Legal And Compliance

- Are contributors independent contractors, sellers, or something else?
- What terms are needed before paid work begins?
- How are intellectual property rights assigned or licensed?
- What jurisdictions will the MVP support?
- What tax reporting obligations apply?
- What worker classification risks exist?

## Technical

- What stack should be used for the first implementation?
- Should the first implementation be a monolith?
- What subsystem contracts should exist before implementation starts?
- Which modules need provider interfaces from day one?
- How strict should subsystem data ownership be inside the first monolith?
- What event format should subsystems emit?
- Should workflow orchestration call subsystem contracts directly, or should applets compose workflows?
- What should the first audit/event bus look like inside a monolith?
- What auth provider should be used?
- What payment provider should be used?
- What artifact storage is needed?
- What artifact records need hashes or immutable references from day one?
- What events must be audit logged from day one?
- Should the database model reserve room for ideas, groups, and contribution events even if UI hides them?
- What provenance fields must be captured from day one to support future AI training compensation?
- What typed ID prefixes should be canonical?
- What action receipt ID format should be used?
- Should project action indexes be global per project, per applet, or per event stream?
- What hash or digest format should action receipts use?

## Subsystems

- Which subsystem owns contribution events?
- Which subsystem owns workflow orchestration?
- Which subsystem owns artifact provenance versus artifact storage?
- How should privacy and consent rules be enforced across applets?
- When should fraud/risk become separate from reputation?
- What is the first useful search and matching model?
- What constitutes a meaningful board/sprint/release abstraction for non-software work in Delivery Forge?
- Should matching require explicit project quality gates before users are surfaced?
- What integrations matter first: GitHub, Google Docs, Figma, payments, publishing, or InfRing?
- Which policy types must be versioned before paid work begins?
- How should notification and messaging boundaries work without becoming a social network?

## Protheus And InfRing

- Which Protheus products should emit contribution or provenance records into Storm?
- What should Storm know about Lycium, PQTS, Lensmap, and other ecosystem activity?
- What ecosystem data is useful enough to share but sensitive enough to keep local or private?
- How should users consent to cross-product provenance, AI training, and value-routing records?
- How should Storm avoid becoming a centralized data sink for the Protheus ecosystem?
- Which Protheus Labs powers are legitimate early stewardship powers, and which would become hidden control if retained too long?
- Which InfRing v2 primitives will be stable enough for Storm to use?
- What Storm events should become receipts first?
- Which Storm-native mechanisms should be treated as scaffolding from day one?
- Which native mechanisms should be phased out first once InfRing primitives mature?
- What criteria decide that an InfRing primitive is ready to replace a native Storm mechanism?
- How should Storm preserve product-facing projections after native authority moves to InfRing?
- Should versioning and fork lineage be an InfRing subsystem or an app-level Storm subsystem first?
- Which originality and rights enforcement records should become InfRing receipts?
- Which agent participation records should become InfRing receipts?
- When should Storm start using InfRing task decomposition?
- What fields must a Storm decomposition request send to InfRing?
- What fields must an InfRing task candidate return to Storm?
- How should Story Forge constraints shape InfRing decomposition?
- What is the boundary between decomposition UI and backend decomposition providers?
- What decomposition-run records should be stored before InfRing integration?
- How should a single Storm instance transition into a Protheus network node?
- How should node identity map to user, group, project, and legal wrapper identity?
- What Storm data should remain local by default?
- What Storm data can be shared as proof-carrying signals?
- How should Storm validate incoming work, reputation, or ledger signals from other nodes?

## Future Product Lines

- Is World Eye part of Storm, a separate product, or only a future input layer?
- Is Bolt part of Storm, a separate product, or a later real-world marketplace?
- What safety, legal, and insurance requirements would be needed before real-world bounties?
- Should public problem discovery exist before or after paid digital tasks work?

## Brand And Community

- What tone should Storm use with contributors and project owners?
- How explicit should the anti-middleman positioning be in public copy?
- Should the product emphasize fairness, efficiency, ownership, autonomy, or all of these?
- What community norms should be enforced from the start?
