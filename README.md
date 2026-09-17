# Confluence Config — {Your Project Name}

Project-specific configuration for documenting **{Your Project Name}** in Confluence
Cloud, following the standards in
[confluence-framework](https://github.com/devla90/confluence-framework).

> **This is a template repository.** Press **Use this template** to create your own
> config repo, then work through the checklist below. The repo you get is yours — no
> ongoing link back here, no shared history.

---

## Setup checklist

- [ ] **1. Create your repo** — press *Use this template* above, name it
      `confluence-config-{your-project}`
- [ ] **2. Clone it next to the framework:**
      ```bash
      git clone https://github.com/devla90/confluence-framework
      git clone <your-new-repo>
      ```
      To pin a framework release: `git clone --branch v1.0.0 <framework-url>`
- [ ] **3. Fill in `project-config.md`** — every `{placeholder}`. Start with Identity and
      Frentes; the rest can follow
- [ ] **4. Adapt `page-structure.md`** to the frentes you actually kept
- [ ] **5. Install your assistant's adapter** — one command, see
      [`adapters/README.md`](https://github.com/devla90/confluence-framework/blob/main/adapters/README.md)
- [ ] **6. Smoke test** — from this repo, generate something small and check it lands in
      `output/`
- [ ] **7. Delete this checklist** and describe your project instead

A filled example to compare against at any point:
[`examples/config-repo/`](https://github.com/devla90/confluence-framework/tree/main/examples/config-repo).

---

## What lives here

| File | Holds |
|------|-------|
| `project-config.md` | Identity, paths, frentes, code repositories, tech labels, secrets platform |
| `page-structure.md` | The Confluence page tree for this project |
| `AGENTS.md` | Entry point every AI assistant reads |
| `CLAUDE.md` | Claude Code's entry point; imports `AGENTS.md` |
| `output/` | Generated documents, one subfolder per source |

Standards, templates and the generation procedure are **not** duplicated here — they
stay in the framework repo, so an update there reaches every project.

## Generating a document

```
/doc-confluence <type> <subject> [source-path-or-url]
```

Types: `func-spec` · `architecture` · `adr` · `api-spec` · `env-config` · `runbook` · `security-doc` ·
`migration` · `test-plan` · `test-strategy` · `infra-request` · `role-request`

Results are filed under `output/{source}/` — one folder per repo documented, `generic/`
for links. Full walkthrough:
[`docs/how-it-works.md`](https://github.com/devla90/confluence-framework/blob/main/docs/how-it-works.md).

## Rules that apply to everything generated here

- **Secrets never appear in Confluence.** Variable names only, plus a pointer to the
  secrets platform named in `project-config.md`
- **Nothing is invented.** What cannot be extracted from the source or supplied by you
  stays a `{placeholder}`
- **Relative repo paths.** This file is shared; absolute paths break for teammates
