# Architecture Decision Records

ADRs are **alignment bundles for AI** — decisions already made so agents don't freestyle. They are **not hard gates** and never fully veto the owner.

**Conflict:** name the ADR + technical tension → one keep-vs-change question → follow Josh → continue work; supersede when practical (not as a gate).

## Format

Each ADR leads with a three-column card:

| What | Why | For AI |
| --- | --- | --- |
| The decision | Real reason (don't invent a stricter why) | Default path; not a veto |

## Protocol

- **Filename:** `NNNN-slug.md`. Use `new-adr <slug>`.
- **Status:** `active` | `draft` | `superseded by NNNN`
- **New / change:** new file; never rewrite superseded substance.
- Index table: `adr-index` regenerates it.

## Index

| # | Decision | Status |
|---|---|---|
