# Website Claim Audit

**Audit date:** 2026-09-09  
**Repository:** `D:\Dev\MyCode\traceboard-site\traceboard-site`

## Audit limitation and confidence

The implementation source of truth is `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md`, based on the TraceBoard Suite implementation repository. The website itself is maintained in the separate repository identified above. The inventory was created using routers, generated OpenAPI schemas, frontend call sites, tests, deployment files, and then documentation; it is therefore the implementation authority for this audit.

The inventory confirms major implemented capabilities including baselines, TraceDocs, TraceTest, Engineering State, AI-assisted query/import/generation/consistency/audit flows, and OIDC. It also confirms the important limits: no ReqIF, no SAML implementation, no managed cloud, no certification or complete standards workflow, bounded export/import behavior, model-dependent AI, and network dependencies for Git/OIDC/cloud LLM use. Website pricing and commercial claims remain outside the product repository’s implementation proof and are marked conservatively.

## 1. Executive Summary

### Scope and counts

- **Pages audited:** 7 sitemap/current pages plus 2 linked product pages; `index-legacy.html` was inspected as a tracked legacy artifact but not counted as current homepage content.
- **Meaningful claim units reviewed:** approximately **53**. A claim unit is a substantive product, deployment, AI, standards, integration, pricing, comparison, or CTA claim; repeated navigation labels and purely descriptive styling text were not counted separately.
- **SUPPORTED:** **12** claims, where the inventory gives direct implementation support and wording is bounded.
- **SUPPORTED — NEEDS PRECISION:** **18** claims.
- **OVERCLAIM:** **9** claims.
- **UNSUPPORTED:** **2** claims.
- **NOT IMPLEMENTED / ROADMAP CLAIM:** **2** claims.
- **AMBIGUOUS:** **10** claims, primarily commercial, historical-case-study, or exact provider-scope claims.
- **Important missing or underrepresented capabilities:** **10**.

These counts are approximate because several pages repeat the same claim in headings, cards, metadata, comparison rows, and CTAs. They should be treated as a review index, not a compliance metric.

### Overall assessment

The current homepage is materially safer and more precise than the legacy page in its treatment of connected engineering, optional AI, and the TraceBoard/TraceDocs/TraceTest relationship. The strongest credible positioning is the combination of a deterministic engineering model with AI that proposes within human review boundaries. The detailed features page, however, contains a critical direct ReqIF claim that conflicts with implementation truth.

The largest risks are on the detailed product/comparison pages: explicit ReqIF claims, absolute language such as “virtually any LLM,” “adapts seamlessly,” “zero lock-in,” “pre-built ... workflows,” “fully offline,” “air-gapped by design,” and broad compliance language can create expectations beyond the implementation. The tracked legacy homepage also contains a managed-cloud roadmap claim and should not be published accidentally.

Confidence is high for the capability and limitation findings covered by the inventory. Confidence remains moderate for commercial/pricing claims and for the exact production release status of implementation files that the inventory notes are currently uncommitted.

## 2. Website Structure

### Repository and publishing model

- **Application/location:** static HTML at the repository root: `index.html`, `resources.html`, `traceboard-features.html`, `traceboard-comparison.html`, `traceboard-ai-approach.html`, `traceboard-tco.html`, and `case-study.html`.
- **Current homepage:** `index.html` (the recently updated page referenced by the brief).
- **Content model:** hard-coded HTML. There is no framework routing, CMS, component library, build manifest, or data-driven content source in this checkout. CSS is embedded per page; navigation is repeated rather than shared through components.
- **Generated/static content:** `sitemap.xml` lists `/`, `/traceboard-comparison`, `/resources`, `/traceboard-ai-approach`, and `/case-study`. The repository also contains linked pages `traceboard-features.html` and `traceboard-tco.html` that are not in the sitemap. `index-legacy.html` is a large tracked older homepage and `old_index.html` is an additional legacy artifact.

### Pages and content areas audited

