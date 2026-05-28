# UAE AI Charter Compliance Assessment

> **Template Origin**: Community | **ArcKit Version**: 5.4.0 | **Command**: `/arckit-uae:uae-ai-charter`

## Document Control

| Field | Value |
|-------|-------|
| Document ID | ARC-001-AICH-v1.0 |
| Document Type | UAE AI Charter Compliance Assessment (AICH) |
| Project | Agentic AI Portfolio (Project 001) |
| Classification | OFFICIAL |
| Status | DRAFT |
| Version | 1.0 |
| Created Date | 2026-05-28 |
| Last Modified | 2026-05-28 |
| Review Cycle | Quarterly (per Ministerial Council reporting cadence) |
| Next Review Date | 2026-08-28 |
| Owner | Chief AI Officer (CAIO), entity to assign |
| Reviewed By | Pending — Entity AI Governance Committee, DPO, CISO |
| Approved By | Pending — Highest Authority of the entity |
| Distribution | CAIO, AI Governance Committee, Ministerial Council Secretariat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-05-28 | ArcKit AI | Initial creation from `/arckit-uae:uae-ai-charter` — baseline assessment for the five directive-named federal pilots | PENDING | PENDING |

---

## Executive Summary

This assessment evaluates the entity's portfolio of agentic AI systems against the **UAE Charter for the Development and Use of Artificial Intelligence** (the "Charter"), per the 23 April 2026 directive of HH Sheikh Mohammed bin Rashid Al Maktoum and the federal framework approved by UAE Cabinet on 18 May 2026 under HH Sheikh Mansour bin Zayed's Ministerial Council for AI and Development.

The portfolio in scope comprises the **four already-live federal pilots** named in the directive narrative — Procurement, Tax Auditing, Customer Happiness, Technical Support — plus the **MoHRE autonomous work-permit decisioning service** operating since 1 May 2026. Together these constitute the entity's Charter-relevant footprint as of the assessment date.

The headline finding is that all twelve Charter principles are **applicable** to every system in scope, that the foundational principles posture is anchored in `ARC-000-PRIN-v1.0` [[ARC-000-PRIN-v1.0]], and that **none** of the twelve principles can yet be marked **fully compliant** because the evidence artefacts that the Charter requires — per-agent Algorithmic Transparency records (ATRS), per-agent PDPL DPIAs, the UAE IAS Statement of Applicability, fairness-measurement reports, dataset-provenance trails, and autonomy-tier classifications — have not yet been produced for the five systems in scope. Twelve principles are therefore assessed as **partially compliant** (foundation present, evidence pending). No principles are assessed as **non-compliant**, conditional on the gap-closure plan in §[12-Principle Assessment] being executed before the next quarterly Ministerial Council reporting cycle.

The **AI System Inventory** below carries explicit `[NEEDS VERIFICATION]` markers where model-family, vendor, and deployment-mode values are placeholder. A federal entity adopting this playbook MUST replace these with verified values from the actual deployments before relying on the assessment.

---

## AI System Inventory

| AI system ID | Use case | Model family | Vendor / source | Deployment mode | User population |
|--------------|----------|--------------|------------------|------------------|-----------------|
| AI-001 | Federal Procurement Agent — autonomous tender drafting, supplier shortlisting, evaluation support per Federal Decree-Law 11/2023 and the MoF Digital Procurement Platform | [NEEDS VERIFICATION] — likely large language model + retrieval over procurement corpus | [NEEDS VERIFICATION] | [NEEDS VERIFICATION] — sovereign-cloud expected (Confidential procurement data) | Federal procurement officers; supplier ICV evidence touched |
| AI-002 | Federal Tax Auditing Agent — autonomous risk-scoring, anomaly detection, draft assessment generation for the Federal Tax Authority workflow | [NEEDS VERIFICATION] — likely ensemble of statistical + LLM models over tax filings | [NEEDS VERIFICATION] | [NEEDS VERIFICATION] — sovereign-cloud expected (Confidential personal/business financial data) | Tax auditors; affected taxpayers (citizens and businesses) |
| AI-003 | Customer Happiness Agent — citizen-facing conversational agent for federal-service queries, intent triage, and routing | [NEEDS VERIFICATION] — conversational LLM | [NEEDS VERIFICATION] | [NEEDS VERIFICATION] — sovereign-cloud expected; Arabic + English minimum | UAE citizens, residents, visitors interacting with federal services |
| AI-004 | Technical Support Agent — internal-staff IT and service-desk agent across federal workforce | [NEEDS VERIFICATION] — conversational LLM + knowledge-base RAG | [NEEDS VERIFICATION] | [NEEDS VERIFICATION] — sovereign-cloud expected | Federal employees (~80,000 in agentic AI training per the directive) |
| AI-005 | MoHRE Autonomous Work-Permit Decisioning — autonomous grant/refusal of work-permit decisions (live since 1 May 2026) | [NEEDS VERIFICATION] — likely rules-based + ML risk-scoring composite | [NEEDS VERIFICATION] | [NEEDS VERIFICATION] — sovereign-cloud, integrated with MoHRE core systems | Work-permit applicants, employers, MoHRE officers |

