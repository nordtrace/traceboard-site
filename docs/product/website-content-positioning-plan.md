# Website Content & Positioning Plan

**Planning date:** 2026-09-09  
**Website repository:** `D:\Dev\MyCode\traceboard-site\traceboard-site`  
**Product source of truth:** `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md`  
**Website audit:** `D:\Dev\MyCode\traceboard-site\traceboard-site\docs\product\website-claim-audit.md`

## 1. Executive Summary

TraceBoard Suite should be positioned as a **self-hosted engineering traceability and evidence platform for teams that need structured, reviewable engineering work without the weight of a traditional enterprise ALM rollout**.

The central message should not be “AI-powered requirements management.” The stronger and more truthful idea is:

> **TraceBoard Suite keeps the engineering model deterministic and reviewable, while AI assists with analysis, generation, import, querying, and narrative work. Humans decide what becomes authoritative engineering data.**

The current homepage is a strong starting point. Its connected engineering model, requirements → work → verification → evidence chain, three-product relationship, optional AI, human review, self-hosting, and regulated-engineering context should be retained. The plan is refinement and cross-page consistency, not a wholesale homepage redesign.

### Immediate priorities

1. Remove the current ReqIF claims from `traceboard-features.html` and the ReqIF roadmap claim from `traceboard-ai-approach.html` unless the product policy intentionally maintains a clearly separated roadmap area.
2. Establish one cross-page vocabulary for deterministic engineering data, AI proposals, review, committed content, baselines, Engineering State, standards-aware assessment, and self-hosted operation.
3. Add Engineering State, provenance, baselines, TraceDocs controlled documentation, and TraceTest evidence as concrete differentiators.
4. Qualify offline, LLM compatibility, standards, portability, and integration claims according to the inventory.
5. Verify all pricing, trial, plan, and TCO claims commercially before implementation.

### Recommended implementation scope

Use the existing information architecture: Home, Features, Comparison, AI Approach, TCO/Pricing, Resources, and Case Study. Do not add a new page in the first implementation phase. Improve the existing pages and exclude the legacy homepage from deployment. A later dedicated interoperability or standards page is optional, not required for the first correction pass.

## 2. Core Product Positioning

### What TraceBoard Suite fundamentally is

TraceBoard Suite is an **integrated engineering traceability and evidence system**. It structures requirements, tasks, bugs, tests, risks, hazards, typed relationships, trace graphs, evidence, documentation, verification results, baselines, assessments, and project-level engineering state.

It is not best described as:

- a generic project-management tool;
- a complete enterprise risk-management platform;
- a certification or automatic compliance product;
- a traditional heavyweight ALM replacement for every enterprise integration;
- an autonomous AI engineering system; or
- a managed cloud service.

### Category

**Primary category:** self-hosted engineering traceability and evidence platform.

**Useful secondary descriptions:**

- regulated engineering management system;
- connected engineering model for requirements, work, verification, and evidence;
- lightweight, integrated ALM for engineering teams that need traceability without enterprise-tool overhead.

“Engineering traceability and evidence platform” is preferred because it describes the implemented center of gravity more accurately than “requirements management” or “compliance platform.”

### Core problem

Engineering teams often have requirements, implementation work, tests, risks, documents, and evidence spread across spreadsheets, documents, issue trackers, test tools, and manually maintained reports. As the work changes, the relationships become difficult to inspect and the team cannot confidently answer:

- Which work implements this requirement?
- What verifies it?
- What evidence supports the result?
- Which risks or hazards are connected to it?
- What changed since the last controlled snapshot?
- Is the project’s engineering state ready for the next review, without confusing readiness with certification?

### Core mechanism

TraceBoard Suite gives teams a shared engineering model with:

1. typed engineering items and explicit relationships;
2. trace graphs, matrices, completeness calculations, impact analysis, and reporting;
3. controlled baselines with approval, comparison, and baseline-scoped documentation/traceability;
4. TraceDocs for documents derived from engineering data;
5. TraceTest for execution, results, evidence, coverage, trends, reports, and commit association;
6. Engineering State as a deterministic aggregate across compliance assessment, traceability, verification, risk, consistency, change impact, and baseline readiness; and
7. optional AI assistance that proposes, analyzes, imports, generates, queries, and narrates, while human review controls what becomes committed engineering data.

### Primary differentiator

**Deterministic engineering knowledge plus reviewable AI assistance.**

Conventional requirements tools generally emphasize storage, workflow, or trace-link management. TraceBoard Suite should emphasize that the engineering model and its deterministic calculations remain inspectable and authoritative, while AI is an assistive layer rather than a hidden source of truth.

### Supporting differentiators

1. **Connected suite:** TraceBoard, TraceDocs, and TraceTest work from shared project/item references and integration events while retaining clear service boundaries.
2. **Engineering State:** a calculated, multi-dimensional view of engineering condition—not an AI opinion, certification, or generic project-health score.
3. **Controlled engineering history:** baselines, approval, comparison, traceability diffs, document generation, restore/history, and commit associations.
4. **Evidence-linked verification:** tests, results, evidence files, coverage, trends, and reports connect back to engineering items.
5. **Standards-aware support without compliance theater:** templates, clause-oriented assessment, evidence, provenance, and documentation support engineering work associated with named standards without claiming certification.
6. **Self-hosted control:** Docker Compose deployment on customer infrastructure, optional local AI, and the ability to keep the core engineering environment within the customer’s network.
7. **Practical adoption:** a lighter-weight alternative for teams that need more structure than Excel/Word but do not need every capability or integration of a large enterprise ALM platform.

