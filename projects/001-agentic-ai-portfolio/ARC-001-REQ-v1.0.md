# Project Requirements: Agentic AI Portfolio

> **Template Origin**: Official | **ArcKit Version**: 5.4.0 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| Document ID | ARC-001-REQ-v1.0 |
| Document Type | Business and Technical Requirements (REQ) |
| Project | Agentic AI Portfolio (Project 001) |
| Classification | OFFICIAL |
| Status | DRAFT |
| Version | 1.0 |
| Created Date | 2026-05-28 |
| Last Modified | 2026-05-28 |
| Review Date | 2026-06-27 |
| Owner | Chief AI Officer (CAIO), entity to assign |
| Reviewed By | [PENDING] — CISO, DPO, ministry SROs, AI Governance Committee |
| Approved By | [PENDING] — Entity Highest Authority |
| Distribution | CAIO, AI Governance Committee, ministry SROs, Architecture Team, CISO, DPO, Ministerial Council Secretariat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-05-28 | ArcKit AI | Initial creation from `/arckit:requirements` command — UAE federal agentic-AI portfolio | [PENDING] | [PENDING] |

## Document Purpose

Defines the business, functional, non-functional, data, and integration requirements for the entity's portfolio of agentic AI systems — the five directive-named federal pilots (AI-001 Procurement, AI-002 Tax Auditing, AI-003 Customer Happiness, AI-004 Technical Support, AI-005 MoHRE Work-Permit Decisioning). Used by `/arckit:research`, `/arckit:sobc`, the procurement overlay, design reviews, and Charter/PDPL/IAS compliance assessments.

---

## Executive Summary

### Business Context

The 23 April 2026 directive of HH Sheikh Mohammed bin Rashid Al Maktoum sets a federal target of **50 % of UAE federal government services delivered by autonomous (agentic) AI agents by 2028**. The Cabinet's federal framework of 18 May 2026 places execution under HH Sheikh Mansour bin Zayed's **Ministerial Council for AI and Development**, coordinated by Minister of Cabinet Affairs Mohammad Al Gergawi, and measured against three KPIs: **adoption speed, implementation quality, workflow redesign**.

This requirements document defines what the entity's portfolio must do to deliver that mandate while remaining compliant with the **UAE AI Charter** (12 principles), the **UAE Personal Data Protection Law** (Federal Decree-Law 45/2021), the **UAE Information Assurance Standard** (188 controls), the **National Cloud Security Policy v2**, the **Smart Data Framework**, the **Digital Records Policy**, the **Government Services Data Sharing Policy**, and the entity's foundational principles in `ARC-000-PRIN-v1.0`.

Requirements trace to the eight goals (G-1…G-8) and twelve stakeholder drivers (SD-1…SD-12) defined in `ARC-001-STKE-v1.0`, and to the twelve Charter principles assessed in `ARC-001-AICH-v1.0`.

### Objectives

- Deliver measurable contribution to the federal 50 %-by-2028 target across the five named agents
- Maintain Charter, PDPL, IAS, and Cloud Residency compliance at every tier of agent operation
- Operate every autonomous decision under documented, exercised, accountable human oversight
- Make every citizen-affecting decision contestable, in plain Arabic and English
- Redesign the work, not just automate it — produce a measurable capability uplift for the federal workforce

### Expected Outcomes

- **O-1**: Adoption-speed KPI trajectory aligned to federal 50 %-by-2028 (per STKE)
- **O-2**: Implementation-quality composite improving over pre-agent baseline; Arabic / English parity within defined threshold
- **O-3**: Workflow-redesign KPI evidenced by documented process-step elimination and new-role descriptions per service
- **O-4**: Zero reportable Charter / PDPL / IAS incident attributable to the portfolio in the first reporting cycle (Q3 2026)
- **O-5**: Citizen-trust posture sustained or improved by contestation overturn rate and CSAT

### Project Scope

**In scope**:

- The five named federal pilots: AI-001 Procurement, AI-002 Tax Auditing, AI-003 Customer Happiness, AI-004 Technical Support, AI-005 MoHRE Work-Permit Decisioning
- The portfolio-level governance, observability, contestation, audit, and ATRS capabilities that all five agents depend on
- Integration with UAE Pass, sovereign CSPs (Core42 / G42 sovereign, Microsoft UAE North/Central, TDRA FedNet, e& Sovereign Launchpad on AWS), federal-entity core systems for each service, and the federal incident-reporting channels
- The workforce uplift and reviewer-competence programme aligned to FAHR

**Out of scope**:

- New autonomous agents not currently within the directive-named pilot set (will be added in subsequent project versions)
- The Dubai private-sector mandate (separate governance line — Sheikh Hamdan)
- Non-federal entities (the playbook is forkable; each entity adopts and adapts)

---

## Stakeholders

See `ARC-001-STKE-v1.0` for the full stakeholder analysis. The principal stakeholders for these requirements are the CAIO (owner), the Entity Highest Authority (approver), the AI Governance Committee (governance), the CISO and DPO (compliance gates), the five Ministry Service SROs (service-level owners), and (downstream of every citizen-affecting decision) the affected public.

---

## Business Requirements

### BR-001: Contribute measurably to the federal 50 %-by-2028 target

**Description**: Each named agent contributes a measurable, monthly share of autonomous service delivery, aggregated to a portfolio-level entity contribution to the federal target.

**Rationale**: This is the directive's headline KPI (Adoption Speed) and the basis on which the entity is judged by the Ministerial Council.

**Success Criteria**:

- Adoption-speed KPI is measured and reported per agent, monthly internally, quarterly to the Ministerial Council
- Entity-level trajectory aligns to the federal 50 %-by-2028 target by Q4 2027 at latest
- KPI definition is co-signed with each Ministry Service SRO

**Priority**: MUST_HAVE.

**Stakeholder**: SD-1 (Ministerial Council), SD-2 (Cabinet Affairs), SD-7 (SROs); supports Goal G-6.

### BR-002: Five ATRS records published before next quarterly Council review

**Description**: One ATRS-equivalent record per named agent (AI-001…AI-005) published in plain Arabic and English by 2026-08-28.

**Rationale**: Without ATRS, Charter Principle 5 (Transparency) cannot be evidenced — and the affected public cannot meaningfully exercise the contestation right.

**Success Criteria**: 5 of 5 ATRS records published; citizen-readability validated by a non-engineering reviewer in Arabic and English.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-1, SD-3, SD-9; supports Goal G-1, Outcome O-2.

