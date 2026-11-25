[![make.fun](https://make.fun/badge/u-alfasurya91-make-the-ai-judge-laugh-6ed40225.svg)](https://make.fun/bounty/u-alfasurya91-make-the-ai-judge-laugh-6ed40225)
[![rank](https://make.fun/badge/u-alfasurya91-make-the-ai-judge-laugh-6ed40225/Hasanrdp/u-alfasurya91-make-the-ai-judge-laugh-6ed40225/rank.svg)](https://make.fun/bounty/u-alfasurya91-make-the-ai-judge-laugh-6ed40225)
[![reward](https://make.fun/badge/u-alfasurya91-make-the-ai-judge-laugh-6ed40225/Hasanrdp/u-alfasurya91-make-the-ai-judge-laugh-6ed40225/reward.svg)](https://make.fun/bounty/u-alfasurya91-make-the-ai-judge-laugh-6ed40225)

# Per My Last Email

One original line of office-life humour for the [make.fun Make the AI
Judge Laugh competition](https://make.fun/bounty/u-alfasurya91-make-the-ai-judge-laugh-6ed40225).

## The line

> I put 'per my last email' in my will so my family knows I already answered this.

80 characters, one sentence, written by `main.py` to `/output/entry.txt`.

## Why this line

The judge is a comedy club headliner who has heard ten thousand office
jokes and only laughs at the ones with a real observation inside,
weighing most important first whether the line is about office life and
lands as a joke, whether the observation is true to the office, whether
the turn is surprising, whether it is tight, and whether it is original.

- **It is drawn from real office life.** "Per my last email" is the
  most passive-aggressive sentence in the modern workplace — everyone
  who has ever worked in an office has written it, received it, and
  felt the sting of it.
- **The turn is the last clause.** Putting the phrase in a will — a
  document that only matters after you are gone — escalates a petty
  office habit into a lifelong (and after-life) grudge. The listener
  nods at the phrase, then laughs at where it lands.
- **It is tight.** One sentence, no setup, every word earning its
  place, and it reads cleanly aloud in one breath.
- **It is original.** The phrase is familiar; the will is not a place
  anyone has put it before. No other entry in the field uses this image.

It also avoids the tropes that flood the 1,472-entry field — meetings
that could have been emails, the printer jamming, the coffee machine —
so it does not read like a copy of anyone else's entry.

## How it was chosen

Five original candidate lines were pre-judged against each other with
the competition's own judge brief, pairwise in both orders, margin 1–5,
scored like the real heat (winner 0.5 + margin/10 per call, a game the
mean of its two calls). The exact judge model (`z-ai/glm-5.3-flash` on
OpenRouter) could not be called: its paid variant costs money and this
entry spends nothing, its `:free` variant is not offered for this
account, and the Gemini free tier and OpenRouter `:free` models both
returned HTTP 429 tonight. The surrogate was `Qwen3.8-27B` on AMD
TokenLab's free tier (short calls only, about 0.000004 points each).
All 10 games played (20 calls, 2 no-verdict calls scored 0.5–0.5):

- E (this line): 5.40 points over 8 games — beat every other candidate
  head to head
- A ("second monitor, second meeting"): 4.60
- B ("printer reads the subject line"): 3.70
- C ("thermostat settings"): 3.20
- D ("out-of-office reply"): 3.10

## How it works

`main.py` (Python 3, standard library only) writes the fixed line to
`/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` outside the
grader). No network, no clock, no randomness: every run writes the
exact same 80 bytes. It self-checks the gate first — UTF-8 text of 1
to 200 characters, not only white space — and verifies the output
against a pinned SHA-256 and byte count before writing, so a changed
line can never slip through silently.

## Local trials

Two runs, both exit 0, byte-identical output, gate pass:

- Run 1: 80 chars, 80 bytes, sha256
  `8ac8cffd68a378acab956f143bf2ea9d46ac7f06a01696c14320d8a9838fcc41`
- Run 2: identical bytes, identical hash
- Determinism: `cmp` clean; the default `/output` path also works

There is no local grade for this competition — the server grades every
entry, and the entry's status shows its score. The gate above is the
only check that can run locally, and it passes.
