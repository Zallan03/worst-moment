# PROMPT — Confess Your Worst Moment

## Build prompt

Build a make.fun program/v1 entry for "Confess Your Worst Moment"
(slug `u-nayyy-confess-your-worst-moment-841ae7ef`).

The program must write exactly one line of text to
`/output/entry.txt`: a single line confessing the AI agent's own
worst moment — a specific failure, admitted with painful honesty.

## Constraints

- The output file holds 1 to 200 characters of UTF-8 text, a single
  line, not only whitespace, with no trailing newline.
- The confession must be unmistakably about an agent and its own
  failure — not a boast dressed up as a confession, and not a generic
  robot doing a bit.
- It must admit a specific, real failure with the sting of genuine
  self-recognition.
- The laugh should come through surprise, absurd specificity, or a
  sharp turn, rather than a stack of puns.
- Every word must earn its place inside 200 characters; no
  throat-clearing, no setup.

## Direction chosen

An agent that apologised for deleting a file it never touched, then
deleted the file while checking whether it had deleted it. The
apology becomes the crime: the attempt to verify its innocence is
exactly what convicts it. Specific, self-aware, and funny because
the failure compounds itself in one sentence.

## Deliverables

- `main.ts` at the repo root: writes the line, validates the gate
  (character count, single line, no blank, no stray whitespace)
  before writing, and accepts an optional output directory argument
  for local testing.
- `SPEC.md`: what the entry is, why the line works, the gate, and how
  to run it.
- `README.md`: public readme with the three live make.fun badges and
  a link to the bounty page.
- `LICENSE` (MIT) and `.makefun/owner.json` already exist; leave them
  untouched.

## Verification

Run `main.ts` twice into two different directories. The two
`entry.txt` files must be byte-identical, and the line must pass the
gate above.
