# UAE CAIO Playbook

A planning workspace for UAE federal Chief AI Officers to govern the path to
**50% autonomous (agentic) AI government services by 2028**, per the directive of
HH Sheikh Mohammed bin Rashid Al Maktoum (23 April 2026) and the federal framework
approved by UAE Cabinet on 18 May 2026.

This repository uses **ArcKit v5.4.0** with the `arckit` core plugin and the
`arckit-uae` community overlay pre-enabled — a ready-to-use governance toolkit
that any federal entity can fork and adapt for its own agentic AI portfolio.

## The directive in brief

- **50% of UAE federal government services delivered by autonomous AI agents by 2028.**
- **Oversight:** HH Sheikh Mansour bin Zayed Al Nahyan, chair of the renamed
  Ministerial Council for AI and Development.
- **Execution coordinator:** Minister of Cabinet Affairs Mohammad Al Gergawi.
- **Performance metrics in the directive:** speed of adoption, implementation
  quality, workflow redesign.
- **Already live (May 2026):** four federal agents — Procurement, Tax Auditing,
  Customer Happiness, Technical Support; MoHRE autonomous work-permit
  decisions (from 1 May 2026); 80,000 employees in training.
- **Parallel Dubai mandate:** Sheikh Hamdan bin Mohammed has directed the
  emirate's private sector onto the same 24-month horizon.

## What this repo is for

A federal Chief AI Officer should be able to clone this repository and produce
a defensible, board-ready governance pack for their entity's agentic AI
portfolio — covering principles, stakeholders, requirements, business case,
roadmap, risk, transparency records, and UAE-specific compliance — in the
language of HH Sheikh Mansour's Ministerial Council, not generic IT-speak.

## Getting Started

### Prerequisites

- [Claude Code](https://claude.ai/code) installed
- GitHub Codespaces (recommended) or a local dev environment

### Setup

1. Open this repo in a GitHub Codespace, or clone locally.
2. Claude Code auto-installs via `.devcontainer/devcontainer.json`.
3. Both ArcKit plugins (`arckit` core, `arckit-uae` overlay) auto-enable via
   `.claude/settings.json`.
4. Restart Claude Code once to resolve the marketplace plugins.

### Recommended first-command sequence (for the agentic AI mandate)

Run these in order. Each command is a slash command in Claude Code.

```bash
# 1. Architecture principles aligned to the UAE AI Charter
/arckit.principles

# 2. UAE AI Charter compliance review
/arckit.uae-charter-ai

# 3. Stakeholders — Ministerial Council, Cabinet Affairs, internal CAIO governance
/arckit.stakeholders

# 4. Candidate services for autonomous delivery
/arckit.requirements

# 5. Strategic Outline Business Case (Green Book 5-case structure)
/arckit.sobc

# 6. 24-month phased roadmap with the directive's three KPIs
/arckit.roadmap

# 7. Risk register — agent autonomy, oversight, contestability
/arckit.risk

# 8. Algorithmic Transparency Recording Standard (per agent)
/arckit.atrs

# 9. Responsible AI Playbook
/arckit.ai-playbook

# 10. UAE Personal Data Protection Law (Federal Decree-Law 45/2021)
/arckit.uae-pdpl

# 11. UAE cybersecurity / NESA controls
/arckit.uae-cybersecurity
```

The `arckit-uae` overlay also ships nine other UAE-specific commands — see
[the ArcKit Documentation](https://tractorjuice.github.io/arc-kit/) for the
full reference.

## Project Structure

```text
projects/
├── 000-global/         # Cross-project artifacts (principles, standards)
└── 001-…/              # Per-portfolio project directories (created by commands)
```

## Links

- [ArcKit Documentation](https://tractorjuice.github.io/arc-kit/)
- [ArcKit Repository](https://github.com/tractorjuice/arc-kit)
- [ArcKit Plugin Marketplace](https://github.com/tractorjuice/arc-kit)

---

*ArcKit v5.4.0 | Test project v52 | Generated 2026-05-28*