**Scope notes**: This inventory captures the directive-named federal pilots only. The entity MUST extend the inventory to cover any additional agents — internal productivity, departmental pilots, embedded vendor capabilities — before the next quarterly review. Each new system requires its own row, its own tier classification per `/arckit-uae:uae-ai-autonomy-tier`, and its own per-system ATRS record.

---

## 12-Principle Assessment

Each row assesses one Charter principle against the five systems in the inventory. **Applies?** is Y where the principle is in scope; **Evidence of compliance** references existing artefacts where present; **Gap** describes what is missing; **Mitigation** names the planned action (with the relevant slash-command where applicable).

| # | Principle | Applies? | Evidence of compliance | Gap | Mitigation |
|---|-----------|----------|------------------------|-----|------------|
| 1 | **Human-Machine Ties** — AI augments, does not displace, the accountable human in matters of public consequence [AICH-3] | Y (all 5) | PRIN §I.1 Human Oversight and Meaningful Control; PRIN §III.14 Explainability. Foundation present in `ARC-000-PRIN-v1.0`. | Per-agent human-machine interaction design not yet documented; reviewer-role training and competence baseline not yet defined for AI-001…AI-005. | Produce per-agent Human-in-the-Loop design (see §[Human-in-the-Loop Design]); train and certify reviewers; record in ATRS per agent. |
| 2 | **Safety** — AI must not endanger users, operators, or third parties, physically or otherwise [AICH-3] | Y (all 5) | PRIN §I.4 Security by Design (IAS-aligned); PRIN §I.5 Resilience and Graceful Degradation. Foundation present. | UAE IAS Statement of Applicability not yet completed; AI-specific threat models (prompt injection, model extraction, data poisoning) not yet produced; safety-incident runbook not yet specific to agentic incidents. | Run `/arckit-uae:uae-ias` for the SoA; add AI-specific threat-model section to `/arckit:risk`; produce agent-incident runbook in `/arckit:operationalize`. |
| 3 | **Bias Mitigation** — AI must be evaluated for and remediated against unjustified disparate impact [AICH-1] | Y (all 5) | PRIN §III.13 Bias, Fairness and Inclusion; Arabic/English parity requirement. Foundation present. | No fairness metrics measured for AI-001…AI-005; demographic representativeness of training/evaluation data not verified for vendor foundation models; continuing-bias monitoring not yet instrumented. | Define fairness metric per use case in `/arckit:requirements`; baseline-measure before next quarterly review; instrument continuing monitoring per PRIN §III.13 validation gates. **Vendor opacity is a known risk for foundation-model-backed agents** — see §[Bias & Fairness Assessment]. |
| 4 | **Data Privacy** — AI must comply with the UAE PDPL and the entity's data-protection obligations [AICH-3] | Y (all 5) | PRIN §II.8 Lawful Basis First (PDPL); PRIN §II.10 Sovereign Data Residency. Foundation present. | Per-agent PDPL DPIA not yet performed; lawful-basis register not yet populated for AI-001…AI-005; cross-border-transfer log not yet maintained; residency map not yet validated against actual deployments. | Run `/arckit-uae:uae-pdpl` per agent for the DPIA and lawful-basis register; run `/arckit-uae:uae-cloud-residency` for the residency map. |
| 5 | **Transparency** — AI processes and decisions must be explainable to those they affect [AICH-3] | Y (all 5) | PRIN §III.14 Explainability and Algorithmic Transparency. Foundation present. | No published ATRS-equivalent record exists for AI-001…AI-005; per-decision rationale generation not yet validated; plain-language citizen-facing version (Arabic and English) not yet produced. | Run `/arckit:atrs` per agent — five ATRS records minimum required before next quarterly review. Validate plain-language readability with a non-engineering reviewer. |
| 6 | **Human Oversight** — meaningful human authority to intervene, override, or halt the agent [AICH-2] | Y (all 5) | PRIN §I.1 Human Oversight (NON-NEGOTIABLE); PRIN §I.2 Autonomy Tiering. Foundation present. | Autonomy tier not yet classified for AI-001…AI-005; oversight-latency SLA not yet defined; override mechanism not yet exercised end-to-end for any of the five. | Run `/arckit-uae:uae-ai-autonomy-tier` per agent — five tier classifications required. Define oversight-latency SLA per tier. Exercise override-and-revoke quarterly. *(Direct follow-up recommended per command guidance.)* |
| 7 | **Governance and Accountability** — clear accountable owner, clear governance forum, clear escalation path [AICH-3] | Y (all 5) | PRIN §I.1, §I.2, §I.6 and Section VI (Exception Process); CAIO role identified. Foundation present. | Named accountable officer per agent not yet recorded; AI Governance Committee terms-of-reference not yet adopted; quarterly reporting line to the Ministerial Council not yet operational. | Record accountable officer per agent in ATRS; adopt AI Governance Committee ToR; establish reporting cadence per `/arckit:stakeholders`. |
| 8 | **Technological Excellence** — AI systems must meet contemporary engineering standards [AICH-3] | Y (all 5) | PRIN §I.4, §I.5, §V.19 (IaC), §V.20 (Automated Testing including AI test pyramid), §V.21 (CI/CD with safety and compliance gates). Foundation present. | AI-specific test corpora (adversarial, fairness, safety) not yet produced for AI-001…AI-005; CI/CD compliance gates not yet automated for classification/residency invariants. | Produce per-agent test corpora; codify compliance gates in `/arckit:devops` and `/arckit:mlops`. |
| 9 | **Human Commitment** — AI must serve genuine human and societal benefit, not be deployed for its own sake [AICH-3] | Y (all 5) | PRIN §I.3 Mission Alignment to National Priorities. Foundation present. | Specific national-priority outcomes (We the UAE 2031 / NIS 2031 / AI 2031 / Digital Economy Strategy) not yet traced to AI-001…AI-005; the directive's three KPIs (adoption speed, implementation quality, workflow redesign) not yet quantified per agent. | Run `/arckit-uae:uae-priorities-alignment` to produce the National Priorities Alignment Statement; quantify the three directive KPIs in `/arckit:roadmap` and `/arckit:sobc`. |
| 10 | **Peaceful Coexistence** — AI must not be used in ways that undermine social harmony or international peaceful relations [AICH-3] | Y (all 5) | PRIN §I.3 Mission Alignment. Foundation present. | No documented assessment that the five systems' use-cases (procurement decisions, tax decisions, citizen-service triage, IT support, work-permit decisions) cannot be repurposed against this principle. | Produce a use-case-impact assessment per agent as part of `/arckit:risk`; record dual-use risk; reflect in autonomy-tier promotion criteria. |
| 11 | **Inclusive Access** — AI must serve all who need the service, including across language, accessibility, and digital-literacy lines [AICH-3] | Y (all 5; most acute for AI-003, AI-005) | PRIN §III.13 (Arabic/English parity); PRIN §IV.18 (UAE Pass for citizen identity). Foundation present. | Arabic-language performance not measured for AI-001…AI-005; accessibility (screen reader, low-bandwidth, low-literacy paths) not assessed for citizen-facing AI-003 and AI-005; secondary languages (Urdu, Hindi, Tagalog given UAE demographics) not considered. | Measure Arabic-language fairness in §[Bias & Fairness Assessment]; perform accessibility audit per `/arckit:requirements` (NFR-A category); plan secondary-language coverage as a roadmap item. |
| 12 | **Lawful Compliance** — AI must operate within UAE federal law and the entity's regulatory perimeter [AICH-3] | Y (all 5) | PRIN §II.8 Lawful Basis First; PRIN §I.4 IAS-aligned Security; PRIN §II.10 Sovereign Residency. Foundation present. | PDPL DPIAs, IAS SoA, Cloud Residency Assessment, Smart Data Classification Register, and (where applicable) UAEPass integration design have not yet been produced for AI-001…AI-005. | Execute the UAE compliance overlay stack per the README plan: `/arckit-uae:uae-pdpl`, `/arckit-uae:uae-ias`, `/arckit-uae:uae-cloud-residency`, `/arckit-uae:uae-classification`, `/arckit-uae:uae-uaepass` (for citizen-facing systems). |

