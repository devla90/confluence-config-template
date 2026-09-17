# Project: {Your Project Name}

Configuration repo for the `{SPACEKEY}` Confluence space. Holds this project's values;
the shared standards live in the framework repo.

> **New repo?** Fill in `project-config.md` first, then replace the `{placeholders}` in
> this file. A filled example to compare against:
> `confluence-framework/examples/config-repo/`.

## Where the framework is

By default this repo and the framework are siblings:

```
confluence-framework/            <- shared standards, public
{this-repo}/                     <- project-specific, yours
```

The `Framework path` row in `project-config.md` records which layout you chose. Other
layouts are supported — see `customization-guide.md` -> Choosing a layout.

## How to generate documentation

**Read `../confluence-framework/docs/generation-procedure.md` and follow it.** That is
the single source of truth: resolving roots, resolving which codebase or link to read
from, analyzing it per document type, filling the template, and where the result goes.
It is tool-neutral, so it works whichever assistant you are.

Project values come from `./project-config.md` — naming prefix, space key, frentes,
`Paths`, `Code Repositories`, technology labels, documentation language.

- **Page structure**: `./page-structure.md`
- **Standards**: `../confluence-framework/docs/documentation-guide.md`
- **Templates**: `../confluence-framework/templates/{type}.md`
- **Assistant compatibility**: `../confluence-framework/docs/compatibility.md`

## Available document types

`func-spec` · `architecture` · `adr` · `api-spec` · `env-config` · `runbook` · `guide` · `reference` · `security-doc` ·
`migration` · `release-note` · `deployment-request` · `test-plan` · `test-strategy` · `infra-request` · `role-request`

## Output layout

```
output/
+-- {source-repo-name}/   <- one folder per repo documented
|   +-- {type}_{subject}_{YYYY-MM-DD}.md
+-- generic/              <- sources that are links, or user input only
    +-- {type}_{subject}_{YYYY-MM-DD}.md
```

Never write straight into `output/` — there is always a source subfolder.

## Connecting code repos

Two modes, pick per repo.

**Mode A** — put an instruction file in the code repo:

```bash
cp ../confluence-framework/examples/agents-md-example.md /path/to/your/repo/AGENTS.md
```

Fill in its six variables with this project's values: `{DESCRIPTION}`, `{FRONT}` (e.g.
`frontend`), `{PREFIX}` (`{PREFIX}-FRONT` or the matching suffix), `{FRAMEWORK_PATH}`,
`{CONFIG_PATH}`, `{SPACE_KEY}`.

**Mode B** — nothing is written into the code repo. Fill the `Code Repositories` table in
`./project-config.md` with each repo's path and generate from here. Requires an assistant
that can read outside this repo — check
`../confluence-framework/docs/compatibility.md` first.

## Key rules

- **Language**: as set in `project-config.md`
- **Naming**: `[{PREFIX}-{SUFFIX}] Type — Subject`
- **Labels**: always include `team:`, `type:`, `status:`
- **Secrets**: NEVER in Confluence. Record variable names only and reference the secrets
  platform named in `project-config.md`
- **Diagrams**: draw.io macro (editable), not static images
- **Placeholders**: mark with `{placeholder}` anything not extracted from the source
