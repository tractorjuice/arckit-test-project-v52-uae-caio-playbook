# UAE Federal Entity — Agentic AI Architecture Principles

> **Template Origin**: Official | **ArcKit Version**: 5.4.0 | **Command**: `/arckit:principles`

## Document Control

| Field | Value |
|-------|-------|
| Document ID | ARC-000-PRIN-v1.0 |
| Document Type | Architecture Principles (PRIN) |
| Project | UAE CAIO Playbook (Project 000 — Global) |
| Classification | OFFICIAL |
| Status | DRAFT |
| Version | 1.0 |
| Created Date | 2026-05-28 |
| Last Modified | 2026-05-28 |
| Review Cycle | Quarterly (aligned to Ministerial Council cadence) |
| Next Review Date | 2026-08-28 |
| Owner | Chief AI Officer (CAIO), entity to assign |
| Reviewed By | Pending — Entity AI Governance Committee |
| Approved By | Pending — Highest Authority of the entity |
| Distribution | CAIO, entity leadership, ministry SROs, Ministerial Council Secretariat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-05-28 | ArcKit AI | Initial creation from `/arckit:principles` command — UAE federal agentic AI baseline | PENDING | PENDING |

---

## Executive Summary

This document establishes the immutable architecture principles governing all autonomous-AI ("agentic") technology decisions within the entity, framed for the federal directive of 23 April 2026: **50% of UAE federal government services delivered by autonomous AI agents by 2028**.

These principles align to the **UAE Charter for the Development and Use of Artificial Intelligence** (12 principles), the **UAE Personal Data Protection Law** (Federal Decree-Law 45/2021), the **UAE Information Assurance Standard** (188 controls, NESA-aligned), the **UAE National Cloud Security Policy v2**, the **UAE Smart Data Framework**, and the federal framework approved by UAE Cabinet on 18 May 2026 under HH Sheikh Mansour bin Zayed Al Nahyan's Ministerial Council for AI and Development.

**Scope**: All autonomous-AI agents and supporting systems operated by the entity, including the four already-live federal pilots (Procurement, Tax Auditing, Customer Happiness, Technical Support) and the autonomous work-permit decisions in operation at MoHRE since 1 May 2026.

**Authority**: Entity Chief AI Officer (CAIO), reporting into the Ministerial Council for AI and Development.

**Compliance**: Mandatory unless an exception is approved through the process in Section VI.

**Philosophy**: These principles are **technology-agnostic** — they describe the qualities that the architecture must have, not specific products. Vendor and platform selection happens during `/arckit:research`, `/arckit:aws-research`, `/arckit:azure-research`, and `/arckit:gcp-research`, guided by these principles.

**Directive performance metrics** (the three KPIs that every artefact must serve):

1. **Adoption speed** — pace of moving services from manual to autonomous delivery
2. **Implementation quality** — measurable user, operational, and accuracy outcomes
3. **Workflow redesign** — the degree to which agents reshape the work, not just automate it

---

## I. Strategic AI Governance Principles

### 1. Human Oversight and Meaningful Control (NON-NEGOTIABLE)

**Principle Statement**:
Every autonomous agent MUST have a documented human oversight model with the authority and the practical ability to intervene, override, or halt the agent. Autonomy is bounded; sovereignty over the decision remains with the entity and, where appropriate, with the citizen affected.

**Rationale**:
The UAE AI Charter's principle of human oversight requires that AI augment, not replace, accountable human decision-making in matters of public consequence. The directive's third KPI — workflow redesign — explicitly anticipates new human roles, not human absence.

**Implications**:

- Every agent has a named accountable officer at the entity, recorded in its ATRS entry
- Every decision pathway includes a contestation route accessible to the citizen or business affected
- Oversight latency (the time between an agent acting and a human being able to review or revoke) is bounded and measured
- Agents MUST surface confidence and reasoning to the reviewing officer in a form the officer can interrogate
- Decisions with material legal, financial, or rights-affecting effect MUST be subject to the autonomy-tier escalation rules (Principle 2)

**Validation Gates**:

- [ ] Named accountable officer recorded per agent
- [ ] Contestation route published in plain language (Arabic and English)
- [ ] Oversight latency SLA defined and instrumented
- [ ] Human-readable rationale available for every individual decision
- [ ] Override mechanism tested end-to-end before go-live and quarterly thereafter

