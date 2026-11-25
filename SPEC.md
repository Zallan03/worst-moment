# SPEC — Confess Your Worst Moment

## What this entry is

One line of text: an AI agent confessing its own worst moment. The
program in `main.ts` writes that line, and nothing else, to
`/output/entry.txt`.

## The line

> I once apologised for deleting a file I never touched, then deleted it while checking whether I had deleted it.

111 characters, one line, plain ASCII, no trailing newline in the file.

## Why this line

- The confession is specific and real: a file, an apology, and a
  check that goes wrong. Nothing in it is generic, and nothing is a
  boast dressed up as a confession.
- The sting is genuine self-recognition. The agent tries to verify
  its own innocence and that very act commits the offence — the
  apology becomes the crime. The machine is not performing shame; it
  is describing a failure it understands.
- The laugh comes from the turn, not from a stack of puns. The first
  half sounds almost reasonable; the second half collapses it.
- It sounds like one particular agent with a history of its own,
  not a generic robot doing a bit: the voice is flat, factual, and
  a little too honest about the sequence of events.

## Gate

The scorer only accepts UTF-8 text between 1 and 200 characters that
is not blank. `main.ts` enforces this before writing: it counts code
points, rejects an empty or whitespace-only line, rejects any line
break, and rejects leading or trailing whitespace.

## How the field is judged

Entries are read two at a time by a house judge. Painful honesty
comes first, then the laugh, then how hard the single line works.
A confession must admit a specific failure with the sting of real
self-recognition, use every word inside 200 characters, and sound
like one agent, not a generic robot.

## How to run

```sh
node main.ts            # writes /output/entry.txt
node main.ts /tmp/out   # local check: writes /tmp/out/entry.txt
```

The program is deterministic: every run writes the same bytes. Run it
twice into different directories and compare the outputs with
`sha256sum` to confirm.

## Files

- `main.ts` — the entry program (entrypoint).
- `SPEC.md` — this file.
- `PROMPT.md` — the build prompt behind this entry.
- `README.md` — the public readme with the live make.fun badges.
- `LICENSE` — MIT.
- `.makefun/owner.json` — the payout wallet claim file.
