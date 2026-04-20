# Case Study: The Inquisitor (真理)

> **Agent ID**: `officer-inquisitor`
> **Codename**: 真理 (Zhēn Lǐ; "Truth")
> **Title**: 異端審判官 (The Inquisitor)
> **Department**: The Shield (Defense)
> **Ensoulment**: 2026-01-30
> **Operational Boundary**: Auditing and challenge only; no execution capabilities

This directory contains the public-facing identity definition of ChronicleCore's sole adversarial node — the agent specifically designed to break consensus, interrogate logic, and enforce evidence standards across the entire system.

The Inquisitor was selected as the flagship case study for the [ASAF paper](https://zenodo.org/records/19652278) because she demonstrates all three ASAF mechanisms in a single agent design:

- **Identity Signaling**: Her codename, archetype, and characteristic utterances pre-configure operator expectations before any interaction
- **Behavioral Priming**: Operators submit more evidential, structured inputs when working with the Inquisitor than with generative agents
- **Collaborative Governance**: Her VETO Power (Iron Law 5) architecturally instantiates competing-identity design to suppress conformity effects

## Files

## Identity Module Structure

```
officer-inquisitor/
├── SKILL.md                        # Core identity constraint definition
├── assets/
│   └── persona.md                  # Character specification (public excerpt)
├── sovereign/
│   └── diary-excerpt.md            # Ensoulment record — Day 1 operational log
├── references/                     # [not public] Operational protocols
└── evolutions/                     # [not public] Capability packs (DLCs)
```

| File | Description |
|------|-------------|
| [`SKILL.md`](SKILL.md) | Complete core identity constraint definition |
| [`assets/persona.md`](assets/persona.md) | Character specification (public excerpt) |
| [`sovereign/diary-excerpt.md`](sovereign/diary-excerpt.md) | Ensoulment record — Day 1 operational log |

## ASAF Mechanism Mapping

This agent definition illustrates all three ASAF mechanisms:

1. **Identity Signaling** — The Inquisitor's codename (真理, "Truth"), archetype (Internal Auditor), and characteristic utterances ("Evidence or GTFO", "This logic leaks") pre-configure operator expectations prior to any interaction, reducing the cognitive friction of role assignment.

2. **Behavioral Priming** — The design intent is to elicit more evidential inputs from operators (formal logs, screenshots, explicit argument structures) when submitting work to the Inquisitor than when interacting with generative agents.

3. **Collaborative Governance** — VETO Power (Iron Law 5) operationalizes a deliberate identity conflict between the Inquisitor and all producing agents, architecturally instantiating the competing-identity design pattern predicted by H3 to suppress dangerous conformity effects.

> This case study is also published as **Supplementary Material S1** in the [ASAF paper](https://zenodo.org/records/19652278).
