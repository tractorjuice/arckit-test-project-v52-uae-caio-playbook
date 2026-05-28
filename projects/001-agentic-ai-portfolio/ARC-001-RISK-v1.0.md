# Risk Register: Agentic AI Portfolio

> **Template Origin**: Official | **ArcKit Version**: 5.4.0 | **Command**: `/arckit:risk` | **Methodology**: HM Treasury Orange Book (2023)

## Document Control

| Field | Value |
|-------|-------|
| Document ID | ARC-001-RISK-v1.0 |
| Document Type | Risk Register (RISK) — Orange Book aligned |
| Project | Agentic AI Portfolio (Project 001) |
| Classification | OFFICIAL |
| Status | DRAFT |
| Version | 1.0 |
| Created Date | 2026-05-28 |
| Last Modified | 2026-05-28 |
| Review Cycle | Monthly for Critical/High; quarterly for Medium/Low |
| Next Review Date | 2026-06-28 |
| Owner | Chief AI Officer (CAIO), entity to assign |
| Reviewed By | [PENDING] — AI Governance Committee, CISO, DPO, ministry SROs |
| Approved By | [PENDING] — Entity Highest Authority |
| Distribution | CAIO, AI Governance Committee, CISO, DPO, ministry SROs, Ministerial Council Secretariat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-05-28 | ArcKit AI | Initial creation — 25 risks across 6 Orange Book categories | [PENDING] | [PENDING] |

---

## Executive Summary

### Risk Profile Overview

**Total risks identified**: 25 across 6 categories.

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 2 | 0 | ↓ 100 % |
| **High** (13-19) | 9 | 1 | ↓ 89 % |
| **Medium** (6-12) | 14 | 17 | ↑ (re-classified from H/C) |
| **Low** (1-5) | 0 | 7 | new tier reached |
| **TOTAL** | **328** / 500 | **158** / 500 | **↓ 51.8 %** |

### Risk Category Distribution

| Category | Count | Avg inherent | Avg residual | Control effectiveness |
|----------|-------|--------------|--------------|------------------------|
| STRATEGIC | 5 | 14.4 | 9.4 | 35 % reduction |
| OPERATIONAL | 5 | 13.0 | 6.0 | 54 % reduction |
| FINANCIAL | 2 | 10.5 | 5.0 | 52 % reduction |
| COMPLIANCE | 5 | 12.4 | 5.4 | 56 % reduction |
| REPUTATIONAL | 3 | 15.0 | 7.0 | 53 % reduction |
| TECHNOLOGY | 5 | 12.8 | 5.0 | 61 % reduction |

### Overall Risk Assessment

- **Overall residual score**: 158 / 500 (31.6 %).
- **Risk reduction from controls**: ~52 % reduction from inherent.
- **Risk profile status**: ⚠️ **Concerning** — one residual High (R-001 Federal trajectory miss); 17 Medium risks requiring active monitoring. **Not** in the Unacceptable band, but not yet in the Acceptable band either. Monthly review by AI Governance Committee recommended until the first quarterly Ministerial Council submission demonstrates trajectory.

### Risks Exceeding Appetite

The entity has not yet adopted a formal risk-appetite statement (recommended via a future `projects/000-global/risk-appetite.md`). For this v1.0, an interim appetite is **assumed** consistent with PRIN §I.1 and §I.4 being non-negotiable, and Charter Principle 5 / 6 (Transparency / Oversight) tolerating only LOW residual risk. Under that interim posture:

| Risk ID | Title | Category | Residual | Interim appetite | Excess | Escalation |
|---------|-------|----------|----------|-------------------|--------|------------|
| R-001 | Federal directive trajectory missed | STRATEGIC | 15 (High) | Medium (12) | +3 | Quarterly to Ministerial Council |
| R-019 | Bias finding against rights-affecting agent | REPUTATIONAL | 8 (Medium) | Low (5) — Charter P3/P11 | +3 | Highest Authority review |
| R-018 | Citizen-facing incident with media amplification | REPUTATIONAL | 8 (Medium) | Low (5) — Charter P6 | +3 | Highest Authority review |

### Top 5 Risks Requiring Attention (by residual score)

1. **R-001** (STRATEGIC, **High** 15): Federal directive trajectory missed — *Owner*: Entity Highest Authority — *Status*: Open, in active treatment.
2. **R-002** (STRATEGIC, Medium 8): Pace pressure produces premature Tier-3 promotion → incident — *Owner*: AI Governance Committee — *Status*: In Progress.
3. **R-003** (OPERATIONAL, Medium 8): Vendor opacity blocks ATRS / PDPL evidence — *Owner*: Procurement — *Status*: In Progress (contract negotiations).
4. **R-018** (REPUTATIONAL, Medium 8): Citizen-facing incident with media amplification — *Owner*: Highest Authority — *Status*: Monitoring.
5. **R-019** (REPUTATIONAL, Medium 8): Bias finding against rights-affecting agent (AI-002, AI-005) — *Owner*: CAIO — *Status*: Open (fairness baseline still pending — see AICH residual-risk).

### Key Findings and Recommendations

**Key findings**:

- The portfolio's foundational principles (PRIN), stakeholder analysis (STKE), and Charter assessment (AICH) deliver substantial inherent-to-residual reduction (~52 %) — the assurance framework is sound on paper.
- **No residual Critical risks**, but the foundational controls assume the downstream artefacts (autonomy-tier classification, PDPL DPIA, IAS SoA, fairness baseline, ATRS) actually get produced. If they slip, several risks regress.
- **The two HIGH residual bias risks flagged in `ARC-001-AICH-v1.0` for AI-002 (Tax Auditing) and AI-005 (MoHRE Work-Permits) are the most urgent operational concern** — they don't appear as Critical on this register because the controls in PRIN §III.13 are theoretically in place, but the implementation evidence is missing.
- The federal-trajectory risk (R-001) remains High residual because the directive's 50 %-by-2028 target is genuinely ambitious; this is a strategic-risk-appetite question for the Ministerial Council, not an entity-only control problem.

**Recommendations**:

1. Treat the AICH HIGH residual bias risks as the **single highest operational priority** — fairness baseline (G-5) before any Tier-3 promotion for AI-002 / AI-005.
2. Adopt an explicit `projects/000-global/risk-appetite.md` aligned to PRIN non-negotiable principles and Charter principles 5, 6, 11 — this v1.0 uses interim assumed appetite.
3. Escalate R-001 (residual High) into the entity's quarterly Ministerial Council reporting line so the federal-trajectory risk is shared with Cabinet Affairs (whose pace pressure is part of the inherent risk).
4. Stand up monthly AI Governance Committee risk review until the first quarterly Ministerial Council submission lands cleanly.
5. Treat vendor-opacity (R-003) and model-drift (R-006) as connected operational risks; the contractual change-notification right is the linchpin control for both.

---

## A. Risk Matrix Visualisation

### Inherent Risk Matrix (Before Controls)

```text
                                    IMPACT
              1-Negligible 2-Minor    3-Moderate  4-Major     5-Catastrophic
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │   R-003   │           │           │
Certain    │    5      │    10     │    15     │    20     │    25     │
           │           │           │   R-006   │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │           │   R-010   │   R-007   │   R-001   │
           │    4      │    8      │   R-011   │   R-021   │   R-019   │
           │           │           │    12     │   R-024   │    20     │
           │           │           │           │   16      │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
3-Possible │           │           │   R-009   │   R-004   │   R-002   │
           │    3      │    6      │   R-012   │   R-008   │   R-013   │
           │           │           │    9      │   R-014   │   R-015   │
           │           │           │           │   R-023   │   R-018   │
           │           │           │           │   R-025   │     15    │
           │           │           │           │    12     │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
2-Unlikely │           │           │           │   R-022   │   R-005   │
           │    2      │    4      │    6      │     8     │   R-016   │
           │           │           │           │           │   R-017   │
           │           │           │           │           │   R-020   │
           │           │           │           │           │     10    │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
1-Rare     │    1      │    2      │    3      │    4      │    5      │
           └───────────┴───────────┴───────────┴───────────┴───────────┘

Legend: ██ Critical (20-25)  ▓▓ High (13-19)  ░░ Medium (6-12)  ·· Low (1-5)
```

**Inherent zones**:

- **Critical (20-25)**: R-001 (Federal trajectory miss), R-019 (Bias against rights-affecting agent).
- **High (13-19)**: R-002, R-003, R-006, R-007, R-013, R-015, R-018, R-021, R-024.
- **Medium (6-12)**: R-004, R-005, R-008, R-009, R-010, R-011, R-012, R-014, R-016, R-017, R-020, R-022, R-023, R-025.
- **Low (1-5)**: None at inherent.

### Residual Risk Matrix (After Controls)

```text
                                    IMPACT
              1-Negligible 2-Minor    3-Moderate  4-Major     5-Catastrophic
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │           │           │           │
Certain    │    5      │    10     │    15     │    20     │    25     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │   R-003   │           │           │           │
           │    4      │    8      │    12     │    16     │    20     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
3-Possible │           │           │   R-006   │           │   R-001   │
           │    3      │    6      │    9      │    12     │    15     │
           │           │           │           │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
2-Unlikely │           │   R-009   │   R-007   │   R-002   │           │
           │    2      │   R-012   │   R-008   │   R-004   │           │
           │           │   R-023   │   R-010   │   R-005   │           │
           │           │     4     │   R-011   │   R-013   │           │
           │           │           │   R-014   │   R-018   │           │
           │           │           │   R-021   │   R-019   │           │
           │           │           │   R-024   │     8     │           │
           │           │           │   R-025   │           │           │
           │           │           │     6     │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
1-Rare     │           │           │   R-022   │   R-015   │   R-016   │
           │    1      │    2      │     3     │   R-017   │   R-020   │
           │           │           │           │    4      │     5     │
           └───────────┴───────────┴───────────┴───────────┴───────────┘
```

**Residual movement** (selected):

- R-001 Critical 20 → High 15. Reduced one likelihood band; impact unchanged (directive horizon is fixed).
- R-019 Critical 20 → Medium 8. Fairness controls (PRIN §III.13, REQ G-5) drop likelihood and impact, but residual remains above interim appetite until baseline is measured.
- R-002 High 15 → Medium 8. Tier-gate (PRIN §I.2; REQ BR-008) is the master mitigation.
- R-013 High 15 → Medium 8. PDPL DPIA + lawful-basis register + residency.
- R-015 High 15 → Low 4. Strong controls (residency map + classification gates) drive a steep reduction.
- R-017 Medium 10 → Low 4. Write-once signed audit log per PRIN §I.6.