### Proof points

The product inventory supports the following proof points:

- projects, requirements, tasks, bugs, tests, risks, hazards, typed relations, trace graphs, search, history, comments, attachments, sprints, and role-protected CRUD;
- baseline snapshots, approval, comparison, and baseline-scoped traceability/document-diff behavior;
- CSV, XLSX, JSON, and PDF outputs in specific endpoints, with exact format dependent on the operation;
- TraceDocs Markdown/folders, links to engineering items, baseline-derived generation, preview, PDF/DOCX export, document import, branding, restore/recycle, and commit history;
- TraceTest runs, Pass/Fail/Blocked results, evidence file management, coverage, trends, reports, and commit association;
- Engineering State across seven dimensions with defined inputs and thresholds;
- AI query, import, task/test generation, consistency checking, and audit-narrative flows;
- OIDC support, RBAC, audit logging, rate limiting, Docker Compose self-hosting, and local Ollama/OpenAI-compatible AI configuration.

## 3. Message Hierarchy

### Level 1 — Core promise

> **Make engineering relationships, verification, and evidence visible—and keep the engineering model reviewable as the work changes.**

Shorter homepage direction:

> **Connected engineering, with a deterministic core.**

This preserves the current homepage’s connected-engineering language while introducing the key differentiator.

### Level 2 — Why it is different

The website should consistently communicate four ideas:

1. **One connected engineering model:** requirements, work, tests, risks, hazards, documents, and evidence are related rather than scattered.
2. **Deterministic engineering state:** traceability, coverage, assessments, risk evidence, consistency, change impact, and baseline readiness are calculated from persisted engineering facts.
3. **AI assists; humans decide:** AI can propose or interpret, but generated content and analytical interpretation do not silently become authoritative data.
4. **Controlled, customer-owned operation:** self-hosted Docker deployment, local AI options, controlled baselines, and customer infrastructure support regulated or privacy-sensitive environments.

### Level 3 — What it actually does

Organize capability explanations into five groups:

- **Model:** requirements, tasks, bugs, tests, risks, hazards, relations, trace graphs, search, history, comments, evidence.
- **Control:** baselines, approval, comparison, versioned documentation, restore/history, audit logs, RBAC.
- **Verify:** test runs, results, evidence, coverage, trends, reports, commit association.
- **Assess:** standards-aware assessments, clause-level evidence/provenance, consistency, risk/hazard evidence, Engineering State.
- **Assist:** AI query, import, task/test proposals, consistency analysis, audit narratives, and controlled generation.

### Level 4 — Evidence

Every high-level claim should link or point to a concrete mechanism. Prefer:

- “baseline-derived document generation” over “audit-ready documents”;
- “coverage and trends from recorded test results” over “complete verification”;
- “assessment findings with provenance and review state” over “automatic compliance”;
- “AI-generated proposals require review” over “AI automates engineering”; and
- “configured local or OpenAI-compatible endpoint” over “works with every LLM.”

### Level 5 — Fit and boundaries

The website should state, without making the page defensive, that TraceBoard Suite is:

- self-hosted rather than a managed cloud service;
- suitable for regulated engineering support, not a certification authority;
- capable of local operation with appropriate configuration, while OIDC, Git, and cloud LLM integrations require connectivity;
- interoperable through specific implemented operations, not ReqIF or arbitrary requirements-tool interchange; and
- a practical fit for small-to-mid-sized engineering teams that value traceability and evidence but may not need a large enterprise ALM ecosystem.

## 4. Product Differentiators

| Differentiator | Product truth | Website treatment |
|---|---|---|
| Deterministic engineering model | Typed items, explicit relations, trace graphs, calculations, assessments, Engineering State | Make this the central conceptual distinction from AI-generated content |
| Reviewable AI | AI query/import/generation/consistency/audit flows; outputs can be empty, incomplete, or semantically wrong | Show the proposal/review/commit boundary, not autonomous automation |
| Engineering State | On-demand aggregate across compliance, traceability, verification, risk, consistency, change impact, and baseline readiness | Add as a concrete feature and explain its limits |
| Baselines | Snapshots, approval, comparison, baseline-scoped traceability/document differences | Explain as controlled answers to “what was true at this point?” |
| TraceDocs | Controlled Markdown/documents, baseline-derived generation, PDF/DOCX, links, history/restore/branding | Present as controlled engineering documentation, not merely PDF generation |
| TraceTest | Runs, results, evidence, coverage, trends, reports, commit associations | Present as evidence-connected verification, not merely test tracking |
| Standards-aware engineering | Named-standard analysis/templates/assessments and evidence/provenance | Use scoped standards language; never imply certification |
| Self-hosted control | Docker Compose, customer infrastructure, local Ollama/OpenAI-compatible option | Preserve prominently, qualify network-dependent options |
| Practical alternative to heavyweight ALM | Integrated scope with candid limits around deep enterprise integrations | Use comparison/TCO pages, but substantiate time/cost claims |

