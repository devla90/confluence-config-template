# Project: Acme Corp Web Portal

## Directory structure requirement

This config repo must be a sibling of the framework repo:

```
../confluence-framework/           <- framework (shared, open source)
../confluence-config-acme-web/  <- this repo (project-specific)
```

## Confluence Documentation

- **Framework**: ../confluence-framework/
- **Config**: ./project-config.md
- **Page structure**: ./page-structure.md

## How to generate documentation

When asked to generate Confluence documentation:

1. Read project config: `./project-config.md` — get prefix (ACME), space key (ACMEWEB), frentes, tech labels, documentation language (english)
2. Read standards: `../confluence-framework/docs/documentation-guide.md` — naming, labels, lifecycle, Page Properties
3. Read the corresponding template: `../confluence-framework/templates/{type}.md`
4. Generate the document in `output/` following the template structure
5. Write content in the language specified in project-config.md (spanish)

## Available document types

| Type | Template |
|------|----------|
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

## Connecting code repos

To enable documentation generation from a code repository, copy the CLAUDE.md template:

```bash
cp ../confluence-framework/examples/repo-claude-md-example.md /path/to/your/repo/CLAUDE.md
```

Fill in the variables with this project's values:
- `{FRONT}` → the frente (e.g., `frontend`)
- `{PREFIX}` → `ACME-FRONT` (or the corresponding suffix)
- `{FRAMEWORK_PATH}` → relative path to `../confluence-framework/`
- `{CONFIG_PATH}` → relative path to `../confluence-config-acme-web/`
- `{SPACE_KEY}` → `ACMEWEB`
- `{DESCRIPTION}` → short repo description

## Key rules

- **Language**: English (as defined in project-config.md)
- **Naming**: `[ACME-{SUFFIX}] Type — Subject`
- **Labels**: Always include `team:`, `type:`, `status:`
- **Secrets**: NEVER in Confluence. Reference path in AWS Secrets Manager
- **Diagrams**: draw.io macro (editable), not static images
