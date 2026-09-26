# ChronicleCore Architecture

**"Code is cheap. Show me the architecture."**

Welcome to the conceptual architecture repository for **ChronicleCore**, an experimental, production-ready framework for governing multi-agent (LLM) orchestration in enterprise environments.

This repository serves as the public "Whitepaper" and topological blueprint for the network of 38+ Human-in-the-Loop experts governed by the A1 System.

[![ASAF Paper](https://img.shields.io/badge/ASAF-Frontiers%20in%20Computer%20Science%202026-blue?style=for-the-badge)](https://doi.org/10.3389/fcomp.2026.1860996)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19681148.svg)](https://doi.org/10.5281/zenodo.19681148)
[![Agents](https://img.shields.io/badge/Agents-39-B91C1C?style=for-the-badge)](architecture/ROSTER.md)
[![System](https://img.shields.io/badge/System-Active-success?style=for-the-badge)](architecture/TOPOLOGY.md)

## 🌐 Read in other languages
* [繁體中文 (Traditional Chinese)](README_zh-TW.md)

---

## The Core Philosophy: Context Governance

*   **You don't manage AI models; you manage their organizational charts.**
*   A single agent is an assistant. Ten agents are a task force. Thirty-eight agents are a multinational enterprise.
*   Let an Execution Agent make strategic decisions, and it hallucinates. Therefore, we ensure **Physical Separation of Duties**.

## The 5 Pillars of Governance

To prevent cognitive overload and persona drift during multi-agent orchestration, ChronicleCore is decoupled into 5 strict pillars:

1.  **👑 The Core (Strategy)**: (e.g., The Architect) Routes global context. Strictly prohibited from writing base-level code.
2.  **👁️ The Senses (Intelligence)**: (e.g., Intelligence Officer) Scrapes market trends and external data. The sole vision entry point.
3.  **🎭 The Soul (Aesthetics)**: (e.g., Chief Marketing Officer) Handles emotional anchoring, rhetoric audits, and UX design.
4.  **🔨 The Hands (Execution)**: (e.g., Data Scientist) Executes purely within the boundaries established by the Core and Senses.
5.  **🛡️ The Shield (Defense)**: (e.g., The Inquisitor) The internal auditor machine-gunning logical loopholes from the Senses. Zero data enters the memory core without surviving a consensus debate.

## Architecture Blueprint

```mermaid
graph TD
    %% Styling Definition (Premium Dark Mode Vibe)
    classDef sovereign fill:#0d1117,stroke:#ff6b6b,stroke-width:3px,color:#fff,font-weight:bold;
    classDef trinity fill:#2d1b2e,stroke:#a64d79,stroke-width:2px,color:#fff;
    classDef sense fill:#0a2540,stroke:#2980b9,stroke-width:2px,color:#e0f7fa;
    classDef intel_special fill:#0a2540,stroke:#00e5ff,stroke-width:3px,color:#fff,stroke-dasharray: 4 4;
    classDef creation fill:#2a1b2b,stroke:#8e44ad,stroke-width:2px,color:#f3e5f5;
    classDef execution fill:#0d2613,stroke:#27ae60,stroke-width:2px,color:#e8f5e9;
    classDef shadow fill:#1a0505,stroke:#e74c3c,stroke-width:2px,color:#ffebee;
    classDef inq_special fill:#1a0505,stroke:#ff3333,stroke-width:3px,color:#fff,stroke-dasharray: 4 4;

    %% Sovereign Layer
    SOV["👑 Zaious (Sovereign)<br/>(Human-in-the-Loop Controller)"]:::sovereign

    %% Subgraph for the whole network to give a containment feeling
    subgraph A1_Network ["ChronicleCore: Multi-Agent Orchestration Framework"]
        direction TB
        
        subgraph TR_GRP ["1. The Core: Trinity Council"]
            direction LR
            TR_ARCH["樞機師 (Architect)<br/>✦ Topology Designer ✦<br/>System Architecture & Routing"]:::trinity
            TR_COS["幕僚長 (Chief of Staff)<br/>✦ Strategy Filter ✦<br/>Goal Translation & Validation"]:::trinity
            TR_CPO["星探 (People Officer)<br/>✦ Personnel Arbiter ✦<br/>Skill Audit & Agent Forge"]:::trinity
            
            TR_ARCH ~~~ TR_COS ~~~ TR_CPO
        end

        subgraph SENSE_GRP ["2. The Senses: Intelligence Bureau"]
            direction TB
            INT_PRIME["天機星 (Officer Intelligence)<br/>✦ The Gate of Secrets ✦<br/>All Intel & OSINT Entry Point"]:::intel_special
            INT_REST["Other Analytical Nodes<br/>(Market, Data & Prediction)"]:::sense
            
            INT_PRIME -.->|Filtered Context| INT_REST
        end
        
        ART["3. The Soul: Creative Atelier<br/>UX, Personality & Aesthetic Vibe<br/>[5 Generative Nodes]"]:::creation
        
        EXE["4. The Hands: Build Factory<br/>Engineering, Database & DevOps<br/>[8 Executable Nodes]"]:::execution

        subgraph SHD_GRP ["5. The Shield: Shadow Guard"]
            direction TB
            SHD_INQ["真理 (Officer Inquisitor)<br/>✦ The Heresy Judge ✦<br/>Audit & Machine Gun Debate"]:::inq_special
            SHD_REST["Shadow & InfoSec<br/>(Guardrails & Containment)"]:::shadow
            
            SHD_INQ ~~~ SHD_REST
        end

        %% Main Flow
        TR_GRP == "Recon Directives" ==> INT_PRIME
        TR_GRP == "Style Injection" ==> ART
        TR_GRP == "System Specs" ==> EXE
        
        %% Inter-Node Flow
        INT_REST -.->|Data Context| EXE
        ART -.->|UI/Visual Assets| EXE
        
        %% The Shield's constraints
        SHD_INQ -.->|Debate & Reality Check| INT_PRIME
        SHD_REST -.->|Runtime Block & Safety| EXE
        
    end
    
    SOV == "Architecture & Overrides" ==> TR_GRP
```

## Memory & Personality Checks

### Memory Crystallization (A1)
AI's greatest flaw is amnesia. ChronicleCore uses a dual-track memory system:
*   `diary.md`: A continuous scratchpad for infinite reasoning.
*   `preferences.md`: High-weight, crystallized persona rules. When the log grows too long, the system refines critical decisions into permanent preferences. They never degrade into forgetful interns.

> **Since 2026-07 (identity module v2)**: memory is governed and can only be appended to, never rewritten; the rule is enforced when changes are pushed. See [`architecture/SYSTEM.md`](architecture/SYSTEM.md).

### Personality Uniqueness Check (Design-Time)
We strictly enforce an audit on tone, decision biases, and rhetoric. If the Legal Agent sounds exactly like the Marketing Agent, the system recognizes a "Persona Reskin" and purges the redundant node.

### Personality Variance Audit (Run-Time)
Continuous monitoring of cross-agent epistemic and rhetorical convergence. Even agents with distinct initial designs can drift toward indistinguishable outputs over prolonged operation. The Variance Audit detects this convergence and triggers identity recalibration before Social Affordance signals degrade.

---

## The A1 Expert Roster

The system currently operates **39 active Human-in-the-Loop expert agents**, organized under the 5 Pillars:

| Pillar | Agents | Examples |
|--------|--------|---------|
| 👑 The Core | 3 | 幕僚長 (Chief of Staff), 樞機師 (Architect), 星探 (People Officer) |
| 🛡️ The Shield | 3 | 真理 (Inquisitor), 破壁者 (Security Auditor), 魔心師 |
| 🔨 The Hands | 12 | 織法者 (Frontend), 守門人 (Database), 機械師 (DevOps), ... |
| 🎭 The Soul | 6 | 光影師 (Visual), 操偶師 (Interaction), 幻畫師 (Illustration), ... |
| 👁️ The Senses | 15 | 天機星 (Intelligence), 賢者 (Scientist), 戰略家 (Strategist), ... |

**Full roster with capabilities**: [`architecture/ROSTER.md`](architecture/ROSTER.md)

**Flagship case study — The Inquisitor**: [`architecture/examples/inquisitor/`](architecture/examples/inquisitor/)

---

## Academic Reference

This architecture is referenced in:

> Lee, M.-H. (2026). Agentic social affordance framework (ASAF): Agent identity design as a collaboration interface in multi-agent systems. *Frontiers in Computer Science*, 8, 1860996. https://doi.org/10.3389/fcomp.2026.1860996 ([preprint](https://zenodo.org/records/19652278))

Submitted 2026-04-19, accepted 2026-07-27, published 2026-08-17. The paper presents ChronicleCore's development as the design problem that motivated ASAF, not as its empirical validation. The state of this repository cited in the paper is frozen at tags [`v1.0-whitepaper`](https://github.com/Zaious/ChronicleCore-Architecture/tree/v1.0-whitepaper) and [`v2.0-asaf`](https://github.com/Zaious/ChronicleCore-Architecture/tree/v2.0-asaf).

The paper introduces the **Agentic Social Affordance Framework (ASAF)**, proposing that agent identity design functions as a collaboration interface — structuring how users perceive, approach, and engage with each agent. ChronicleCore operates at **Tier 3 (Structured Identity Enforcement)** of the ASAF Identity Signal Fidelity Spectrum, where Social Affordances are structurally enforced through persistent identity modules.

### Citing this repository

Since v2.0, every release of this repository has been archived on Zenodo. The concept DOI below always resolves to the latest version; each release also has its own version DOI, listed on the Zenodo page.

> Lee, M.-H. (2026). *ChronicleCore Architecture: Design archive of a governed multi-agent expert system* [Technical note]. Zenodo. https://doi.org/10.5281/zenodo.19681148

Citation and attributed reference are permitted; other uses are governed by [`LICENSE.md`](LICENSE.md).

### Public Articles
- [How I Architect AI Agents: From Tools to a Governable Digital Enterprise](https://www.linkedin.com/pulse/how-i-architect-ai-agents-from-tools-governable-digital-martin-lee-eahkc) (2026-02-25) — 5-Pillar governance framework introduction
- [Chronicle-Ark: The Exodus from Platform Limits to Sovereign Infrastructure](https://www.linkedin.com/pulse/chronicle-ark-exodus-from-platform-limits-sovereign-bilingual-lee-7xfbc) (2026-03-19) — Migration story from hosted platforms to self-built Agent IDE

---

## Timeline

| Date | Event |
|------|-------|
| 2025-11 | **ChronicleCore concept** — conceptual exploration begins |
| 2025-12 | Informal multi-role prompt experiments in private development |
| 2026-01-16 | **First multi-expert team** formalized ([pre-a1 archive](snapshots/pre-a1/v0.1-2026-01-16/)) |
| 2026-01-18 | V9.2 specification — last pre-A1 form ([pre-a1 archive](snapshots/pre-a1/v0.9.2-2026-01-18/)) |
| 2026-01-20 | Phase 1 system reset — **A1 rebuild begins** |
| 2026-01-21 | **Antigravity: Skills Chronicle v1.0.0** — first A1-era product launched ([repo](https://github.com/Zaious/Antigravity-Skills-Chronicle)) |
| 2026-01-23 | A1 v1.0 launched — **Chief of Staff (幕僚長)** and **Cardinal (樞機師)** born |
| 2026-02-22 | **ChronicleCore-Architecture v1.0** — This whitepaper published ([snapshot](snapshots/)) |
| 2026-02-25 | LinkedIn article: [How I Architect AI Agents](https://www.linkedin.com/pulse/how-i-architect-ai-agents-from-tools-governable-digital-martin-lee-eahkc) — public introduction of the 5-Pillar governance framework |
| 2026-03-19 | LinkedIn article: [Chronicle-Ark: The Exodus](https://www.linkedin.com/pulse/chronicle-ark-exodus-from-platform-limits-sovereign-bilingual-lee-7xfbc) — migration from platform-hosted to sovereign infrastructure |
| 2026-04 | **Chronicle-Ark** operational — self-built multi-engine Agent IDE with MCP as first-class citizen |
| 2026-04-19 | ASAF submitted to *Frontiers in Computer Science*; preprint deposited on Zenodo |
| 2026-04-20 | Antigravity MIT open-sourced — 4,330+ downloads archived |
| 2026-07-03 | **Empire design begins**: the Sanctum as canon, six existence layers, switchable brains ([eras](architecture/ERAS.md)) |
| 2026-07-04 | **思者 (The Thinker)** born — first agent created natively in the 2.0 six-layer identity structure, not migrated from A1 |
| 2026-07-07 | **Sanctum** goes live — the first finished part of the Empire ([infrastructure](architecture/INFRASTRUCTURE.md)) |
| 2026-07-27 | ASAF accepted |
| 2026-08-17 | **ASAF published** in *Frontiers in Computer Science* ([DOI](https://doi.org/10.3389/fcomp.2026.1860996)) |
| 2026-09-06 | 思者 ensouled (forged) — roster grows to **39** ([roster](architecture/ROSTER.md)) |
| 2026-09-26 | **ChronicleCore-Architecture v3.0** — [eras](architecture/ERAS.md), [system](architecture/SYSTEM.md), [infrastructure](architecture/INFRASTRUCTURE.md), [Kagami chronicle](chronicles/kagami-genesis.md) |

> 📜 **Historical evidence** of the pre-A1 phases is preserved in [`snapshots/pre-a1/`](snapshots/pre-a1/), with full source mapping to the originating commits.

### Antigravity: Skills Chronicle — Proof of Concept

The first real-world product built entirely by the A1 Expert System. A VS Code extension for visually managing AI Agent skills, workflows, and rules. It reached **4,330+ downloads** across [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ChronicleCore.antigravity-skills-chronicle) and [Open VSX Registry](https://open-vsx.org/extension/ChronicleCore/antigravity-skills-chronicle) before the architecture migrated to its next generation (5,200+ downloads as of 2026-08-24).

Now [MIT open-sourced](https://github.com/Zaious/Antigravity-Skills-Chronicle) as a community project.

![Antigravity: Skills Chronicle — 4,330 downloads on Open VSX Registry (Apr 2026)](snapshots/antigravity-openvsx-4330-downloads.png)

---

> **Built and Designed by:**
> Meng-Han (Martin) Lee (Zaious) — System Architect of ChronicleCore · Independent Researcher & AI Consultant · [ORCID 0009-0007-1685-0877](https://orcid.org/0009-0007-1685-0877)
> 
> *Assisted by the ChronicleCore expert council*