## 5. Website Information Architecture

### Recommended structure

Retain the existing publishable structure:

1. **Home — `index.html`**
2. **Features — `traceboard-features.html`**
3. **Comparison — `traceboard-comparison.html`**
4. **AI Approach — `traceboard-ai-approach.html`**
5. **TCO / Pricing — `traceboard-tco.html`**
6. **Resources — `resources.html`**
7. **Case Study — `case-study.html`**

Do not create dedicated TraceBoard, TraceDocs, TraceTest, Security, Standards, or Integrations pages in the first implementation. The existing pages can communicate these subjects if their sections are made more concrete and consistent.

### Page roles

- Home creates understanding and interest.
- Features proves breadth and mechanism.
- AI Approach explains trust and review boundaries.
- Comparison explains fit against Excel and traditional ALM.
- TCO explains commercial assumptions, not product truth.
- Resources routes visitors to deeper material.
- Case Study demonstrates the architecture in one bounded scenario.

### Legacy artifact

`index-legacy.html` should be **explicitly excluded from deployment**, then moved outside the publishable tree or deleted in a separate implementation task after confirming source-control needs. It is not a page to improve. It contains managed-cloud availability/plans, stronger offline claims, older pricing/trial claims, and broader portability language that conflict with current product truth.

## 6. Page-by-Page Content Plan

| Page | Primary audience | Purpose | Primary message | Supporting messages | Important capabilities | Claims to remove | Claims to qualify | New content | CTA |
|---|---|---|---|---|---|---|---|---|---|
| `index.html` Home | Engineering leads, founders, regulated-team evaluators | Establish category, problem, mechanism, fit | Connected engineering with a deterministic core and optional reviewable AI | Requirements → work → verification → evidence; three products; self-hosting; regulated context | Connected model, TraceBoard/TraceDocs/TraceTest, baselines, evidence, AI review, self-hosting | Any remaining absolute offline, full/complete traceability, unsupported portability | Air-gapped scope, pricing/trial, “truth” wording, AI limits | Brief Engineering State and baseline explanation; bounded OIDC mention | Keep trial/demo CTAs after commercial verification |
| `traceboard-features.html` Features | Technical evaluators and engineering managers | Answer “what does it actually do?” | A concrete engineering model with controlled evidence and reviewable assistance | Model, traceability, baselines, Engineering State, TraceDocs, TraceTest, standards, deployment | All major inventory capabilities grouped by workflow | Both ReqIF claims; “COMMITTED — ReqIF”; universal LLM; zero lock-in; pre-built standards workflows | Export/import direction and fidelity; standards scope; air-gapped; provider list | Capability matrix and Engineering State section; exact interoperability matrix | Walkthrough/live demo |
| `traceboard-comparison.html` Comparison | Buyers comparing Excel, ReqView, DOORS/Polarion/Jama/Codebeamer | Explain fit and tradeoffs honestly | More structured than spreadsheets, lighter than a heavyweight enterprise ALM rollout | Connected evidence, self-hosting, reviewable AI, candid integration boundaries | Traceability, baselines, evidence, pricing assumptions, self-hosting | Universal “full traceability,” unsupported DOORS/ReqIF implication, zero lock-in | Cost, setup time, air-gapped, “enterprise,” LLM, standards | Add “best fit / not fit” capability boundaries and exact integration wording | Live demo / walkthrough |
| `traceboard-ai-approach.html` AI | AI-risk-conscious engineering and compliance evaluators | Explain why AI can be trusted within boundaries | AI assists the engineering model; it does not own engineering truth | Propose → validate → approve → commit; deterministic state; local/control options | AI query/import/task/test generation/consistency/audit narrative, provenance, human review | ReqIF roadmap row if roadmap is not intentionally public; no-cloud dependency; every-module offline; universal LLM | Local/cloud network conditions; model limitations; deterministic versus semantic truth | Add a simple trust diagram and “what AI does / does not do” table | Read case study / book walkthrough |
| `traceboard-tco.html` TCO/Pricing | Commercial buyer, budget owner, tool evaluator | Explain cost assumptions and fit | Compare total cost transparently, without pretending the comparison is a quote | License/setup assumptions, team size, admin overhead, when a larger tool is justified | Pricing model, self-hosted deployment, fit boundaries | Any stale or inconsistent price/trial claims | All values, competitor assumptions, setup-time claims, “lower cost” generalizations | “Verified as of” date, methodology note, commercial owner sign-off | View verified pricing / contact sales |
| `resources.html` Resources | Visitors seeking proof | Route to comparison, AI, engineering note | Learn the product’s approach before buying | AI review model, comparison, internal engineering note | Links to deeper evidence | “All-in-one” if it implies arbitrary ALM scope; fully offline zero-AI claim | Resource descriptions and engineering-note generalization | Add Engineering State/baseline resource link if existing page capacity allows | Open resource / book walkthrough |
| `case-study.html` Engineering Note | Automotive technical and compliance reviewers | Explain one bounded internal test scenario | Reviewable-AI boundaries helped expose a specific import traceability defect | Source-ID preservation, deterministic versus LLM information, human checkpoint | AI import, Audit Narrative, provenance, source IDs, review, ISO 26262 context | Any implication that all traceability bugs are automatically caught | Internal-test scope, publication date, pending release version, model names, historical defect status | Add scenario scope, diagram, metadata, and explicit non-guarantee note | Read AI approach / request walkthrough |
| `index-legacy.html` Legacy artifact | None; publishing-risk review only | Prevent accidental publication | Not a public page | — | — | Managed cloud, old pricing, absolute offline, zero lock-in, unsupported broad claims | Do not improve or republish | Add deployment exclusion/removal task | None |

