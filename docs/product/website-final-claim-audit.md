# TraceBoard Suite Final Website Claim Audit

**Audit date:** 2026-09-09  
**Repository:** `D:\Dev\MyCode\traceboard-site\traceboard-site`  
**Audit type:** Independent final claim audit; no website or product corrections made.

## 1. Executive Summary

### Rating: **Significant corrections required**

The current, intended seven-page website is substantially more credible than the legacy content. It generally communicates a self-hosted product, an optional AI layer, human review, configured local/cloud model endpoints, explicit network dependencies, bounded data operations, and a deterministic Engineering State boundary. Current pages do **not** make a positive ReqIF or SAML support claim, and the current comparison page explicitly places ReqIF/requirements-tool interchange outside scope.

It is nevertheless not safe to publish as-is. The most serious issue is publication control: the repository contains `index-legacy.html`, and no deployment, build, server, hosting, or ignore configuration exists that prevents an arbitrary root HTML file from being served. That file contains stale positive claims including “Air-Gap Ready,” “deterministic, end-to-end traceability,” compliance exports, “full audit trail,” custom templates, and CI/CD-generated test runs. A direct URL could therefore expose materially misleading content even though it is absent from the sitemap.

Current-page risks are mainly targeted rather than systemic: an AI metadata claim says local models operate “without data leaks”; some traceability and audit-language remains stronger than the product boundary; the case study and competitor/TCO/pricing claims require evidence or commercial approval; and repeated pages can drift. The site also still undersells or inconsistently explains provenance, baselines, Engineering State, OIDC boundaries, and the precise TraceDocs/TraceTest relationship.

The product inventory named in the brief was not present in this website repository. The referenced sibling file at `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md` was available and used as product evidence. The report distinguishes that external inventory from evidence available in this repository.

## 2. Audit Scope

### Authoritative and contextual sources inspected

- `D:\Dev\MyCode\traceboard-suite\docs\product\product-capability-inventory.md` — external product implementation inventory, used because the requested local inventory is absent.
- `D:\Dev\MyCode\traceboard-site\traceboard-site\docs\product\website-claim-audit.md`.
- `D:\Dev\MyCode\traceboard-site\traceboard-site\docs\product\website-content-positioning-plan.md`.
- `D:\Dev\MyCode\traceboard-site\traceboard-site\docs\product\website-content-positioning-implementation.md`.

### Current website pages inspected

- `index.html`
- `resources.html`
- `traceboard-features.html`
- `traceboard-comparison.html`
- `traceboard-ai-approach.html`
- `traceboard-tco.html`
- `case-study.html`
- `sitemap.xml`

### Legacy and other publication candidates inspected

- `index-legacy.html` — large stale homepage.
- `old_index.html` — minimal older homepage.
- `README.md`, workspace file, root file inventory, Git metadata, and all root-level HTML.

### Deployment/publication configuration inspected

No deployment configuration, build manifest, package manifest, hosting rule, web-server configuration, Docker configuration, CI/CD workflow, `robots.txt`, or valid `.gitignore` was found in this repository. `.gitignore` is deleted in the current working tree. The existing implementation report reaches the same conclusion.

### Verification performed

- Read all current and legacy HTML files.
- Searched all HTML for ReqIF, SAML, OIDC, cloud/SaaS, offline/air-gap, traceability absolutes, certification/compliance, AI/LLM, integrations, export/import, pricing and trial language.
- Parsed all nine HTML files with Python `html.parser`.
- Checked local HTML links and fragments. Current-page checks produced no missing local targets or fragments. The legacy page has stale empty/removed fragment targets including `#privacy`, `#terms`, and `#contact`.
- Parsed `sitemap.xml` as XML successfully.
- Inspected sitemap membership against root HTML files.
- Inspected Git status without changing pre-existing dirty files.
- No browser, deployed-site, responsive, visual, CSS, or hosting-runtime verification was available.

## 3. Claim Classification Summary

Counts are audit units, not occurrences; repeated wording is grouped where it expresses the same claim. They are approximate because the static pages repeat claims in headings, metadata, cards, tables, and CTAs.

