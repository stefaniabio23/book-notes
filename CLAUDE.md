# Project: book-notes

Chapter notes for every book read. Parker-style atomic bullets by default; flowing prose only for foundational worldview books (Atlas Shrugged, Jung CW, Pirsig, etc.). One file per book at `[slug].md`. Source library symlinked at `sources/` → `~/Desktop/Sources/books/`.

## What lives here

- `[book-slug].md` — one file per book, named in kebab-case
- `BIBLIOGRAPHY.md`, `CONCEPTS.md`, `QUOTES.md` — auto-generated indices (do not hand-edit; use the relevant skill)
- `README.md` — book index table
- `.book-meta-files` — canonical list of files to exclude from skill scans
- `.concept-aliases.txt`, `.concept-stopwords.txt`, `.concept-seeds.txt` — concept-skill sidecars (hand-edited; preserved across regenerations)
- `.biblio-aliases.txt`, `.biblio-stopwords.txt`, `.biblio-notes.md` — bibliography-skill sidecars
- `sources/` — symlink to `~/Desktop/Sources/books/`

## House style

- Stop-slop. No em dashes in book-notes prose. No AI filler.
- Named concepts in `[brackets]` so `/concepts` extracts them cleanly.
- Italics reserved for titles (books, papers, works) and pure emphasis. Bold for bullet-section headers.
- Cite paragraphs as `[¶42]` or pages as `[p.105]` only when the source has stable numbering. Omit for epubs.
- Frontmatter required on every book file: run `/book-frontmatter` to seed/repair.

## Meta-file convention

All four book-notes skills (`/book-frontmatter`, `/concepts`, `/bibliography`, `/quotes`) skip files listed in `.book-meta-files` plus anything starting with `.`. If a new meta file is added (e.g. a `STYLE_GUIDE.md`), append its name to that file — do not edit each skill spec.

## What this project does NOT do

- Does not edit source PDFs/epubs in `~/Desktop/Sources/books/`.
- Does not publish anywhere.
- Does not generate review prose (that's `~/Projects/book-reviews/`).