## 7. Homepage Strategy

The homepage should remain concise and should continue to function as the visitor’s first orientation. Do not turn it into the complete product catalog.

### Required visitor understanding

Within the hero and first two sections, a visitor should understand:

1. TraceBoard Suite is for engineering teams managing requirements, work, verification, and evidence.
2. It connects those relationships in a shared engineering model.
3. The model is deterministic and inspectable; AI is optional assistance, not silent authority.
4. The suite includes TraceBoard, TraceDocs, and TraceTest.
5. It is self-hosted and relevant to regulated engineering teams.

### Recommended homepage flow

1. **Hero:** retain “Traceable engineering for modern engineering teams,” but add a concise deterministic-core distinction in the supporting copy.
2. **Engineering model:** retain the current need → requirement → work → verification → evidence chain and the explanation that it is a model, not a mandatory workflow.
3. **Problem/foundation:** retain connected relationships, but use “connected engineering data/model” where “single source of truth” could be interpreted literally.
4. **Suite views:** retain TraceBoard/TraceDocs/TraceTest; add one concrete line per product:
   - TraceBoard: structure items and relationships.
   - TraceDocs: create controlled documents from engineering data and baselines.
   - TraceTest: execute tests and connect results/evidence to engineering items.
5. **Trust model:** add a compact “deterministic core / AI assistance / human review” block.
6. **Evidence and control:** strengthen baselines, evidence, and Engineering State without listing every submetric.
7. **Deployment:** retain Docker/self-hosted/customer infrastructure. Qualify that OIDC, Git, and cloud AI require connectivity.
8. **Fit/pricing:** retain pricing/trial only after commercial verification; otherwise use a neutral “see current plans” CTA.
9. **FAQ:** add bounded answers for Engineering State, baselines, OIDC, standards scope, and offline operation.
10. **Final CTA:** retain trial/demo direction after validating endpoint and offer details.

### Homepage content not to add

Do not add a long standards matrix, exhaustive format list, provider list, or deep security architecture to the homepage. Link those details to Features, AI Approach, Comparison, or a future dedicated page if needed.

### Example positioning direction

This is direction, not final website copy:

> TraceBoard Suite connects requirements, work, verification, risks, documents, and evidence in a deterministic engineering model. AI can help import, analyze, query, and propose; your team reviews what becomes part of the committed engineering record.

## 8. Features Page Strategy

The Features page should become the evidence-backed product map. Replace broad principles and unsupported claims with a small number of capability groups.

### Recommended section order

1. **The engineering model** — items, relations, trace graphs, search, history, comments, evidence.
2. **Traceability and impact** — explicit links, matrices, completeness calculations, impact analysis, reporting, specific exports.
3. **Baselines and controlled change** — snapshots, approval, comparison, baseline-scoped traceability, document differences.
4. **Engineering State** — seven dimensions, deterministic inputs/thresholds, on-demand calculation, limits.
5. **TraceDocs** — controlled documents, Markdown/folders, baseline-derived generation, preview, PDF/DOCX, links, branding, restore/history.
6. **TraceTest** — runs, results, evidence, coverage, trends, reports, commit association.
7. **Standards-aware engineering** — named standards, templates, assessments, clause-level evidence/provenance; explicit non-certification note.
8. **AI assistance** — link to the full AI Approach page rather than repeating provider marketing.
9. **Deployment and control** — Docker Compose, self-hosted, local AI, OIDC/RBAC, network-dependent integrations.
10. **Interoperability matrix** — exact operation and direction by format.

### Feature page content rules

- Use “implemented” only for capabilities confirmed by the inventory.
- Use “supports” with a specific operation, not a vague ecosystem promise.
- Do not say “complete,” “full,” “seamless,” “virtually any,” or “zero lock-in” unless a separately reviewed claim is genuinely supportable.
- For every standards section, state that the product supports engineering assessment/evidence work and does not certify the customer’s product.

## 9. AI Page Strategy

The AI page should be one of the strongest pages because it explains the product’s most defensible differentiation.

### Recommended conceptual sequence

Use:

> **Understand → Propose → Validate → Review → Commit**

This is clearer for non-technical visitors than “Propose → Validate → Approve → Commit,” while preserving the existing approval concept. “Understand” should not imply that AI independently understands the complete engineering domain; it should refer to the configured project context and source material it is given.

If implementation terminology or UI labels require exact consistency, retain “Propose → Validate → Approve → Commit” as the product workflow label and use “Understand” only as explanatory framing.

### What AI does