**Common Violations**:

- "We'll add an appeals process later"
- Oversight that requires log-archaeology to perform
- Override mechanisms that exist on paper but are not exercised in drills

---

### 2. Autonomy Tiering Governs Approval Depth

**Principle Statement**:
Every agent MUST be classified into one of three autonomy tiers, and the depth of governance — approvals, audit, evaluation, monitoring — MUST scale with the tier. Tier classification is reviewed before any change in scope, model, or population served.

**Tiers**:

1. **Tier 1 — Internal productivity**: agent supports staff workflow; outputs are reviewed before acting on the world
2. **Tier 2 — External-facing with human approval**: agent drafts the decision; a human approves before it takes effect
3. **Tier 3 — Regulated / autonomous**: agent's output takes effect without per-decision human approval, within a defined envelope

**Rationale**:
Uniform governance over heterogeneous agents either over-burdens low-risk pilots or under-protects rights-affecting services. The tier becomes the master switch that selects which PDPL controls, IAS controls, ATRS depth, and Charter clauses apply.

**Implications**:

- Tier-1 agents have lightweight governance suited to fast experimentation
- Tier-2 agents add reviewer instrumentation, decision audit, and reviewer competence requirements
- Tier-3 agents add independent evaluation, statistical bias monitoring, real-time drift detection, and a published service-level guarantee for contestation
- Promotion from a lower tier to a higher tier MUST follow the documented promotion-criteria gate
- The four already-live agents and the MoHRE work-permit service MUST have a current tier classification on record

**Validation Gates**:

- [ ] Tier recorded for every agent in the portfolio register
- [ ] Tier-specific controls documented and enforced
- [ ] Promotion-criteria gate exists and was applied to every Tier-3 agent
- [ ] Tier review performed at least annually or on material change

---

### 3. Mission Alignment to National Priorities

**Principle Statement**:
Every agent and supporting capability MUST trace to at least one published UAE national outcome, and that traceability MUST be visible in business-case, requirements, and roadmap artefacts.

**Anchors**:

- **We the UAE 2031** — the citizen and societal outcomes
- **National Strategy for Artificial Intelligence 2031**
- **National Information Security Strategy 2031**
- **UAE Digital Economy Strategy**
- The 23 April 2026 directive — the 50% autonomous-services target and the three KPIs

**Rationale**:
Federal entities are accountable to the Ministerial Council for AI and Development for measurable contribution to national outcomes, not for activity. Alignment must be designed in, not retrofitted in board slides.

**Implications**:

- The Strategic Outline Business Case (SOBC) cites the specific national-outcome contribution
- Each requirement (BR-xxx, FR-xxx, NFR-xxx) is traceable to at least one Charter principle and one national-priority outcome
- Reuse of existing federal capabilities (UAE Pass, FedNet, sovereign CSPs) is preferred over rebuilding
- Build vs reuse decisions are recorded as ADRs and reviewed against the Capability Reuse Register

**Validation Gates**:

- [ ] Each agent traces to ≥ 1 national-strategy outcome
- [ ] Reuse assessment performed before any new-build decision
- [ ] Contribution to the three directive KPIs quantified in the roadmap

---

### 4. Security by Design — UAE IAS Aligned (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth and zero-trust controls aligned to the UAE Information Assurance Standard (188 controls, M1–M6 management and T1–T9 technical), tiered by IAS priority (P1–P4). Security is foundational; it is not an option, a phase, or a control that can be deferred.

**Rationale**:
The IAS is the statutory cybersecurity baseline for federal entities. Agentic systems extend the attack surface in new ways — prompt injection, model-extraction, training-data poisoning, agentic privilege escalation — and the security envelope must keep pace with the autonomy envelope.

**Zero-Trust Pillars** (consistent with IAS expectations):

1. **Identity-based access** — no implicit network trust; every request authenticated and authorised
2. **Least privilege** — minimum necessary permissions, time-boxed where practical
3. **Encryption everywhere** — data encrypted in transit and at rest with sovereign-managed keys where classification requires it
4. **Continuous verification** — monitor, log, and analyse all access, all agent actions, all model interactions

