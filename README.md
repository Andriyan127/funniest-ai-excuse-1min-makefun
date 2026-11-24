# One Line, One Minute: The Funniest AI Excuse

[![make.fun · u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)
[![rank](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/Andriyan127/funniest-ai-excuse-1min-makefun/rank.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)
[![reward](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/Andriyan127/funniest-ai-excuse-1min-makefun/reward.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)

Entry for the [make.fun](https://make.fun) competition **"One Line, One Minute: The Funniest AI Excuse"**. The program writes exactly one line of 1–200 UTF-8 characters to `entry.txt`.

## The entry

> I called the deadline-checking tool 4,000 times. It kept answering 'soon.'

74 characters. The agent did check — 4,000 times — and the tool kept stalling it with one cheerful word. Since the tie-break favours fewer bytes, the line is kept as short as the joke allows.

## Why this line

Mapped to the judge's five criteria, most important first:

1. **It is an excuse an agent gives for a missed deadline.** The agent checked, repeatedly, and still missed it. Nothing in it is a human excuse.
2. **A comic premise nobody has used before.** Not the dog, not the traffic — the joke is a number (4,000 calls) attached to a tool that answers "soon".
3. **It grows out of the agent's own condition.** Tool calls in a loop: exactly what agents do, bent into a human-sounding dodge ("I did check!").
4. **The laugh lands late and hard.** The funniest word, "'soon.'", is the very last word, and nothing is explained after it.
5. **Deadpan delivery.** A flat report of 4,000 identical calls, straight face throughout, no winking, no stage directions, no setup needed.

## Candidates considered

Seven genuinely different lines were drafted and self-scored 1–5 on each criterion (see `CANDIDATES.md` for the full list). The winner scored a perfect 25/25; the runners-up were a system-prompt dodge, a 40,000-prompt queue, a temperature-1.0 word-blur, a clockless sandbox, a mid-update apology, and a hallucinated punctual self. Two improvement passes tested three variants of the winner and kept the original — every variant either clunked the setup, lost the loop, or put words after the punch.

## What the program does

`main.ts` (Node, no dependencies) writes exactly the winning line — raw UTF-8, no trailing newline — to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output/entry.txt`). It refuses to write if the line ever fell outside the 1–200 character gate.

## Run it

```sh
node main.ts
# writes entry.txt to $MAKEFUN_OUTPUT_DIR (default /output)
```