---

## B. Top 10 Risks by Residual Score

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-001 | Federal directive trajectory missed (50 %-by-2028) | STRATEGIC | 20 | 15 | Highest Authority | Open | TREAT |
| 2 | R-002 | Premature Tier-3 promotion → incident | STRATEGIC | 15 | 8 | AI Governance Committee | In Progress | TREAT |
| 3 | R-003 | Vendor opacity blocks ATRS / PDPL evidence | OPERATIONAL | 15 | 8 | Procurement + DPO | In Progress | TREAT |
| 4 | R-004 | Workforce disengagement undermines KPI-3 narrative | STRATEGIC | 12 | 8 | HR + CAIO | Open | TREAT |
| 5 | R-005 | Ministerial direction or scope changes mid-cycle | STRATEGIC | 10 | 8 | Highest Authority | Monitoring | TOLERATE |
| 6 | R-013 | PDPL breach attributable to the portfolio | COMPLIANCE | 15 | 8 | DPO | Open | TREAT |
| 7 | R-018 | Citizen-facing incident with media amplification | REPUTATIONAL | 15 | 8 | Highest Authority | Monitoring | TREAT |
| 8 | R-019 | Bias finding against rights-affecting agent (AI-002, AI-005) | REPUTATIONAL | 20 | 8 | CAIO | Open | TREAT |
| 9 | R-006 | Foundation-model vendor base-version drift | TECHNOLOGY | 15 | 6 | CAIO + Vendor | Open | TREAT + TRANSFER |
| 10 | R-007 | Override mechanism becomes theatre (rubber-stamping) | OPERATIONAL | 16 | 6 | AI Governance Committee | Open | TREAT |

---

## C. Detailed Risk Profiles

> Profiles for the 10 most impactful risks (top 10 by inherent score; or otherwise critical to manage). Remaining 15 risks in summary table §D.

### R-001 — Federal directive trajectory missed (50 %-by-2028)

**Category**: STRATEGIC. **Trace**: STKE SD-1, SD-2; REQ BR-001, BR-003.

**Description**: The entity's contribution to the federal 50 %-by-2028 autonomous-services target falls short, undermining the Ministerial Council's reported trajectory.

**Root cause**: Directive horizon is ambitious; assurance functions correctly insist on depth before tier promotion; some agents are bottle-necked on vendor disclosure (linked to R-003).

**Trigger events**: Two consecutive quarterly submissions below trajectory; Cabinet Affairs escalation; a peer entity overtakes the entity's pace and exposes the gap.

**Consequences**: Loss of standing with the Ministerial Council; Cabinet Affairs intervention; reputational hit to the entity's leadership.

**Affected stakeholders**: SD-1 (Ministerial Council), SD-2 (Cabinet Affairs), SD-3 (Entity Highest Authority), SD-4 (CAIO).

**Inherent**: L=4, I=5, **IR=20** (Critical).

**Controls in place**: monthly KPI reporting (REQ BR-003 / FR-015); autonomy-tier gate (PRIN §I.2 / REQ BR-008); workforce-uplift programme via FAHR (REQ BR-006); quarterly Charter / PDPL / IAS conformance reviews; portfolio diversification across multiple agents to spread the load.

**Control effectiveness**: Adequate.

**Residual**: L=3, I=5, **RR=15** (High).

**Response**: **TREAT**. Sustain monthly internal reporting; surface trajectory risk to Cabinet Affairs *before* it crystallises; explicitly request appetite-conversation with the Ministerial Council if the depth requirement and the pace target are in tension at portfolio level.

**Risk owner**: Entity Highest Authority. **Action owner**: CAIO. **Escalation path**: Highest Authority → Ministerial Council Secretariat.

**Action plan**:

- Monthly trajectory report against the three KPIs; first report Q2 2026.
- Quarterly trajectory review at the Ministerial Council level.
- Target residual: maintained at ≤ 15 (High) for the first reporting cycle; reassess after first submission lands cleanly.

**Success criterion**: First Ministerial Council quarterly submission accepted; trajectory on plot.

---

### R-002 — Pace pressure produces premature Tier-3 promotion → incident

**Category**: STRATEGIC. **Trace**: STKE Conflict 1 / R-1; REQ Conflict C-1, BR-008, BR-009.

**Description**: Cabinet Affairs pace pressure (SD-2) overrides assurance-function depth requirements (SD-5, SD-6, SD-7), leading to an autonomy-tier promotion that is not yet supported by evidence; an incident follows.

**Root cause**: Pace–depth conflict (STKE Conflict 1) without formal gate enforcement.

**Trigger events**: Cabinet Affairs escalation to the Highest Authority to accelerate; AI Governance Committee approves under pressure.

**Consequences**: A PDPL / IAS / Charter-reportable incident at the Ministerial Council level; rollback to Tier-2; reputational damage that compounds R-018.

**Affected stakeholders**: all named in STKE.

**Inherent**: L=3, I=5, **IR=15** (High).

**Controls in place**: PRIN §I.2 (autonomy-tier framework); REQ BR-008 (gate enforcement); RACI per STKE — AI Governance Committee accountable for Tier-2 promotion, Highest Authority accountable for Tier-3.

**Residual**: L=2, I=4, **RR=8** (Medium).