1. `index.html` — homepage: navigation, hero, engineering model, products, evidence, deployment, FAQ, pricing, metadata, CTAs, privacy/terms/contact sections.
2. `traceboard-features.html` — feature/differentiator page: engineering model, workflows, AI, standards, deployment, pricing, LLM compatibility, data export, CTAs.
3. `traceboard-comparison.html` — comparison page: ALM comparison, pricing, deployment, AI approval, standards, integrations/fit, LLM compatibility, portability.
4. `traceboard-ai-approach.html` — AI approach page: propose/validate/approve/commit, deterministic core, local/cloud models, offline statements, data freedom.
5. `traceboard-tco.html` — pricing/TCO page: license and setup estimates, competitor comparisons, Excel/Word/Jira context, deployment CTAs.
6. `resources.html` — public resources index: comparison, AI approach, and engineering-note product claims.
7. `case-study.html` — public engineering note: AI import, audit narrative, deterministic engine, source-ID preservation, human review, and ISO 26262 context.
8. `index-legacy.html` — inspected but excluded from “current homepage” counts; contains older claims including managed cloud planned, extensive compliance/product claims, and older pricing/trial language.

### Navigation and page relationships

The current homepage links to in-page sections (`#chain`, `#products`, `#pricing`, `#faq`), `traceboard-comparison.html`, `resources.html`, `traceboard-ai-approach.html`, and external trial/demo endpoints. Other pages generally link back to `index.html`, resources, the AI approach, and the case study. There are no dedicated current public TraceBoard, TraceDocs, TraceTest, security, standards, deployment, or FAQ routes; those topics are embedded in the homepage and feature/comparison pages.

## 3. Claim Audit

The locations below use the source file and the section/heading because some current HTML sections are single long lines. Line numbers refer to the checked-in source where practical.

