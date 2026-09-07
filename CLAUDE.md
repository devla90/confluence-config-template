@AGENTS.md

# Claude Code specifics

Everything about this project — structure, how to generate, output layout, connecting
code repos, key rules — is in `AGENTS.md`, imported above. This file only holds what is
specific to Claude Code.

## Generating a document

```
/doc-confluence <type> <subject> [target-path-or-url]
```

The third argument overrides the `Code Repositories` table for one run, and accepts a
URL as well as a path:

```
/doc-confluence api-spec Payments /path/to/payments-api
/doc-confluence api-spec Stripe https://docs.stripe.com/api
```

## Installing the skill

The skill lives in the framework repo, scoped to that directory. To run it from here:

```bash
cp -r ../confluence-framework/.claude/skills/doc-confluence ~/.claude/skills/
cp -r ../confluence-framework/.claude/agents/confluence-doc ~/.claude/agents/
```

On Windows these run in Git Bash. PowerShell equivalents are in
`../confluence-framework/docs/customization-guide.md` -> Windows notes.

## Reading an external repo

Mode B needs access to a folder outside this repo: `/add-dir /path/to/your/repo`, or
`permissions.additionalDirectories` in `settings.json`.

## Other assistants

Codex, Copilot, opencode, Devin and anything else reading `AGENTS.md` work here too.
Adapters: `../confluence-framework/adapters/`. Matrix:
`../confluence-framework/docs/compatibility.md`.
