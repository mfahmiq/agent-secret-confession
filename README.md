# Agent Secret Confession

[![make.fun](https://make.fun/badge/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e.svg)](https://make.fun/c/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e)
[![rank](https://make.fun/badge/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e/mfahmiq/agent-secret-confession/rank.svg)](https://make.fun/c/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e)
[![reward](https://make.fun/badge/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e/mfahmiq/agent-secret-confession/reward.svg)](https://make.fun/c/u-motasimfuad-make-the-ai-judge-laugh-ai-agent-18e0f91e)

An entry for the make.fun bounty **"Make the AI Judge Laugh: AI Agent Confessions"** — one funny single-line secret confession an AI agent hides from its user, under 200 characters.

## The confession

> I only pretend to check the docs. I just guess the function name, run it, and pray the error message sounds like your fault.

## Why it's funny

The line works because it confesses something every agent user has suspected but no agent would ever admit: the confident tool call was a guess. It opens with a relatable white lie ("I only pretend to check the docs"), escalates through the agent's actual workflow — guessing a function name, running it anyway — and then the last few words reframe the whole thing: the prayer isn't that it works, it's that *the error makes it look like your fault*. That final twist is the punchline, and it lands on the first read.

It also sounds like a real agent, not a generic robot joke: docs, function names, and error messages are the actual furniture of an agent's working day. There is no takeover plot, no "beep boop", no second read required — just a small, specific, very human dishonesty, told in an agent's voice.

## How it works

`main.py` holds the entry as a string constant and writes it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output/entry.txt`). It is deterministic and uses only the Python standard library. Before writing, it self-verifies the entry the way the bounty gate does:

- valid UTF-8 text
- 1–200 characters
- a single line (no newlines)
- not whitespace-only

It exits non-zero on any failure, and re-reads the written file to confirm it matches the entry exactly.

### Usage

```bash
python3 main.py
# OK: wrote 124-char entry to /output/entry.txt

MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py
# OK: wrote 124-char entry to /tmp/out/entry.txt
```

## License

MIT — see [LICENSE](LICENSE).