- project-grounded querying where configured;
- assistance with importing source material;
- proposed task and test generation;
- consistency analysis;
- audit narrative generation;
- suggestions and analysis around engineering data;
- controlled interpretation of deterministic metrics and findings.

### What AI does not do

- guarantee correctness;
- certify compliance;
- independently maintain authoritative engineering truth;
- know that an unentered relationship should exist;
- make every engineering decision autonomously;
- turn every imported PDF, DOCX, Excel workbook, or external tool export into a full-fidelity model;
- work with every LLM or integration without configuration and testing.

### What remains deterministic

- stored engineering items and relationships;
- graph traversal and traceability calculations;
- coverage/report calculations from recorded results;
- Engineering State inputs and thresholds;
- baseline snapshots, comparison, and approval state;
- persisted evidence, provenance, and review/commit state;
- deterministic parts of assessment and narrative evidence.

### What requires human review

Generated or proposed tasks/tests, imported interpretations, AI-created relationships, consistency findings, narrative recommendations, and any content that will become committed engineering data. The language should emphasize that review is a product boundary, not a disclaimer added after the fact.

### Where AI can run

- local Ollama configuration;
- OpenAI-compatible HTTP endpoint configuration;
- cloud LLM use where configured and network access is available.

Do not claim that every named provider is a separately tested native integration unless product evidence is added. The useful message is control over the endpoint and data path, not a long provider logo list.

### Offline explanation

Recommended direction:

> The core suite can be self-hosted, and AI can use a local model. OIDC, remote Git integrations, and cloud LLMs require connectivity to those external services.

Do not use “no cloud dependency” as the headline, because it is too broad across all optional configurations.

## 10. Standards & Compliance Strategy

### Positioning model

TraceBoard Suite should say that it **supports standards-aware engineering and evidence work**. It should not say that it makes a customer’s product compliant or certified.

### Recommended standards wording

Preferred concepts:

- standards-aware templates and assessments;
- clause-level or requirement-level assessment where implemented;
- evidence and provenance connected to engineering items;
- controlled documentation and baseline comparison;
- support for audit preparation and engineering review;
- human and qualified compliance review remain necessary.

Avoid:

- “compliant with IEC 62304”;
- “automatic compliance”;
- “certification-ready” unless narrowly defined and approved;
- “complete compliance management”;
- “guaranteed audit success.”

### Standards scope table

A concise table on the Features page is recommended:

| Standard/topic | Truthful product scope | Boundary |
|---|---|---|
| IEC 62304 | Standards-aware analysis, templates, assessment/evidence support where implemented | Not certification or complete standard implementation |
| ISO 14971 | Risk/hazard items, relations, matrices, deterministic evidence and assessment support | Not a complete enterprise risk-management system or automatic compliance verdict |
| ISO 26262 | Standards-aware engineering context, assessment/evidence support, normative-strength context where implemented | Not proof of functional-safety compliance or certification |
| DO-178C | Standards-aware analysis/template/assessment support where implemented | Not a complete DO-178C workflow or certification |

The exact table contents should be checked against the inventory’s detailed standard coverage before publication. The table should communicate scope, not serve as a standards logo wall.

## 11. Engineering State Strategy

Engineering State should become a meaningful product differentiator, but it must be explained as a deterministic calculated view rather than a release verdict.

### Simple explanation

> **Engineering State summarizes the condition of the project’s recorded engineering model across compliance assessment, traceability, verification, risk, consistency, change impact, and baseline readiness.**

### What it answers

Engineering State helps answer:

> “Based on the engineering facts currently recorded, where does this project need attention?”

It should not be framed as answering:

> “Is the product certified?” or “Can we release?”

### Recommended placement

1. Homepage: one compact differentiator card after the connected suite section.
2. Features page: a dedicated detailed section with the seven dimensions.
3. AI page: explicitly distinguish deterministic Engineering State from AI narrative interpretation.
4. FAQ: explain that it is calculated from available persisted facts and is not an independent compliance verdict.

### Recommended dimensions

- Compliance assessment state
- Traceability
- Verification
- Risk
- Consistency
- Change impact
- Baseline readiness

### Guardrails

State that it is on-demand, deterministic, threshold-based, and dependent on the data recorded in the system. Do not call it a generic health score, AI opinion, certification, or release approval.

## 12. TraceDocs / TraceTest Strategy

### TraceDocs

Position TraceDocs as:

> **Controlled engineering documentation derived from project data and selected baselines.**

Emphasize:

- Markdown documents and folders;
- links between documents and engineering items;
- baseline-derived generation and preview;
- PDF/DOCX export;
- document import within the implemented scope;
- branding;
- restore/recycle behavior and commit history;
- document differences tied to controlled engineering snapshots.

Avoid reducing TraceDocs to “PDF generation” or implying arbitrary document generation, arbitrary specification parsing, or user-defined template support unless that capability is confirmed as current rather than planned.

### TraceTest

Position TraceTest as:

> **Verification execution and evidence connected back to the engineering model.**

Emphasize:

- test runs;
- Pass/Fail/Blocked results;
- evidence file management;
- requirement/test relationships;
- coverage and trends;
- reports;
- commit association.