**Compliance posture summary**:

| Compliance level | Count |
|------------------|-------|
| Fully compliant | 0 |
| Partially compliant | 12 |
| Non-compliant | 0 |

All twelve principles have a documented foundational position in `ARC-000-PRIN-v1.0` and a defined mitigation route. None can be marked fully compliant until the named downstream artefacts have been produced and reviewed.

---

## Bias & Fairness Assessment

| AI system ID | Protected attributes considered | Fairness metric(s) measured | Dataset provenance | Mitigation taken | Residual risk |
|--------------|----------------------------------|------------------------------|---------------------|-------------------|----------------|
| AI-001 (Procurement) | Supplier nationality, supplier-size category (ICV-related), language of submission | [NONE MEASURED YET] | [NEEDS VERIFICATION] — vendor foundation model corpus is opaque; retrieval corpus is internal procurement records | None yet beyond foundational PRIN §III.13 commitment | **MEDIUM** — risk of bias against smaller / non-Arabic-primary suppliers in tender-drafting and evaluation support |
| AI-002 (Tax Auditing) | Taxpayer nationality, business size, sector, residency status | [NONE MEASURED YET] | [NEEDS VERIFICATION] — risk models may be trained on historical audit outcomes which themselves can encode prior selection bias | None yet | **HIGH** — risk-scoring of taxpayers is a high-stakes context where bias can drive disparate audit burden; explicit fairness measurement is essential before any expansion of scope |
| AI-003 (Customer Happiness) | Language (Arabic, English, plus UAE-resident communities: Urdu, Hindi, Tagalog), age, accessibility status, digital-literacy proxy | [NONE MEASURED YET] | [NEEDS VERIFICATION] — vendor foundation model; Arabic-language coverage and dialect performance is a known issue for many foundation models | None yet | **HIGH** — citizen-facing inclusion is a direct Charter Principle 11 requirement; opaque foundation-model corpus is a structural risk |
| AI-004 (Technical Support) | Workforce demographics (nationality, role, seniority, language) | [NONE MEASURED YET] | [NEEDS VERIFICATION] | None yet | **LOW–MEDIUM** — internal-facing reduces citizen-rights stakes, but workforce-fairness is still in scope |
| AI-005 (MoHRE Work-Permit) | Applicant nationality, employer size, sector, occupation category | [NONE MEASURED YET] | [NEEDS VERIFICATION] — autonomous decisioning over work-permit grants is a rights-affecting decision class; training data is likely historical decisions which can encode prior selection effects | None yet | **HIGH** — autonomous decisioning over work-permit decisions is the most rights-consequential system in the inventory; fairness measurement and explicit Charter Principle 3 evidence is a precondition for continued operation per this assessment |