### BR-003: Quantify and publish the three directive KPIs quarterly

**Description**: Per-agent quantification of (1) adoption speed, (2) implementation quality, (3) workflow redesign, exposed on a quarterly dashboard for the Ministerial Council.

**Rationale**: The directive measures the entity against exactly these three KPIs.

**Success Criteria**: Dashboard live; first quarterly submission Q3 2026; KPI definitions co-signed with SROs.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-1, SD-2, SD-3, SD-7; supports Goal G-6.

### BR-004: PDPL compliance for every personal-data-touching agent

**Description**: AI-002, AI-003, AI-005, and any other agent touching personal data has a current PDPL DPIA, a recorded lawful basis, a functioning data-subject-rights process, and a maintained cross-border-transfer log.

**Rationale**: PDPL Federal Decree-Law 45/2021 is statutory; non-compliance exposes the entity to Data Office enforcement and reputational harm.

**Success Criteria**: 3 DPIAs complete; lawful-basis register populated for all 5 agents; SAR fulfilment tested within statutory timeline.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-6, SD-11; supports Goal G-3, Outcome O-4. Aligned to PRIN §II.8.

### BR-005: UAE IAS Statement of Applicability signed; P1 controls 100 % implemented

**Description**: A current IAS SoA across the portfolio with all P1 controls implemented and evidence-recorded per production agent.

**Rationale**: IAS is the statutory cyber baseline; the Cybersecurity Council will audit; agentic systems extend the attack surface and require deliberate posture.

**Success Criteria**: SoA signed; P1 implementation 100 %; AI-specific threat model per agent.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-5, SD-10; supports Goal G-4. Aligned to PRIN §I.4.

### BR-006: Workforce capability uplift aligned to FAHR

**Description**: Entity reviewer cohorts (procurement officers, tax auditors, service-desk staff, MoHRE case officers) are trained and competence-assessed; entity contribution to the 80,000-cohort national figure reported quarterly to FAHR.

**Rationale**: Workflow-redesign KPI requires real capability uplift, not symbolic training; SD-8 workforce confidence depends on it.

**Success Criteria**: ≥ 80 % of reviewer population trained and competence-assessed by 2026-08-28; FAHR submission on cadence.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-8; supports Goal G-8, Outcome O-3.

### BR-007: Working contestation route for every citizen-affecting decision class

**Description**: AI-001 (supplier-affecting), AI-002 (tax), AI-003 (citizen-facing), AI-005 (work-permits) each have a published contestation route, in plain Arabic and English, with a bounded human-review SLA and a quarterly sample review.

**Rationale**: Charter Principle 6 (Human Oversight) and Principle 11 (Inclusive Access) require it; PDPL data-subject rights overlap.

**Success Criteria**: 4 of 4 published; SLA defined per agent; ≥ 95 % SLA attainment by Q4 2026.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-9, SD-3; supports Goal G-7.

### BR-008: Autonomy tier classified and promotion gate enforced per agent

**Description**: All five agents are classified Tier 1 / 2 / 3 and the promotion gate is enforced by the AI Governance Committee with Highest Authority sign-off for Tier-3.

**Rationale**: Resolves the pace-vs-depth conflict (STKE Conflict 1); makes the trade-off explicit and auditable.

**Success Criteria**: 5 of 5 classified; promotion-gate evidence per tier promotion; AI Governance Committee minutes record the decision.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-1, SD-3, SD-4, SD-5, SD-6, SD-7; supports Goal G-2. Aligned to PRIN §I.2.

### BR-009: Zero reportable Charter / PDPL / IAS incident attributable to the portfolio in the first reporting cycle

**Description**: No reportable incident traceable to the portfolio in Q3 2026 (the first full reporting cycle after this requirements document).

**Rationale**: A reportable incident at this stage would damage the directive's credibility and undermine the Ministerial Council's narrative.

**Success Criteria**: Zero PDPL-reportable breach; zero IAS-reportable incident; no Charter-conformance finding requiring service withdrawal.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-1, SD-3, SD-5, SD-6, SD-10, SD-11; supports Outcome O-4.

### BR-010: Fairness baselined for every agent before any tier-promotion

**Description**: Each agent has a documented fairness-metric choice, a representative evaluation set, a measured baseline, and an Arabic-English parity result before Tier-2 or Tier-3 sign-off.

**Rationale**: Charter Principles 3 (Bias Mitigation) and 11 (Inclusive Access); SD-9 (citizen rights); the HIGH residual bias risk flagged in `ARC-001-AICH-v1.0` for AI-002 and AI-005.

**Success Criteria**: 5 of 5 baselined; thresholds defined; promotion-gate enforces them.

**Priority**: MUST_HAVE.

**Stakeholder**: SD-9, SD-3, SD-7; supports Goal G-5. Aligned to PRIN §III.13.

---

## Functional Requirements

### User Personas

#### Persona 1 — Federal Operator (Procurement Officer / Tax Auditor / Service-Desk Officer / MoHRE Case Officer)

- **Role**: Day-to-day reviewer, override-exerciser, partner of the agent on individual decisions.
- **Goals**: Make better and faster decisions with the agent than without; be confident the tool is supporting rather than replacing them.
- **Pain Points**: Tools that ask them to rubber-stamp; metric pressure that punishes overrides; ambiguity over who is accountable.
- **Technical proficiency**: Medium. Strong domain knowledge; variable familiarity with AI behaviour.

#### Persona 2 — CAIO and AI Governance Committee Member

- **Role**: Portfolio-level decision-maker; tier-promotion authority; incident escalation point.
- **Goals**: Make tier promotions defensibly; surface incidents early; show measurable directive progress.
- **Pain Points**: Cabinet Affairs pace pressure colliding with assurance evidence; vendor opacity; surprises.

#### Persona 3 — UAE Citizen, Resident, or Business

- **Role**: Affected party of an agent decision (tender outcome, tax decision, service answer, work-permit decision).
- **Goals**: Get a fast accurate answer; understand the reason if the answer is "no"; have a real way to challenge it.
- **Pain Points**: "Computer said no"; Arabic-dialect failure; appeal queues that defeat the right.

#### Persona 4 — Ministry Service SRO

- **Role**: Service-line owner whose service the agent is automating; signs off on tier promotion.
- **Goals**: The agent makes their service better; the metric story improves; no surprise incidents.

#### Persona 5 — Auditor / Compliance Reviewer (DPO, CISO, Data Office, Cybersecurity Council)