| Classification | Count |
|---|---:|
| SUPPORTED | 18 |
| SUPPORTED — NEEDS PRECISION | 19 |
| OVERCLAIM | 8 |
| UNSUPPORTED | 1 |
| NOT IMPLEMENTED / ROADMAP CLAIM | 0 current-page positive claims; 1 legacy publication-surface occurrence |
| AMBIGUOUS | 14 |
| MISSING IMPORTANT CAPABILITY | 6 |

The counts include current-page and legacy-publication findings where relevant. Negative ReqIF/SAML boundary statements are not counted as unsupported capability claims.

## 4. Critical Findings

### P0 — legacy pages can probably be served directly

There is no repository-local mechanism restricting the served root to the seven intended pages. `index-legacy.html` is a root-level HTML file and contains stale claims such as:

- “Air-Gap Ready — Fully Self-Hosted”;
- “deterministic, end-to-end traceability ... across your entire development lifecycle”;
- “full audit trail” and “full traceability”;
- compliance exports and audit-ready submissions;
- custom document templates;
- CI/CD integration that creates test runs automatically from commits.

Sitemap exclusion is not access control. The hosting configuration must be checked or constrained before publication.

### P0 — current AI metadata makes a data-loss/security guarantee

`traceboard-ai-approach.html` metadata describes local private models “without data leaks.” The inventory supports configured local endpoints and customer-controlled deployment, but does not establish a guarantee of no data leakage. A reasonable buyer could interpret this as a security guarantee.

### P1 — current language still risks semantic completeness or compliance inference

The intended pages use careful qualifications in many places, but “audit-ready,” “full audit trail,” “end-to-end,” “coverage,” and strong “traceability” wording remains repeated. The inventory says relationships are based on recorded facts and cannot establish semantic completeness for relationships users never entered. Standards support is standards-aware analysis/templates/assessments/evidence, not certification or guaranteed compliance.

### P1 — commercial and competitor claims are not independently established

The site publishes exact prices, 30-day trial language, team/user ranges, “no usage-based AI billing,” competitor price comparisons, a 15-person TCO calculation, and statements about competitor setup/admin burden. The product inventory does not prove these commercial statements. They require commercial owner approval and an as-of date.

## 5. Detailed Claim Findings