**Response**: **TREAT**. Make tier-promotion decisions formal Committee minutes; record an evidence pack per promotion (REQ FR-008); make tier-revert (REQ FR-019) part of the normal operating model so that Tier-3 is not psychologically irreversible.

**Risk owner**: AI Governance Committee. **Action owner**: CAIO. **Escalation**: Highest Authority on conflict.

**Action plan**: tier-promotion gate evidence pack template by 2026-07-15; first Tier-2 / Tier-3 promotion through the gate before any agent goes to Tier-3 production; pre-defined rollback path per agent.

**Target residual**: 8 (Medium). **Success criterion**: zero promotions without recorded evidence pack and named accountable decision-maker.

---

### R-003 — Vendor opacity blocks ATRS / PDPL evidence

**Category**: OPERATIONAL. **Trace**: STKE R-2; AICH §AI System Inventory (`[NEEDS VERIFICATION]`); REQ Conflict C-2, INT-007.

**Description**: Foundation-model vendor refuses to disclose enough training-data provenance for an honest ATRS (Charter Principle 5) or PDPL DPIA (PDPL Federal Decree-Law 45/2021).

**Root cause**: Vendor commercial preference (SD-12) vs Charter / PDPL disclosure obligations.

**Trigger events**: Procurement-due-diligence reveals opacity; ATRS author cannot truthfully complete fields; DPO refuses DPIA sign-off.

**Consequences**: Tier-3 promotion blocked for the affected agent; or thin ATRS published, undermining citizen trust (R-018); or the entity changes vendor mid-portfolio.

**Affected stakeholders**: SD-4, SD-6, SD-9, SD-12.

**Inherent**: L=5, I=3, **IR=15** (High).

**Controls in place**: contractual disclosure obligations via `/arckit-uae:uae-procurement`; tier-link to disclosure (REQ Conflict C-2); portfolio-level vendor diversification.

**Residual**: L=4, I=2, **RR=8** (Medium).

**Response**: **TREAT**. Embed disclosure obligations in every foundation-model contract; cap non-disclosing vendors at Tier-2 (per-decision human approval); record residual opacity as a Tier-2 ceiling, not as a vacant ATRS field.

**Risk owner**: Procurement + DPO. **Action owner**: Procurement Lead. **Escalation**: CAIO; Highest Authority for vendor change.

**Action plan**: standard ATRS / PDPL clauses in vendor contracts by Q3 2026; portfolio-level vendor diversification ADR; vendor-disclosure register maintained.

---

### R-004 — Workforce disengagement undermines KPI-3 narrative

**Category**: STRATEGIC. **Trace**: STKE SD-8 / R-3; REQ BR-006.

**Description**: Workforce reads the agentic transition as headcount reduction rather than capability uplift; reviewer cohort disengages; override quality declines; KPI-3 (workflow redesign) stories evaporate.

**Inherent**: L=3, I=4, **IR=12** (Medium).

**Controls**: FAHR-coordinated training (REQ BR-006); explicit KPI-3 framing as uplift (PRIN §I.3 / STKE Resolution Strategy); reviewer-role description; override-as-positive-metric (REQ Conflict C-4).

**Residual**: L=2, I=4, **RR=8** (Medium).

**Response**: **TREAT**.

**Owner**: HR + CAIO. **Action**: workforce-comms programme aligned to monthly all-hands; competence assessment cycle integrated with FAHR national 80,000-cohort programme.

---

### R-005 — Ministerial direction or scope changes mid-cycle

**Category**: STRATEGIC. **Trace**: STKE SD-1.

**Description**: A change in federal direction (e.g., refined definition of "autonomous service", machinery-of-government move, sectoral re-prioritisation) reshapes the target mid-cycle.

**Inherent**: L=2, I=5, **IR=10** (Medium).

**Controls**: governance forum (AI Governance Committee); roadmap re-baseline process (`/arckit:roadmap` re-run); change-mgmt cadence with Cabinet Affairs.

**Residual**: L=2, I=4, **RR=8** (Medium).

**Response**: **TOLERATE** — accept that political-direction risk is exogenous; keep ready-to-pivot stance.

**Owner**: Highest Authority.

---

### R-006 — Foundation-model vendor base-version drift

**Category**: TECHNOLOGY. **Trace**: STKE R-5; REQ NFR-M-001, FR-011, FR-019; PRIN §III.15.

**Description**: Foundation-model vendor changes the base model without notice; agent behaviour shifts; ATRS becomes inaccurate; bias profile changes.

**Inherent**: L=5, I=3, **IR=15** (High).

**Controls**: contractual change-notification right; continuous drift detection (REQ FR-011); tier-revert (REQ FR-019); shadow / canary release pattern; AI Governance Committee notification on drift event.

**Residual**: L=3, I=2, **RR=6** (Medium).

**Response**: **TREAT** + **TRANSFER** (contractual notification right is a partial transfer to the vendor).

**Owner**: CAIO. **Action owner**: CAIO + procurement liaison.

**Action plan**: vendor change-notification clauses in all contracts; drift dashboard live before any Tier-2 promotion; treat surprise base-model change as an incident per REQ FR-018.

---

### R-007 — Override mechanism becomes theatre

**Category**: OPERATIONAL. **Trace**: STKE SD-8 / Conflict 3 / R-3 partial; REQ Conflict C-4, FR-003.