| Page | Location | Claim | Capability | Classification | Risk | Evidence / Reasoning | Recommended Action |
|---|---|---|---|---|---|---|---|
| Homepage | `index.html:6-7`, title/meta | Traceable engineering connecting requirements, work, verification, and evidence | Core traceability model | SUPPORTED | Low | Inventory confirms requirements, tasks, tests, risks, hazards, typed relations, trace graphs, and reporting; evidence includes TraceBoard routers/services/tests summarized in `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md:12-18` | KEEP |
| Homepage | Hero / `#truth` | “One connected engineering truth” / one system with three specialized views | Suite architecture and shared engineering graph | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms integrated TraceBoard/TraceDocs/TraceTest references, but specifically says TraceBoard owns domain data while satellite services retain operational data (`inventory:25`, architecture evidence summarized at `inventory:189`) | Keep with explicit “connected engineering data/model” framing; do not imply every record is literally stored in one database |
| Homepage | `#chain` | Engineering need → requirement → work → verification → evidence | Traceability relationships | SUPPORTED | Low | Bounded model statement; page says it is not a mandatory workflow | KEEP |
| Homepage | `#chain` regulated example | Hazard → risk → requirement → task → test → evidence | Risk/hazard relationships and evidence | SUPPORTED — NEEDS PRECISION | Moderate | The brief confirms risks, hazards, chains, matrices, evidence, and traceability; this is not proof of complete enterprise risk management | Say “supports linked risk/hazard analysis,” not “complete risk management” |
| Homepage | `#products` | TraceBoard structures work; TraceDocs documents from controlled data; TraceTest verifies against the same truth | Three product views / shared data | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms TraceDocs baseline-derived generation and TraceTest runs/results/coverage, while noting separate services with shared references and event/API integration (`inventory:15-16,25`) | KEEP, but qualify “same truth” as shared engineering data |
| Homepage | product cards | Requirements, risks, tasks, tests and evidence remain connected | Engineering graph | SUPPORTED | Low | Matches known product scope in brief and repeated site model | KEEP |
| Homepage | evidence section | Baselines, traceability and evidence-linked verification are available to all users | Baselines and verification evidence | SUPPORTED | Low | Inventory confirms baseline snapshots, approval, comparison, baseline-scoped traceability/document diffs, TraceTest evidence files, coverage, trends, reports, and commit association (`inventory:13-16`) | KEEP |
| Homepage | deployment section | Runs as Docker Compose with databases on customer infrastructure | Self-hosted deployment | SUPPORTED | Low | Inventory evidence method explicitly inspected `docker-compose.yml` and `nginx.conf`; inventory confirms Docker Compose self-hosting and optional Cloudflare Tunnel (`inventory:32,214`) | KEEP, but do not imply managed hosting |
| Homepage | deployment/FAQ | “Air-gapped operation” / “fully offline operation” | Self-hosted and air-gapped capability | SUPPORTED — NEEDS PRECISION | High | Docker self-hosting/local Ollama support are implemented, but inventory states Git, OIDC, and cloud LLM features require configuration/external services and are not all available disconnected (`inventory:18,202`) | Say “core self-hosted stack can operate air-gapped; external integrations, OIDC, and cloud AI require connectivity” |
| Homepage | deployment card | Import/export uses JSON, PDF, SQL and DOCX | Export/import formats | AMBIGUOUS | Moderate | Website asserts formats; inventory/code unavailable; generic format support must not imply ReqIF or full-fidelity interchange | Verify each direction and fidelity; list only confirmed operations |
| Homepage | FAQ | 30-day trial with full current feature set and downloadable license | Trial/licensing | AMBIGUOUS | Moderate | CTA endpoint exists, but entitlement behavior is not in this repository | Verify trial scope and keep only if operationally true |
| Homepage | FAQ | AI is optional; it proposes in context; deterministic checks remain inspectable; human decides approval | AI assistance and review boundaries | SUPPORTED | Low | Inventory confirms optional configured local/OpenAI-compatible AI flows and warns outputs can be incomplete or semantically wrong; deterministic checks and human review reduce but do not eliminate that limitation (`inventory:18,200`) | KEEP; make this a primary differentiator |
| Homepage | pricing | Flat pricing / team-size bundles / no usage-based AI billing | Pricing model | AMBIGUOUS | Moderate | Pricing is marketing content; no billing/configuration source is present | Verify current commercial terms and date-stamp pricing |
| Features | hero/quick facts | Suite connects requirements, work, verification and evidence | Traceability | SUPPORTED | Low | Consistent core claim | KEEP |
| Features | differentiator cards | Deterministic engineering core; AI proposes and does not silently commit | Deterministic core and human review | SUPPORTED | Low | Consistent with supplied product philosophy and case study | KEEP |
| Features | standards section/comparison row | “Pre-built ISO 26262 / IEC 62304 / DO-178C workflows from day one” | Standards-aware workflows | OVERCLAIM | High | Inventory confirms named-standard analysis/template/assessment support, but explicitly says there is no complete workflow or proof of compliance for these standards (`inventory:22,31`) | REWRITE as standards-aware engineering workflows/templates/assessments; state scope |
| Features | standards/compliance copy | Compliance data, compliance portability, audit-ready outputs | Evidence/documentation | SUPPORTED — NEEDS PRECISION | High | Product can provide evidence/provenance/documentation, but “audit-ready” can imply acceptance or certification | Qualify as “supports audit preparation” and retain human/qualified review caveat |
| Features | AI section | AI-generated/proposed tasks and tests; consistency analysis; audit narratives | AI-assisted generation/analysis | SUPPORTED — NEEDS PRECISION | Moderate | Brief confirms these capabilities; model output is configuration-dependent and proposed, not authoritative | KEEP with “proposed,” “reviewable,” and model-dependence language |
| Features | model compatibility | Works with “virtually any” LLM; adapts “seamlessly” from 3B to 1.6T models | LLM integrations | OVERCLAIM | High | Inventory confirms local Ollama/OpenAI-compatible HTTP configuration, but explicitly says not every named provider is separately tested and outputs can be incomplete or semantically wrong (`inventory:18,187,200`) | Limit to configured local/OpenAI-compatible endpoints and disclose quality/latency variation |
| Features | local/cloud provider list | Supports Ollama, LM Studio, Mistral, OpenAI, Anthropic, DeepSeek and compatible endpoints | AI provider integrations | AMBIGUOUS | Moderate | Website lists providers, but implementation evidence is absent; provider-specific behavior is not demonstrated here | Verify configuration adapters and label provider support accurately |
| Features | data freedom | No proprietary binary/encrypted stores; full PostgreSQL access; zero lock-in | Data portability/database access | OVERCLAIM | High | Inventory confirms multiple endpoint-specific exports but explicitly limits CSV import, Excel synchronization, PDF/DOCX fidelity, and says no public API-support program was established (`inventory:14,195-203`) | Replace with enumerated supported exports and a bounded portability claim |
| Features | CTA | Evaluate against “a messy spreadsheet” and “an existing DOORS export” | Import/interoperability | OVERCLAIM | High | Inventory finds no ReqIF support and no arbitrary DOORS/requirements-tool interchange; Excel support is product-specific and PDF/DOCX parsing/fidelity are bounded (`inventory:195-198`) | Remove “DOORS export” or identify the exact supported non-ReqIF format |
| Comparison | page title/meta | Self-hosted, modular architecture delivers faster traceability at lower costs | Deployment/commercial comparison | SUPPORTED — NEEDS PRECISION | Moderate | Self-hosted is consistent; speed/cost are comparative claims requiring substantiation and assumptions | Retain only with methodology and scope |
| Comparison | feature table | TraceBoard has full traceability, built-in compliance workflows, AI assistance, audit evidence | Core product capabilities | SUPPORTED — NEEDS PRECISION | High | Core capabilities are credible; “full” and “compliance workflows” need bounded scope | Replace “full” with “linked/visualizable/deterministically calculated” and define workflows |
| Comparison | feature table | AI suggestions are validated and human-approved before commit | AI review gate | SUPPORTED | Low | Directly supported by case study/product philosophy | KEEP |
| Comparison | feature table | Self-hosted and air-gapped by design, not exception | Deployment | SUPPORTED — NEEDS PRECISION | High | Air-gapped core is in brief; universal “by design” can imply every integration is offline | Qualify core stack versus network-dependent integrations |
| Comparison | fit section | Works productively in hours, including air-gapped environments | Setup/deployment | AMBIGUOUS | Moderate | “Hours” is a performance/implementation promise; no deployment evidence in checkout | Present as target/typical experience only if measured |
| Comparison | fit section | Does not provide deep DOORS/PLM/OSLC integrations | Integration limitation | SUPPORTED — NEEDS PRECISION | Low | Page is appropriately candid, but must be checked against actual current integrations | KEEP if still accurate |
| Comparison | pricing | Flat annual pricing €999–€11,990 for 5–100 users; no usage-based AI billing | Pricing | AMBIGUOUS | Moderate | No commercial source here; numbers may age quickly | Verify and timestamp |
| Comparison | model/data section | Portable compliance data and no proprietary lock-in | Portability | OVERCLAIM | High | Absolute lock-in claim exceeds verifiable evidence | QUALIFY |
| AI approach | metadata | “Deterministic AI approach” / automated consistency checks and trace validation | Deterministic engine plus AI | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms deterministic traceability/consistency flows and warns AI can be semantically wrong; deterministic graph calculations cannot know about relationships never entered (`inventory:18,200`) | Explain limits of graph-based calculations |
| AI approach | pipeline | Propose → validate → approve → commit | Human review workflow | SUPPORTED | Low | Explicitly supported by case study and brief | KEEP |
| AI approach | core principle | Deterministic engine fully functional without AI | AI optionality | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms AI calls are optional and the deterministic product capabilities are implemented; some AI-dependent flows naturally require a configured model | Keep, but scope to deterministic core capabilities and avoid implying every advanced workflow runs without AI |
| AI approach | offline stats | No cloud dependency; no data leaves infrastructure; every module works with AI disabled | Offline/local operation | OVERCLAIM | Critical | These are broad absolutes. External identity, Git, and cloud AI integrations necessarily require connectivity; “every module” needs implementation proof | Split core/local AI/offline claims and list exceptions |
| AI approach | provider compatibility | Supports local Ollama/LM Studio and cloud providers; any OpenAI-compatible endpoint | AI integrations | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms local Ollama and OpenAI-compatible HTTP configuration, but says broad provider descriptions are not proof of separately tested integrations (`inventory:18,187`) | State supported configuration pattern; avoid claiming every named provider is natively tested |
| AI approach | data freedom | All import/export is JSON, PDF, SQL, DOCX; entire project export without assistance | Interoperability/export | OVERCLAIM | High | Inventory confirms endpoint-specific CSV/XLSX/JSON/PDF plus TraceDocs PDF/DOCX/document import, while explicitly rejecting arbitrary interchange/full fidelity and general CSV import (`inventory:14-15,195-198`) | Enumerate operations and limitations |
| TCO | comparison table | TraceBoard annual license and low setup cost; 15-user total-cost comparison | Pricing/TCO | AMBIGUOUS | Moderate | Website discloses estimates, which is good, but no current price source exists in checkout | Keep methodology and verify current prices |
| TCO | fit section | Productive in hours/days rather than weeks/months | Implementation effort | AMBIGUOUS | Moderate | A customer outcome claim without measured evidence | Recast as an intended fit or provide evidence |
| TCO | data examples | Excel, Word, lightweight Jira project are migration starting points | Import/migration | AMBIGUOUS | High | Context examples may imply import support; implementation absent | Say “starting data sources” only when importer details are stated |
| Resources | card | All-in-one requirements traceability, document management and test tracking ALM platform | Suite breadth | SUPPORTED — NEEDS PRECISION | Moderate | Three suite views are consistently described; “all-in-one” can imply arbitrary ALM coverage | Use “integrated suite” and name boundaries |
| Resources | AI card | Works fully offline with zero AI configured | Offline operation | OVERCLAIM | High | Same broad claim as AI page; needs core/integration qualification | REWRITE |
| Resources | case-study card | Real testing example, not hypothetical; caught silent data-integrity bug | Case study evidence | SUPPORTED — NEEDS PRECISION | Moderate | This is a claim about the authors’ test, but external reproducibility/evidence is not available | Label as internal case study and avoid generalizing to guaranteed detection |
| Case study | title/meta | Architecture caught a real traceability bug that auto-commit would miss | Human review architecture | SUPPORTED — NEEDS PRECISION | Moderate | The described scenario supports the example; it does not prove all bugs are caught | Add “in this test scenario” scope |
| Case study | setup | AI Import and AI Audit Narrative with independent Mistral/DeepSeek runs | AI import/audit narrative | SUPPORTED — NEEDS PRECISION | Moderate | Inventory confirms AI import and audit-narrative flows, but model-dependent output remains fallible (`inventory:18,200`); the specific historical run is not independently reproduced by the inventory | Label as an internal test scenario and retain model/date details |
| Case study | failure explanation | Traceability was silently broken by import flattening/renumbering | Import behavior | SUPPORTED — NEEDS PRECISION | High | The repository contains import-source-ID regression material (`test_import_source_ids.py` and inventory discussion), but the historical defect/fix should remain version-scoped rather than implying universal detection | State version/date and provide regression-test evidence |
| Case study | fix | Original IDs preserved; ambiguous structures flagged for review | Import provenance/human review | SUPPORTED | Low | Inventory investigation includes import-session/source-ID implementation and tests; the brief also confirms human-review boundaries | Keep with versioned evidence |
| Case study | audit narrative | Sections mark deterministic counts/statuses/links versus LLM interpretation | Provenance | SUPPORTED | Low | Inventory lists evidence/governance services and tests for narrative, metrics, and meta evidence, while still warning that LLM output is interpretive (`inventory:17-18,190,200`) | KEEP; this is valuable differentiation |
| Case study | ISO 26262 paragraph | SHALL/SHOULD/performance constraints have different compliance weight under ISO 26262 | Standards context | AMBIGUOUS | Moderate | The standards reference is contextual, not a certification promise; exact product standard coverage is unverified | Retain as explanatory context, not product compliance claim |
| Features | principles / `traceboard-features.html:267` | “ReqIF import and export” means the product is portable | ReqIF interchange | UNSUPPORTED | Critical | Inventory explicitly found no ReqIF parser, exporter, route, schema, frontend action, or test (`inventory:29,195`) | REMOVE OR REPLACE; do not substitute generic JSON/CSV/Excel/API wording |
| Features | capability matrix / `traceboard-features.html:299` | “COMMITTED — ReqIF import / export” | ReqIF interchange | UNSUPPORTED | Critical | Direct contradiction of implementation source; the inventory says ReqIF is absent | REMOVE immediately |
| AI approach | roadmap row / `traceboard-ai-approach.html:550` | “ReqIF schema mapping on import” | ReqIF interchange | NOT IMPLEMENTED / ROADMAP CLAIM | High | Explicitly labeled roadmap and inventory confirms no current ReqIF implementation; inventory does not establish a committed delivery date | REMOVE from marketing or move to a clearly controlled roadmap, if product policy permits |
| Legacy homepage | `index-legacy.html:1757-1775` | Managed cloud is planned; vendor handles updates, backups, infrastructure | Managed hosting | NOT IMPLEMENTED / ROADMAP CLAIM | High | Inventory confirms no managed-cloud service; Docker self-hosting and optional Cloudflare Tunnel do not establish a cloud product (`inventory:32,203`) | REMOVE from any deployable/current site |
| Legacy homepage | older deployment/pricing sections | Air-gapped support, compliance exports, full traceability, “no admin overhead,” older trial/pricing claims | Deployment/compliance/commercial | OVERCLAIM | High | Legacy content uses stronger wording than current homepage and may conflict with current product state | Archive outside publish path or audit separately before deployment |