Avoid “complete verification,” “every requirement proven,” or other absolute language. The product can report on recorded tests and relationships; it cannot prove that an unrecorded test or omitted relationship should exist.

### Suite relationship

Use “integrated suite with shared project/item references and event/API integration.” Avoid saying every operational record is literally stored in one database. TraceBoard owns domain data; TraceDocs and TraceTest are separate services with their own operational data.

## 13. Interoperability Strategy

Interoperability should be explicit and operational rather than aspirational.

### Recommended capability matrix

The Features or Comparison page should include a compact matrix like this, with final operation names verified against the inventory before implementation:

| Format/integration | Truthful direction/scope | Website wording |
|---|---|---|
| CSV | Specific report/matrix exports; no general CSV import established | “CSV export in supported reporting/matrix operations” |
| XLSX/Excel | Product-specific workbook import/export | “Supported workbook operations,” not Excel synchronization |
| JSON | API/project/report operations where implemented | Name the endpoint or operation category |
| PDF | Reports, snapshots, and generated documents | Do not imply arbitrary PDF specification parsing |
| DOCX | TraceDocs export/document-model conversion and supported import | Do not imply full-fidelity arbitrary DOCX interchange |
| Markdown | TraceDocs document authoring/organization | Safe to describe as a document authoring format |
| API | Implemented APIs and generated schemas | Do not imply a public support program or unlimited integration guarantee |
| GitHub/GitLab/Gitea | Only describe the exact implemented provider, direction, verification/webhook behavior, and connectivity requirements | Avoid broad “Git integrations” unless scoped |
| ReqIF | Not implemented | Never claim or imply |
| DOORS | No generic/ReqIF interchange established | Do not use “DOORS export” as a migration promise |

### Interoperability language

Prefer:

- “specific import/export operations”;
- “endpoint-specific JSON/CSV/XLSX/PDF outputs”;
- “TraceDocs PDF/DOCX document operations”; and
- “configured Git provider integration,” where exact provider and direction are known.

Avoid:

- “works with everything”;
- “full portability”;
- “zero lock-in”;
- “seamless interchange”; and
- “open standards” when the visitor could reasonably infer ReqIF.

## 14. Deployment & Security Strategy

### Core deployment message

> **Run the suite on your infrastructure with Docker Compose, with the option to keep engineering data and AI processing inside your network.**

This is accurate and commercially meaningful without promising managed hosting.

### Distinguish operation classes

| Operation | Core truth | Network qualification |
|---|---|---|
| Core self-hosted suite | Docker Compose on customer infrastructure | Can be operated locally according to deployment configuration |
| Local AI | Ollama/OpenAI-compatible local endpoint | Can avoid external AI service calls when configured locally |
| Cloud LLM | Configurable cloud/provider endpoint | Requires network access and provider configuration |
| OIDC | Supported SSO | Requires reachable external identity provider/configuration |
| Git integration | Implemented scope depends on provider/configuration | Remote provider access requires connectivity |
| Managed cloud | Not implemented | Must not be offered as current deployment |
| SAML | Not implemented; planned in internal product documentation | Must not be presented as supported |

### Security content

The website may mention OIDC, RBAC, audit logging, rate limiting, customer infrastructure, and local AI if each statement is scoped. It must not imply security certification, enterprise SLA, managed operations, encryption guarantees, or comprehensive enterprise security beyond the inventory.

Recommended placement:

- homepage: one concise self-hosting/control statement;
- Features: deployment and access-control details;
- AI page: local/cloud model path;
- Comparison: self-hosted versus cloud-only fit;
- FAQ: OIDC and network-dependent integrations.

## 15. Pricing / Commercial Verification

The product inventory does not establish commercial terms. Before content implementation, a commercial owner must verify:

- current license prices and currencies;
- plan names and included features;
- supported team-size ranges;
- whether pricing is flat, per-seat, or otherwise constrained;
- trial duration and whether it includes the full current feature set;
- license download and activation behavior;
- whether AI usage is included or separately metered;
- TCO assumptions and competitor pricing sources;
- setup-time and admin-effort claims;
- whether “available Q4 2026” or any managed-cloud language remains in legacy materials.

### Page consistency concern

The current site has conflicting or outdated commercial material across `index.html`, `traceboard-features.html`, `traceboard-tco.html`, and `index-legacy.html`, including different trial language and managed-cloud plan references. Do not change prices or trial copy as part of a technical content pass. Mark each commercial fact for sign-off, then update all pages from one approved source.

### TCO methodology

Retain the TCO page’s transparency about assumptions, but label estimates as estimates, date the inputs, separate TraceBoard facts from competitor generalizations, and avoid presenting a lower cost as proof of better fit for every team.

## 16. Case Study Strategy

The case study should support the broader architecture story, not become a product guarantee.

### Core role

Demonstrate how a specific internal test scenario exposed a source-ID/traceability problem through the interaction of deterministic import behavior, independent AI analysis, and human review.

### What to emphasize

- the source document had messy hierarchical IDs;
- AI Import and Audit Narrative operated on the available data;
- the deterministic import transformation was the relevant defect location;
- source-ID preservation and ambiguity flags were added;
- deterministic counts/statuses/links can be separated from LLM interpretation;
- generated tasks/tests are opt-in and reviewable.

