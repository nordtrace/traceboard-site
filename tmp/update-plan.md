# Proposal: update the TraceBoard Suite product pages

I reviewed all seven HTML files against `changes.txt`. The site already has a strong, credible positioning around traceability, self-hosting, human review, and AI boundaries. The main issue is that several pages now understate the product, while a few claims are explicitly obsolete.

The most important correction is:

> The site currently says that ReqIF is unsupported. TraceBoard Suite 1.4.0 now supports ReqIF import and export, including baseline-scoped export and ReqIF 1.0/1.2 selection.

No files were changed.

---

## 1. Cross-site messaging changes

### Update the product version

The current product level is **TraceBoard Suite 1.4.0**.

Add a consistent release marker in suitable locations:

> TraceBoard Suite 1.4 — Requirements, verification, evidence and controlled engineering change in one connected suite.

Recommended locations:

- `D:\Dev\MyCode\traceboard-site\traceboard-site\index.html`
- `D:\Dev\MyCode\traceboard-site\traceboard-site\traceboard-features.html`
- `D:\Dev\MyCode\traceboard-site\traceboard-site\resources.html`
- potentially the footer or a small “Current release” line

Avoid presenting the version as a guarantee that every feature is available in every deployment unless the deployed environment is confirmed to be running 1.4.0.

### Remove obsolete ReqIF claims

The following type of copy appears in multiple places:

> ReqIF and arbitrary full-fidelity interchange are not supported.

This is no longer accurate. Replace it with a qualified claim:

> ReqIF 1.0 and 1.2 import/export are supported for the implemented TraceBoard exchange model. Import includes preview, schema-aware field mapping and transactional confirmation. Export supports current project data and frozen baseline scope. Cross-tool compatibility should be validated against the customer’s specific DOORS, Jama, Polarion or other ReqIF workflow.

Do not claim universal or lossless interchange. The change log explicitly says that cross-tool validation with Eclipse RMF, ProR and real DOORS/Jama installations has not yet been completed.

### Use more precise AI language

The site currently describes AI conservatively, which is good. It should now also mention:

- deterministic output-quality signals,
- grounded classification handling,
- contradiction detection,
- duplicate assessment removal,
- narrative section and item-coverage checks,
- AI-generated output remaining informational or proposed,
- human review before committing generated assessments.

Recommended positioning:

> TraceBoard combines model-assisted analysis with deterministic safeguards. Generated assessments and narratives are checked for structural completeness, source coverage, duplicate clauses, contradictory status claims and unsupported classification tokens before reviewers decide what enters the engineering record.

Avoid saying AI “validates compliance” or “guarantees correct findings.”

### Promote the product from “proposed” to “available”

The features page currently contains capability inventory-style labels such as `PROPOSES`. Based on the change log, several should now be marked as implemented or described as available:

- ReqIF import
- ReqIF export
- baseline-scoped exchange
- suspect-link workflow
- recycle bin and item restoration
- personal work queue
- deterministic item-quality checks
- audit output-quality signals
- historical test-case snapshots
- evidence timeline
- user management
- baseline-to-test-run workflow

The terminology should be marketing-oriented rather than internal inventory-oriented. Use labels such as:

- `AVAILABLE`
- `BUILT IN`
- `SUPPORTED`
- `OPTIONAL`
- `QUALIFIED`

---

# 2. File-by-file proposal

## `D:\Dev\MyCode\traceboard-site\traceboard-site\index.html`

This should become the primary current-capability page. It should lead with the full suite story rather than mostly describing the older requirements/traceability foundation.

### Hero section

Current positioning around connected engineering is sound. Strengthen it to mention controlled change and verification:

> Requirements are only useful when teams can prove what changed, what it affects and whether it was verified. TraceBoard Suite connects requirements, tasks, tests, risks, hazards, documents, baselines and evidence in one reviewable engineering model.

Suggested supporting copy:

> Import existing requirements, trace relationships across the project, run verification, generate controlled documents and exchange data through supported ReqIF workflows—without giving up ownership of your infrastructure or engineering record.

### Add a “What is new in 1.4” section

Place this after the hero or after the suite overview.

Suggested cards:

#### ReqIF exchange

> Import ReqIF with preview and schema-aware mapping, including common proSTEP-style title and description attributes. Export current project data or a frozen baseline in ReqIF 1.0 or 1.2 format.

Qualification:

> Exchange behavior is defined by the implemented TraceBoard mapping. Validate customer-specific tool compatibility before production migration.

#### Reviewable change impact

> When an item endpoint changes after a relation was reviewed, TraceBoard marks the link as suspect. Reviewers can clear the link with an optional note, preserving reviewer and review-time context.

#### Safer lifecycle management

> Soft-delete preserves items and relations instead of destroying them. The recycle bin supports project-scoped restoration, while delete and restore actions remain visible in the item history.

#### Personal work queue

> My Work consolidates active owned items, pending compliance assessments and pending engineering findings across accessible projects.

#### Historical verification context

> TraceTest captures the test-case title, identifier and description at first terminal execution, so archived runs can retain the procedure that was actually executed even after later edits.

### Update the suite/product cards

The three-product section should explicitly describe the current handoff:

**TraceBoard**

> Model requirements, tasks, tests, risks, hazards, bugs and relations. Use baselines, trace filters, coverage analysis, suspect-link review, item quality checks and change timelines.

**TraceDocs**

> Generate controlled SRS, design, user-manual and test-plan documents from project data and selected baselines. Import Markdown, DOCX and TXT files while retaining source files, provenance and folder hierarchy.

**TraceTest**

> Create verification runs from test plans or baselines, execute Pass/Fail/Blocked workflows, attach evidence and retain execution-time test-case snapshots and result-change history.

### Add the baseline workflow to the main narrative

The change log now supports a clear cross-product marketing story:

> Freeze a baseline in TraceBoard, generate a TraceDocs Test Plan from that baseline, create a TraceTest run directly from the plan, and retain the baseline identifier as run provenance.

This is a compelling differentiator and should be shown as a simple four-step visual:

1. Define and review the engineering model.
2. Capture an immutable baseline.
3. Generate a baseline-scoped Test Plan.
4. Execute and report the corresponding TraceTest run.

### Update FAQ

Add questions:

**Can TraceBoard exchange ReqIF data?**

> Yes. TraceBoard supports ReqIF import with preview and field-mapping controls, and ReqIF export for current project items or frozen baselines. Export supports ReqIF 1.0 and 1.2. Exact data fidelity depends on the source schema and the implemented mapping, so customer tool compatibility should be validated before migration.

**How does TraceBoard protect archived test evidence?**

> At first terminal execution, TraceTest captures the test-case title, short ID and description. Archived runs prefer those execution-time values and indicate when they must fall back to current live values.

**What happens when a traced item is deleted?**

> Items are soft-deleted and hidden from normal views rather than destroyed. Relations and history are preserved, and authorized project members can restore the item from the recycle bin.

**How does TraceBoard identify changed trace links?**

> Relations can become suspect when either endpoint is edited after the relation was last reviewed. A reviewer can clear the suspect state with an optional note, creating a review record.

### Correct deployment language

The deployment section can be strengthened from general self-hosting to concrete operational claims:

> TraceBoard Suite is distributed as a packaged Docker Compose deployment for online or offline installation. The 1.4 deployment documentation includes a first-time installation runbook, OIDC and license configuration, health verification, backups covering database and file volumes, image rollback guidance and migration policy.