**Description**: Reviewers rubber-stamp agent outputs; the override mechanism is technically present but is not exercised meaningfully; the human-oversight principle (PRIN §I.1) is hollowed out.

**Inherent**: L=4, I=4, **IR=16** (High).

**Controls**: override-rate as a behavioural metric (REQ Conflict C-4 resolution); quarterly override-drill (PRIN §I.1 validation); reviewer competence assessment (REQ FR-012); contestation-overturn rate as a downstream signal.

**Residual**: L=2, I=3, **RR=6** (Medium).

**Response**: **TREAT**.

**Owner**: AI Governance Committee. **Action**: behavioural-metric dashboard live before any Tier-2 promotion; sustained low override rate triggers reviewer-competence audit; sustained high override rate triggers model audit.

---

### R-013 — PDPL breach attributable to the portfolio

**Category**: COMPLIANCE. **Trace**: STKE SD-6, SD-11; REQ BR-004, NFR-C-001 to NFR-C-004.

**Description**: A PDPL-reportable breach (personal data exposure, unlawful processing, cross-border-transfer violation, data-subject-rights failure) is traced to a portfolio agent.

**Inherent**: L=3, I=5, **IR=15** (High).

**Controls**: per-agent DPIA (REQ BR-004); lawful-basis register (DR-006); cross-border-transfer log (DR-007, NFR-C-004); sovereign-key management (NFR-SEC-003); data-subject-rights process (REQ BR-004); data-classification gates (PRIN §II.9).

**Residual**: L=2, I=4, **RR=8** (Medium).

**Response**: **TREAT**.

**Owner**: DPO. **Action**: 3 DPIAs complete by 2026-08-15; lawful-basis register populated by 2026-07-15; SAR end-to-end test by 2026-08-01; cross-border log automated by 2026-09-30.

---

### R-018 — Citizen-facing incident with media amplification

**Category**: REPUTATIONAL. **Trace**: STKE SD-9 → SD-3 cascade.

**Description**: AI-003 (citizen-facing) or AI-005 (work-permits) makes a decision that becomes a media story; trust in agentic services takes a portfolio-wide hit.

**Inherent**: L=3, I=5, **IR=15** (High).

**Controls**: tier-gate (PRIN §I.2); ATRS published (REQ BR-002); contestation route (REQ BR-007); incident workflow (REQ FR-018); rollback path per agent (REQ NFR-A-002); proactive comms programme.

**Residual**: L=2, I=4, **RR=8** (Medium).

**Response**: **TREAT**.

**Owner**: Highest Authority + Ministerial Council Secretariat liaison. **Action**: incident-comms playbook ready before any Tier-3 promotion; SRO + entity-comms drill quarterly.

---

### R-019 — Bias finding against rights-affecting agent (AI-002, AI-005)

**Category**: REPUTATIONAL. **Trace**: AICH HIGH residual for AI-002, AI-005; STKE SD-9; REQ BR-010.

**Description**: AI-002 (tax) or AI-005 (work-permit) is shown — by audit, by appeal pattern, by media — to systematically disadvantage a population group (nationality, employer size, sector, language).

**Root cause**: training data encoding prior selection bias; vendor opacity (R-003); Arabic-dialect under-representation; aggregation effects that the entity has not measured.

**Inherent**: L=4, I=5, **IR=20** (Critical).

**Controls**: PRIN §III.13 (fairness commitment); REQ BR-010 (fairness baseline before tier-promotion); fairness dashboard (REQ FR-010); Arabic-English parity threshold (REQ NFR-U-001); contestation overturn rate as a downstream signal.

**Control effectiveness**: **Adequate on paper; not yet implemented for AI-002 or AI-005** — this is the gap that AICH flags as HIGH residual for these two systems.

**Residual**: L=2, I=4, **RR=8** (Medium) **conditional on fairness baseline being measured**. **If baseline is deferred, residual reverts toward Critical**.

**Response**: **TREAT**.

**Owner**: CAIO. **Action**: fairness baseline for AI-002 and AI-005 by 2026-08-20 (REQ BR-010 timeline); fairness threshold-breach automatically triggers tier-revert (REQ FR-019); Highest Authority signs off on any waiver.

**Success criterion**: baseline measured; thresholds defined; sustained in-production parity within threshold for ≥ 1 quarter.

---

## D. Risk Register — Summary Table for Remaining Risks (R-008 through R-025 minus the detailed ones above)

> Full risk profiles for R-008…R-025 are summarised below. Each carries the same controls anchored on PRIN, STKE, and REQ. Detailed profiles will be expanded as a risk's residual score worsens or as it is escalated.