| Page | Section | Claim | Classification | Buyer Interpretation | Evidence | Recommended Action |
|---|---|---|---|---|---|---|
| `traceboard-ai-approach.html` | meta description | “local, private models ... without data leaks” | OVERCLAIM | Local AI guarantees no leakage | Inventory supports local Ollama/OpenAI-compatible configuration, not a security guarantee | Remove the guarantee; state local endpoint/customer-controlled deployment and configuration responsibility |
| `index-legacy.html` | hero/meta | “Air-Gap Ready — Fully Self-Hosted”; “without sending sensitive ... to external clouds” | OVERCLAIM / publication risk | Every deployment is disconnected and safe from external transfer | Inventory says Git, OIDC, and cloud LLMs require external services; no deployment exclusion exists | P0: prevent serving legacy file; do not rely on sitemap exclusion |
| `index-legacy.html` | trace chain | “Complete Hazard-to-Test Traceability”; “unbroken, verifiable audit chains” | OVERCLAIM | Product proves complete semantic coverage from hazard to test | Inventory supports typed relationships and deterministic calculations, not relationships never recorded | Exclude legacy; if retained internally, qualify around recorded relationships |
| `index-legacy.html` | TraceDocs/TraceTest | “full audit trail,” compliance exports, custom templates, CI/CD-created test runs | SUPPORTED — NEEDS PRECISION / AMBIGUOUS | All listed workflows and entitlements are generally available | Inventory supports TraceDocs exports, TraceTest runs/evidence/coverage; exact template and CI/CD scope is not established as universal | Exclude legacy; verify each workflow against released product before any reuse |
| `index.html` | pricing/CTA | “Start 30-Day Trial” and displayed plan/pricing values | AMBIGUOUS — COMMERCIAL VERIFICATION REQUIRED | Trial, price, billing, and entitlement terms are current and guaranteed | Not established by product inventory | Commercial approval, current date, and endpoint/entitlement verification |
| `index.html` | hero/chain | connected “engineering model” and explicit recorded relationships | SUPPORTED | Requirements, work, verification, evidence and typed relations share a reviewable structure | Inventory confirms implemented engineering items, typed relations, trace graphs | Keep; retain the explicit “recorded relationships” boundary |
| `index.html` | Engineering State | deterministic aggregate across compliance, traceability, verification, risk, consistency, change impact and baseline readiness; not certification/release approval | SUPPORTED | A bounded project-condition aggregate, not regulatory approval | Directly matches inventory | Keep and make this concept a primary differentiator |
| `index.html` | deployment/FAQ | self-hosted core, local AI, with OIDC/remote Git/cloud LLM network dependencies | SUPPORTED — NEEDS PRECISION | Core can run locally, but selected integrations need network access | Matches inventory | Keep; name OIDC as external identity-provider configuration rather than implying built-in disconnected identity |
| `traceboard-features.html` | standards | standards-aware templates, assessments, evidence and named standards | SUPPORTED — NEEDS PRECISION | Product delivers complete compliance workflows for IEC 62304, ISO 14971, ISO 26262 and DO-178C | Inventory explicitly limits this to standards-aware support | Keep named scope but repeat “not certification/guaranteed compliance” near the claim |
| `traceboard-features.html` | AI | configured local/OpenAI-compatible endpoint; output depends on model/configuration | SUPPORTED | Supported endpoints are bounded, not every LLM/provider | Inventory supports configured local/OpenAI-compatible calls | Keep; avoid provider-universal interpretation |
| `traceboard-features.html` | data freedom | JSON, CSV, XLSX, PDF, DOCX and Markdown operations; ReqIF/arbitrary interchange not supported | SUPPORTED — NEEDS PRECISION | Some named operations exist, but a buyer may still assume bidirectional/full-fidelity exchange | Inventory says exact direction depends on endpoint; no ReqIF | Add directionality/operation matrix where commercially important |
| `traceboard-features.html` | TraceDocs | controlled documentation from engineering data and selected baselines | SUPPORTED — NEEDS PRECISION | Generated outputs are baseline-derived and controlled, not arbitrary document generation | Inventory confirms baseline-derived generation and PDF/DOCX export | State exact supported document workflows/templates; avoid implying custom arbitrary templates |
| `traceboard-features.html` | TraceTest | evidence-connected verification, runs, results and coverage | SUPPORTED | Test execution and evidence are linked to engineering items | Inventory confirms runs, Pass/Fail/Blocked, evidence, coverage and reports | Keep; qualify “full” coverage as calculated coverage of recorded links |
| `traceboard-comparison.html` | comparison table | competitor feature, deployment, security, integration and pricing cells | AMBIGUOUS — COMMERCIAL/EDITORIAL VERIFICATION REQUIRED | Single-cell comparison is a definitive current competitor fact | No competitor evidence in product inventory | Verify each cell, source/date it, and avoid unsupported competitor generalizations |
| `traceboard-comparison.html` | fit limits | deep ReqIF/DOORS interchange, PLM and OSLC connectors are outside current scope | SUPPORTED | No ReqIF/DOORS migration support | Inventory confirms no ReqIF; no broad legacy integration evidence | Keep; this is an important boundary |
| `traceboard-comparison.html` | traceability | recorded relationships and deterministic traceability calculations | SUPPORTED — NEEDS PRECISION | Deterministic calculations prove the model’s recorded links, not semantic completeness | Matches inventory | Keep this wording consistently; avoid “full/complete” elsewhere |
| `traceboard-ai-approach.html` | propose/validate/approve/commit | AI output remains proposed until human acceptance; deterministic core remains authoritative | SUPPORTED — NEEDS PRECISION | All AI features have an identical universal approval pipeline | Inventory confirms several AI flows and human-review positioning, but exact behavior varies by feature | Preserve “illustrative/feature-dependent” qualification |
| `traceboard-ai-approach.html` | local/cloud models | local Ollama or OpenAI-compatible HTTP endpoint; cloud requires network | SUPPORTED | Model quality and data path depend on endpoint/configuration | Direct inventory evidence | Keep; state that cloud provider data handling is outside the self-hosted core |
| `traceboard-ai-approach.html` | model sizing | smaller models may be less detailed and larger models deeper | SUPPORTED — NEEDS PRECISION | Larger always means better or “scales” universally | Inventory supports model-dependent output, not a quality guarantee | Use “may” and avoid universal model-size claims |
| `traceboard-tco.html` | cost ledger | exact TraceBoard/ReqView 15-user Year 1 figures and published-price assertions | AMBIGUOUS — COMMERCIAL VERIFICATION REQUIRED | Current market prices and assumptions are verified | Not established in product inventory | Verify sources, currency, date, tax/support assumptions, and competitor permission |
| `traceboard-tco.html` | fit assessment | hours/days setup, no dedicated admin, and enterprise tools’ recurring configuration burden | AMBIGUOUS | Universal implementation-time and competitor TCO outcome | No repository evidence sufficient to verify | Reframe as scenario/assumption or substantiate with dated sources |
| `resources.html` | resource cards | product is an “all-in-one ... ALM platform” | SUPPORTED — NEEDS PRECISION | Complete ALM replacement | Product plan explicitly rejects universal heavyweight ALM positioning | Prefer engineering traceability/evidence platform wording |
| `case-study.html` | internal engineering test | a bounded scenario made an import traceability defect visible through two LLMs, deterministic data, and human review | AMBIGUOUS | Result is reproducible/general and defect detection is guaranteed | Page identifies the internal scope and does not promise universal detection | Keep as bounded engineering note; retain publication date and pending release-version status |
| `case-study.html` | compliance/ISO 26262 discussion | scenario uses ISO 26262 terminology to identify the audience and semantic impact | SUPPORTED — NEEDS PRECISION | Engineering note demonstrates compliance or ISO certification value | Inventory supports standards-aware analysis, not certification | Keep context; explicitly avoid implying compliance outcome |