**Cross-cutting mitigation plan**:

1. Define the fairness metric per system before next quarterly review — typically **demographic parity** plus **equal opportunity** for selection / scoring systems; **error-rate parity by language** for citizen-facing systems.
2. Baseline-measure each system against its chosen metric using a demographically representative evaluation set (within lawful constraints).
3. For each foundation-model-backed system, **record the vendor's disclosed (or undisclosed) training-data provenance** and flag opacity as a residual risk in the entity's risk register per PRIN §III.16.
4. Establish continuing in-production monitoring with named thresholds and named owners; material disparity triggers a remediation plan per PRIN §III.13.

---

## Human-in-the-Loop Design

| AI system ID | Decision class | Reviewer role | Trigger for human review | Override mechanism | Audit trail of human decisions |
|--------------|----------------|---------------|---------------------------|---------------------|---------------------------------|
| AI-001 (Procurement) | Tender drafting, supplier shortlist, evaluation support | Federal procurement officer | All Confidential-or-above outputs reviewed before issue; ICV-related shortlisting always reviewed | Officer edits or rejects draft; rejection reason captured | Per-document audit log: officer ID, time, action (accept/edit/reject), reason where rejected; retention per UAE Digital Records Policy |
| AI-002 (Tax Auditing) | Risk score, anomaly flag, draft assessment | Tax auditor (case-team lead for material assessments) | All material assessments reviewed; risk scores above tier-threshold trigger case-team review; randomly sampled below-threshold cases reviewed for quality | Auditor can downgrade risk-score, dismiss anomaly, edit or reject draft assessment; reason recorded | Per-case audit log with full decision chain; affected taxpayer entitled to summary on request per PDPL data-subject-rights; retention per records schedule |
| AI-003 (Customer Happiness) | Conversational response, intent routing, escalation to human officer | Service-desk officer (for escalated cases) | Confidence below threshold; sensitive context (complaint, vulnerable user signal, security event); explicit user request for human | User pressed escalation; officer takes over conversation; agent state handed off with full conversation context | Conversation log retained per PDPL; officer actions logged with reason for intervention; user-visible "you are now talking to a human" signal must be unmistakable |
| AI-004 (Technical Support) | Diagnostic response, change recommendation, ticket auto-resolution | Service-desk engineer (for ticket auto-close and any change-recommendation) | Auto-close gated by confidence + ticket-class allowlist; change recommendations always reviewed before action | Engineer reopens or escalates; auto-close decisions reviewable by user via standard support escalation | Per-ticket audit log; auto-close-reversal rate tracked as a behavioural metric |
| AI-005 (MoHRE Work-Permit) | Grant / refuse / refer-for-review of work-permit applications | MoHRE officer (case-review and appeals); designated officer for autonomous-decision oversight | All refusals subject to officer signature OR autonomous-tier escalation rule; randomly sampled grants reviewed for quality; any contestation triggers full human review | Applicant has contestation right per Charter Principle 6 and PDPL; officer can overturn the agent's decision; reason recorded; agent retrained where the override volume passes threshold | Per-decision audit log with full input/output/rationale/officer-action chain; **write-once, signed** per PRIN §I.6 because the decision has legal effect; retention per UAE Digital Records Policy and MoHRE retention schedule |