### What to avoid

- “TraceBoard automatically catches traceability bugs”;
- “AI cannot make mistakes”;
- “every audit finding is correct”;
- “the system guarantees traceability”; and
- extrapolating one internal test to universal product performance.

### Recommended framing

Label it as an internal test case with the product/version and model context where available. State that it demonstrates the value of the review boundary in this scenario; it does not guarantee detection of every import or traceability defect.

## 17. Terminology Guide

| Concept | Preferred wording | Avoid | Reason |
|---|---|---|---|
| Engineering truth | “authoritative committed engineering data” or “deterministic engineering model” | “AI truth,” “single database truth” | Separates authority from marketing metaphor and architecture detail |
| Engineering data | “requirements, work, verification, risks, documents, evidence, and relationships” | “all data everywhere” | Defines scope concretely |
| Engineering model | “connected model of recorded items and relationships” | “complete model of the product” | The system cannot infer omitted relationships |
| Deterministic | “calculated from persisted engineering facts using defined rules/thresholds” | “always correct” | Determinism does not guarantee input completeness or semantic correctness |
| AI-assisted | “AI proposes, analyzes, generates, queries, imports, or narrates within configured context” | “AI-powered autonomous engineering” | Reflects implementation and review boundaries |
| AI-generated | “proposed/generated content labeled for review” | “approved content” | AI output is not authoritative by default |
| Proposed | “not yet committed as authoritative engineering data” | “validated truth” | Makes state explicit |
| Reviewed/approved | “human-reviewed and accepted according to the workflow” | “guaranteed correct” | Review is a control, not proof of perfection |
| Committed | “accepted into the project’s authoritative engineering record” | “certified” | Commitment is product state, not regulatory approval |
| Traceability | “explicit relationships and calculations over recorded relationships” | “guaranteed complete traceability” | Avoids semantic-completeness overclaim |
| Compliance assessment | “standards-aware assessment with findings/evidence/provenance” | “compliant,” “certified,” “automatic compliance” | Correctly scopes the product’s role |
| Audit preparation | “evidence and documentation that support review/audit preparation” | “audit approval” | Customer/qualified reviewers remain responsible |
| Baseline | “controlled snapshot for comparison, traceability, and documentation” | “immutable compliance proof” | Captures actual function without overclaim |
| Engineering State | “deterministic aggregate of defined engineering dimensions” | “release approval,” “certification score,” “AI health score” | Explains scope and limits |
| Self-hosted | “deployed by the customer on customer infrastructure” | “managed private cloud” | Managed cloud is not implemented |
| Air-gapped | “core self-hosted/local configuration can operate without external network calls” | “every integration works offline” | OIDC, Git, and cloud LLMs need connectivity |
| Offline | “local operation under a specified configuration” | “fully offline in every configuration” | Makes dependencies explicit |
| Integration | “implemented connection with a named provider and direction” | “works with all tools” | Prevents vague compatibility promises |
| Interoperability | “specific supported import/export/API operations” | “zero lock-in/full portability” | Exact operations are the evidence |

## 18. Claim Guardrails

### Never claim in the current product

Unless the implementation changes and the capability inventory is updated:

- ReqIF import/export;
- SAML support;
- managed cloud hosting;
- automatic certification or guaranteed compliance;
- complete implementation of IEC 62304, ISO 14971, ISO 26262, or DO-178C;
- universal LLM/provider compatibility;
- zero lock-in or full-fidelity export of everything;
- universal offline operation;
- complete enterprise risk management;
- guaranteed or complete traceability;
- AI that independently maintains engineering truth;
- a generic Engineering State release/certification verdict.

### Prefer

- exact supported formats and directions;
- named and verified integrations;
- standards-aware assessments, templates, evidence, and provenance;
- deterministic calculations over recorded engineering relationships;
- AI-assisted/proposed/generated content;
- explicit human review and commit boundaries;
- self-hosted/local operation with network exceptions;
- baselines as controlled snapshots;
- Engineering State as a deterministic aggregate;
- TraceDocs as controlled documentation and TraceTest as evidence-connected verification.

### Editorial review checklist

Before publishing any new claim, ask:

1. Is the capability in the current inventory as implemented rather than planned or limited?
2. Does the exact wording match the operation, direction, and scope actually implemented?
3. Could a reasonable buyer infer certification, managed hosting, universal compatibility, or semantic completeness?
4. Does the claim distinguish deterministic data from AI interpretation?
5. Does the same concept use the same wording on every page?
6. Is the claim commercial, and if so, has a commercial owner verified it?

## 19. Cross-Page Consistency Matrix

Legend: **✓** present; **△** present but incomplete/needs qualification; **—** absent; **REMOVE** contradictory/unsupported content.