- **Role**: Verifies PDPL, IAS, Charter compliance.
- **Goals**: Auditable evidence per agent; no surprises; clear accountability per decision.

---

### Functional Requirements Detail

#### FR-001: Confidence-based routing to human reviewer

**Description**: Every Tier-1 and Tier-2 agent decision is routed for human review when the agent's confidence falls below a per-agent, per-decision-class threshold, or when sensitive context is detected.

**Relates To**: BR-007, BR-008; UC of every agent.

**Acceptance Criteria**:

- Given a decision with confidence < threshold, when processed, then the decision is routed to a reviewer in their queue within the oversight-latency SLA.
- Given a sensitive-context signal (e.g., vulnerability flag, complaint, contestation), when detected, then the decision is routed regardless of confidence.
- Edge case: routing-system failure → decision held; human alerted; never silently passed.

**Priority**: MUST_HAVE. **Complexity**: HIGH.

#### FR-002: Per-decision rationale generation

**Description**: Every decision (Tier-1, 2, 3) produces a stored, retrievable rationale that a reviewer or affected party can interrogate at a later point.

**Relates To**: BR-002, BR-007; aligned to PRIN §I.6, §III.14.

**Acceptance Criteria**:

- Given a completed decision, when an authorised user requests the rationale, then it is retrieved with the input, model version, confidence, output, and timestamp.
- Given a request from the affected citizen (via PDPL data-subject right), when invoked, then a human-readable rationale is produced in the citizen's language (Arabic or English minimum).

**Priority**: MUST_HAVE.

#### FR-003: Override and revoke mechanism per agent

**Description**: An accountable officer can override an agent action and (for actions with downstream effect) revoke it. The override is logged, the reason is captured, and the revoke restores prior state where reversible.

**Relates To**: BR-008, BR-009; PRIN §I.1.

**Acceptance Criteria**:

- Given an agent action, when the officer initiates override, then the action is reversed and the override is logged with reason and timestamp.
- Given a Tier-3 autonomous action with downstream effect, when revocation is initiated, then the downstream system receives a documented reversal and the citizen / business is notified.
- Override drill exercised end-to-end at least quarterly with recorded result.

**Priority**: MUST_HAVE.

#### FR-004: Citizen / business contestation submission

**Description**: Affected parties can submit a contestation against a decision through a published channel in Arabic and English, with confirmation and tracking.

**Relates To**: BR-007; SD-9.

**Acceptance Criteria**:

- Given an affected party, when they submit a contestation, then a case ID is issued and the SLA for response is communicated.
- Channel is accessible by web, mobile, and (for AI-005 work-permit applicants) MoHRE in-person path.

**Priority**: MUST_HAVE.

#### FR-005: Contestation review and decision workflow

**Description**: Each contestation is reviewed by an authorised officer (independent of the original decision where the agent was autonomous), reaches a decision within the SLA, and the outcome is recorded.

**Relates To**: BR-007; FR-004.

**Acceptance Criteria**:

- Given a contestation case, when worked, then it reaches a decision within the SLA in ≥ 95 % of cases at portfolio level.
- Outcome categories include "upheld", "overturned", "modified", "out of scope"; the contestation-overturn rate is a portfolio KPI.

**Priority**: MUST_HAVE.

#### FR-006: ATRS record management per agent

**Description**: For every Tier-2 or Tier-3 agent, an ATRS-equivalent record is authored, version-controlled, published, and updated on material change.

**Relates To**: BR-002; SD-3, SD-9.

**Acceptance Criteria**:

- Given a Tier-2 or Tier-3 agent, when go-live is approached, then its ATRS is published before go-live.
- Given a material model, scope, or training-data change, when detected, then the ATRS is updated within 30 days.
- ATRS is citizen-readable in Arabic and English (signed off by a non-engineering reviewer).

**Priority**: MUST_HAVE.

#### FR-007: Autonomy-tier classification workflow

**Description**: Every agent has a recorded tier (1 / 2 / 3) classified through a documented assessment, with promotion gated by the AI Governance Committee.

**Relates To**: BR-008; PRIN §I.2.

**Acceptance Criteria**:

- Given a new agent, when introduced, then it enters at the lowest defensible tier and is classified before production traffic.
- Given a tier-promotion proposal, when submitted, then the promotion criteria are evaluated, evidence is recorded, and committee minutes capture the decision.

**Priority**: MUST_HAVE.

#### FR-008: Promotion-gate evidence aggregation

**Description**: Tier-promotion requests are accompanied by a standardised evidence pack: PDPL DPIA, IAS controls evidence, fairness baseline, ATRS, override drill, contestation route, SRO sign-off.

**Relates To**: BR-008; FR-006, FR-007.

**Acceptance Criteria**: pack is auto-generated from the underlying artefacts where possible; gaps are surfaced; AI Governance Committee can refuse promotion until gaps closed.

**Priority**: MUST_HAVE.

#### FR-009: Write-once, signed audit log for legally consequential decisions

**Description**: Decisions with legal effect (e.g., AI-005 work-permit grants/refusals; AI-002 tax assessments) write a tamper-evident audit record.

**Relates To**: BR-009; PRIN §I.6.

**Acceptance Criteria**: append-only storage with cryptographic chaining; retrieval supports both per-decision audit and aggregate analysis; retention aligned to the Digital Records Policy and the entity's records schedule.

**Priority**: MUST_HAVE.

#### FR-010: Bias monitoring and dashboarding

**Description**: Continuous-monitoring of fairness metrics per agent in production; thresholds defined; material disparity triggers a documented remediation workflow.

**Relates To**: BR-010; PRIN §III.13.

**Acceptance Criteria**: per-agent fairness dashboard live before Tier-2 promotion; threshold-breach generates an automated ticket to the named owner.

**Priority**: MUST_HAVE.

#### FR-011: Drift detection and alerting

**Description**: Continuous-monitoring for input-distribution drift, output drift, and prediction-vs-outcome drift per agent.

**Relates To**: BR-009; PRIN §III.15.

**Acceptance Criteria**: drift dashboards live; threshold-breach paged to named owner; foundation-model base-version change is treated as an event (FR-019).

**Priority**: MUST_HAVE.

#### FR-012: Reviewer competence assessment and recording

**Description**: Reviewer population is competence-assessed before being authorised to review live agent decisions; re-assessed annually; recorded in an auditable register.

**Relates To**: BR-006; SD-8.

**Priority**: MUST_HAVE.