### Required term safety-net results

The final website search found the following high-priority claims:

- **ReqIF:** explicit unsupported claim at `traceboard-features.html:267`, explicit `COMMITTED` claim at `traceboard-features.html:299`, and an explicit roadmap claim at `traceboard-ai-approach.html:550`.
- **SAML:** no website claim found. The inventory confirms no implementation and says internal roadmap/release documentation treats it as planned; it must not be presented as supported.
- **OIDC:** no current marketing claim found. The inventory confirms OIDC support and states that OIDC requires configuration/external services, so a bounded SSO/security note is a significant communication opportunity.
- **Engineering State:** not meaningfully communicated on current pages despite being implemented as an on-demand aggregate of compliance assessments, traceability, verification, risk, consistency, change impact, and baseline readiness (`inventory:17,24`).

Current pages also contain standards, compliance, traceability, verification, AI, air-gapped/offline, self-hosted/cloud, enterprise, security, GitHub, Excel, CSV/PDF/DOCX/JSON/API, baseline, audit, evidence, and findings language. GitLab and Gitea are not named as website integrations; the product repository does contain Gitea configuration and Git-related capability evidence, but the website should not imply provider breadth or synchronization direction without a specific verified claim.

## 4. High-Priority Corrections

### Critical

1. **AI approach, offline stats:** remove or qualify “NO CLOUD DEPENDENCY,” “NO DATA LEAVES YOUR INFRASTRUCTURE,” and “every module works with AI fully disabled.” The safe scope is the local/self-hosted core and local-model configuration; cloud AI, external identity, and remote integrations are network-dependent.
2. **Features/comparison:** remove “pre-built ISO 26262 / IEC 62304 / DO-178C workflows from day one” unless the inventory and code prove exact workflow coverage. Standards-aware engineering support is not certification or complete compliance.
3. **Features/comparison/AI:** remove “virtually any LLM,” “adapts seamlessly,” and universal endpoint implications until provider adapters and tested compatibility are evidenced.
4. **Features/AI:** replace “zero lock-in” and “entire project export ... at any time” with enumerated, tested exports and restoration limitations.