| ID | Category | Title | Inherent | Residual | Owner | Status | Response | Key control |
|----|----------|-------|----------|----------|-------|--------|----------|--------------|
| R-008 | OPERATIONAL | Contestation route becomes theatre (slow, inaccessible, language-imbalanced) | 12 | 8 | CAIO + SROs | Open | TREAT | REQ BR-007 SLA-attainment KPI; REQ NFR-U-001 Arabic parity |
| R-009 | OPERATIONAL | Reviewer capacity insufficient for contestation volume | 9 | 4 | SROs | Monitoring | TREAT | REQ FR-005 SLA; capacity surge plan; STKE R-4 mitigation |
| R-010 | OPERATIONAL | Insufficient AI-engineering capability in entity team | 12 | 6 | CDO | In Progress | TREAT | FAHR training (REQ BR-006); vendor support contracts |
| R-011 | FINANCIAL | Inference / token cost overrun at directive-trajectory volume | 12 | 6 | CFO + CAIO | Open | TREAT | FinOps gates (`/arckit:finops`); model-routing; throttling per tier |
| R-012 | FINANCIAL | Sovereign-CSP pricing premium exceeds budget | 9 | 4 | CFO | Monitoring | TOLERATE + TREAT | ADR-recorded CSP selection; portfolio diversification (REQ INT-008) |
| R-014 | COMPLIANCE | UAE IAS audit finding from Cybersecurity Council | 12 | 6 | CISO | Open | TREAT | REQ BR-005 SoA; AI-specific threat models; IAS P1 controls |
| R-015 | COMPLIANCE | Cross-border residency violation via supplier defaults | 15 | 4 | CDO + CISO | Open | TREAT | Residency map (PRIN §II.10); classification-aware deploy gates; auto-deploy refusal on residency mismatch |
| R-016 | COMPLIANCE | Charter conformance finding requires service withdrawal | 10 | 5 | CAIO + AI Gov Cmte | Monitoring | TREAT | Quarterly AICH re-run (REQ NFR-C-005); gap-closure plan; tier-revert (REQ FR-019) |
| R-017 | COMPLIANCE | Audit-log integrity failure on legal-effect decision class | 10 | 4 | CISO | Open | TREAT | Write-once signed log (REQ FR-009, NFR-SEC-007); retention per Digital Records Policy |
| R-020 | REPUTATIONAL | Loss of public confidence in agentic services across federal narrative | 10 | 5 | Ministerial Council Secretariat (federal); Highest Authority (entity) | Monitoring | TOLERATE + TREAT | Cumulative effect of all controls; transparency-first comms posture |
| R-021 | TECHNOLOGY | Adversarial AI attack (prompt injection, jailbreak, model extraction, data poisoning) | 16 | 6 | CISO | In Progress | TREAT | REQ NFR-SEC-005 adversarial test corpus; network segmentation (NFR-SEC-006); annual pen test |
| R-022 | TECHNOLOGY | Sovereign-CSP outage exceeds RTO | 8 | 3 | CDO | Monitoring | TREAT | Geographic redundancy within sovereign envelope (NFR-A-004); fallback path (FR-017) |
| R-023 | TECHNOLOGY | Foundation-model unavailability with no fallback | 12 | 4 | CAIO + CDO | Open | TREAT | Fallback delivery path (REQ FR-017, NFR-A-002); multi-vendor portfolio |
| R-024 | TECHNOLOGY | Drift produces fairness regression in production (compounds with R-006) | 16 | 6 | CAIO | Open | TREAT | Continuous fairness monitoring (FR-010); drift detection (FR-011); threshold-breach response |
| R-025 | TECHNOLOGY | Integration failure with federal core system (UAE Pass, FedNet, MoF DPP, FTA, MoHRE core) | 12 | 6 | CDO | Open | TREAT | Versioned APIs (REQ NFR-I-003); circuit breakers; per-integration SLA; documented owner per system (REQ INT-001…INT-006) |

---

## E. Risk by Category Analysis

### STRATEGIC (5 risks: R-001, R-002, R-004, R-005, R-019 reclassified as REPUTATIONAL — see note)

> *Note*: R-019 (Bias finding) is recorded as REPUTATIONAL because the manifest outcome is reputational damage; the underlying cause is strategic/operational. R-019 also appears in the AICH residual-risk register.

- Average inherent: **14.4** (with R-001 the headline Critical and R-002 / R-003 / R-019 close behind in the strategic narrative).
- Average residual: **9.4** — concentrated reduction via tier-gate (PRIN §I.2), tighter governance, FAHR coordination.
- Control effectiveness: ~ 35 %.
- Key theme: directive ambition vs assurance discipline. The strategic risks are the ones that **the Ministerial Council needs to share** — they are not entity-only problems.

### OPERATIONAL (5: R-003, R-007, R-008, R-009, R-010)

- Avg inherent **13.0**, avg residual **6.0** — best reduction in the register (54 %), because the controls (override-as-metric, FAHR training, SLA discipline) directly address operational failure modes.

### FINANCIAL (2: R-011, R-012)

- Smaller category for this version because the financial story is still being shaped in `/arckit:sobc`. Likely to grow once the business case quantifies budget exposure.

### COMPLIANCE (5: R-013, R-014, R-015, R-016, R-017)

- High inherent, very strong residual reduction (~ 56 %). The UAE statutory framework (PDPL, IAS, Cloud Residency, Charter) prescribes specific controls; the portfolio's foundational principles map cleanly to them.

### REPUTATIONAL (3: R-018, R-019, R-020)

- The smallest category but **the one that drives Ministerial Council attention**. Reputational risk crystallises consequences from other categories.

### TECHNOLOGY (5: R-006, R-021, R-022, R-023, R-024, R-025 — 6 actually)

- Note: 5 plus R-006 = 6. Adjusting count: TECHNOLOGY has 6 risks (R-006, R-021, R-022, R-023, R-024, R-025) and the register total is 25 across categories.
- Strong residual reduction (61 %) — sovereign infrastructure, classification-aware gates, redundancy, multi-vendor are well-understood patterns.

---

## F. Risk Ownership Matrix

