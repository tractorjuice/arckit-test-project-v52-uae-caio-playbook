# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project: UAE CAIO Playbook

A planning workspace for UAE federal Chief AI Officers to govern the path to
50% autonomous AI government services by 2028, per the 23 April 2026 directive
of HH Sheikh Mohammed bin Rashid Al Maktoum and the federal framework approved
by UAE Cabinet on 18 May 2026.

**This is a documentation/governance workspace, not a code project.** There is
no build, lint, or test loop. All outputs are markdown artefacts under
`projects/`. Work is driven by ArcKit slash commands invoked through Claude
Code.

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
NESA/UAE IAS controls, UAE PDPL, UAE AI Charter — not generic IT governance.

## Architecture Toolkit

This project uses two ArcKit plugins (v5.4.0) auto-enabled via
`.claude/settings.json`:

- **`arckit`** (core) — 71 commands for enterprise architecture governance.
- **`arckit-uae`** (community overlay) — 12 UAE-specific commands:
  `uae-ai-charter`, `uae-pdpl`, `uae-ias`, `uae-ai-autonomy-tier`,
  `uae-cloud-residency`, `uae-classification`, `uae-data-sharing`,
  `uae-digital-records`, `uae-priorities-alignment`, `uae-procurement`,
  `uae-uaepass`, `uae-zero-bureaucracy`.

Slash-command syntax is colon-namespaced: `/arckit:<name>` for core,
`/arckit-uae:<name>` for the overlay.

### Orientation commands (use these when the user is vague)

- `/arckit:start` — guided onboarding; recommends a command sequence by
  sector and stage.
- `/arckit:navigator` — coverage report against the ArcKit baseline; surfaces
  DRAFT, stale, or orphan artifacts and recommends the next command.
- `/arckit:build` — parallel bulk-build orchestrator; resumable via
  `.arckit/state.json`.
- `/arckit:health` — finds stale research, forgotten ADRs, unresolved review
  conditions, and version drift across all projects.

### First-command sequence for an agentic AI portfolio

1. `/arckit:principles` — entity-level AI principles aligned to UAE AI Charter
2. `/arckit-uae:uae-ai-charter` — Charter compliance check (12 principles)
3. `/arckit:stakeholders` — Ministerial Council, Cabinet Affairs, CAIO governance
4. `/arckit:requirements` — candidate services for autonomous delivery
5. `/arckit:sobc` — Strategic Outline Business Case (Green Book 5-case)
6. `/arckit:roadmap` — 24-month plan with directive KPIs
7. `/arckit:risk` — agent autonomy risks, contestability, oversight
8. `/arckit:atrs` — Algorithmic Transparency Recording Standard, per agent
9. `/arckit:ai-playbook` — Responsible AI deployment
10. `/arckit-uae:uae-pdpl` — UAE PDPL (Federal Decree-Law 45/2021)
11. `/arckit-uae:uae-ias` — UAE Information Assurance Standard (NESA-aligned,
    188 controls)

### Project Structure

- `projects/000-global/` — cross-project artifacts (principles, standards)
- `projects/001-*/` — numbered project directories with architecture documents
- `docs/` — documentation and reference guides

### Document Naming Convention

All documents follow: `ARC-{PROJECT_ID}-{TYPE_CODE}-v{VERSION}.md`

- Example: `ARC-001-REQ-v1.0.md` (Requirements for project 001)
- Multi-instance types (ADR, DIAG): `ARC-001-ADR-001-v1.0.md`

## Environment notes

- `.devcontainer/devcontainer.json` raises `CLAUDE_CODE_MAX_OUTPUT_TOKENS` to
  `64000` — ArcKit artefacts often need large single outputs; do not assume
  the default 32k limit.
- `.arckit/memory/sessions.md` is appended automatically by an ArcKit
  session-learner hook after each session. Do not hand-edit it.
- `.arckit/state.json` (when present) is owned by `/arckit:build` for
  resumable parallel builds.