### High

5. Qualify all “audit-ready,” “compliance data,” and “compliance workflows” language as support for evidence preparation, assessment, provenance, and documentation—not certification, approval, or guaranteed compliance.
6. Qualify “full/complete traceability” as traceability over relationships entered into the engineering graph and calculations derived from that graph; do not imply the product knows whether an omitted relationship should exist.
7. Clarify the air-gapped boundary: local deployment/local model operation can be offline; cloud AI, OIDC providers, and remote Git integrations require network access.
8. Remove the managed-cloud roadmap wording from `index-legacy.html` or ensure the file cannot be published. Do not present it as an available deployment option.

### Medium

9. Make the comparison page’s DOORS export and spreadsheet examples explicit about supported formats and one-way/manual migration. Do not let “DOORS export” imply ReqIF.
10. Verify and date-stamp prices, trial duration, team-size ranges, and “full current feature set” claims.

### Low

11. Replace generic adjectives (“seamlessly,” “all-in-one,” “enterprise,” “modern”) with a few evidence-backed specifics.
12. Add a short limitation note to standards and AI pages explaining that deterministic graph state and generated/proposed content have different authority.

## 5. Unsupported / Not Implemented Claims

### Explicitly unsupported or not implemented by the audit brief

- **ReqIF / Requirements Interchange Format import/export:** current claims are explicitly present at `traceboard-features.html:267` and `traceboard-features.html:299`, with a further roadmap claim at `traceboard-ai-approach.html:550`. The inventory found no ReqIF parser, exporter, route, schema, frontend action, or test. Remove these claims; generic Excel/CSV/JSON/API support is not ReqIF.
- **SAML authentication:** no current website claim was found. Do not add it. Current product decision is OIDC support; SAML was not implemented and should not be presented as available or automatically as an active roadmap commitment.
- **Managed cloud:** not currently implemented. The claim appears in `index-legacy.html` as “planned,” so it is a `NOT IMPLEMENTED / ROADMAP CLAIM` and should be removed from publishable content.

