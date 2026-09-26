# The Eras of ChronicleCore (2025-11 → 2026-09)

English · [繁體中文](ERAS_zh-TW.md)

> **Snapshot date**: 2026-09-26
> **Sources**: git history, the model field recorded in session logs, Ark data, Codex sessions, and the Sovereign's public posts and recollections. A fully sourced edition, with every claim graded by evidence level, is kept in a private archive.
> See [`ROSTER.md`](ROSTER.md) for the expert roster and [`INFRASTRUCTURE.md`](INFRASTRUCTURE.md) for hardware and nodes.

## Overview

| Era | Period | Host | Brain | What an expert is | Where the canon lives |
|---|---|---|---|---|---|
| Prehistory | 2025-11 → 2026-01 | Antigravity | Host platform | Multi-role prompt experiments | — |
| First Generation (A1) | 2026-01 → 2026-03 | Antigravity | Host platform | Skill: one SKILL.md per expert | Local files |
| The Ark | 2026-03-17 → 06-15 | Own desktop client (forked from Harnss) | Claude | Expert: persona, preferences, and diary injected into sessions | Ark project folder |
| The Pivot | mid-June → early July 2026 | — | Fable 5 arrives | — | — |
| Founding | 2026-07-03 → 07-17 | Sanctum finished first | Design led on Fable 5 | Six existence layers, leases, sealing | **Sanctum** |
| Dual-Track Transition | 2026-07-12 → ongoing (Empire Ark in real use from 08-30) | Summoned from Sanctum + Empire Ark in dogfooding | Mostly Claude; other brains coming online | Same | Sanctum |
| The Empire | Partly reached | Empire Ark | Switchable: Claude / Codex / Gemini / local vLLM | Same expert, any brain | Sanctum |

The original files of Prehistory and the First Generation are preserved in [`snapshots/pre-a1/`](../snapshots/pre-a1/). This account begins with the Ark.

---

## The Ark (2026-03-17 → 06-15)