**Cross-cutting requirements**:

- Override mechanism MUST be **exercised end-to-end** before any agent goes live, and at least quarterly thereafter (per PRIN §I.1 validation gates).
- Reviewer competence baseline: documented training, periodic refresher, recorded competence assessment. Reviewers must be able to **interrogate** the agent's output, not merely accept it.
- **Oversight latency** (time between agent action and earliest possible human review) MUST be defined per agent and instrumented. For AI-005 this is a critical control because the decision has immediate legal effect on the applicant.
- The contestation route for every citizen-affecting system (AI-001 via supplier disputes, AI-002 via taxpayer appeals, AI-003 via service-desk escalation, AI-005 via MoHRE appeal pathway) MUST be published in plain language in Arabic and English per PRIN §III.14.

**Follow-up recommendation**: Run `/arckit-uae:uae-ai-autonomy-tier` next. It will classify each of AI-001…AI-005 into Tier 1 / 2 / 3 and produce the autonomy-posture artefact that this Human-in-the-Loop design depends on for tier-appropriate controls.

---

## External References

### Document Register

| Doc ID | Title | URL | Verified date |
|--------|-------|-----|---------------|
| UAE-AI-CHARTER | UAE Charter for the Development and Use of Artificial Intelligence | <https://uaelegislation.gov.ae/en/policy/details/the-uae-charter-for-the-development-and-use-of-artificial-intelligence> | 2026-05-28 |
| ARC-000-PRIN-v1.0 | UAE Federal Entity — Agentic AI Architecture Principles | `projects/000-global/ARC-000-PRIN-v1.0.md` | 2026-05-28 |

### Citations

| Citation | Doc ID | Section | Used in |
|----------|--------|---------|---------|
| AICH-1 | UAE-AI-CHARTER | Principle 3 (Bias Mitigation) | Bias & Fairness Assessment; 12-Principle Assessment row 3 |
| AICH-2 | UAE-AI-CHARTER | Principle 6 (Human Oversight) | Human-in-the-Loop Design; 12-Principle Assessment row 6 |
| AICH-3 | UAE-AI-CHARTER | All 12 principles | 12-Principle Assessment (all rows) |

### Unreferenced Documents

None — the UAE Charter is the sole external authority cited. Federal entities adopting this playbook are expected to load (i) the Charter text, (ii) the UAE PDPL Federal Decree-Law 45/2021, (iii) the UAE IAS, and (iv) any entity-specific governance policies into `projects/000-global/policies/`, then re-run this command to lift inline citations into the 12-Principle Assessment rows.

---

**Generated by**: ArcKit `/arckit-uae:uae-ai-charter` command
**Generated on**: 2026-05-28
**ArcKit Version**: 5.4.0
**Project**: Agentic AI Portfolio (Project 001)
**Model**: Claude Opus 4.7 (1M context)