### Unsupported by available evidence, but not conclusively disproved

These are not necessarily absent, but they are unsafe as currently worded:

- Complete/pre-built compliance workflows for ISO 26262, IEC 62304, and DO-178C. The inventory confirms only standards-aware analysis/template/assessment support.
- Certification, guaranteed compliance, regulatory approval, or replacement for qualified compliance processes. No explicit “certified” claim was found on current pages, but adjacent “audit-ready/compliance” language risks that interpretation.
- Universal LLM/provider compatibility and seamless behavior across model sizes. The inventory confirms local Ollama/OpenAI-compatible configuration, not every named provider as a separately tested native integration.
- Zero lock-in, full-fidelity export, and universal offline operation. The inventory explicitly bounds export/import behavior and says Git, OIDC, and cloud LLM features require external services.
- Automatic determination that traceability relationships are semantically correct or complete.

## 6. Missing / Underrepresented Capabilities

These are product capabilities identified in the audit brief or visible in the website’s own evidence but not adequately communicated as differentiators. They are not claims that the product lacks them.

| Capability | Current website coverage | Why it matters | Suggested location | Positioning direction |
|---|---|---|---|---|
| Deterministic engineering truth plus AI assistance | AI approach and case study explain it well; homepage says AI is optional but does not lead with the contrast | Strongest product philosophy and trust differentiator | Homepage hero/foundation and AI page | “AI proposes; the deterministic engineering model remains authoritative.” |
| Engineering State | Not found as a meaningful current concept | Gives buyers a project-level readiness/state view beyond isolated artifacts | Homepage or features page | Explain as a calculated state derived from multiple engineering dimensions, not a vague health score |
| Human review boundaries and committed vs proposed content | Strong in AI page/case study, weak in homepage feature summary | Critical for regulated teams evaluating AI risk | Homepage AI section and comparison table | Show the approval boundary and what becomes authoritative only after review |
| Assessment provenance and deterministic versus LLM-derived output | Case study mentions it, but not as a product capability | Lets reviewers distinguish reproducible facts from interpretation | Features/AI page | Use a provenance model: counts/statuses/links versus narrative/recommendation |
| Clause-level standards assessments/templates/evidence | Current pages use broad “compliance workflows” language but do not show the concrete capability | Specific evidence is more credible than compliance adjectives | Features/standards section | Describe supported assessment/template/evidence workflows with standard/version scope |
| Baselines as controlled snapshots | Homepage FAQ/cards mention baselines; their comparison/history purpose is absent | Important for controlled change, audit comparison, and TraceDocs output | Homepage evidence section and TraceDocs explanation | Explain snapshots, comparison, traceability, and document generation |
| Risk/hazard chains and matrices | Homepage has a single example chain | Differentiates engineering traceability from ordinary requirements tracking | Homepage regulated example or feature page | Show hazard/risk/requirement/verification/evidence relationships without claiming full ERM |
| TraceTest coverage trends and evidence | Test verification is named, but coverage/trend behavior is underexplained | Buyers need to understand how verification status is measured | Product relationship section | Describe test execution/results, coverage, and links back to requirements |
| Git provider synchronization/verification | GitHub appears mainly as a repository link; GitLab/Gitea are absent | Integration boundaries matter to engineering buyers | Integration section/FAQ | Specify providers, directionality, manual/webhook behavior, and network requirements |
| TraceDocs restore/history/branding/baseline behavior | TraceDocs is described as document generation, not controlled document lifecycle | Makes the document product materially more than PDF export | TraceDocs card/features section | Position controlled documents generated from selected engineering snapshots |

