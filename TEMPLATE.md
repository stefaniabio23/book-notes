# Book notes, extraction spec v2.1

Extract notes as future atom-seeding material, not as summaries.

**Optimization function**: maximize *reusable ideas per total words*. Completeness is not the goal. Books vary enormously: a Jung Prologue might yield 8-12 strong claims; an Atlas Shrugged chapter might yield 2-3; a dense philosophy text might yield 20+. There is no quota.

Goal: preserve a book's mechanisms, models, tensions, hidden assumptions, and surprising observations in a form that compounds in a long-lived knowledge graph as atoms (single claims), molecules (clusters of related claims), and compounds (essays, frameworks, blog posts).

## Output format

```
## [Book Title]

by [Author]

*Notes I took while reading this book to further my own learning. If you enjoy these notes, please [buy the book](https://example.com).*

*Published review: [stephanierebecca.com/books/slug](https://stephanierebecca.com/books/slug/)*

### Part 1: [Part Title]

#### Ch 1: [Chapter Title]

##### Core claims

- Domain-portable claim that reveals a mechanism, model, assumption, surprise, or tension.

##### Assumptions

- Hidden premise the chapter relies on but does not argue.

##### Tensions

- Force A ↔ force B

##### Terms

- Named Concept

##### Quotes (rare)

> "Exact wording that itself matters." [p.NN]

- Interpretation of what the quote actually claims.

#### Ch 2: [Chapter Title]

##### Core claims

- Claim.

### Metadata

Themes:
- theme

Candidate entities:
- Person or concept

Candidate links:
- [[Note Title]]
```

Omit any per-chapter section that is empty. Most chapters have Core claims; Assumptions, Tensions, Terms, and Quotes are conditional. Chapters with zero Quotes are the expected case.

## Gatekeepers (apply before writing any bullet)

### 1. Future reuse test

Could this become an independent atom linked to 3+ unrelated domains? If not, omit.

Bad: "The reader who came for Freud-Jung gossip has been warned."

Good: "Establishing an interpretive frame before presenting evidence makes later disagreement appear as category error." (Links to ideology, startups, politics, narratives, religion.)

### 2. Chapter-deletion test

If you deleted the chapter title and book title entirely, would this note still be useful?

Bad: "Jung says the rhizome metaphor structures the book."

Good: "Visible outcomes are often temporary expressions of deeper generative structures."

### 3. Quality threshold

Extract a claim only if it satisfies at least one of:

- reveals mechanism
- introduces reusable model
- exposes hidden assumption
- captures a tension
- surprises or updates prior beliefs
- compresses many observations
- likely links to multiple domains

If none apply, omit.

### 4. No quota

Do not target a fixed number of bullets. Quotas force inclusion of weak claims. Some chapters yield two strong claims; some yield twenty. Both are correct.

## Per-bullet rules

Within each section, every bullet follows these:

### 5. One idea = one bullet

Bad: "The author discusses repetition, persuasion, and media effects."

Good: "Humans often mistake familiarity for truth because repeated exposure reduces cognitive friction."

### 6. Mechanisms over conclusions

Ask "why would this happen?" and extract the answer.

Bad: "Stress causes poor decisions."

Good: "Stress narrows attention toward immediate threats, reducing cognitive bandwidth for long-term planning."

### 7. Structure beneath examples

Examples are evidence; models are reusable.

Bad: "The author describes a company that failed after becoming bureaucratic."

Good: "Organizations often accumulate process faster than they accumulate information, causing responsiveness to decay over time."

### 8. Domain-portable phrasing

A bullet should read and function outside its book context. Avoid "as discussed earlier," "this chapter argues," "the author claims," "Jung says X." Cite the claim, not the citation.

### 9. Compressing terminology only

Keep terms that compress meaning ([antifragility], [skin in the game], [collective unconscious]). Drop jargon that merely renames an ordinary idea. Each term goes once in the chapter's Terms section in plain Title Case; use `[brackets]` inline only when the term carries the claim.

### 10. Quotes rare, always with interpretation

Quote only when the wording itself is valuable. Follow with an interpretation bullet.

> "Until you make the unconscious conscious, it will direct your life and you will call it fate."

- Unexamined psychological patterns often appear subjectively as external events.

### 11. Ignore filler

Skip anecdotes that don't reveal a principle, historical details without broader relevance, repetition, rhetorical flourishes, chapter transitions, "this chapter argues" framings.

### 12. Compression target

Every bullet should be near-atom-ready. If it would require substantial rewriting before atomization, rewrite it now.

## Section semantics

- **Core claims**: domain-portable mechanisms, models, or surprising observations. The chapter's load-bearing extractables.
- **Assumptions**: premises the chapter relies on but does not argue. Hidden axioms.
- **Tensions**: paired forces, written as `A ↔ B`. Captures useful contradictions explicitly.
- **Terms**: named concepts the chapter introduces. Plain Title Case, no brackets in this section. Use `[brackets]` inline in claims only when the term is the load-bearing word.
- **Quotes (rare)**: included only when the wording itself is valuable, always with an interpretation bullet.

## Metadata section (book-level, at end of file)

Three optional lists:

- **Themes**: broad subject tags.
- **Candidate entities**: people, organisations, named concepts. *Candidates* for downstream graph materialisation, not authored frontmatter.
- **Candidate links**: `[[wikilinks]]` to related notes, including ones that may not exist yet.

## House rules

- Stop-slop. No em dashes, no AI filler, no false agency, no "not X, but Y" binary contrasts.
- Italics reserved for titles (books, papers, works).
- Cite paragraphs as `[¶42]` or pages as `[p.105]` only when the source has stable numbering. Omit for epubs.
- Worldview-construction commentary (craft moves, vocabulary seeding, authorial staging) belongs in the book-reviews project, not in chapter notes. Chapter notes are domain-portable claims only.