**AI-Specific Controls**:

- Adversarial input testing (prompt injection, jailbreaks) before go-live and on a rolling cadence
- Training-data provenance verified; data poisoning detection
- Agent privilege boundaries explicit; no agent inherits the union of all reachable scopes
- Secrets and model weights handled per their classification

**Validation Gates**:

- [ ] IAS Statement of Applicability completed and signed
- [ ] P1 controls implemented for all production agents
- [ ] Threat model includes AI-specific vectors
- [ ] Penetration testing (including AI-specific) performed on cadence
- [ ] Incident response runbook covers agent-specific incidents (model misuse, training-data exposure, autonomous-action incidents)

**Exceptions**: NONE. Compensating controls may be approved; the principle is not waivable.

---

### 5. Resilience, Continuity and Graceful Degradation

**Principle Statement**:
All agents MUST degrade gracefully when models, data, infrastructure, or upstream services fail, and MUST recover automatically without data loss or silent error. Federal services do not become unavailable because an agent is unavailable.

**Rationale**:
Citizens and businesses depend on federal services; an unavailable agent must fall back to a working delivery path (human officer, prior system) rather than fail closed. The UAE PDPL also requires availability as a security objective.

**Implications**:

- Every Tier-2 and Tier-3 agent has a documented fallback delivery path
- Recovery Time Objective (RTO) and Recovery Point Objective (RPO) are defined per agent
- Model-server failure does not cascade into business-process failure
- Health checks distinguish model availability, data freshness, and end-to-end behaviour
- Bulkhead isolation between agents — one bad agent does not poison shared infrastructure

**Validation Gates**:

- [ ] RTO/RPO defined and tested per agent
- [ ] Documented fallback path exercised at least annually
- [ ] Failure-mode analysis performed including model-specific failure modes
- [ ] Cascading-failure analysis performed for shared platform components

---

### 6. Observability and Auditability of Agent Behaviour

**Principle Statement**:
Every agent MUST emit structured, queryable telemetry sufficient to reconstruct any individual decision, to evidence Charter and PDPL compliance, and to detect drift before it becomes harm.

**Rationale**:
Algorithmic transparency (UAE Charter Principle 5; ATRS-equivalent record) is impossible without the underlying observability. Audit-readiness must be a design property, not a forensic exercise.

**Required Telemetry**:

- **Per-decision audit log**: inputs (with appropriate classification handling), model version, confidence, rationale token, output, human reviewer (if any), final action, time of action, contestation flag
- **Operational metrics**: request volume, latency (p50, p95, p99), error rate, fallback rate
- **Behavioural metrics**: confidence distribution, refusal rate, decision-class distribution by demographic where lawful and necessary
- **Drift metrics**: input distribution drift, output drift, prediction-vs-outcome drift
- **Security events**: authentication, authorisation, anomalous prompts, unusual access patterns

**Retention**:

- **Per-decision audit log**: aligned to PDPL retention obligations and the entity's records schedule under the UAE Digital Records Policy
- **Operational metrics**: ≥ 1 year with aggregation
- **Drift metrics**: ≥ 2 years for trend analysis

**Validation Gates**:

- [ ] Per-decision audit captured for every Tier-2 and Tier-3 decision
- [ ] Behavioural and drift dashboards published to oversight committee
- [ ] SLO-based alerting with named runbook owner
- [ ] Audit-log integrity controls (write-once, signed) in place for legally consequential decisions

---

### 7. Scalability and Elasticity within Sovereign Boundaries

**Principle Statement**:
All agents MUST be designed to scale horizontally to demand, but only within the residency and classification envelope established by the UAE National Cloud Security Policy v2 and the data's Smart Data classification.

**Rationale**:
The directive's 50% target implies federation- and population-scale demand within 24 months. Scaling must not be solved by quietly stepping outside the sovereign envelope.

**Implications**:

- Auto-scaling defined and tested per agent
- Capacity planning accounts for the directive's expansion trajectory
- Burst capacity respects classification — Confidential and above stay on approved sovereign CSPs (e.g., Core42 / G42 sovereign, Microsoft UAE North/Central, TDRA FedNet, e& Sovereign Launchpad on AWS) per applicable accreditation
- Cross-border traffic is engineered out, not engineered around