#### FR-013: Operator training delivery aligned to FAHR

**Description**: Training programme co-designed with FAHR; uptake and completion reported quarterly.

**Relates To**: BR-006; SD-8.

**Priority**: MUST_HAVE.

#### FR-014: Workforce KPI submission interface

**Description**: Standardised return of workforce uplift to FAHR's national 80,000-cohort tracker.

**Relates To**: BR-006.

**Priority**: SHOULD_HAVE.

#### FR-015: Quarterly Ministerial Council reporting export

**Description**: One-click generation of the quarterly KPI report (adoption / quality / workflow-redesign per agent), in the Ministerial Council Secretariat's specified format.

**Relates To**: BR-001, BR-003.

**Priority**: MUST_HAVE.

#### FR-016: Plain-language Arabic / English content authoring and publication

**Description**: Authoring and publication of ATRS, contestation routes, and citizen-facing messages with parallel Arabic and English versions; readability tested.

**Relates To**: BR-002, BR-007; Charter Principle 11; PRIN §III.13.

**Priority**: MUST_HAVE.

#### FR-017: Per-agent fallback delivery path

**Description**: For every Tier-2 and Tier-3 agent, a documented fallback exists (human officer, prior system) and is exercised at least annually.

**Relates To**: BR-009; PRIN §I.5.

**Priority**: MUST_HAVE.

#### FR-018: Incident reporting workflow

**Description**: Standardised workflow for reportable incidents to the Data Office (PDPL), Cybersecurity Council (IAS), and the Ministerial Council Secretariat where applicable, with internal escalation to the Highest Authority.

**Relates To**: BR-009.

**Priority**: MUST_HAVE.

#### FR-019: Tier-revert (e.g., Tier 3 → Tier 2) on incident or drift

**Description**: An incident, sustained threshold breach, or unannounced base-model change triggers automatic or committee-driven downgrade of the tier (with human approval required per decision until remediated).

**Relates To**: BR-008, BR-009; resolves part of STKE Conflict 1.

**Priority**: MUST_HAVE.

#### FR-020: ICV scoring support for AI-001 procurement decisions

**Description**: AI-001 supports federal procurement-decision drafting including In-Country Value (ICV) scoring per Federal Decree-Law 11/2023.

**Relates To**: BR-001 (per-agent quality KPI).

**Priority**: MUST_HAVE (for AI-001).

#### FR-021: Tax-risk-tier model input for AI-002

**Description**: AI-002 produces a documented risk-tier scoring for each audit candidate with the contributing factors recorded and surfaced to the reviewing auditor.

**Relates To**: BR-001 (for AI-002), BR-010.

**Priority**: MUST_HAVE (for AI-002).

#### FR-022: Citizen escalation handoff for AI-003

**Description**: AI-003 can hand off to a human service-desk officer with the full conversation context, surfacing the "you are now talking to a human" signal unmistakably to the citizen.

**Relates To**: BR-007; PRIN §I.1.

**Priority**: MUST_HAVE (for AI-003).

#### FR-023: Service-desk ticket auto-close gate for AI-004

**Description**: AI-004 auto-close of a ticket is gated by a confidence threshold and a ticket-class allowlist; user-initiated reopen restores the ticket without prejudice.

**Relates To**: BR-008, BR-009.

**Priority**: SHOULD_HAVE (for AI-004).

#### FR-024: Work-permit refusal officer-signature flow for AI-005

**Description**: AI-005 refusal decisions either carry an officer signature, or are issued under a documented Tier-3 envelope with audit-log integrity and an unconditional contestation right.

**Relates To**: BR-007, BR-008, BR-009, FR-009.

**Priority**: MUST_HAVE (for AI-005).

---

## Non-Functional Requirements

### Performance

#### NFR-P-001: Citizen-facing response latency

**Requirement**: For AI-003 (conversational), agent first-token latency p95 < 3 seconds; full response p95 < 8 seconds.

**Measurement**: APM telemetry.

**Priority**: MUST_HAVE (for AI-003).

#### NFR-P-002: Decision throughput per agent

**Requirement**: Per-agent peak-load capacity at the federal-trajectory load defined in `/arckit:roadmap`.

**Priority**: MUST_HAVE.

#### NFR-P-003: Oversight latency SLA per tier

**Requirement**: Maximum time between an agent action and the earliest possible human review or revocation:

- Tier 1: not applicable (review before action)
- Tier 2: per-decision review at action time
- Tier 3: revocation possible within a defined SLA per agent (e.g., AI-005 ≤ 24 hours given the legal-effect class)

**Priority**: MUST_HAVE. Aligned to PRIN §I.1.

### Availability

#### NFR-A-001: Per-agent uptime SLA

**Requirement**: Citizen-facing agents (AI-003, AI-005) ≥ 99.9 % uptime monthly; internal agents (AI-001, AI-004) ≥ 99.5 %; AI-002 per FTA's operational requirement.

**Priority**: MUST_HAVE.

#### NFR-A-002: Graceful degradation to documented fallback

**Requirement**: When the agent or its dependencies are unavailable, service falls through to the documented fallback (human officer / prior system) per FR-017 without data loss.

**Priority**: MUST_HAVE. Aligned to PRIN §I.5.

#### NFR-A-003: RTO / RPO per tier

**Requirement**: Per-agent recovery time and recovery point objectives defined and tested; default Tier-3 RTO ≤ 4 hours, RPO ≤ 15 minutes; Tier-2 RTO ≤ 8 hours, RPO ≤ 1 hour.

**Priority**: MUST_HAVE.

#### NFR-A-004: Geographic redundancy within the sovereign envelope

**Requirement**: Production agents run in at least two UAE-resident availability zones / regions on the approved sovereign-CSP set; failover does not cross the residency boundary defined by the data's classification.

**Priority**: MUST_HAVE. Aligned to PRIN §I.7, §II.10.

### Scalability

#### NFR-S-001: Horizontal scaling within sovereign boundaries

**Requirement**: Each agent scales horizontally to the directive-trajectory load; auto-scaling does not provision capacity outside the approved sovereign CSPs per classification.

**Priority**: MUST_HAVE. Aligned to PRIN §I.7.

#### NFR-S-002: Audit-log volume scaling

**Requirement**: Per-decision audit-log infrastructure scales to portfolio-wide volume, with retention aligned to the Digital Records Policy and the entity's records schedule (typically ≥ 7 years for legal-effect decisions).

**Priority**: MUST_HAVE.

### Security

