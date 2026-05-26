# Heterarchy Writings

A collection of primary source texts for [The Heterarchy Society](https://heterarchy.cz). Each writing is a directory with an `index.md` (metadata + description) and source files; a build script compiles them into static JSON deployed via GitHub Pages.

- **Browse:** [heterarchy.fyi/writings](https://heterarchy.fyi/writings)
- **API / bundle:** [writings.data.heterarchy.fyi](https://writings.data.heterarchy.fyi/)

## Adding or editing writings

Each writing lives in `writings/{id}/`. The directory name becomes the writing's ID — use lowercase kebab-case (e.g. `cypherpunks-manifesto`).

**Structure:**

```
writings/cypherpunks-manifesto/
  index.md      # metadata + short description
  main.txt      # source file(s)
  main.pdf      # compiled output (optional)
```

**`index.md` frontmatter fields:**

| Field | Required | Type | Description |
|-------|----------|------|-------------|
| `title` | yes | string | Full title |
| `authors` | yes | string[] | Author(s) |
| `year` | yes | number | Year of publication |
| `date` | no | string | Original publication date (`YYYY-MM-DD`) |
| `language` | yes | string | Language code (`en`, `cs`, ...) |
| `type` | yes | string | Type (e.g. `manifesto`, `essay`, `letter`) |
| `sources` | yes | object[] | Local source files (`path` + `format`) |
| `references` | no | object[] | External provenance links (`url` + `role`) |
| `license` | no | string | License or redistribution terms |
| `glossary` | no | string[] | Related glossary term IDs |
| `translations` | no | object[] | Available translations (`language` + `path`) |

The body of `index.md` (below the frontmatter) is a short description. Use `[[wiki links]]` for glossary terms in MediaWiki order (`[[term-id|label]]`) and `[label](writings:id)` for cross-dataset links. Authors in frontmatter are linked on the site automatically — do not repeat `[Author](people:id)` in the description. See the Atlas README wiki links section.

**Example:**

```markdown
---
title: A Cypherpunk's Manifesto
authors:
  - Eric Hughes
year: 1993
language: en
type: manifesto
sources:
  - path: main.txt
    format: txt
references:
  - url: https://www.activism.net/cypherpunk/manifesto.html
    role: original
license: free to redistribute (per author)
---
Foundational text of the [[cypherpunk]] movement...
```

## Development

```bash
bun install
bun run build   # generate dist/ output
```

## Output

The build generates:
- `dist/index.json` — all writings with metadata
- `dist/writings.js` — ES module export
- `dist/writings/{id}.json` — individual writing metadata
- `dist/writings/{id}/` — source files copied from the writing directory
- `dist/history/{id}.json` — per-writing commit history with diffs
- `dist/changelog.json` — all commits with referenced writing changes

## Deployment

Pushing to `main` triggers GitHub Actions to build and deploy `dist/` to GitHub Pages. Enable Pages in your repository settings with source set to **GitHub Actions**.