## 7. Product Positioning Observations

### Strengths

- The current homepage communicates the core connected model without requiring a regulated workflow and correctly says the chain is a model rather than a mandatory process.
- The AI approach and case study articulate a credible propose/validate/approve/commit boundary and distinguish deterministic facts from LLM interpretation.
- The suite relationship is understandable: TraceBoard structures work, TraceDocs documents it, and TraceTest verifies it.
- Self-hosted deployment and customer-controlled data are prominent and appropriate for the target audience, provided offline exceptions are stated.
- The comparison and TCO pages are unusually candid about fit limits, deep legacy integrations, and the difference between a lower price and a tool doing the job.

### Weaknesses and risks

- The site uses generic AI and portability absolutes on detail pages even though its strongest story is bounded, reviewable AI.
- Standards language compresses assessment/templates/evidence into “pre-built workflows,” risking a certification/compliance interpretation.
- Traceability is presented strongly, but the important distinction between entered graph relationships and semantic completeness is not explicit.
- Engineering State, assessment provenance, controlled baselines, and concrete TraceDocs/TraceTest behavior are largely absent or buried, despite being implemented and evidence-backed.
- The current site does not state the authentication boundary: OIDC is supported; SAML is not implemented. A concise security/deployment note would prevent assumptions without making a negative feature list the headline.
- The current site contains a direct ReqIF contradiction: the feature page says ReqIF is committed even though the inventory finds no ReqIF implementation.
- There is no dedicated public standards, security, deployment, or integration page. Those claims are spread across hard-coded pages with repeated, sometimes inconsistent wording.
- `index-legacy.html` remains in the repository and contains materially different claims. In a static deployment, accidental publication is a real content-governance risk.