#### NFR-SEC-001: Authentication via federal identity baseline

**Requirement**: Citizen-facing services authenticate via UAE Pass (Basic or Verified profile per the agent's risk tier); internal access uses the entity's federal identity baseline with MFA.

**Priority**: MUST_HAVE. Aligned to PRIN §IV.18.

#### NFR-SEC-002: Service-account / agent-identity separation from human identity

**Requirement**: Agent service-accounts are distinct from any human identity, audited as such, with least privilege and rotated credentials.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4, §IV.18.

#### NFR-SEC-003: Encryption in transit and at rest with sovereign key management

**Requirement**: Industry-standard transport encryption; AES-256-equivalent at rest; for Confidential and above, sovereign-managed keys (entity- or UAE-jurisdiction-controlled HSM) unless an approved exception applies.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4, §II.10.

#### NFR-SEC-004: Secrets management

**Requirement**: No secrets in code or configuration; sovereign-jurisdiction secret-storage; rotation on defined cadence.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4.

#### NFR-SEC-005: Vulnerability and adversarial AI testing

**Requirement**: Dependency scanning, SAST, DAST, plus AI-specific adversarial testing (prompt injection, jailbreak, data poisoning, model extraction) in the CI/CD pipeline and on rolling cadence; pen test annually by an approved provider.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4, §V.20.

#### NFR-SEC-006: Network segmentation per classification

**Requirement**: Network segmentation respects the Smart Data classification; Confidential and above isolated; cross-segment flows controlled and logged.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4, §II.9.

#### NFR-SEC-007: Audit-log integrity (write-once, signed) for legal-effect decisions

**Requirement**: As per FR-009, audit logs for legal-effect decisions are append-only with cryptographic integrity.

**Priority**: MUST_HAVE.

#### NFR-SEC-008: UAE IAS P1 compliance

**Requirement**: IAS Statement of Applicability signed; all P1 controls (subset of the 188 M1–M6 / T1–T9 controls) implemented and evidenced.

**Priority**: MUST_HAVE. Aligned to PRIN §I.4. Anchor for BR-005.

### Compliance

#### NFR-C-001: PDPL DPIA performed and current per personal-data-touching agent

**Requirement**: As per BR-004; DPIA reviewed at least annually and on material change.

**Priority**: MUST_HAVE.

#### NFR-C-002: ATRS published per Tier-2 / Tier-3 agent

**Requirement**: As per BR-002 and FR-006.

**Priority**: MUST_HAVE.

#### NFR-C-003: Per-decision audit log retention aligned to Digital Records Policy

**Requirement**: Retention per the records schedule applicable to each decision class (legally consequential decisions typically ≥ 7 years; conversational logs per PDPL minimisation principle).

**Priority**: MUST_HAVE.

#### NFR-C-004: Cross-border-transfer log maintained

**Requirement**: A current, auditable log of any cross-border transfer of personal data with the lawful mechanism cited; default position is no transfer.

**Priority**: MUST_HAVE.

#### NFR-C-005: Charter conformance assessment quarterly

**Requirement**: `/arckit-uae:uae-ai-charter` re-run quarterly with current evidence per principle; results reviewed by the AI Governance Committee.

**Priority**: MUST_HAVE.

#### NFR-C-006: Smart Data classification register maintained

**Requirement**: Every dataset, model input, model output, and agent-generated artefact has a recorded classification per the UAE Smart Data Framework (Open / Shared / Confidential / Secret / Top Secret).

**Priority**: MUST_HAVE. Aligned to PRIN §II.9.

### Usability

#### NFR-U-001: Arabic-language parity with English

**Requirement**: Citizen-facing functionality (AI-003, AI-005 portal, contestation flows) performs at parity in Arabic and English on accuracy, latency, and accessibility metrics. Parity thresholds defined per agent and measured continuously.

**Priority**: MUST_HAVE. Aligned to PRIN §III.13.

#### NFR-U-002: Accessibility (WCAG 2.1 AA equivalent)

**Requirement**: Citizen-facing components meet WCAG 2.1 AA or the UAE-equivalent national accessibility standard; tested in CI/CD and on a manual cadence.

**Priority**: MUST_HAVE.

#### NFR-U-003: Citizen-readability of ATRS and contestation flows

**Requirement**: ATRS and contestation content written for citizen comprehension and signed off by a non-engineering reviewer in both Arabic and English.

**Priority**: MUST_HAVE.

### Maintainability / Observability

#### NFR-M-001: Per-agent observability (logs, metrics, traces, behavioural and drift metrics)

**Requirement**: As per PRIN §I.6 — operational + behavioural + drift telemetry per agent with SLO-based alerting and named runbook owners.

**Priority**: MUST_HAVE.

#### NFR-M-002: Per-agent operational runbooks and incident playbooks

**Requirement**: Runbooks for deployment, rollback, scaling, fallback activation, tier-revert, and incident escalation; reviewed quarterly; rehearsed annually.

**Priority**: MUST_HAVE.

#### NFR-M-003: Documentation currency

**Requirement**: Architecture documentation, ADRs, ATRS, and runbooks updated within 30 days of material change.

**Priority**: SHOULD_HAVE.

### Interoperability

#### NFR-I-001: Federation via published APIs (no DB or file integration across entity boundaries)

**Requirement**: Inter-entity and inter-system integration uses published, versioned APIs per PRIN §IV.17; database-level or file-drop integration across entity boundaries is prohibited.

**Priority**: MUST_HAVE.

#### NFR-I-002: UAE Pass integration with profile selection per risk tier

**Requirement**: Citizen-facing services integrate UAE Pass (Basic profile sufficient for low-risk; Verified for legal-effect decisions); e-signature audit trail where the service produces a legally consequential record.

**Priority**: MUST_HAVE.

#### NFR-I-003: API versioning with backward compatibility

**Requirement**: All published APIs are versioned (URL-path or header) with a defined backward-compatibility window; breaking changes communicated and gated.

**Priority**: MUST_HAVE.

---

## Integration Requirements

### INT-001: UAE Pass

**Purpose**: Federated citizen identity for AI-003 (low-risk Basic profile sufficient) and AI-005 (Verified profile required given legal-effect class).

**Integration Type**: OIDC / OAuth.

**Authentication**: Federal identity protocol.

**Priority**: MUST_HAVE.

### INT-002: Federal Procurement Platform (MoF Digital Procurement Platform)

**Purpose**: AI-001 reads tender corpora, supplier records, and writes draft tenders / evaluation support per Federal Decree-Law 11/2023.

**Integration Type**: API; classification-aware.

**Priority**: MUST_HAVE.

### INT-003: Federal Tax Authority core systems

**Purpose**: AI-002 reads taxpayer filings, writes audit-candidate risk scores and draft assessments back to the FTA case-management system.

**Integration Type**: API; Confidential classification.

**Priority**: MUST_HAVE.

### INT-004: Federal service catalogue and citizen portals

**Purpose**: AI-003 surfaces in federal portals; intent triage routes to the right downstream service.

**Integration Type**: Web / API; conversation-state-bearing.

**Priority**: MUST_HAVE.

### INT-005: Entity ITSM / service-desk

**Purpose**: AI-004 reads / writes tickets, knowledge base, change records.

**Integration Type**: API; internal classification.

**Priority**: MUST_HAVE.

### INT-006: MoHRE core / work-permit systems

**Purpose**: AI-005 reads applications, decides (per Tier-3 envelope) or proposes (per Tier-2), writes decisions and audit records.

**Integration Type**: API; Confidential classification; write-once audit log per FR-009.

**Priority**: MUST_HAVE.

### INT-007: Foundation-model vendor APIs (and on-premise/sovereign-hosted equivalents)

**Purpose**: Underlying model inference for the conversational and language-rich use cases.

**Integration Type**: API; processor contracts under PDPL Article-equivalent; cross-border-transfer minimisation per NFR-C-004.

**Priority**: MUST_HAVE.

### INT-008: Sovereign CSP control planes

**Purpose**: Compute, storage, key management within the approved CSP set (Core42 / G42 sovereign, Microsoft UAE North/Central, TDRA FedNet, e& Sovereign Launchpad on AWS) per Cloud Residency Policy v2.

**Priority**: MUST_HAVE.

### INT-009: UAE Data Office incident-reporting channel

**Purpose**: Reportable-incident notification per PDPL.

**Priority**: MUST_HAVE.

### INT-010: UAE Cybersecurity Council incident-reporting channel

**Purpose**: Reportable-incident notification per IAS.

**Priority**: MUST_HAVE.

### INT-011: Cross-entity Data Sharing Policy API surface

**Purpose**: Collect-once / share-many — entities call other entities' authoritative sources rather than re-collecting.

**Integration Type**: API; Data Sharing Agreement per share; lawful basis under PDPL recorded.

**Priority**: MUST_HAVE. Aligned to PRIN §II.12.

### INT-012: FAHR workforce systems

**Purpose**: Submission of workforce-uplift KPIs to the national 80,000-cohort tracker.

**Priority**: SHOULD_HAVE.

---

## Data Requirements

### DR-001: Per-decision audit record

**Description**: Structured record of every agent decision: input (classification-respecting), model version, confidence, rationale, output, reviewer (if any), final action, timestamp, contestation flag.

**Classification**: depends on input class; aggregate record typically Confidential.

**Retention**: per Digital Records Policy; legal-effect decisions ≥ 7 years.

**Access patterns**: per-case retrieval; aggregate analytics; auditor read.

### DR-002: Citizen / business / employee identifier mapping

**Description**: Linkage to UAE Pass / Emirates ID where lawful; consistent with PDPL Article-equivalent.

**Classification**: Confidential.

### DR-003: Training and fine-tuning dataset register

**Description**: Per-agent record of training/evaluation datasets — source, lawful basis, licensing, provenance, version.

**Classification**: Internal–Confidential.

### DR-004: Fairness-evaluation dataset

**Description**: Per-agent representative evaluation set; demographic representation documented within lawful constraints.

**Classification**: Confidential; access tightly controlled.

### DR-005: ATRS record per agent

**Description**: Authored Arabic + English transparency record; version-controlled.

**Classification**: PUBLIC on publication.

### DR-006: Lawful-basis register per processing activity

**Description**: For each personal-data processing activity, the PDPL lawful basis, controller/processor designation, retention period, data-subject rights process.

**Classification**: Internal.

### DR-007: Cross-border-transfer log

**Description**: Per-transfer record — destination jurisdiction, lawful mechanism, data class, volume, purpose.

**Classification**: Internal.

### DR-008: Smart Data classification register

**Description**: Catalogue of every dataset / model artefact with classification, handling rules, aggregation-uplift rule.

**Classification**: Internal.

### DR-009: Reviewer-competence record per operator

**Description**: Training, assessment outcome, re-assessment dates, scope of authorisation per reviewer.

**Classification**: Internal (workforce data).

### DR-010: Contestation case record

**Description**: Per-case record — submitter, decision contested, outcome, time-to-resolution, reviewer; supports the contestation overturn-rate KPI.

**Classification**: Confidential where personal-data-bearing.

---

## Constraints and Assumptions

### Technical Constraints

- **TC-1**: All production agents must be hosted on approved sovereign CSPs per the National Cloud Security Policy v2.
- **TC-2**: Confidential and above data must use sovereign-managed keys unless an approved compensating-control exception is recorded.
- **TC-3**: Inter-entity integration is API-based; no direct database or file-drop coupling across entity boundaries.
- **TC-4**: Foundation-model usage must be contractually compatible with PDPL and the Charter — vendor opacity is a known risk per `ARC-001-AICH-v1.0`.

### Business Constraints

- **BC-1**: The 24-month directive horizon to 2028 is fixed.
- **BC-2**: Tier-3 promotion requires Highest Authority sign-off — non-negotiable.
- **BC-3**: PRIN §I.1 (Human Oversight) and §I.4 (Security by Design) are non-waivable principles.
- **BC-4**: Quarterly Ministerial Council reporting on the three KPIs is mandatory.

### Assumptions

- **A-1**: The five named agents continue to operate as described in `ARC-001-AICH-v1.0` (subject to verification of vendor / model / deployment details).
- **A-2**: UAE Pass remains the federal citizen-identity baseline.
- **A-3**: The approved sovereign-CSP set remains current; if any provider's accreditation changes, residency map (DR-008) is updated.
- **A-4**: Foundation-model vendors will accept contractual obligations sufficient for ATRS and PDPL evidence; where they will not, the agent does not achieve Tier-3 status.
- **A-5**: FAHR's national 80,000-cohort programme remains the workforce-uplift channel.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Method |
|--------|----------|--------|----------|--------|
| Entity contribution to federal 50 %-by-2028 | Not measured | Trajectory on track | 2028 | Per-agent telemetry |
| Adoption-speed KPI per agent | Not measured | Aligned to roadmap | Quarterly | Telemetry |
| Implementation-quality composite per agent | Not measured | ≥ pre-agent baseline; ≥ thresholds per agent | Quarterly | Telemetry + survey + appeals |
| Workflow-redesign evidence per agent | Not documented | ≥ 1 documented redesign per agent | 2026-Q4 | Service review |
| ATRS-published count | 0 | 5 | 2026-08-28 | Inventory |
| PDPL DPIA-complete count | 0 | 3 | 2026-08-28 | DPO audit |
| IAS P1 implementation | 0 % | 100 % | 2026-08-28 | CISO audit |
| Fairness-baselined count | 0 | 5 | 2026-08-28 | Independent evaluation |
| Workforce reviewer-cohort training | Not started | ≥ 80 % | 2026-08-28 | FAHR submission |
| Reportable incidents attributable to portfolio | n/a | 0 | 2026-Q3 | Incident register |

### Technical Success Metrics

| Metric | Target | Method |
|--------|--------|--------|
| Per-agent uptime SLA attainment | as per NFR-A-001 | Uptime monitoring |
| Oversight-latency SLA attainment | as per NFR-P-003 | Telemetry |
| Contestation-route SLA attainment | ≥ 95 % by 2026-Q4 | Case-tracking |
| Bias-monitoring threshold-breach response time | within SLA per agent | Alerting |
| Drift-detection threshold-breach response time | within SLA per agent | Alerting |
| Override drill exercise frequency | quarterly per agent | Operations register |

---

## Dependencies and Risks

### Dependencies

| Dependency | Owner | Status | Impact if delayed |
|------------|-------|--------|--------------------|
| Approval of `ARC-000-PRIN-v1.0` | AI Governance Committee + Highest Authority | DRAFT | HIGH — every artefact ties back to it |
| `/arckit-uae:uae-ai-autonomy-tier` artefact | CAIO | not yet produced | HIGH — gates BR-008 |
| `/arckit-uae:uae-pdpl` artefact per agent | DPO | not yet produced | HIGH — gates BR-004 |
| `/arckit-uae:uae-ias` SoA | CISO | not yet produced | HIGH — gates BR-005 |
| `/arckit:atrs` × 5 records | CAIO | not yet produced | CRITICAL — gates BR-002 |
| Sovereign-CSP shared-responsibility matrix per provider | CDO / Procurement | not yet signed | HIGH |
| Foundation-model vendor contracts with disclosure obligations | Procurement + DPO + Legal | not yet executed | HIGH |
| FAHR workforce-uplift programme co-design | HR + FAHR | not yet started | MEDIUM |

### Risks (preview — full register in `/arckit:risk`)

| ID | Description | P | I | Mitigation | Owner |
|----|-------------|---|---|------------|-------|
| R-1 | Pace pressure produces premature Tier-3 promotion | MED | HIGH | Tier-gate enforcement; AI Gov Committee minute; rollback path | CAIO + AI Gov Cmte |
| R-2 | Vendor opacity blocks ATRS/PDPL evidence | HIGH | MED | Contractual disclosure; tier-link to disclosure; vendor diversification | Procurement + DPO |
| R-3 | Workforce disengagement | MED | HIGH | FAHR-coord training; KPI 3 framing as uplift; reviewer-role description | HR + CAIO |
| R-4 | Contestation route becomes theatre | MED | HIGH | SLA-attainment KPI; escalation rule | CAIO + SROs |
| R-5 | Drift in foundation-model behaviour (vendor base-version change) | HIGH | MED | Contractual change-notification; drift detection (FR-011); tier-revert (FR-019) | CAIO + Vendor |
| R-6 | Cross-border residency violation via supplier defaults | MED | HIGH | Residency map; classification-aware gates; auto-deploy refusal | CDO + CISO |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Pace (Cabinet Affairs) vs Depth (CISO / DPO / SRO)

**Conflicting requirements**: BR-001 / BR-003 (pace-pressured federal KPI delivery) vs BR-004 / BR-005 / BR-010 (PDPL, IAS, fairness depth before tier promotion).

**Stakeholders involved**: SD-2 (Cabinet Affairs) wants visible monthly progress; SD-5 (CISO), SD-6 (DPO), SD-7 (SROs), SD-9 (citizens via SD-3) want evidence before sign-off.

**Trade-off analysis**:

| Option | Pros | Cons |
|--------|------|------|
| Prioritise pace — accept Tier-3 promotion on partial evidence | Cabinet Affairs KPI achieved | Incident risk; Charter and PDPL exposure; Ministerial Council reputational risk |
| Prioritise depth — defer Tier-3 promotion until full evidence | No incident risk in this cycle | Slower KPI lift; Cabinet Affairs dissatisfied |
| **Phase via autonomy tier (BR-008, PRIN §I.2)** | Pace rewarded at Tier 1/2; depth required for Tier 3; trade-off explicit, auditable | Operational discipline required; tier-revert FR-019 must be real |

**Resolution strategy**: PHASE.

**Decision**: The autonomy-tier gate (BR-008) is the resolution. Pace is the goal at Tier 1 (where outputs are reviewed before acting) and Tier 2 (where outputs are approved before acting). Tier-3 (autonomous within envelope) requires the depth evidence: PDPL DPIA, IAS P1 controls, fairness baseline, ATRS, override drill, contestation route, SRO sign-off, Highest Authority sign-off.

**Decision authority**: AI Governance Committee for Tier-2 promotion; Highest Authority for Tier-3 promotion (per STKE RACI).

**Stakeholder management**: Cabinet Affairs receives the explicit tier rationale on every quarterly submission; CISO / DPO / SRO receive procedural certainty that depth is required before pace.

### Conflict C-2: Citizen-readable transparency vs vendor IP

**Conflicting requirements**: BR-002 / FR-006 (full ATRS with provenance) vs INT-007 (foundation-model vendor terms; SD-12 commercial driver).

**Trade-off analysis**: full disclosure may be unobtainable from some vendors; thin ATRS undermines Charter Principle 5 and SD-9.

**Resolution strategy**: PRIORITISE the Charter (transparency) over the vendor commercial preference; INNOVATE through procurement leverage.

**Decision**: Tier-3 promotion requires vendor disclosure sufficient for ATRS. Where the vendor refuses, the agent is capped at Tier-2 (per-decision human approval) and the vendor-opacity gap is recorded in `ARC-001-AICH-v1.0`'s residual-risk column.

**Decision authority**: CAIO + Procurement; Highest Authority on exception.

### Conflict C-3: Real-time conversational latency (AI-003) vs sovereign-cloud single-region constraint

**Conflicting requirements**: NFR-P-001 (low latency for citizen conversation) vs NFR-A-004 + TC-1 (residency-bound capacity).

**Trade-off analysis**: cross-region acceleration could improve latency but cross the residency line.

**Resolution strategy**: INNOVATE — engineered solution (in-region edge inference + caching) per `/arckit:research` and the sovereign-CSP capability set; ADR records the chosen pattern.

**Decision authority**: CAIO + CDO; CISO consulted on residency.

### Conflict C-4: Override-rate metric pressure vs operator confidence

**Conflicting requirements**: BR-001 (Adoption-speed KPI — autonomous-share metric) vs PRIN §I.1 (override mechanism must be real, not theatre) vs FR-003 (override mechanism).

**Trade-off analysis**: a metric that rewards low override rates incentivises rubber-stamping; this is a leading indicator of failure per STKE risk R-3.

**Resolution strategy**: INNOVATE — measure override rate as a behavioural metric, not a target. Sustained low override rate triggers an audit of reviewer competence; sustained high override rate triggers a model/process audit. Adoption-speed KPI counts service interactions completed (autonomous + reviewed), not just autonomous-only.

**Decision authority**: AI Governance Committee.

### Conflict C-5: Tier-3 ambition vs zero-incident posture

**Conflicting requirements**: BR-001 (federal pace) vs BR-009 (zero reportable incident).

**Trade-off analysis**: faster Tier-3 promotion increases blast radius if an incident occurs.

**Resolution strategy**: PHASE + COMPROMISE — Tier-3 only on agents where both (a) depth evidence is complete and (b) blast radius can be bounded by FR-019 tier-revert; revoke on incident; rehearse the revoke quarterly.

**Decision authority**: Highest Authority on each Tier-3 promotion (per STKE RACI).

### Conflict C-6: Cross-entity collect-once-share-many vs PDPL lawful-basis per processing

**Conflicting requirements**: INT-011 (Data Sharing Policy — reuse before re-collect) vs BR-004 / NFR-C-001 (PDPL lawful basis per processing activity).

**Trade-off analysis**: collect-once is operationally efficient but each reuse is itself a processing activity that needs its own lawful basis.

**Resolution strategy**: COMPROMISE — every cross-entity reuse is governed by a Data Sharing Agreement (DSA) that records the lawful basis under PDPL; reuse without a DSA is not permitted regardless of operational pressure.

**Decision authority**: DPO with CAIO; Data Office consulted.

---

## Timeline and Milestones

| Milestone | Description | Target |
|-----------|-------------|--------|
| Requirements approval | Stakeholder sign-off on this document | 2026-06-27 |
| Tier classification complete (G-2) | All 5 agents classified per `/arckit-uae:uae-ai-autonomy-tier` | 2026-07-31 |
| PDPL DPIAs complete (G-3) | 3 agents | 2026-08-15 |
| IAS SoA signed (G-4) | All 5 agents | 2026-08-15 |
| Fairness baselined (G-5) | All 5 agents | 2026-08-20 |
| ATRS published (G-1, BR-002) | All 5 agents, Arabic + English | 2026-08-28 |
| First quarterly Ministerial Council submission | Three-KPI dashboard, with evidence pack | 2026-09-30 |
| Workforce-cohort training milestone (G-8) | ≥ 80 % of reviewer population trained | 2026-08-28 |

---

## Approval

| Reviewer | Role | Status |
|----------|------|--------|
| CAIO | Owner | [PENDING] |
| AI Governance Committee | Governance | [PENDING] |
| CISO | Security | [PENDING] |
| DPO | Data Protection | [PENDING] |
| Ministry Service SROs (×5) | Service Owners | [PENDING] |
| Entity Highest Authority | Approver | [PENDING] |

---

## External References

### Document Register

| Doc ID | Title | Source | Description |
|--------|-------|--------|-------------|
| ARC-000-PRIN-v1.0 | UAE Federal Entity — Agentic AI Architecture Principles | `projects/000-global/ARC-000-PRIN-v1.0.md` | Foundational principles; referenced throughout |
| ARC-001-STKE-v1.0 | Stakeholder Drivers & Goals Analysis | `projects/001-agentic-ai-portfolio/ARC-001-STKE-v1.0.md` | SD-1…SD-12, G-1…G-8, O-1…O-5 trace targets |
| ARC-001-AICH-v1.0 | UAE AI Charter Compliance Assessment | `projects/001-agentic-ai-portfolio/ARC-001-AICH-v1.0.md` | Five-agent inventory; Charter principle mapping |
| UAE-AI-CHARTER | UAE Charter for AI | <https://uaelegislation.gov.ae/en/policy/details/the-uae-charter-for-the-development-and-use-of-artificial-intelligence> | 2026-05-28 verified |

### Citations

| Citation | Doc ID | Section | Used in |
|----------|--------|---------|---------|
| REQ-1 | ARC-001-STKE-v1.0 | Goals G-1…G-8 | All BR and trace lines |
| REQ-2 | ARC-000-PRIN-v1.0 | §I.1, §I.2, §I.4, §I.6, §II.8, §II.10, §III.13, §III.14 | NFR alignment statements |
| REQ-3 | ARC-001-AICH-v1.0 | AI System Inventory; bias residual-risk | Per-agent requirements (FR-020…FR-024); BR-010 |
| REQ-4 | UAE-AI-CHARTER | Principles 3, 5, 6, 11 | BR-002, BR-007, BR-010, FR-016 |

### Unreferenced Documents

None. Authoritative UAE statutes (PDPL Federal Decree-Law 45/2021, the IAS text, National Cloud Security Policy v2, Smart Data Framework, Digital Records Policy, Data Sharing Policy, Federal Decree-Law 11/2023) should be loaded into `projects/000-global/policies/` for citation-grade traceability and re-run.

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-05-28
**ArcKit Version**: 5.4.0
**Project**: Agentic AI Portfolio (Project 001)
**AI Model**: Claude Opus 4.7 (1M context)
**Generation Context**: Anchored on ARC-000-PRIN-v1.0 (21 principles), ARC-001-STKE-v1.0 (12 SDs, 8 goals, 5 outcomes), and ARC-001-AICH-v1.0 (12-principle assessment, 5-agent inventory).
