# Website Content & Positioning Implementation

**Implementation date:** 2026-09-09  
**Website repository:** `D:\Dev\MyCode\traceboard-site\traceboard-site`  
**Product source of truth:** `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md`  
**Inputs:** `website-claim-audit.md` and `website-content-positioning-plan.md`

## 1. Summary

Implemented the approved content and positioning plan as a targeted refinement of the existing static website. The homepage structure and visual identity were preserved. The implementation focused on:

- removing unsupported or materially misleading claims;
- making the deterministic engineering model and human review boundary clearer;
- adding Engineering State and baseline positioning;
- strengthening TraceDocs, TraceTest, evidence, provenance, and self-hosted/local-AI explanations;
- replacing universal interoperability and LLM language with bounded operations;
- correcting stale internal links and expanding the sitemap to include the existing Features and TCO pages; and
- removing unpublished Privacy and Terms footer links, standardizing confirmed support/sales contact routes, and adding a factual evaluation-build notice; and
- documenting remaining commercial and publishing risks without inventing new commercial facts.

No product repository files, capability inventory, audit, or positioning plan were modified.

The site currently does not publish formal privacy information or terms of service. Until those documents receive appropriate review, public pages use a support contact rather than presenting placeholder legal links.

## 2. Pages modified

### `index.html`

- Preserved the existing hero, navigation, layout, typography, trust bar, engineering-chain diagram, product cards, evidence imagery, pricing structure, FAQ, and CTA flow.
- Added a concise deterministic engineering model / AI assistance explanation to the hero.
- Changed “One connected engineering truth” to “One connected engineering model” in the hero/foundation framing.
- Clarified that the model represents recorded items and explicit relationships and cannot infer relationships that were never entered.
- Clarified the TraceBoard/TraceDocs/TraceTest relationship as shared project/item references around recorded engineering data rather than a literal single database claim.
- Added an Engineering State section covering deterministic aggregate behavior, controlled baselines, and evidence context.
- Reworked deployment copy to distinguish self-hosted core, local AI, network-dependent OIDC/Git/cloud LLM integrations, and specific data operations.
- Added Engineering State and bounded offline behavior to the FAQ.
- Replaced stale privacy/terms fragment links with the existing privacy/legal email addresses.

### `traceboard-features.html`

- Removed the direct ReqIF support claim and the `COMMITTED — ReqIF import / export` row.
- Replaced pre-built/complete standards workflow language with standards-aware templates, assessments, evidence, and qualified review wording.
- Replaced “Air-gapped by design” with scoped self-hosted/local-operation language.
- Replaced ReqIF portability language with specific JSON/CSV/XLSX/PDF/DOCX/Markdown operation language.
- Added a dedicated Engineering State section explaining its seven dimensions, deterministic inputs, and non-certification boundary.
- Added a standards-aware engineering section naming IEC 62304, ISO 14971, ISO 26262, and DO-178C with scope limitations.
- Reframed the suite as one connected engineering model with shared references and product-specific operational work.
- Replaced “AI that can’t lie to your audit trail” with accountable, reviewable AI wording.
- Replaced universal LLM, zero-lock-in, full-export, and arbitrary interchange language with configured endpoint and supported-operation wording.
- Narrowed feature labels around Engineering State, reporting, and API-supported test/commit workflows.
- Replaced the DOORS-export CTA example with a generic spreadsheet/document example that explicitly excludes ReqIF.
- Repaired placeholder navigation/CTA links.

### `traceboard-ai-approach.html`

- Replaced absolute fully-offline/no-cloud statements with scoped self-hosted/local-AI/network-dependency language.
- Removed the public ReqIF roadmap row.
- Reframed the committed-data section around deterministic core capabilities rather than universal offline operation.
- Reworked the deployment stat cards to communicate self-hosted core, local AI option, and explicit external-service dependencies.
- Replaced “virtually any LLM,” “adapts seamlessly,” and zero-lock-in language with configured local/OpenAI-compatible endpoint and supported-operation wording.
- Clarified that AI output depends on model/configuration/context/review.
- Limited the four-stage pipeline claim to an illustrative AI-assisted workflow rather than asserting identical behavior for every feature.
- Clarified that approval creates a committed product object but does not guarantee underlying engineering judgment is correct.
- Repaired Features and legal/contact links.

### `traceboard-comparison.html`

