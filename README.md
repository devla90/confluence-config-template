# Confluence Config — Acme Corp Web Portal

Project-specific configuration for generating Confluence documentation using the [Confluence Framework](../confluence-framework/).

## Overview

| Field | Value |
|-------|-------|
| Space Key | `ACMEWEB` |
| Prefix | `ACME` |
| Language | English |
| License | Apache 2.0 |

## Repository Structure

```
├── project-config.md    # Project identity, frentes, tech labels, tools
├── page-structure.md    # Full Confluence page tree and section definitions
├── output/              # Generated documentation (not committed)
├── CLAUDE.md            # AI agent instructions for document generation
└── LICENSE
```

## Sections (Frentes)

| Section | Prefix | Owner |
|---------|--------|-------|
| Frontend | `ACME-FRONT` | Tech Lead Frontend |
| Backend & Services | `ACME-BACK` | Tech Lead Backend |
| UI/UX Design | `ACME-DESIGN` | Design Lead |
| Business & Product | `ACME-BIZ` | Product Owner |
| Architecture & Cloud | `ACME-ARCH` | Solution Architect |
| Security & Compliance | `ACME-SEC` | Security Lead |
| QA & Testing | `ACME-QA` | QA Lead |
| Governance Hub | `ACME-HUB` | Documentation Champion |

## How to Generate Documentation

1. Ensure the framework repo is a sibling directory:
   ```
   ../confluence-framework/   ← framework (shared)
   ../confluence-config-acme-web/  ← this repo
   ```

2. Register the repos you want documented in the `Code Repositories` table of
   `project-config.md`, then use the AI agent (Claude Code) from this directory:
   ```
   Generate a [document type] for [subject]
   ```
   or run the skill directly, optionally pointing at a path or a link:
   ```
   /doc-confluence api-spec Payments Service /path/to/payments-api
   /doc-confluence api-spec Stripe https://docs.stripe.com/api
   ```

3. The generated document is placed under `output/{source}/`, following the framework
   templates and project conventions:

   ```
   output/
   +-- {source-repo-name}/   <- one folder per repo documented
   |   +-- {type}_{subject}_{YYYY-MM-DD}.md
   +-- generic/              <- sources that are links, or user input only
       +-- {type}_{subject}_{YYYY-MM-DD}.md
   ```

## Available Document Types

| Type | Template Key |
|------|-------------|
| Functional Specification | `func-spec` |
| Architecture Decision Record | `adr` |
| API Specification | `api-spec` |
| Environment Configuration | `env-config` |
| Operational Runbook | `runbook` |
| Security/Compliance Document | `security-doc` |
| Migration (AS-IS to TO-BE) | `migration` |
| Test Plan | `test-plan` |
| Testing Strategy | `test-strategy` |
| Infrastructure Request | `infra-request` |
| Deployment Role Request | `role-request` |

## Connecting Code Repositories

To enable documentation generation from a code repo, copy the CLAUDE.md template:

```bash
cp ../confluence-framework/examples/repo-claude-md-example.md /path/to/your/repo/CLAUDE.md
```

See `CLAUDE.md` in this repo for the full variable reference.
