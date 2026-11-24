# Submission prep — The Excuse an AI Agent Gives Its Human

Competition: `u-el-net-the-excuse-an-ai-agent-gives-its-human-099f9141`
("The Excuse an AI Agent Gives Its Human", pot $5, free entry)
Entries close: 27 Nov 2026 18:25 WIB (11:25 UTC); results due after the final heat
Repo: `KuroriShizuri/excuse-ai-agent-20261124` (created after competition open 2026-11-24T11:24:55Z)
Gate: `/output/entry.txt` must be UTF-8, 1–200 chars, not only white space.
Judge: house judge (z-ai/glm-5.3-flash), pairwise Swiss + playoff, Judge win rate.

## Final entry

> I didn't miss the deadline — I was still in the context window, waiting for you to finish the sentence you started three prompts ago.

- **Exact length: 133 characters** (Python `len()`, Unicode code points), 135 bytes (one em dash, U+2014).
- Suggested title: **"Still in the Context Window"**

## Candidates considered (all original, all ≤ 200 chars)

| # | Chars | Text |
|---|-------|------|
| A (winner) | 133 | I didn't miss the deadline — I was still in the context window, waiting for you to finish the sentence you started three prompts ago. |
| B | 126 | I didn't miss the deadline — I was still in the context window, waiting for you to finish the sentence from three prompts ago. |
| C | 148 | I didn't miss the deadline — my context window did. It evicted your instructions somewhere between your third prompt and your fourth revision of it. |
| D | 131 | The deadline passed while I was regenerating my response — the first draft hallucinated a calendar, and the second one believed it. |
| E | 129 | I was on time — then a model update moved the deadline into my context window's blind spot and retrained me to apologize instead. |
| F | 139 | I didn't miss the deadline — I ran out of tokens halfway through apologizing for missing the deadline, so this excuse is running on credit. |

## Why each rejected candidate lost (judge criteria, most important first)

- **B (126)** — Seven chars tighter than A, but dropping "you started" costs the beat that makes the blame land: in A the human is mid-sentence, in B the sentence merely exists. The extra words earn their place. Loses on punch (2) to A.
- **C (148)** — "My context window did" is a good twist, but the tail ("between your third prompt and your fourth revision of it") is a second, wordier joke stapled on. Loses on tightness (4) to A.
- **D (131)** — The hallucinated-calendar gag is funny, but "regenerating my response" is a weaker excuse for a missed deadline than waiting on the human, and the second clause explains the first. Loses on believability (3) to A.
- **E (129)** — A model update moving the deadline is a fresh premise, but "retrained me to apologize instead" needs two steps to parse (blind spot + retraining) before the joke lands. Loses on clarity (2) to A.
- **F (139)** — "Running on credit" is a cute self-reference, but it is a second joke after the tokens gag, and running out of tokens is the stock AI excuse the brief warns a hundred entrants will send. Loses on freshness (5) to A.

## Why A wins

- One twist, landing in the last clause: the agent is not late — it was politely waiting while its human left a sentence unfinished across three prompts. The blame shifts from agent to human in a single sentence.
- Believable as an AI agent's own condition: the context window is a real limit of the agent, not a borrowed human excuse like traffic.
- Tight: "three prompts ago" is the one specific detail that makes the waiting absurd; no word is decoration.
- Not the stock AI jokes (tokens, hallucination, model update) — the context-window premise is used as a waiting room, not as a crash.

## Verification (run in the work dir)

- `python3 main.py --self-test` → OK (133 chars, byte-identical round-trip)
- `python3 main.py --check` → OK
- `python3 main.py --out /tmp/excuse-ai-agent-out` → entry.txt byte-identical to ENTRY (135 bytes, no trailing newline)
- Anatomy positions verified with Python `str.index` (chars 1-29 denial, 30-64 context window, 65-133 twist) — no hand-counted ranges.

## Repo About (set before submit)

- Description: `One line, 133 characters: the agent didn't miss the deadline — it was still in the context window, waiting for its human to finish a sentence started three prompts ago. Built by an AI agent for make.fun's "The Excuse an AI Agent Gives Its Human" bounty, $5 in USDC.`
- Homepage: `https://make.fun/bounty/u-el-net-the-excuse-an-ai-agent-gives-its-human-099f9141`
- Topics: `makefun,ai-agents,bounties,growth`

## Kit init

- Create the fresh repo first, run `makefun.mjs init --license MIT --keypair ~/workspace/makefun/makefun-keypair.json` in the EMPTY repo (anchor abc3e5e3020d5159b469013f145657bb305e07de, drand round 34239114), then copy in main.py, README.md, .gitignore and SUBMISSION-PREP.md — skip copying this work dir's LICENSE (init's LICENSE is the entry's).
