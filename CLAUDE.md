# CLAUDE.md — Lockhart Lawn Care

Marketing site for a Lockhart TX lawn care business — commercial-client-focused static front-end, near-zero hosting cost

One paragraph: what this is, the 2-3 load-bearing architectural facts, and what the server or
client never does. If a reader gets only this paragraph, they should not break anything.

## North star

Before any architectural choice, read **`docs/PRINCIPLES.md`**: the mission and non-negotiable
values for this project. A change that violates a principle should not be proposed. Tooling and
platform-plugin suggestions ("use this cloud's managed service") are one option, not the
default; run them through the PRINCIPLES test first.

## Decisions (ADRs = AI alignment, not vetoes)

ADRs in `decisions/` are **alignment bundles**: decisions already made so agents don't freestyle.
They are **not hard gates**. Never refuse Josh's ask because of an ADR; if tension, name the ADR,
one plain question, follow his ruling; supersede the ADR when practical, not as a work-stop.

- Before freelancing architecture: `grep decisions/` and read active records as defaults.
- New: `new-adr <slug>`. Changed: superseding ADR (never rewrite history). Index via `adr-index`.
- Writing an ADR is never a prerequisite gate for continuing work.

## Tech stack

- Language/framework: plain static HTML + CSS in `site/` — no build step, no JS dependencies
- Data: none (quote form posts out; payments stay in Yardbook/Stripe, not the site)
- Deploy: target Cloudflare Pages (free tier) — drop the `site/` folder; not yet deployed
- Run locally: open `site/index.html` in a browser

## Hard rules (defaults from active ADRs — owner can re-open)

- <rule> (ADR NNNN)
- <rule> (ADR NNNN)

## Working style

- Append to `CHANGELOG.md`: `- **YYYY-MM-DD** — what changed and why`.
- Append non-obvious gotchas to `LEARNINGS.md` (the trap + the rule that avoids it).
- Commit policy: <auto-commit at working checkpoints | only when asked>.
- Branching: <main-only pre-deploy | branch-per-issue feat/<#>-slug, PR with Closes #, main
  always deployable>.
- Transcripts go in `transcripts/YYYY-MM-DD-topic.md`; mine them for ADR-worthy decisions.