### ReqIF-specific result

No current intended page contains a positive ReqIF import, export, interchange, migration, or ReqIF-compatible exchange claim. Current occurrences are boundary statements such as “ReqIF and arbitrary ... interchange are not supported,” which are safe and useful. The legacy page scan did not find a positive ReqIF claim, but that does not reduce the P0 serving risk. The implementation report’s claim that current positive ReqIF content was removed is independently confirmed.

### SAML-specific result

No page claims SAML support. OIDC is mentioned as an external identity dependency in current pages. The inventory confirms OIDC-related functionality and no SAML implementation. No SAML roadmap claim is present in current HTML. Do not add SAML as a marketing or roadmap feature merely because it is absent.

## 6. False-Negative Findings

| Capability | Current visibility | Why it matters | Recommended attention |
|---|---|---|---|
| Engineering State | Present on homepage and features, but not consistently used as the suite differentiator | It is a rare deterministic aggregate of recorded engineering condition across multiple dimensions | P1: make it a core story, not a secondary feature |
| Controlled baselines | Mentioned, but often compressed to “versioning” or compliance context | Baselines preserve a controlled engineering state and enable comparison/document generation | P1: explain the controlled-state purpose once |
| Evidence/provenance | Present in pieces; provenance is not consistently tied to assessment/review/generated content | Buyers need to distinguish evidence lineage from correctness guarantees | P1: concise, concrete explanation |
| TraceDocs relationship | Current pages describe baseline-derived controlled documentation, but visibility varies | Stronger than a PDF generator: it turns engineering data and selected baselines into controlled artifacts | P1: use the relationship consistently |
| TraceTest relationship | Runs, evidence and coverage appear, but the engineering-state connection is not always prominent | Differentiates it from generic test tracking | P1: connect requirements, verification, evidence and state in one short explanation |
| OIDC boundary | OIDC appears mainly as a dependency, not as the supported identity mechanism | Prevents buyers from assuming SAML or generic SSO breadth | P2: add one concrete identity statement |