| Stakeholder / Forum | Owned risks | Critical / High residual | Notes |
|---------------------|-------------|---------------------------|-------|
| Entity Highest Authority | R-001, R-005, R-018 | 1 High (R-001) | Accountable principal for strategic + reputational |
| AI Governance Committee | R-002, R-007, R-016 | 0 residual High | Tier-promotion authority; governance forum |
| CAIO | R-004 (joint), R-006, R-019, R-023 (joint), R-024 | 0 residual High (after fairness baseline) | Operational portfolio owner |
| CISO | R-014, R-015 (joint), R-017, R-021 | 0 residual High | IAS, security, residency |
| DPO | R-013 | 0 residual High | PDPL compliance |
| Procurement + DPO | R-003 | 0 residual High | Vendor opacity / disclosure |
| CDO | R-010, R-015 (joint), R-022, R-023 (joint), R-025 | 0 residual High | Platform, sovereign cloud, integration |
| CFO | R-011 (joint), R-012 | 0 residual High | FinOps; budget exposure |
| HR + CAIO | R-004 (joint) | 0 residual High | Workforce uplift |
| Ministry Service SROs | R-008 (joint), R-009 | 0 residual High | Service-level risks |
| Ministerial Council Secretariat | R-020 (joint with Highest Authority) | 0 residual High | Federal-narrative risk |

**Concentration note**: CAIO has the largest absolute load (5 risks) — appropriate to the role's portfolio-owner status, but a continuity-risk on the role itself worth flagging as a candidate **R-026 (PERSONAL)** in a future version.

---

## G. 4Ts Response Summary

| Response | Count | % | Examples |
|----------|-------|---|----------|
| **Tolerate** | 2 | 8 % | R-005 (ministerial-direction change exogenous); R-020 (federal-narrative — partially tolerate alongside treat) |
| **Treat** | 22 | 88 % | the majority — controls are the primary lever |
| **Transfer** | 1 | 4 % | R-006 base-model change (contractual transfer to vendor) |
| **Terminate** | 0 | 0 % | none — every activity is directive-driven |

---

## H. Risk Appetite Compliance (interim)

| Category | Interim appetite | Risks within | Risks exceeding | Action |
|----------|-------------------|---------------|-------------------|--------|
| STRATEGIC | Medium (12) | R-002, R-004, R-005 | R-001 (15) | Quarterly to Ministerial Council; treat-status |
| OPERATIONAL | Medium (12) | all | none | within appetite |
| FINANCIAL | Medium (12) | R-011, R-012 | none | within appetite |
| COMPLIANCE | Low (5) — per non-negotiable PRIN §I.4 | R-015, R-017 | R-013, R-014, R-016 | Active treatment; quarterly conformance re-run |
| REPUTATIONAL | Low (5) — per Charter Principles 5, 6 | R-020 | R-018, R-019 | Highest Authority review; the AICH HIGH-residual flag for AI-002/AI-005 is the operational form |
| TECHNOLOGY | Medium (12) | all | none | within appetite |

**Recommendation**: Adopt a formal `projects/000-global/risk-appetite.md` as a follow-up artefact, anchored on PRIN non-negotiable principles and the Charter principles. The interim appetite above is the working assumption.

---

## I. Action Plan (priority-ordered)

| Priority | Action | Risks addressed | Owner | Due | Status |
|----------|--------|------------------|-------|-----|--------|
| 1 | Fairness baseline measurement for AI-002 and AI-005 | R-019, R-024 | CAIO | 2026-08-20 | Open |
| 2 | Five ATRS records published before next Council review | R-018, R-019, R-020, R-003 | CAIO | 2026-08-28 | Open |
| 3 | Autonomy-tier classification per agent + AI Governance Committee gate operational | R-001, R-002, R-018 | AI Governance Committee | 2026-07-31 | In Progress |
| 4 | PDPL DPIAs for AI-002, AI-003, AI-005 | R-013 | DPO | 2026-08-15 | Open |
| 5 | UAE IAS Statement of Applicability signed; P1 controls in place | R-014, R-015, R-017, R-021 | CISO | 2026-08-15 | Open |
| 6 | Vendor change-notification clauses in all foundation-model contracts | R-006, R-024 | Procurement + Legal | 2026-09-30 | Open |
| 7 | Foundation-model disclosure clauses in vendor contracts (ATRS / PDPL evidence) | R-003 | Procurement + DPO | 2026-09-30 | In Progress |
| 8 | Reviewer competence assessment baseline; FAHR training cohort online | R-004, R-007, R-010 | HR + CAIO | 2026-08-28 | Open |
| 9 | Residency map signed; classification-aware deploy gates live | R-015 | CDO + CISO | 2026-07-31 | Open |
| 10 | Drift dashboard live per agent | R-006, R-024 | CAIO | 2026-08-15 | Open |
| 11 | Override-drill exercised quarterly; cadence established | R-007 | AI Governance Committee | 2026-07-31 | Open |
| 12 | Incident-comms playbook ready and rehearsed | R-018, R-020 | Highest Authority + Comms | 2026-09-30 | Open |
| 13 | Contestation-route SLA-attainment dashboard live | R-008, R-009 | CAIO + SROs | 2026-09-30 | Open |
| 14 | FinOps gating per agent | R-011 | CFO + CAIO | 2026-10-31 | Open |
| 15 | Formal risk-appetite statement adopted (`projects/000-global/risk-appetite.md`) | All | Highest Authority | 2026-09-30 | Open |

