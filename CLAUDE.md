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

1. Read project config: `./project-config.md` — get prefix (ACME), space key (ACMEWEB), frentes, `Paths`, `Code Repositories`, tech labels, documentation language (english)
2. Read standards: `../confluence-framework/docs/documentation-guide.md` — naming, labels, lifecycle, Page Properties
3. Read the corresponding template: `../confluence-framework/templates/{type}.md`
4. Resolve the source to document: the path **or URL** given in the request, otherwise the `Code Repositories` row matching the chosen frente. Analyze that codebase with Glob/Grep/Read, or fetch the link with WebFetch. Skip if nothing is available and use placeholders instead
5. Generate the document in `{Output path}/{source}/` (default base `./output/`), where `{source}` is the basename of the source repo, or `generic` when the source was a link or user input only. Create the folder with `mkdir -p` — never write straight into `output/`
6. Write content in the language specified in project-config.md

Never copy secret values out of the target repo — record variable names only and reference AWS Secrets Manager.

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

Two modes, pick per repo.

### Mode A — CLAUDE.md inside the code repo

```bash
cp ../confluence-framework/examples/repo-claude-md-example.md /path/to/your/repo/CLAUDE.md
```

Fill in the variables with this project's values:
- `{DESCRIPTION}` → short repo description
- `{FRONT}` → the frente (e.g., `frontend`)
- `{PREFIX}` → `ACME-FRONT` (or the corresponding suffix)
- `{FRAMEWORK_PATH}` → relative path to `../confluence-framework/`
- `{CONFIG_PATH}` → relative path to `../confluence-config-acme-web/project-config.md`
- `{SPACE_KEY}` → `ACMEWEB`

### Mode B — aim at an external path from this repo

Nothing is written into the code repo.

1. Fill the `Code Repositories` table in `./project-config.md` with each repo's local path
2. Install the skill globally so it works from here:
   ```bash
   cp -r ../confluence-framework/.claude/skills/doc-confluence ~/.claude/skills/
   cp -r ../confluence-framework/.claude/agents/confluence-doc ~/.claude/agents/
   ```

   On Windows these run in Git Bash. For PowerShell equivalents and path-format rules see `docs/customization-guide.md` -> Windows notes.
3. Grant read access to the target: `/add-dir /path/to/your/repo`
4. Run from this repo: `/doc-confluence api-spec Authentication Service`

Pass a path as the third argument to override the table for one run:
`/doc-confluence api-spec Payments /path/to/payments-api`

A URL works too — the result is filed under `output/generic/`:
`/doc-confluence api-spec Stripe https://docs.stripe.com/api`

## Output layout

```
output/
+-- {source-repo-name}/          <- one folder per repo documented
|   +-- {type}_{subject}_{YYYY-MM-DD}.md
+-- generic/                     <- sources that are links, or user input only
    +-- {type}_{subject}_{YYYY-MM-DD}.md
```

## Key rules

- **Language**: English (as defined in project-config.md)
- **Naming**: `[ACME-{SUFFIX}] Type — Subject`
- **Labels**: Always include `team:`, `type:`, `status:`
- **Secrets**: NEVER in Confluence. Reference path in AWS Secrets Manager
- **Diagrams**: draw.io macro (editable), not static images