These are not requests for broad copy expansion. Targeted terminology and one concise explanation per concept should be sufficient.

## 7. Cross-Page Consistency

- **AI:** Generally consistent: optional/configured, model-dependent, proposed/reviewable, local or cloud. The metadata “without data leaks” contradicts this otherwise careful posture.
- **Offline:** Current pages consistently say self-hosted/local operation depends on selected configuration and that OIDC, remote Git and cloud LLMs require network access. Legacy content says “Air-Gap Ready” without these boundaries.
- **ReqIF/interoperability:** Current pages consistently state ReqIF/arbitrary full-fidelity interchange is unsupported. Legacy material is not safe to expose; generic “full traceability” wording can still imply broad interoperability to a buyer.
- **Standards/compliance:** Current pages mostly qualify standards-aware support and Engineering State as non-certification. Legacy compliance/audit language is materially stronger.
- **Traceability:** Homepage/features/comparison use more careful recorded-relationship language, but legacy and residual “full,” “complete,” “unbroken,” and “end-to-end” language can undermine it.
- **TraceDocs/TraceTest:** Current pages are directionally consistent but uneven in prominence and specificity; the homepage/FAQ is clearest.
- **Pricing:** Homepage, comparison and TCO use different contexts and claims. Exact values, user bands and competitor assumptions need one commercially controlled source.
- **Deployment:** Current pages say self-hosted; no current page implies managed SaaS directly. Legacy metadata/footer and the absence of deployment controls create the practical conflict.

## 8. AI / Deterministic Model Assessment

The current site **mostly succeeds** at the central positioning. It communicates a recorded/connected engineering model, deterministic calculations/Engineering State, optional AI, proposed output, review/approval, and model-dependent results. It also distinguishes local from cloud endpoints and states network dependencies.

It does not fully succeed because:

1. The AI metadata security guarantee (“without data leaks”) overstates what the inventory establishes.
2. “Propose → validate → approve → commit” can be read as universal behavior for every AI or import path; the implementation report itself says the pipeline is illustrative and feature-dependent.
3. The case study’s confident language about identical model output and detection must remain explicitly bounded, which the body mostly does.
4. Current wording should say deterministic checks validate recorded structures, not that AI or the platform guarantees semantic correctness.

The key buyer interpretation should be: TraceBoard records authoritative engineering data and relationships; AI proposes or assists; people decide what is committed; deterministic checks calculate/report from recorded facts. That meaning is present but should be protected from the metadata and legacy page.

## 9. Standards / Compliance Assessment

Current pages generally communicate standards-aware templates, assessments, evidence and named standards without directly claiming certification. Engineering State is explicitly described as not certification or release approval. This is acceptable with targeted wording cleanup.

Remaining concern is cumulative interpretation. “Audit-ready,” “compliance,” “hazard-to-test,” “complete,” and “full audit trail” can make a technically competent buyer infer that using the product establishes compliance. The inventory expressly says it does not. Standards support should remain scoped to assistance, assessment, templates, evidence and provenance; no page should imply automatic compliance, regulatory approval, or certification.

## 10. Deployment / Publication Assessment

- **Self-hosting:** Supported by the inventory and accurately prominent on current pages.
- **Local operation:** Supported for the self-hosted core and configured local AI; current pages appropriately mention selected integration dependencies.
- **Network dependencies:** OIDC/external identity, remote Git, and cloud LLMs require connectivity. Current pages communicate this reasonably well.
- **Managed cloud/SaaS:** No positive current managed-cloud claim found. The inventory confirms no managed-cloud service. Do not use “cloud-ready” or “deploy anywhere” without equivalent boundaries.
- **Legacy exposure:** High risk. `index-legacy.html` and `old_index.html` are root-level files. Sitemap omission does not prevent direct serving, and no local hosting rule was found.
- **Sitemap:** Valid XML. It lists seven intended URLs, including Features and TCO, and excludes the legacy files. It is not a publication allowlist.
- **Browser/visual:** Not verified; browser tooling and a deployed URL were unavailable.