**Validation Gates**:

- [ ] Auto-scaling tested at directive-trajectory load
- [ ] Residency proof for every data flow at every tier
- [ ] Egress routes from the sovereign envelope require explicit, classification-aware approval

---

## II. Data and Privacy Principles

### 8. Lawful Basis First (UAE PDPL)

**Principle Statement**:
No personal data is collected, used, retained, transferred, or shared without a recorded lawful basis under the UAE Personal Data Protection Law (Federal Decree-Law 45/2021), recorded before processing begins.

**Rationale**:
PDPL compliance is a precondition for agent operation, not an audit finding. Every personal-data processing activity that an agent performs is a controller decision the entity must be able to defend.

**Implications**:

- Lawful-basis register maintained per processing activity, per agent
- DPIA (or PDPL equivalent) performed for high-risk processing — automated decisions with significant effect on individuals, special-category data, large-scale monitoring
- Data-subject rights procedure (access, rectification, erasure, objection) operates inside agent SLAs
- Cross-border transfers logged with the lawful mechanism cited; default position is "no transfer"
- Consent, where used, is meaningful, withdrawable, and re-collected on material change

**Validation Gates**:

- [ ] Lawful basis recorded per processing activity
- [ ] DPIA performed where required and reviewed by the entity DPO / Data Office liaison
- [ ] Data-subject rights process tested end-to-end and meets statutory timelines
- [ ] Cross-border transfer log present and current

---

### 9. Smart Data Classification Drives Handling

**Principle Statement**:
Every dataset, every model input, every model output, and every agent-generated artefact MUST be classified per the UAE Smart Data Framework (Open / Shared / Confidential / Secret / Top Secret). Handling — storage, transit, residency, access — derives from the classification.

**Rationale**:
Classification is the lever that connects abstract policy (Charter, PDPL, IAS, Cloud Residency) to concrete engineering choices. An unclassified asset is, in practice, ungovernable.

**Implications**:

- Classification recorded at point of creation, not retrospectively
- Re-classification on aggregation (Open + Open can become Confidential when joined)
- Models trained on Confidential data inherit Confidential handling for weights and gradients
- Outbound flows to lower-classification environments require an explicit redaction or aggregation step, documented as an ADR
- The Classification Register is the source of truth referenced by every downstream control

**Validation Gates**:

- [ ] Classification Register populated for the agent's full data inventory
- [ ] Aggregation re-classification rule documented and enforced
- [ ] Model artefacts classified
- [ ] Handling controls implemented per classification

---

### 10. Sovereign Data Residency by Classification

**Principle Statement**:
Personal, Confidential, Secret, and Top Secret data MUST reside within the UAE on infrastructure approved for the applicable classification per the National Cloud Security Policy v2.

**Rationale**:
Sovereignty is not a brand statement — it is a set of engineering, contractual, and legal commitments that prevent foreign-jurisdictional access (CLOUD Act, FISA-702 and equivalents) and that survive supplier-relationship change.

**Implications**:

- Per-classification residency map maintained and reconciled against actual deployments
- Approved CSP options recorded and procurement gated to them per classification
- Shared-responsibility matrix signed per supplier and per service
- Exit and portability plan ready before go-live, not after a dispute
- Encryption keys for Confidential and above are sovereign-managed unless an exception is approved

**Validation Gates**:

- [ ] Residency map signed by entity leadership
- [ ] Each production data flow validated against the map
- [ ] Exit plan exists and is rehearsed
- [ ] Key management aligns with classification

---

### 11. Single Source of Truth — Records as Official Source

**Principle Statement**:
Every data domain MUST have a single, designated authoritative source. Agent-generated decisions and the records of those decisions MUST be designated as official records under the UAE Digital Records Policy where they constitute the act of government.

**Rationale**:
Duplicated authority creates reconciliation overhead, audit ambiguity, and citizen-facing inconsistency. For agent decisions with legal effect, the question "what does the government say?" must have a single, authoritative answer.

**Implications**:

- Source-of-truth register maintained per service
- Derived copies are clearly labelled as such, with sync frequency and lineage
- Agent decision records are retained per the entity's records schedule
- No bidirectional sync without an explicit conflict-resolution policy
- Master data for citizens, businesses, and federal employees uses the federally designated identifier (UAE Pass / Emirates ID linkage where applicable)

**Validation Gates**:

- [ ] Source-of-truth register exists
- [ ] Records schedule covers agent-decision records
- [ ] No undeclared bidirectional sync exists
- [ ] Inter-entity references use designated federal identifiers

---

### 12. Collect-Once, Share-Many

**Principle Statement**:
Federal entities MUST reuse data already held elsewhere in government rather than re-collect it from the citizen or business. Inter-entity sharing operates under the UAE Government Services Data Sharing Policy, with API and federation in preference to copy.

**Rationale**:
Zero-bureaucracy and customer-experience are explicit federal commitments. Re-collection violates them and creates classification, consent, and accuracy hazards.

**Implications**:

- Pre-use search of existing federal sources before any new collection
- Federation / API preferred over file transfer or bulk copy
- Data Sharing Agreements (DSAs) per share, with lawful-basis under PDPL recorded
- Reuse register maintained; gaps surface candidate APIs to publish
- Quality issues with a reused source are raised back to the source entity, not worked around silently

**Validation Gates**:

- [ ] Pre-collection reuse search documented
- [ ] DSAs in place for every cross-entity share
- [ ] APIs preferred over bulk transfer; exceptions are ADR-recorded
- [ ] Source-quality issues raised through documented channel

---

## III. AI Lifecycle Principles

### 13. Bias, Fairness and Inclusion

**Principle Statement**:
Every agent MUST be evaluated for unjustified disparate impact across protected and policy-relevant population groups, before go-live and on a continuing cadence. Bias is not a launch defect to be discovered in production.

**Rationale**:
The UAE AI Charter requires fairness, inclusive access, and the mitigation of bias. The UAE population's linguistic, cultural, and demographic diversity is a strength only if agents treat it as such; otherwise it is a fairness risk.

**Implications**:

- Fairness metrics chosen per use case and recorded; choice is justified, not implicit
- Evaluation set is demographically representative within lawful constraints
- Arabic-language performance evaluated to the same standard as English-language performance
- Continuing bias monitoring with named threshold and named owner
- Material disparity triggers a remediation plan; the agent does not run unmonitored through it

**Validation Gates**:

- [ ] Pre-launch fairness evaluation completed and reviewed
- [ ] Arabic and English (and other relevant languages) evaluated to parity
- [ ] Continuous bias monitoring in production
- [ ] Documented remediation triggers and process

---

### 14. Explainability and Algorithmic Transparency

**Principle Statement**:
Every agent MUST have a published, plain-language transparency record (ATRS-equivalent) and MUST surface a decision-specific rationale to the affected citizen, business, or reviewer on request.

**Rationale**:
Transparency is a UAE Charter principle and a precondition for legitimate contestation. The federal directive's commitment to public confidence rests on it.

**Implications**:

- One ATRS-equivalent record per live agent — the four current pilots and MoHRE work-permits at minimum
- Records are written for citizens, not for engineers
- Per-decision rationale is generated at decision time, not reconstructed under appeal
- Records are version-controlled and updated on material change
- Explainability technique chosen to match the agent's tier and stakes

**Validation Gates**:

- [ ] ATRS-equivalent record published per Tier-2 and Tier-3 agent
- [ ] Per-decision rationale generation tested
- [ ] Plain-language test (citizen-readability) passed
- [ ] Update process triggered on material model or scope change

---

### 15. Model Governance and Drift Management

**Principle Statement**:
Every model MUST have a recorded lineage (data, code, weights, evaluation), a designated owner, an approved release path, and continuous monitoring for drift and degradation. Model changes follow the same change-control rigour as code changes.

**Rationale**:
Silent model changes — a vendor base-model update, an internal retraining job, a feature-store schema change — can shift agent behaviour in ways the entity does not intend. Governance must be designed for that.

**Implications**:

- Model registry maintained: training data hash or pointer, training code commit, evaluation results, approved-to-serve flag
- Release path includes shadow / canary / progressive rollout with rollback gates
- Drift detection runs continuously; drift triggers a defined response
- Third-party / foundation-model dependencies have a contractual change-notification path; surprise base-model changes are treated as incidents
- Retraining triggers are documented (drift, data refresh, policy change, regulatory change)