## 8. Recommended Content Changes

### Must change

1. Remove/qualify universal offline and no-cloud statements and document network-dependent exceptions.
2. Replace standards “pre-built workflow” and broad compliance wording with scoped standards-aware assessment/template/evidence language.
3. Remove “virtually any LLM,” “seamlessly,” and similar universal compatibility claims unless code and test evidence support them.
4. Replace “zero lock-in” and absolute full-export claims with an exact capability matrix.
5. Remove both current ReqIF claims and the ReqIF roadmap row; do not imply ReqIF through generic JSON/CSV/Excel/API language.
6. Remove the managed-cloud roadmap claim from the legacy artifact and prevent legacy pages from being deployed.

### Should change

7. Reframe “full/complete traceability” around explicit graph relationships and deterministic calculations.
8. Add OIDC as the supported SSO/authentication mechanism, with configuration/external-service boundaries; do not mention SAML as supported.
9. Turn the AI approach into a concise trust model: deterministic engineering state, proposed AI output, review/acceptance, committed record.
10. Describe baselines, provenance, and TraceDocs/TraceTest behavior with concrete examples.
11. Validate all pricing, trial, provider, and deployment claims against the actual release/configuration and add an “as of” date.

### Could improve

12. Add a focused integration/interoperability page with directionality and network requirements for each supported integration.
13. Add a standards scope table that names supported assessment/template/evidence workflows without suggesting certification.
14. Consolidate repeated claims into a maintainable content source or shared template to prevent homepage/detail-page drift.
15. Use the case study as evidence for review boundaries, but label it as an internal test scenario rather than implying guaranteed defect detection.

## Final consistency check

Search coverage included: ReqIF, Requirements Interchange Format, SAML, OIDC, compliance, certification, IEC 62304, ISO 14971, ISO 26262, DO-178C, risk management, hazard, traceability, verification, AI, autonomous, automation, air-gapped, offline, self-hosted, cloud, enterprise, SSO, security, GitHub, GitLab, Gitea, Excel, CSV, PDF, DOCX, Markdown, JSON, API, Engineering State, baseline, audit, evidence, and findings.

The most important results are:

- ReqIF is explicitly claimed twice on the current features page and once as a roadmap item on the AI page, despite no implementation. SAML is not claimed and must not be added.
- OIDC is not currently explained on the website despite being implemented; its external identity-provider dependency should be stated if marketed.
- Engineering State is implemented but absent as a product concept.
- Air-gapped/offline language is present and currently too absolute in the AI approach/resource content.
- Standards, portability, and universal LLM language carry the highest current claim risk.
- The legacy homepage contains the managed-cloud roadmap claim and must be excluded from publishing.

## Repository-state issues affecting confidence

1. The implementation inventory is available at `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md` and was used as the implementation authority for this revision.
2. The inventory covers the current product checkout, including uncommitted implementation files, and notes that release/production status of those files should be confirmed before publication.
3. Commercial claims such as prices, trial terms, and comparative TCO are not established by product implementation evidence and remain conservatively classified.
4. The website working tree already contains unrelated changes/untracked files (`.gitignore` deletion, modified `index.html`, `New Text Document.txt`, `index-legacy.html`, and `tmp/`). They were not modified by this audit.
5. The static site has multiple tracked versions/pages with differing claims, and the sitemap does not enumerate every HTML page. Publishing configuration should be checked before treating “current website” as equivalent to every tracked HTML file.