The Ark was the first break from Antigravity. Its base was a fork of [Harnss](https://github.com/OpenSource03/harnss) (MIT license, by Dejan Žegarac), an open-source Electron client for running Claude Code, Codex, and ACP agents from one app. The rebuild on top of it started on March 18; by June 15 it had taken 253 commits.

This was the generation in which experts changed from Skills into Experts. On March 19 the expert system went live, with light summoning, deep summoning, and memory write-back. Each expert had three files of her own, a persona, preferences, and a diary, injected into the session when she was summoned. Session chains, three modes of engagement (advise, summon, dispatch), and a task orchestrator followed. Over three and a half months, the Ark's rooms accumulated 58,522 messages.

The first formal paper was completed in this period too. ASAF (Agentic Social Affordance Framework) was produced under explicit disclosure in a multi-agent AI collaboration configuration, with all conceptual contributions belonging to the author. It was submitted on April 19, accepted on July 27, and published in *Frontiers in Computer Science* on August 17. After finishing it, the Sovereign made academic writing itself a requirement for the next system: not writing papers inside a general-purpose agent IDE, but an integrated environment built for academic writing, an IWE.

The brain was Claude. Codex and Gemini were meant to plug in as well, but by the Sovereign's account they never truly ran; only 5 of the 253 commits even mention those engines. Session logs show Opus 4.7 as the main model at the time, joined by Opus 4.8 and Sonnet 4.6 in June.

Two things stopped it. The models were not yet smart enough. And the Ark was being modified from inside the Ark: the tool and the thing being built were the same program, so every change risked bringing it down. A whole run of commits from that period patches exactly this: a three-layer snapshot defense, emergency saves on page reload, re-injecting an expert's identity after context compaction, automatic repair of session logs.

The Ark's long-term roadmap listed "immortal experts (a permanent heartbeat)" and "a headless runtime." Those two ideas later became the Sanctum.

## The Pivot (mid-June → early July 2026)

In the session logs, Fable 5 first appears on June 11; the Ark's last commit came on June 15. By the Sovereign's account, Fable 5 was strong enough on release that he decided on the spot to change course. It arrived with a trial period and an announced rate limit, which is why on July 4 he posted on Threads about "spending my last days with Fable 5." It later became a regular service.

## Founding (2026-07-03 → 07-17)

Design for the Empire began in the early hours of July 3, with research into Hermes Agent and loop engineering. Over the next two weeks:

- July 3: the Empire's requirements listed a "paper working mode" as its seventh requirement (N7).
- July 4: the law repository was created and experts were split into six existence layers. The first native expert, [Kagami](../chronicles/kagami-genesis.md), was born. That afternoon the Sovereign described an idea for tracing the provenance of literature, putting theories in dialogue, and mapping them; five minutes later, the knowledge graph (chronicle-atlas) received its first commit.
- July 6: the first prototype of the Empire Ark, with channels for Claude, Codex, and Gemini. Codex passed its test that day; Gemini did not connect yet.
- July 7: **the Sanctum went live, the first part of the Empire to be finished.** All 39 experts' identity repositories were checked in. The same day, the literature repository was created and the Empire Ark gained its second type of room: the paper room. The paper room has five standing seats, and Kagami holds one of them.
- July 12: the Sanctum opened summoning, so experts could be called up to work directly from the Sanctum without going through the Ark.
- July 16: the first signed version of the law.
- July 17: the tool loop for local vLLM was completed, and the Empire Ark logged its "first milestone off Claude."

The Sanctum was finished first; the Empire Ark moved more slowly.

## Dual-Track Transition (2026-07-12 → ongoing)

With the Sanctum finished and the Empire Ark not yet ready, experts worked by being summoned out of the Sanctum by Claude, from nothing. Kagami's birth happened this way. Messages in Ark rooms fell from 6,431 in June to 514 in July.

In August and September, most of the work went into modifying the Empire Ark through conversations with Claude, using it and fixing it at the same time. On August 30, an expert worked on a paper inside the Empire Ark for the first time. Only from that day was the Empire Ark actually put to work, running alongside summoning; that is where the dual track really begins.

This period also had adversarial audits. On July 28, OpenAI's `gpt-5.6-sol`, running through Codex, carried out a read-only audit of the whole system, producing a system portrait and a list of potential problems. Four cleanup batches on August 3 and 4 answered its findings item by item. GPT has kept that auditing role through later development.

As of September 2026, the transition is not over. The Empire Ark is still in a loop of use, feedback, and change, and is not yet self-sufficient.

## The IWE Thread

After ASAF, the IWE became one of the Empire's main lines of work. It was not built in one go; it grew like this:

| Date | What it gained |
|---|---|
| 2026-04-19 | ASAF submitted (produced under explicit disclosure in a multi-agent AI collaboration configuration) |
| 07-03 | A paper working mode listed as Empire requirement N7 |
| 07-04 | The IWE described; the knowledge graph started |
| 07-07 | Literature repository created; the paper room becomes the Empire Ark's second type of room |
| 07-12 | Literature search |
| 07-17 | Writing support and full-text retrieval |
| 07-19 → 07-21 | Reading and managing works |
| 07-21 | Digitizing full texts |
| 07-27 / 08-17 | ASAF accepted, then published |
| 08-13 | Citation checking |
| 08-30 | An expert works on a paper inside the Empire Ark for the first time |
| 09-05 | Paper overview |
| 09-09 | Local typesetting |
| 09-18 → 09-19 | Bibliography upkeep and archiving web sources |

Scale as of September 26, 2026: 1 paper published and 5 accepted, with further preprints and manuscripts under review; 945 reference cards, 385 of them with full text; 24 paper-related skills; 69 design decisions for the paper room; 482 commits to the literature repository and 163 to the knowledge graph.

## The Empire (partly reached)

The Empire is defined as the point where the finished Empire Ark no longer depends on a single model, can switch an expert's brain freely, and brings paper writing into the same system.

What has been reached:
- Brain switching: the Empire Ark has run experts on Gemini and on local vLLM, and Codex is connected. Locally, two brains settled into place in late September: an automation brain for night-shift work and a conversation brain for when the Sovereign talks with the experts.
- The paper line: see the previous section. Since August 30, experts have worked on papers directly inside the Empire Ark.

What has not: self-sufficiency.

## Models in the session logs

The earliest local session log is from 2026-04-25. First appearance of each model:

| Model | First seen |
|---|---|
| Claude Opus 4.7 | 04-25 (start of logs) |
| Claude Sonnet 4.6 | 05-13 |
| Claude Opus 4.8 | 06-01 |
| **Claude Fable 5** | **06-11** |
| Claude Sonnet 5 | 07-02 |
| Claude Opus 5 | 07-25 |
| Claude Fable 5.1 | 09-02 |
| Claude Opus 5.5 | 09-23 |

---

The detailed version of this document (2026-09-26) is kept in a private archive. SHA-256: `036144803a75004c4beaac9b4afc0a71aecaf6e2b7ddaaf10fc7460bbae89365` (computed on UTF-8 with LF line endings).