Do not claim automatic database rollback. The change log specifically says rollback is image rollback only and migrations are handled uniformly.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\traceboard-features.html`

This is the most important page to update because it already functions as the detailed product capability inventory.

### Replace “ReqIF is not supported”

There are at least two places where this claim appears:

- the “Specific data operations” section,
- the closing evaluation section.

Replace with:

> Supported ReqIF exchange is now available. TraceBoard can preview and import ReqIF documents using schema-aware mapping, and export current or baseline-scoped project data in ReqIF 1.0 or 1.2. This is a defined exchange model, not a promise of arbitrary full-fidelity interchange across every requirements tool.

### Update the differentiator/principle list

The existing “Every link, both directions” principle is strong. Extend it:

> Every link, both directions—and every review state. TraceBoard shows relationships across requirements, tasks, tests, bugs and documents, flags suspect links after endpoint edits and records when a reviewer clears the concern.

Add a new principle:

#### 07 — Preserve the engineering record

> Soft-delete, recycle-bin restoration, item history, evidence timelines and execution-time test snapshots keep the record understandable after change.

Add another:

#### 08 — Exchange without losing control

> Import ReqIF through preview and mapping controls. Export live project or frozen baseline data in ReqIF 1.0 or 1.2, with customer-controlled deployment and explicit compatibility boundaries.

### Update feature categories

The feature page should contain explicit sections for:

#### Traceability and coverage

Include:

- project matrix,
- Tree, Flow and Grid views,
- configurable item/relation/depth filters,
- requirement verification coverage,
- task-mediated verification,
- traceability completeness,
- baseline comparison,
- unfiltered export caveat where applicable.

#### Change governance

Include:

- suspect links,
- review notes and reviewer metadata,
- soft-delete,
- recycle bin,
- restore events,
- evidence timeline,
- deterministic audit ordering.

#### Verification

Include:

- test runs,
- Pass/Fail/Blocked execution,
- result status-change history,
- evidence,
- risk signals,
- execution-time snapshots,
- baseline provenance,
- TraceDocs Test Plan → TraceTest run flow.

#### Data exchange and migration

Include:

- ReqIF import preview,
- schema-aware title/description detection,
- hierarchy/relation synthesis,
- transactional confirmation,
- 100 MB ReqIF upload support through the packaged nginx path,
- ReqIF 1.0/1.2 export,
- live versus baseline scope,
- JSON/CSV/XLSX/PDF/DOCX/Markdown operations where already supported.

Do not turn the 100 MB upload limit into a general claim that every import format accepts 100 MB. Qualify it specifically as the packaged ReqIF/API upload limit.

### Update the “AI that stays accountable” section

Suggested revised copy:

> AI-generated assessments and narratives remain reviewable rather than silently becoming engineering truth. TraceBoard grounds classifications in source data, detects contradictory clause-level assessments, removes duplicate siblings, and exposes output-quality signals when required sections, source-item coverage or consistency findings appear incomplete.

Add the limitation:

> These safeguards improve reviewability and evidence grounding; they do not guarantee semantic correctness or replace qualified engineering judgment.

### Update the standards section

The current standards section is appropriately cautious. Keep the disclaimer that TraceBoard does not certify compliance.

Strengthen the implemented-boundary column to mention:

- clause-oriented assessments,
- evidence-backed audit narratives,
- readiness scoring,
- requirement verification,
- review reasons for contradictory or deduplicated assessments,
- source-grounded classification handling,
- output-quality signals.

Avoid suggesting that all listed standards have equivalent depth. The change log demonstrates specific standard-aware behavior, but not complete certification coverage for every named standard.

### Update pricing/product maturity language

The page currently reads partly like an early capability inventory. Recast it as a mature release:

> TraceBoard Suite 1.4 brings together traceability, verification, controlled documents, baselines, ReqIF exchange, reviewable AI and operational governance in one self-hosted suite.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\traceboard-ai-approach.html`

This page is already one of the strongest pages from a credibility perspective. It should be updated to reflect the new deterministic safeguards.

### Expand the AI pipeline

The current Propose → Validate → Approve → Commit model should be retained, but “Validate” should now have concrete examples:

**Propose**

- audit assessments,
- narrative sections,
- consistency findings,
- optional generated tasks and tests.