- Reframed the product as a right-sized engineering traceability/evidence system rather than a universal enterprise ALM replacement.
- Removed the DOORS-format migration implication and explicitly bounded ReqIF/requirements-tool interchange as outside current scope.
- Replaced universal LLM and zero-lock-in claims with configured endpoint and specific data-operation wording.
- Replaced “Full traceability” with recorded relationships and deterministic traceability calculations.
- Qualified deployment language and removed the fully-air-gapped setup/time implication.
- Retained competitor and pricing comparisons without inventing new values.
- Repaired Features and legal/contact links.

### `traceboard-tco.html`

- Updated the Features navigation target to the actual Features page.
- Did not change prices, estimates, team sizes, or TCO methodology values.

### `resources.html`

- Replaced the resource-card “fully offline with zero AI configured” statement with scoped local-operation language.
- Repaired the Features and legal/contact links.

### `case-study.html`

- Preserved the internal scenario, source-ID preservation, deterministic transformation, AI narrative, and human-review evidence.
- Reframed the result as a bounded internal test scenario rather than a universal defect-detection guarantee.
- Replaced “propose-only AI” with reviewable-AI wording and clarified the limited conclusion.
- Repaired the Features and legal/contact links.
- Repositioned the page as an Engineering Note while preserving its stable URL.
- Removed the duplicate sentence, explained the review workflow, corrected the architecture claim, and removed the redundant closing argument.
- Added target-audience, author/date, fix-status metadata, an inline source-ID diagram, and AI-approach/walkthrough CTAs.

### `sitemap.xml`

- Added the existing `traceboard-features` and `traceboard-tco` pages to the sitemap.
- Kept legacy pages out of the sitemap.

## 3. Accuracy corrections

### ReqIF

- Removed current ReqIF support claims from the Features page.
- Removed the ReqIF roadmap claim from the AI page.
- Removed DOORS-export wording that could imply a supported interchange mechanism.
- Retained concise negative boundary language where useful: ReqIF is not supported.

### SAML

- No SAML support claim was added.
- No current publishable page presents SAML as available.

### Managed cloud

- No managed-cloud offering was added or presented as current.
- `index-legacy.html` still contains stale managed-cloud content but remains outside the sitemap and was not modified as marketing content.

### Offline / no-cloud

- Removed “NO CLOUD DEPENDENCY,” “NO DATA LEAVES YOUR INFRASTRUCTURE,” and “every module works fully offline” messaging from the AI page.
- Replaced it with self-hosted core, local AI option, and explicit OIDC/Git/cloud-LLM network boundaries.
- Replaced homepage and comparison absolute offline language with configuration-dependent local-operation wording.

### LLM compatibility

- Removed “virtually any LLM,” “adapts seamlessly,” and universal provider language from current publishable product pages.
- Replaced it with configured local Ollama/OpenAI-compatible endpoint wording and model-dependent output qualification.

### Portability and interoperability

- Removed zero-lock-in, full-portability, and entire-project/full-fidelity export claims from current publishable pages.
- Added specific JSON, CSV, XLSX, PDF, DOCX, and Markdown operation wording.
- Explicitly excluded ReqIF and arbitrary requirements-tool interchange.

### Standards and compliance

- Replaced pre-built/complete workflow language with standards-aware templates, assessments, evidence, provenance, and review preparation.
- Added a scope section covering IEC 62304, ISO 14971, ISO 26262, and DO-178C.
- Kept certification/compliance wording only in explicit boundary statements.

### Traceability

- Replaced “full traceability” language with explicit relationships and deterministic calculations over recorded engineering data.
- Added the limitation that deterministic calculations cannot infer relationships that were never entered.

### AI authority

- Strengthened the distinction between deterministic engineering data, AI proposals/interpretation, human review, and committed engineering data.
- Removed wording implying universal AI behavior or guaranteed AI correctness.

## 4. Product differentiation added

The website now communicates the following implemented differentiators more clearly:

- **Deterministic engineering model:** recorded items, explicit relationships, defined calculations, baselines, evidence, and state remain inspectable.
- **Engineering State:** a deterministic aggregate across compliance assessment, traceability, verification, risk, consistency, change impact, and baseline readiness.
- **Baselines:** controlled snapshots used for comparison, traceability, and documentation rather than immutable compliance proof.
- **TraceDocs:** controlled documentation from engineering data and selected baselines, rather than generic PDF generation.
- **TraceTest:** verification runs, results, evidence, and coverage connected to engineering items, rather than generic test tracking.
- **Evidence/provenance:** recorded results, assessments, relationships, documents, and deterministic versus AI-derived interpretation are distinguished.
- **Reviewable AI:** AI can propose, analyze, generate, query, import, or narrate; humans decide what becomes committed engineering data.
- **Self-hosted control:** Docker-based customer infrastructure and local AI options are communicated without claiming that every integration is offline.

## 5. Commercial issues

Commercial values were not invented or silently changed. The following remain subject to commercial-owner verification:

- homepage 30-day trial scope and “full current feature set” wording;
- current prices, currencies, plan names, team-size limits, and feature entitlements;
- whether AI use is included or separately metered;
- comparison-page competitor prices and annual-cost ranges;
- TCO setup-time, admin-effort, and labor-rate assumptions;
- “published annual tiers,” “no per-seat licensing,” and “no usage-based AI billing” claims;
- live-demo, trial-license, activation, and download endpoint behavior.

The TCO page methodology remains an estimate and should receive a commercial review before publication as authoritative pricing material.

## 6. Legacy/publishing findings

- `index-legacy.html` remains in the repository as historical material and was not rewritten.
- `old_index.html` remains in the repository as a historical artifact and was not rewritten.
- Both legacy files are excluded from `sitemap.xml`.
- The website repository contains no deployment configuration, build manifest, robots file, or hosting rule that can enforce exclusion of arbitrary root-level HTML files.
- Therefore, the hosting/deployment configuration must explicitly publish only the intended current pages or move the legacy files outside the served tree in a separate publishing task.
- The current sitemap now includes the existing Features and TCO pages, which were linked/usable pages but previously omitted.

## 7. Verification

### Static checks performed

- Read and used the product capability inventory, website claim audit, and approved positioning plan.
- Searched current publishable HTML for ReqIF, SAML, managed cloud, SaaS, zero-lock-in, universal LLM, offline/no-cloud, traceability completeness, certification, standards, DOORS, and related high-risk terms.
- Confirmed no positive ReqIF or SAML support claim remains on the current publishable pages. Remaining ReqIF mentions are explicit negative boundary statements.
- Checked expected positioning terms including deterministic, Engineering State, baseline, TraceDocs, TraceTest, OIDC, human review, committed engineering data, self-hosted, and local AI.
- Parsed all seven current publishable HTML files with Python’s `html.parser`; all parsed without parser errors.
- Checked internal local file links and fragments; final result: `link_errors=0`.
- Parsed `sitemap.xml` as XML successfully.
- Confirmed the sitemap contains Home, Comparison, Features, TCO, Resources, AI Approach, and Case Study.

### Checks not available

- No website package/build/test manifest exists in this repository.
- No browser automation, visual regression, CSS validator, or deployed-site check is configured here.
- Responsive behavior was preserved by avoiding structural CSS changes; browser-level visual verification remains recommended.

## 8. Remaining risks

1. The working tree contained pre-existing changes, including a modified `index.html`, deleted `.gitignore`, untracked legacy/content directories, and other files. The homepage diff is therefore not attributable solely to this task when compared with Git HEAD; the current starting file was preserved and edited in place.
2. Commercial copy remains unverified by the product inventory.
3. The comparison page contains competitor descriptions and pricing estimates that require normal commercial/editorial review.
4. The current publishable pages contain negative/boundary mentions of ReqIF and certification. These are intentional accuracy boundaries, not support claims, but should be reviewed for tone during the independent claim audit.
5. `index-legacy.html` still contains stale unsupported content. It must not be served by deployment configuration.
6. The inventory notes that some evidence/governance implementation files were present but uncommitted in the product repository; release status should be confirmed before treating those capabilities as generally available.
7. Some old page-specific claims about provider scope, Git behavior, document templates, and plan entitlements may require a further implementation-level review even though the broad wording was narrowed.

## 9. Recommended next step

Run a **final independent website claim audit** against the modified publishable website and the current product capability inventory. That audit should specifically verify:

- no accidental positive ReqIF/SAML/managed-cloud claims;
- all standards wording remains scoped;
- all AI/local/offline boundaries are consistent;
- commercial claims have been approved;
- legacy files cannot be served; and
- the current sitemap and hosting configuration match the intended publishable page set.