## 11. Commercial Verification

The following cannot be independently verified from the available product repository evidence and must be commercially approved:

- exact plan prices such as `€999` through `€11,990`;
- 5–100 user bands and “flat annual pricing”;
- “no per-seat licensing” and “no usage-based AI billing”;
- “Start 30-Day Trial,” trial-license endpoint, and trial entitlements;
- live demo availability and the wording “Watch 2-Minute Demo”;
- competitor prices, published-price status, and ReqView comparisons;
- the 15-person Year 1 TCO calculation and assumptions;
- claims about competitor configuration time, dedicated administrators, workshops, and support/maintenance inclusion;
- exact feature entitlements by plan.

Classification: **AMBIGUOUS — COMMERCIAL VERIFICATION REQUIRED**, not a guessed correction.

## 12. Positioning Assessment

### Strongest aspects

- Self-hosted engineering traceability/evidence category is clear.
- The connected engineering model and requirements/work/verification/evidence chain are credible.
- AI is framed as optional and reviewable rather than autonomous.
- Engineering State and baselines are now visible.
- TraceDocs and TraceTest are presented as connected suite components.
- Comparison content acknowledges fit limits and lack of ReqIF/DOORS interchange.

### Weak or missing aspects

- Provenance and controlled engineering history are not consistently prominent.
- TraceDocs and TraceTest need a stable one-sentence relationship to engineering data, baselines, evidence and state.
- OIDC is not presented as a clear supported identity mechanism with an external-provider boundary.
- Traceability wording still varies between bounded calculations and absolute audit-chain language.
- Publication control is absent.

### Unnecessary content

The current intended pages are somewhat repetitive, especially in AI and model/data-operation caveats, but the repetition is mostly serving credibility. The greater problem is not excess qualification; it is inconsistent legacy content and repeated commercial/comparison assertions without a controlled source. No general rewrite is warranted.

## 13. Recommended Actions

### P0 — Must fix before publication

1. Establish an actual deployment/publication allowlist or move legacy HTML outside the served root. Verify direct requests for `/index-legacy.html` and `/old_index.html` cannot expose them.
2. Remove or qualify the AI metadata phrase “without data leaks”; do not make a security guarantee not supported by product evidence.
3. Re-run a positive-capability search after publication configuration is fixed, including all served aliases and generated routes.

### P1 — Strongly recommended

1. Replace residual absolute traceability/audit wording with “recorded relationships,” “calculated coverage,” and “evidence linked to recorded items.”
2. Keep all named standards explicitly standards-aware and non-certifying near the claim, including the case study.
3. Add a concise controlled-state explanation for baselines, provenance and Engineering State.
4. Make TraceDocs’ baseline-derived controlled-document relationship and TraceTest’s requirements/evidence/coverage relationship consistent across Home, Features and FAQ.
5. Verify and source every current price, trial, plan, competitor, and TCO statement with a date and commercial owner.
6. Qualify the AI pipeline as illustrative/feature-dependent and state that deterministic validation does not guarantee semantic correctness.

### P2 — Optional refinement

1. Add one precise OIDC identity statement; do not turn SAML absence into a feature pitch.
2. Add a compact integration/data-operation matrix with direction and network requirements.
3. Remove stale fragment links from legacy artifacts if those files must remain in the repository, while still preventing publication.
4. Consolidate repeated marketing vocabulary in a maintainable content source in a later site-maintenance pass.

## 14. Final Verdict

**NOT READY**

The intended current pages are close to a credible, targeted correction state and contain no positive current ReqIF or SAML claim. However, the absence of publication controls means a stale legacy page can likely be served directly, and the current AI metadata contains an unsupported security guarantee. Commercial claims also remain unverified. These are material buyer-expectation risks, not cosmetic issues.

## Change-control statement

This audit created only:

`D:\Dev\MyCode\traceboard-site\traceboard-site\docs\product\website-final-claim-audit.md`

No HTML, sitemap, CSS, JavaScript, product code, documentation source, inventory, positioning plan, or existing audit file was modified. Pre-existing Git working-tree changes were preserved.