**Validate**

- schema and structure checks,
- source-reference grounding,
- classification allow-list enforcement,
- duplicate assessment removal,
- contradictory status detection,
- section completeness,
- item coverage,
- consistency output-quality signals.

**Approve**

> Reviewers inspect proposed assessments, explanations, review reasons and quality signals before deciding what to commit.

**Commit**

> Only accepted results become part of the managed engineering record. Informational output-quality signals do not silently block generation or export.

### Correct the data-operations section

The current statement:

> ReqIF and arbitrary full-fidelity interchange are not supported.

Should become:

> ReqIF import and export are supported through defined TraceBoard mappings. Import includes preview and field overrides; export supports current project or baseline scope in ReqIF 1.0 and 1.2. The product does not promise arbitrary full-fidelity interchange with every requirements tool.

### Add an “AI output quality” section

Suggested copy:

> TraceBoard does not treat a non-empty model response as proof of a good result. Deterministic signals identify suspiciously short or missing narrative sections, low source-item coverage and cases where deterministic anomalies exist but an LLM returned no findings. These signals are surfaced to reviewers and do not replace review.

### Add grounding examples

The page should mention specific safeguards from the changes:

- unsupported classification tokens such as DAL/SIL/ASIL levels outside the applicable source/standard are removed or flagged,
- duplicate `(standard, clause)` assessments are deduplicated before persistence,
- contradictory status claims receive a review reason,
- traceability language distinguishes direct, indirect/task-mediated, unlinked and absent data.

This is a strong technical-marketing story because it explains how the product avoids presenting generated prose as unqualified truth.

### Correct the case-study linkage

The case study still says:

> Fix implemented in current development build; release version pending.

Since the current release is 1.4.0, either:

- update the case study to say the fix is included in the current 1.4 release, if that is factually confirmed, or
- keep it explicitly historical:

> Historical engineering note. The scenario describes an internal test and the remediation path; current product behavior should be evaluated against the deployed release.

Do not leave “release version pending” on a current product website.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\traceboard-comparison.html`

This page needs the most careful update because it makes direct competitive claims and currently uses the absence of ReqIF as a product boundary.

### Correct the “not a fit” section

Current copy says TraceBoard may not be suitable if the buyer needs:

> deep legacy integrations with established enterprise toolchains such as ReqIF/DOORS interchange

This should be narrowed:

> deep, pre-validated integrations with established enterprise toolchains, PLM systems or custom OSLC connectors.

Then add:

> TraceBoard now supports defined ReqIF 1.0/1.2 import and export workflows, but customers requiring a mature, vendor-certified interchange ecosystem across many legacy tool variants should validate their specific mappings during evaluation.

This is both accurate and commercially credible.

### Add comparison rows

The comparison table should include rows for:

- ReqIF import,
- ReqIF export,
- baseline-scoped ReqIF export,
- schema-aware import preview,
- soft-delete and restoration,
- suspect-link review workflow,
- execution-time test snapshots,
- result-change history,
- baseline-to-test-run provenance,
- deterministic AI output-quality signals,
- project-scoped personal work queue,
- built-in user administration.

Recommended values for TraceBoard:

| Capability | TraceBoard Suite position |
|---|---|
| ReqIF import | Supported with preview, mapping and transactional confirmation |
| ReqIF export | Supported for current project or baseline scope |
| ReqIF versions | 1.0 and 1.2 |
| Cross-tool compatibility | Defined mapping; validate specific customer tools |
| Item deletion | Soft-delete with recycle bin and restore |
| Trace-link governance | Suspect-link state with reviewer clearance and note |
| Test history | Execution-time snapshots and result status history |
| AI controls | Deterministic checks, grounded output and human review |
| Deployment | Self-hosted Docker Compose; online and offline packages |
| Identity | Optional OIDC configuration |
| User administration | Superadmin-only management, activation/deactivation, role changes and password reset |

### Revisit competitor claims

The comparison page makes assertions about competitors’ capabilities, prices and deployment models. The change log does not validate those claims. Keep them only if independently sourced and current.

A senior-engineer-style marketing page should distinguish:

- product facts verified from the current TraceBoard build,
- competitor facts requiring dated source citations,
- opinionated positioning.

Avoid presenting competitor limitations as absolute facts without evidence.

### Update “Your models. Your data.”

This section is good, but add the distinction between self-hosting and external integrations:

> The suite can run on customer-controlled infrastructure. OIDC, remote Git and cloud LLM providers remain explicit network-dependent integrations. Offline operation depends on the configured deployment, license, identity model and selected integrations.

### Add a product-maturity callout

Suggested copy:

> TraceBoard Suite 1.4 is not only a traceability viewer. It now provides a governed lifecycle for import, baseline capture, verification, review, restoration, exchange and evidence preservation.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\resources.html`