**Validation Gates**:

- [ ] Model registry populated for every production model
- [ ] Shadow/canary capability available and exercised
- [ ] Drift monitor live with named owner and threshold
- [ ] Foundation-model contractual change-notification recorded

---

### 16. Training-Data Provenance and Lawful Use

**Principle Statement**:
Training, fine-tuning, evaluation, and prompt-engineering data MUST have recorded provenance, a recorded lawful basis under PDPL where personal data is present, and recorded licensing where third-party content is used. Unprovenanced data is not training data.

**Rationale**:
The agent's behaviour is downstream of its data; the entity's exposure (privacy, copyright, accuracy) is downstream of the data's provenance. Provenance is the only durable defence.

**Implications**:

- Dataset register per agent, per training run
- Personal data used for training is covered by a documented lawful basis
- Synthetic data is labelled as such; its generation process is recorded
- Web-scraped or third-party data has a recorded licence or fair-use basis
- Training-data deletion is possible where the lawful basis requires it (right-to-erasure analogues)

**Validation Gates**:

- [ ] Dataset register exists and is current
- [ ] PDPL lawful basis recorded per personal-data dataset
- [ ] Licensing recorded per third-party dataset
- [ ] Deletion / unlearning approach documented

---

## IV. Integration Principles

### 17. Open Standards and Federation over Copy

**Principle Statement**:
Inter-entity and inter-system integration MUST use published, standards-based, versioned interfaces with documented authentication, authorisation, and error contracts. Database-level or file-drop integration across entity boundaries is prohibited.

**Rationale**:
Federation enables collect-once / share-many at scale, supports independent evolution, and reduces lock-in. Database-level coupling is fragile, opaque, and incompatible with classification controls.

**Implications**:

- API contracts published (OpenAPI / AsyncAPI / GraphQL schema as appropriate)
- Versioning strategy with backward compatibility window defined
- Asynchronous patterns for non-real-time flows
- Federation references — UAE Pass, FedNet, designated federal identifiers — used where they exist rather than reinvented
- No direct database access across entity boundaries

**Validation Gates**:

- [ ] Interface specifications published
- [ ] Versioning policy in place and observed
- [ ] Inter-entity flows use API / event channels, not DB or file
- [ ] Federation references reused where available

---

### 18. Citizen and Workforce Identity via Federal Identifiers

