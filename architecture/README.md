# Architecture Directory

Detailed architectural documents and artifacts for the ChronicleCore A1 Expert System.

## Contents

| Path | Description |
|------|-------------|
| [`TOPOLOGY.md`](TOPOLOGY.md) | Mermaid topology diagram — 5 Pillars governance structure |
| [`ROSTER.md`](ROSTER.md) | Full 38-agent roster with codenames, titles, ensoulment dates, and capabilities |
| [`examples/inquisitor/`](examples/inquisitor/) | Flagship case study — complete identity module of the Inquisitor (真理), the system's sole adversarial node |

## Identity Module Pattern

Every A1 agent follows this standard directory structure:

```
<agent-id>/
├── SKILL.md                    # Core identity constraint definition (required entrypoint)
├── assets/
│   └── persona.md              # Extended character and speaking style specifications
├── sovereign/
│   ├── diary.md                # Longitudinal operational log
│   ├── preferences.md          # Crystallized persona rules (high-weight)
│   └── DIRECTIVES.md           # Standing orders from the Sovereign
├── references/                 # Operational protocols and review standards
└── evolutions/                 # Modular capability packs (DLCs)
```

This pattern extends the `SKILL.md` architecture (Anthropic, 2025) into a persistent, multi-layer identity framework. The separation between `SKILL.md` (identity-defining constraints) and `sovereign/diary.md` (transient reasoning logs) is the structural implementation of **Memory Crystallization** — ensuring that accumulated task-specific reasoning does not erode the agent's core social identity over time.

> Only the Inquisitor's identity module is publicly available as a case study. The remaining 37 agents' modules are maintained in the private system.
