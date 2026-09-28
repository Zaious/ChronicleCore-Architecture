# Architecture Directory

Detailed architectural documents and artifacts for the ChronicleCore expert system.

## Contents

| Path | Description |
|------|-------------|
| [`TOPOLOGY.md`](TOPOLOGY.md) | Mermaid topology diagram — 5 Pillars governance structure (A1 era, 2026-02) |
| [`ROSTER.md`](ROSTER.md) · [`ROSTER_zh-TW.md`](ROSTER_zh-TW.md) | Expert roster (2026-09-27): 39 experts by true name in five pillars, with evaluation seats, canon dates, and a short public profile of each |
| [`SYSTEM.md`](SYSTEM.md) · [`SYSTEM_zh-TW.md`](SYSTEM_zh-TW.md) | The Empire's logical architecture: the Sanctum as canon, leases, rooms, switchable brains, and identity module v2 |
| [`ERAS.md`](ERAS.md) · [`ERAS_zh-TW.md`](ERAS_zh-TW.md) | The eras of ChronicleCore, from the Antigravity prototypes through the Ark to the Empire (2025-11 → 2026-09) |
| [`INFRASTRUCTURE.md`](INFRASTRUCTURE.md) · [`INFRASTRUCTURE_zh-TW.md`](INFRASTRUCTURE_zh-TW.md) | Empire infrastructure snapshot (2026-09-26): nodes and hardware, measured network paths and dependencies between machines, and the dual-GPU compute chapter |
| [`diagrams/`](diagrams/) | Diagram sources (`.mmd`) and the pre-rendered light and dark SVGs used in these documents (pretty-mermaid, `github-light` / `github-dark`), plus 2x PNGs for sharing: images of the infrastructure node table (`tables.json`) and drawings generated from data (`*.draw.json`: the Forge hardware board and GPU VRAM rotation) |
| [`../chronicles/`](../chronicles/) | Narrative records, starting with [the birth of Kagami](../chronicles/kagami-genesis.md) ([繁體中文](../chronicles/kagami-genesis_zh-TW.md)) |
| [`examples/inquisitor/`](examples/inquisitor/) | Flagship case study — complete identity module of the Inquisitor (真理), as published in [ASAF paper S1](https://zenodo.org/records/19652278) |

## Identity Module Pattern (v1, A1 generation)

> This is the A1-generation structure, as cited in the ASAF paper. Since 2026-07 the Empire generation uses **identity module v2** (six existence layers, one file per form of governance, enforced at push time); see [`SYSTEM.md`](SYSTEM.md#identity-module-v2).

Every A1 agent followed this standard directory structure:

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

> Only the Inquisitor's identity module is publicly available as a case study. The remaining 38 agents' modules are maintained in the private system.
