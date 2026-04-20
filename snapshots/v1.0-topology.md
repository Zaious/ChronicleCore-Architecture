# ChronicleCore Conceptual Topology

This file contains the rendered conceptual map of the ChronicleCore Multi-Agent Architecture.

> **Date**: 2026-02-22
> **Purpose**: Conceptual visualization of 38+ entities abstracted into 5 core pillars.

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