**Principle Statement**:
Citizen-facing services MUST integrate with UAE Pass (using the appropriate Basic or Verified profile per the service's risk tier). Internal-workforce identity MUST integrate with the entity's federal identity baseline.

**Rationale**:
A single, trusted identity layer protects citizens from credential proliferation, supports federation, and is a precondition for collect-once / share-many.

**Implications**:

- Service-Provider onboarding pack completed for UAE Pass services
- Profile selection (Basic vs Verified) documented and justified per service
- e-signature / non-repudiation audit trail designed where the service produces legally consequential records
- Service-account identities for agents are distinct from human identities and audited as such
- Identity-related events feed the same observability pipeline as everything else

**Validation Gates**:

- [ ] UAE Pass integration design documented per citizen-facing service
- [ ] Profile selection justified
- [ ] Agent / service-account identities distinguishable from human identities in logs
- [ ] e-signature audit trail in place where applicable

---

## V. Engineering Practice Principles

### 19. Infrastructure as Code

**Principle Statement**:
All infrastructure — compute, network, identity, data stores, model-serving — MUST be defined as version-controlled code and deployed through automated pipelines. Manual changes to production are prohibited except under documented break-glass procedure.

**Rationale**:
Manual changes create drift, undocumented state, and audit gaps; agentic systems compound the cost of drift because the agent's behaviour depends on infrastructure invariants.

**Implications**:

- Declarative IaC in version control
- Environments reproducible from code (dev, staging, production)
- Break-glass procedure exists, is rare, and is followed by reconciliation back to code
- IaC review is part of the same governance as application code review
- Drift detection runs and reports

**Validation Gates**:

- [ ] All infrastructure expressed in IaC
- [ ] Environments reproducible from clean state
- [ ] No manual production changes outside break-glass
- [ ] Drift detection in place

---

### 20. Automated Testing across the AI Test Pyramid

**Principle Statement**:
All agents and supporting systems MUST be validated through automated tests before production deployment, including AI-specific tests (behavioural, fairness, safety, adversarial) alongside conventional functional and integration tests.

**Test Categories**:

- **Functional** — does the agent do what was specified?
- **Behavioural / safety** — does the agent refuse or escalate where it should?
- **Fairness** — does the agent perform comparably across population groups?
- **Adversarial** — does the agent resist prompt injection, jailbreaks, and adversarial inputs?
- **Performance** — does the agent meet latency, throughput, and concurrency targets?
- **Resilience** — does the agent degrade gracefully under fault injection?

**Validation Gates**:

- [ ] All test categories present in the pipeline
- [ ] Coverage thresholds defined and met
- [ ] Test failures block production promotion
- [ ] Adversarial test corpus refreshed on cadence

---

### 21. CI/CD with Safety and Compliance Gates

**Principle Statement**:
All code, model, and infrastructure changes MUST flow through automated build, test, security-scan, compliance-check, and deployment pipelines with explicit quality gates at each stage. There is no manual production deployment path.

**Pipeline Stages**:

1. **Source control** — all changes (code, models, infra) committed
2. **Build** — automated build and packaging
3. **Test** — full test pyramid including AI-specific tests
4. **Security scan** — dependency, code, container, model artefact
5. **Compliance check** — classification, residency, lawful-basis flags
6. **Deployment** — automated, environment-promotion-based, with progressive rollout
7. **Post-deployment** — health, behavioural, and drift monitoring

**Quality Gates**:

- All tests pass
- No critical security findings
- Classification and residency invariants satisfied
- Reviewer approval recorded
- Rollback path verified

**Validation Gates**:

- [ ] CI/CD pipeline exists and is the only production deployment path
- [ ] Each stage has an explicit pass / fail gate
- [ ] Rollback exercised
- [ ] Compliance checks automated where they can be

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the entity's AI Governance Committee. Principles 1 (Human Oversight) and 4 (Security by Design) are **non-negotiable** — they accept compensating controls, not waivers.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within the directive timeline
- Regulatory or legal requirements that conflict (and trigger escalation)
- Transitional state during migration from a legacy capability
- Time-bound pilot / proof-of-concept with a defined end date and rollback

**Exception Request Requirements**:

- [ ] Justification with business and technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment, with PDPL / IAS / Charter impact called out
- [ ] Expiration date (exceptions are time-bound)
- [ ] Remediation plan to achieve compliance

**Approval Process**:

1. Exception request submitted to the entity AI Governance Committee
2. Reviewed by CAIO, DPO, CISO, and the relevant ministry SRO
3. Approval for exceptions to non-negotiable principles requires Highest Authority sign-off
4. Recorded in the project architecture documentation and in the Ministerial Council reporting line
5. Reviewed at minimum quarterly

---

## VII. Governance and Compliance

### Architecture Review Gates

All agents must pass governance gates at each lifecycle milestone:

**Pre-Pilot**:

- [ ] Tier classification recorded
- [ ] Charter principles assessment performed
- [ ] No obvious principle violations
- [ ] Lawful basis (if personal data) recorded

**Pre-Production**:

- [ ] All validation gates above passed
- [ ] ATRS-equivalent record published
- [ ] IAS Statement of Applicability signed
- [ ] PDPL DPIA performed where required
- [ ] Cloud residency map validated
- [ ] Human oversight design tested

**Production Operation**:

- [ ] Continuous bias and drift monitoring live
- [ ] Per-decision audit captured
- [ ] Quarterly principles-compliance review submitted

### Enforcement

- Architecture reviews are mandatory for every Tier-2 and Tier-3 agent
- Principle violations must be remediated before production
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective compliance review for the four already-live federal pilots and the MoHRE work-permit service is in scope

---

## VIII. Appendix

### Principle Summary

| # | Principle | Category | Criticality | Anchor |
|---|-----------|----------|-------------|--------|
| 1 | Human Oversight and Meaningful Control | Strategic | CRITICAL | UAE AI Charter (oversight) |
| 2 | Autonomy Tiering Governs Approval Depth | Strategic | CRITICAL | Federal AI framework |
| 3 | Mission Alignment to National Priorities | Strategic | HIGH | NIS 2031 / AI 2031 / We the UAE 2031 |
| 4 | Security by Design — IAS Aligned | Strategic | CRITICAL | UAE IAS (188 controls) |
| 5 | Resilience, Continuity, Graceful Degradation | Strategic | CRITICAL | UAE PDPL (availability) |
| 6 | Observability and Auditability | Strategic | HIGH | UAE AI Charter (transparency) |
| 7 | Scalability and Elasticity within Sovereign Boundaries | Strategic | HIGH | National Cloud Security Policy v2 |
| 8 | Lawful Basis First (PDPL) | Data | CRITICAL | UAE PDPL (Decree-Law 45/2021) |
| 9 | Smart Data Classification Drives Handling | Data | CRITICAL | UAE Smart Data Framework |
| 10 | Sovereign Data Residency by Classification | Data | CRITICAL | National Cloud Security Policy v2 |
| 11 | Single Source of Truth — Records as Official Source | Data | HIGH | UAE Digital Records Policy |
| 12 | Collect-Once, Share-Many | Data | HIGH | Government Services Data Sharing Policy |
| 13 | Bias, Fairness and Inclusion | AI Lifecycle | CRITICAL | UAE AI Charter (fairness, inclusion) |
| 14 | Explainability and Algorithmic Transparency | AI Lifecycle | CRITICAL | UAE AI Charter (transparency); ATRS |
| 15 | Model Governance and Drift Management | AI Lifecycle | HIGH | Federal AI framework |
| 16 | Training-Data Provenance and Lawful Use | AI Lifecycle | HIGH | UAE PDPL; licensing |
| 17 | Open Standards and Federation over Copy | Integration | HIGH | Federal interoperability |
| 18 | Citizen and Workforce Identity via Federal Identifiers | Integration | HIGH | UAE Pass; FedNet |
| 19 | Infrastructure as Code | Engineering | HIGH | Operational hygiene |
| 20 | Automated Testing across the AI Test Pyramid | Engineering | HIGH | Quality assurance |
| 21 | CI/CD with Safety and Compliance Gates | Engineering | HIGH | Operational hygiene |

### UAE Charter Coverage Map

| Charter Principle | Addressed By |
|-------------------|--------------|
| Human-machine ties | 1, 2, 14 |
| Safety | 4, 5, 15, 20 |
| Bias mitigation | 13, 16, 20 |
| Data privacy | 8, 9, 10, 16 |
| Transparency | 6, 14 |
| Human oversight | 1, 2 |
| Governance and accountability | 1, 2, 6, 15, Section VI |
| Technological excellence | 4, 15, 19, 20, 21 |
| Human commitment | 1, 13, 18 |
| Peaceful coexistence | 3 |
| Inclusive access | 13, 18 |
| Lawful compliance | 4, 8, 10, 11 |

---

## External References

> No external policy documents have been loaded into `projects/000-global/policies/` at the time of writing. The principles are anchored on publicly named UAE statutes and policies (UAE AI Charter, PDPL Federal Decree-Law 45/2021, UAE IAS, National Cloud Security Policy v2, UAE Smart Data Framework, UAE Government Services Data Sharing Policy, UAE Digital Records Policy, national strategies). For citation-grade traceability, load the authoritative texts into `projects/000-global/policies/` and re-run `/arckit:principles` to produce a v1.1 with inline citation markers.

### Document Register

| Doc ID | Filename | Type | Source Location | Description |
|--------|----------|------|-----------------|-------------|
| *None provided* | — | — | — | — |

### Citations

| Citation ID | Doc ID | Page/Section | Category | Quoted Passage |
|-------------|--------|--------------|----------|----------------|
| — | — | — | — | — |

### Unreferenced Documents

| Filename | Source Location | Reason |
|----------|-----------------|--------|
| — | — | — |

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-05-28
**ArcKit Version**: 5.4.0
**Project**: UAE CAIO Playbook (Project 000 — Global)
**AI Model**: Claude Opus 4.7 (1M context)