| Concept | Homepage | Features | AI | Comparison | TCO | Resources | Case Study | Required wording |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| Connected engineering model | ✓ | ✓ | △ | ✓ | — | △ | ✓ | Connected model of recorded engineering items and relationships |
| Requirements → work → verification → evidence | ✓ | ✓ | △ | ✓ | — | — | ✓ | Core engineering chain, not mandatory workflow or guaranteed completeness |
| TraceBoard / TraceDocs / TraceTest | ✓ | △ | — | △ | — | — | △ | Integrated suite with shared references and service boundaries |
| Deterministic engineering model | △ | △ | ✓ | △ | — | △ | ✓ | Deterministic calculations over recorded engineering data |
| AI optional | ✓ | ✓ | ✓ | ✓ | — | ✓ | ✓ | AI is optional and configured; deterministic core remains authoritative |
| AI proposal/generation | △ | ✓ | ✓ | ✓ | — | ✓ | ✓ | AI-generated/proposed content requires review |
| Human approval/review | ✓ | ✓ | ✓ | ✓ | — | △ | ✓ | Review/approval controls what becomes committed |
| Engineering State | — | — | △ | — | — | — | — | Add bounded deterministic aggregate explanation |
| Baselines | ✓ | △ | — | △ | — | — | — | Controlled snapshots for comparison, traceability, and documents |
| Evidence/provenance | △ | △ | ✓ | △ | — | — | ✓ | Distinguish deterministic evidence from LLM interpretation |
| Standards | △ | ✓ | — | ✓ | — | △ | △ | Standards-aware assessments/evidence, not certification |
| Risk/hazard | ✓ | △ | △ | △ | — | — | △ | Typed risk/hazard relationships and evidence, not full ERM |
| Air-gapped/self-hosted | ✓ | ✓ | ✓ | ✓ | ✓ | △ | — | Core local/self-hosted operation; external integrations need connectivity |
| OIDC/SSO | — | — | — | — | — | — | — | Add bounded OIDC mention; do not add SAML |
| Git integrations | △ | △ | — | △ | — | — | — | Name provider, direction, verification, and network need |
| Excel/CSV/PDF/DOCX/JSON | △ | ✓ | △ | △ | △ | — | — | Exact endpoint/operation, not generic portability |
| ReqIF | — | REMOVE | REMOVE | △ | — | — | — | Never claim or imply; remove DOORS/ReqIF ambiguity |
| Managed cloud | — | △ | — | △ | △ | — | — | Not current; exclude legacy page |
| Pricing/trial | ✓ | ✓ | — | ✓ | ✓ | — | — | Commercially verified, dated, and consistent |

The matrix should be used as a copy-review checklist during implementation. A page may omit a concept intentionally, but it must not contradict the required wording.

## 20. Prioritized Implementation Plan

### Phase 1 — Accuracy fixes (**MUST**)

1. Remove both ReqIF claims from `traceboard-features.html`.
2. Remove or clearly segregate the ReqIF roadmap row from `traceboard-ai-approach.html`.
3. Exclude `index-legacy.html` from deployment and plan its removal/move outside the publishable tree.
4. Remove/qualify absolute offline, no-cloud, universal LLM, zero lock-in, full export, and pre-built standards-workflow claims.
5. Remove DOORS/ReqIF implications from comparison and feature CTAs.

### Phase 2 — Cross-page consistency (**MUST**)

1. Apply the terminology guide to all seven publishable pages.
2. Establish one approved statement for self-hosted/air-gapped/local AI operation.
3. Establish one approved statement for standards-aware assessment and non-certification boundaries.
4. Establish one approved statement for deterministic model, AI proposals, human review, and committed data.
5. Ensure pricing/trial references are either verified and synchronized or temporarily narrowed to a neutral CTA.

### Phase 3 — Product differentiation (**SHOULD**)

1. Add Engineering State to the homepage and Features page.
2. Strengthen baseline positioning as controlled snapshots for comparison, traceability, and documentation.
3. Explain provenance and deterministic versus LLM-derived evidence.
4. Replace generic feature cards with the five capability groups: Model, Control, Verify, Assess, Assist.
5. Reframe TraceDocs and TraceTest around their relationship to the engineering model.

### Phase 4 — AI positioning (**SHOULD**)

1. Reorganize the AI page around Understand → Propose → Validate → Review → Commit.
2. Add “what AI does” and “what AI does not do” sections.
3. Explain local/configured endpoint options and cloud/network exceptions.
4. Use the case study as bounded evidence of the architecture, not a product guarantee.

### Phase 5 — Supporting content (**SHOULD**)

1. Add the standards scope table.
2. Add the interoperability capability matrix.
3. Add bounded OIDC/RBAC/security and external-service language.
4. Clarify comparison fit and integration boundaries.
5. Add a compact Engineering State/baseline FAQ.

### Phase 6 — Commercial verification (**MUST before commercial copy changes**)

1. Obtain approved current pricing, trial, plan, and feature-entitlement facts.
2. Verify TCO inputs, competitor assumptions, and date them.
3. Reconcile every commercial statement across Home, Features, Comparison, TCO, and legacy artifacts.
4. Verify all trial/download/demo endpoints and CTA behavior.

### Phase 7 — Final truth audit (**MUST**)

1. Re-run the website claim audit against the modified website.
2. Search specifically for ReqIF, SAML, managed cloud, certification, complete/full, seamless, universal, zero lock-in, offline, Engineering State, baseline, OIDC, and standards terms.
3. Compare every claim against the updated product inventory.
4. Check the publishing tree and sitemap for legacy files.
5. Confirm that no page contradicts the cross-page matrix.