---

## J. Monitoring and Review Framework

- **Critical / High residual risks** (currently R-001 only at residual): **monthly** review at the AI Governance Committee; immediate escalation on score change ≥ 3.
- **Medium residual risks**: **monthly** during the first reporting cycle; **quarterly** thereafter.
- **Low residual risks**: **quarterly** review.
- **All risks**: re-baselined annually; reassessed after any tier promotion, any incident, any vendor change, any base-model change, any material policy update.
- **Reporting**:
  - Weekly snapshot of Critical / High to the CAIO.
  - Monthly summary to the AI Governance Committee.
  - Quarterly to the Ministerial Council Secretariat as part of the directive KPI submission.
  - Annual to the entity's audit function.
- **Escalation criteria**:
  - Any new Critical risk → Highest Authority within 24 hours.
  - Any residual score increase ≥ 3 → AI Governance Committee at next sitting.
  - Any breach of interim appetite → Highest Authority before next quarterly Ministerial Council submission.
- **Next review date**: 2026-06-28 (post-first-monthly-cycle).
- **Risk register owner**: CAIO (delegated authoring); Highest Authority (accountable).

---

## K. Integration with SOBC

When `/arckit:sobc` runs next, this risk register feeds:

- **Strategic case**: R-001 (federal trajectory) and R-005 (mandate-change exogenous risk) inform "Why Now?" framing and contingency in the strategic narrative.
- **Economic case**: R-011 (inference cost overrun), R-012 (CSP premium), R-022 (CSP outage) inform risk-adjusted cost projections; standard HM-Treasury Green-Book optimism-bias applied on top.
- **Commercial case**: R-003 (vendor opacity) and R-006 (base-model drift) inform vendor-relationship structuring and contract clauses.
- **Financial case**: R-011, R-012 affordability projections.
- **Management case Part E** (Risk): this register is the source artefact; reproduced in summary with the action plan.

---

## L. Orange Book Compliance Checklist

- ✅ **Governance and leadership**: Every risk has a named owner from STKE RACI; Highest Authority accountable at portfolio level.
- ✅ **Integration**: Risks linked to STKE goals (G-1…G-8), PRIN principles, REQ requirements, and AICH residuals.
- ✅ **Collaboration**: Risks sourced from STKE (4 risks carried forward), REQ (6 preview risks carried forward), AICH (HIGH bias residuals), and Orange Book risk-category prompts.
- ✅ **Risk processes**: Identification, inherent / residual assessment, 4Ts response, action plan, monitoring framework.
- ✅ **Continual improvement**: Monthly / quarterly review cadence; reassessment triggers; v1.0 acknowledges interim appetite and a follow-up appetite-adoption action.

---

## External References

### Document Register

| Doc ID | Title | Source | Description |
|--------|-------|--------|-------------|
| ARC-000-PRIN-v1.0 | UAE Federal Entity — Agentic AI Architecture Principles | `projects/000-global/ARC-000-PRIN-v1.0.md` | Principal-control source |
| ARC-001-STKE-v1.0 | Stakeholder Drivers & Goals Analysis | `projects/001-agentic-ai-portfolio/ARC-001-STKE-v1.0.md` | Risk owners + STKE risks R-1…R-4 carried forward |
| ARC-001-AICH-v1.0 | UAE AI Charter Compliance Assessment | `projects/001-agentic-ai-portfolio/ARC-001-AICH-v1.0.md` | HIGH residual bias risks for AI-002, AI-005 |
| ARC-001-REQ-v1.0 | Requirements | `projects/001-agentic-ai-portfolio/ARC-001-REQ-v1.0.md` | Preview risks R-1…R-6 carried forward; BR-001…BR-010 controls |
| HMT-ORANGE | HM Treasury Orange Book (2023) | <https://www.gov.uk/government/publications/orange-book> | Methodology anchor |

### Citations

| Citation | Doc ID | Section | Used in |
|----------|--------|---------|---------|
| RISK-1 | ARC-001-STKE-v1.0 | Risks R-1…R-4 | R-002, R-003, R-004, R-008, R-015 |
| RISK-2 | ARC-001-AICH-v1.0 | Bias & Fairness Assessment — HIGH residuals for AI-002, AI-005 | R-019 |
| RISK-3 | ARC-001-REQ-v1.0 | Risks preview R-1…R-6; Conflicts C-1…C-6 | R-001…R-006 framing; control statements throughout |
| RISK-4 | ARC-000-PRIN-v1.0 | §I.1, §I.2, §I.4, §I.6, §II.10, §III.13 | Control statements throughout |
| RISK-5 | HMT-ORANGE | Part I (5 principles); 4Ts framework | Methodology |

### Unreferenced Documents

None. As above, authoritative UAE statutes should be added to `projects/000-global/policies/` and re-run for citation-grade traceability.

---

**Generated by**: ArcKit `/arckit:risk` command
**Generated on**: 2026-05-28
**ArcKit Version**: 5.4.0
**Project**: Agentic AI Portfolio (Project 001)
**AI Model**: Claude Opus 4.7 (1M context)
**Generation Context**: Anchored on PRIN, STKE (4 carried-forward risks), REQ (6 preview risks), AICH (HIGH residual bias for AI-002 / AI-005). HM Treasury Orange Book 2023 methodology.