The resources page should be expanded beyond comparisons and AI.

### Add a current-release capability resource

New card:

**What’s new in TraceBoard Suite 1.4**

> ReqIF import and baseline-scoped export, suspect-link review, recycle-bin restoration, personal work queues, deterministic quality checks, historical test snapshots and integrated user administration.

This page is the natural place to summarize the release.

### Add a ReqIF resource

Recommended new resource card:

**ReqIF Exchange Guide**

> Learn how TraceBoard previews ReqIF files, maps source attributes, handles hierarchy and relations, and exports current or baseline-scoped project data in ReqIF 1.0 or 1.2.

Include a qualification:

> Cross-tool compatibility depends on the source and target tool’s ReqIF profile and should be validated with representative customer files.

### Add a baseline-to-test-run resource

Recommended card:

**From Baseline to Verification Run**

> See how a frozen TraceBoard baseline becomes a TraceDocs Test Plan and then a provenance-linked TraceTest run.

This is a high-value workflow for buyers evaluating the suite as an integrated platform rather than three separate applications.

### Update the engineering note card

The current card says the case study is an internal test, which is appropriate. Update the metadata and description so it does not imply an unreleased fix.

Suggested description:

> An engineering note on how source-ID preservation, deterministic checks, independent model comparison and human review make an import defect visible instead of silently propagating it.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\case-study.html`

This page should remain a bounded technical case study rather than becoming a generic sales page. It is already admirably honest.

### Update stale release metadata

Current text:

> Fix implemented in current development build; release version pending.

Recommended replacement:

> Historical internal test scenario. The remediation described here is reflected in the current product direction; evaluate the deployed 1.4.0 build for current behavior.

If the specific fix is confirmed included in 1.4.0, stronger wording is acceptable:

> Fix included in TraceBoard Suite 1.4.0.

### Add a short “What changed since this test” note

Because the change log shows substantial hardening after the case study, add a note near the beginning or end:

> Since this scenario was investigated, the surrounding workflow has been strengthened with schema-aware ReqIF mapping, deterministic output-quality signals, source-grounded classification handling, contradiction and duplicate detection, baseline-aware exchange and explicit review states. These controls do not eliminate the need for human review; they make the review surface more inspectable.

### Clarify what the case study demonstrates

The existing page correctly says it does not prove that every defect will be found. Preserve that qualification.

Add a distinction between:

- deterministic import correctness,
- deterministic traceability calculations,
- model-generated interpretation,
- human approval.

Suggested sentence:

> The example demonstrates reviewability and defect visibility, not universal automated detection. TraceBoard’s deterministic services compute recorded facts and relationships; AI-generated interpretation remains model-dependent and subject to review.

### Link to new capabilities

Add links to:

- the AI approach page,
- the features page,
- a proposed ReqIF exchange guide,
- the baseline-to-test-run workflow.

---

## `D:\Dev\MyCode\traceboard-site\traceboard-site\traceboard-tco.html`

The TCO page is less about product capabilities, but it should still reflect the stronger current product.

### Update the opening value proposition

Current positioning focuses on requirements management cost. Broaden it:

> The relevant comparison is not only the cost of storing requirements. It is the cost of connecting requirements to verification, evidence, documents, baselines and reviewable change.

### Add operational cost reductions now supported

The TCO argument can credibly include:

- no separate manual recovery process for deleted items because of recycle-bin restoration,
- less manual investigation of changed links through suspect-link states,
- less report rework through deterministic narrative-quality signals,
- fewer handoffs between requirements, document and testing tools through baseline-to-test-run flow,
- reduced migration friction through ReqIF preview and mapping,
- reduced audit reconstruction effort through execution-time snapshots and result-change history,
- reduced administrative overhead through built-in user management.

Avoid quantifying time savings unless measured. Use “reduces manual effort” rather than specific percentage claims.

### Update fit assessment

The “not the right fit if…” section should no longer list ReqIF as categorically outside scope.

Replace:

> You need deep legacy integrations with ReqIF/DOORS interchange.

With:

> You need a broad, pre-validated network of legacy integrations, PLM connectors or OSLC customizations beyond TraceBoard’s defined exchange and API surface.

### Add a qualification around deployment cost

The current “hours-not-months” messaging should be softened unless supported by customer evidence. A senior marketing version would say:

> The packaged deployment and installation runbook are designed to reduce deployment friction. Actual setup time depends on infrastructure, identity, backup, licensing and integration requirements.

This is especially important because the latest deployment documentation now explicitly includes resources, OIDC, license configuration, health checks, backups and migration policy.

---

# 3. Capabilities that should not be overclaimed

The change log provides strong evidence for the following, so these can be marketed confidently:

- ReqIF import with preview and mapping
- ReqIF export in versions 1.0 and 1.2
- Current-project and baseline-scoped export
- ReqIF uploads up to 100 MB through the packaged API path
- ProSTEP-style title and description attribute recognition
- transactional import execution
- hierarchy and relation synthesis during import
- soft-delete and recycle-bin restoration
- delete/restore history
- suspect-link detection and review
- personal cross-project work queue
- deterministic requirement-quality checks
- audit output-quality signals
- grounded classification and clause-level assessment deduplication
- contradiction detection
- execution-time test-case snapshots
- test-result status-change history
- baseline-to-Test Plan-to-Test Run provenance
- document import for Markdown, DOCX and TXT with hierarchy/provenance
- user-management MVP
- self-hosted Docker deployment
- online/offline installation packages
- OIDC configuration support
- deployment runbook and operational health checks

The following should remain qualified:

- universal ReqIF compatibility,
- lossless interchange with every requirements-management tool,
- semantic correctness of AI output,
- automatic compliance certification,
- complete historical reconstruction for all old test runs,
- complete audit persistence for every administrative action,
- air-gapped operation with all integrations,
- arbitrary full-fidelity import/export,
- enterprise-scale feature parity with DOORS, Polarion, Jama or Codebeamer,
- exact setup duration,
- competitor pricing and capability claims.

---

# 4. Recommended new top-level positioning

A stronger overall product message would be:

> **TraceBoard Suite makes engineering change reviewable.**  
> Connect requirements, implementation, verification, risks, documents and evidence; freeze meaningful baselines; detect suspect links after change; preserve execution history; and use AI as a reviewable assistant rather than an unchecked source of truth.

Supporting bullets:

- **TraceBoard:** structure, trace and govern the engineering model.
- **TraceDocs:** generate controlled documents and test plans from selected baselines.
- **TraceTest:** execute verification with evidence, snapshots and result history.
- **ReqIF exchange:** import with preview and mapping; export live or baseline-scoped data in ReqIF 1.0/1.2.
- **Reviewable AI:** grounded assessments, deterministic quality signals and human approval.
- **Self-hosted control:** run on customer infrastructure with explicit identity and integration boundaries.

This positioning reflects the latest implementation without turning the product into an unsupported claim of automatic compliance or universal interchange.