# Project Configuration — {Your Project Name}

> Fill in every `{placeholder}` below. This file is what makes the framework
> project-specific; the framework itself never holds these values.
> A filled example: `confluence-framework/examples/config-repo/project-config.md`.

---

## Identity

| Field | Value |
|-------|-------|
| Project name | {Your Project Name} |
| Organization | {Your Organization} |
| Naming prefix | {PREFIX} |
| Confluence space key | {SPACEKEY} |
| Space shared with other projects | {yes / no} |
| Confluence URL | {https://your-org.atlassian.net/wiki} |
| Documentation language | {english / spanish / portuguese} |
| Team size | {e.g. 5-15} |

## Paths

| Field | Value |
|-------|-------|
| Framework path | ../confluence-framework |
| Output path | ./output |

## Frentes (Sections)

These seven are a common starting point. Delete the ones you do not have and rename the
rest — the suffix is what appears in every page title as `[{PREFIX}-{SUFFIX}]`.

| Front | Suffix | Technologies | Section Owner | Team Label |
|-------|--------|-------------|---------------|------------|
| Frontend | FRONT | {tech, tech} | {role} | team:frontend |
| Backend | BACK | {tech, tech} | {role} | team:backend |
| UI/UX | DESIGN | {tech, tech} | {role} | team:design |
| Business | BIZ | {tech, tech} | {role} | team:business |
| Architecture | ARCH | {tech, tech} | {role} | team:architecture |
| Security | SEC | {tech, tech} | {role} | team:security |
| QA & Testing | QA | {tech, tech} | {role} | team:qa |

## Code Repositories

Fill in the path of each repo you want documented. Empty rows are skipped — the AI
generates placeholders instead of reading code.

**Prefer relative paths** — they resolve from this config repo, so they keep working on
a teammate's machine and on your next one. This file is committed and shared; absolute
paths are specific to one machine.

| Front | Suffix | Local path | Description |
|-------|--------|-----------|-------------|
| Frontend | FRONT | {../my-frontend-repo} | {short description} |
| Backend | BACK | {../my-backend-repo} | {short description} |
| UI/UX | DESIGN | | No code — Figma only |
| Business | BIZ | | No code — Jira only |
| Architecture | ARCH | {../my-infra-repo} | {short description} |
| Security | SEC | | |
| QA & Testing | QA | {../my-e2e-repo} | {short description} |

> A path passed as the third argument to `/doc-confluence <type> <subject> [target-path]`
> overrides whatever is in this table.

## Technology Labels

One row per technology your team will want to filter pages by in Confluence.

| Label | Description |
|-------|-------------|
| tech:{name} | {what it is} |
| tech:{name} | {what it is} |

## Secrets Platform

Never a credential — only where credentials live, so generated documents can point at
the right place instead of inlining a value.

| Field | Value |
|-------|-------|
| Tool | {AWS Secrets Manager / Azure Key Vault / HashiCorp Vault / GCP Secret Manager} |
| Reference format in docs | {e.g. "See AWS Secrets Manager: {path}"} |

## Tools

| Tool | Purpose |
|------|---------|
| {Jira / Azure DevOps / Linear} | Task management and backlog |
| {Figma / Sketch} | UI/UX design |
| {GitHub / GitLab / Bitbucket} | Source code |
| {draw.io} | Architecture and flow diagrams |

## Overrides

None.
