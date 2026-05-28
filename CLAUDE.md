# CLAUDE.md

## Project: UAE CAIO Playbook

A planning workspace for UAE federal Chief AI Officers to govern the path to
50% autonomous AI government services by 2028, per the 23 April 2026 directive
of HH Sheikh Mohammed bin Rashid Al Maktoum and the federal framework approved
by UAE Cabinet on 18 May 2026.

## Mandate context (load this when reasoning about the project)

- **Target:** 50% of UAE federal government services delivered by autonomous
  (agentic) AI agents within 24 months — by 2028.
- **Oversight:** Ministerial Council for AI and Development, chaired by
  HH Sheikh Mansour bin Zayed Al Nahyan.
- **Execution coordinator:** Mohammad Al Gergawi, Minister of Cabinet Affairs.
- **Directive KPIs:** adoption speed, implementation quality, workflow redesign.
- **Live agents (May 2026):** Procurement, Tax Auditing, Customer Happiness,
  Technical Support. MoHRE autonomous work-permit decisions live since
  1 May 2026.
- **Workforce:** 80,000 federal employees in agentic AI training.
- **Parallel Dubai private-sector mandate** (Sheikh Hamdan, May 2026): same
  24-month horizon.

When generating artefacts, frame outputs in the language of this directive —
the Ministerial Council, the three KPIs, the four already-live agents,
NESA cyber controls, UAE PDPL, UAE AI Charter — not generic IT governance.

## Architecture Toolkit

This project uses two ArcKit plugins (v5.4.0):

- **`arckit`** (core) — 71 commands for enterprise architecture governance.
- **`arckit-uae`** (community overlay) — 12 UAE-specific commands including
  `uae-charter-ai`, `uae-pdpl`, `uae-cybersecurity`, and others.

### First-command sequence for an agentic AI portfolio

1. `/arckit.principles` — entity-level AI principles aligned to UAE AI Charter
2. `/arckit.uae-charter-ai` — Charter compliance check
3. `/arckit.stakeholders` — Ministerial Council, Cabinet Affairs, CAIO governance
4. `/arckit.requirements` — candidate services for autonomous delivery
5. `/arckit.sobc` — Strategic Outline Business Case
6. `/arckit.roadmap` — 24-month plan with directive KPIs
7. `/arckit.risk` — agent autonomy risks, contestability, oversight
8. `/arckit.atrs` — Algorithmic Transparency Recording Standard, per agent
9. `/arckit.ai-playbook` — Responsible AI deployment
10. `/arckit.uae-pdpl` — UAE PDPL (Federal Decree-Law 45/2021)
11. `/arckit.uae-cybersecurity` — UAE/NESA cyber controls

### Project Structure

- `projects/000-global/` — cross-project artifacts (principles, standards)
- `projects/001-*/` — numbered project directories with architecture documents
- `docs/` — documentation and reference guides

### Document Naming Convention

All documents follow: `ARC-{PROJECT_ID}-{TYPE_CODE}-v{VERSION}.md`

- Example: `ARC-001-REQ-v1.0.md` (Requirements for project 001)
- Multi-instance types (ADR, DIAG): `ARC-001-ADR-001-v1.0.md`
