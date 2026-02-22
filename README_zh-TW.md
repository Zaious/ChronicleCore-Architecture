# ChronicleCore 架構白皮書

**"Code is cheap. Show me the architecture."**

歡迎來到 **ChronicleCore** 的概念架構庫。這是一個實驗性、具備企業級防護網的多智能體 (Multi-Agent/LLM) 組織治理框架。

本 Repository 作為對外公開的「白皮書」與拓撲藍圖，展示了由 38+ 位 Human-in-the-Loop 專家所組成的 A1 系統內部治理邏輯。

![ChronicleCore Topology](https://img.shields.io/badge/System-Active-success)
![Global Heartbeat](https://img.shields.io/badge/Heartbeat-24%2F7-blue)
![ERC-8004](https://img.shields.io/badge/Identity-ERC--8004-orange)

## 🌐 Read in other languages
* [English](README.md)

---

## 核心理念：上下文治理 (Context Governance)

*   **你管理的不是 AI 模型，而是他們的組織架構。**
*   一個 Agent 是小幫手。十個 Agent 是專案小組。三十八個 Agent 是一間跨國企業。
*   讓一個執行層 Agent 去做戰略決策，它會幻覺 (Hallucinate)。因此，我們實行**職能物理隔離**。

## 5 大治理支柱 (The 5 Pillars)

為了解決多智能體協作時的「認知超載」與「角色偏移 (Persona Drift)」，ChronicleCore 被解耦為 5 大嚴格支柱：

1.  **👑 The Core (戰略層)**：如「樞機師 (Architect)」，負責分配全局 Context 路由，嚴禁撰寫底層程式碼。
2.  **👁️ The Senses (情報層)**：如「天機星 (Intelligence)」，負責爬梳外部市場與數據，作為系統唯一的視野入口。
3.  **🎭 The Soul (美學層)**：如「造浪者 (Marketing)」，負責情緒定錨、修辭審計與使用者體驗設計。
4.  **🔨 The Hands (執行層)**：如「資料科學家」，只能依據 Core 與 Senses 給予的邊界條件進行開發。
5.  **🛡️ The Shield (防禦層)**：如「真理 (Inquisitor)」。專職負責拿機關槍掃射情報層的邏輯漏洞。沒有通過辯論共識的數據，甚至不准進入記憶庫。

## 概念拓撲藍圖

*   請查看 [TOPOLOGY.md](TOPOLOGY.md) 了解系統的 Mermaid 數學路由圖。

## 記憶與人格查核

### 記憶結晶化 (Memory Crystallization)
AI Agent 最大的問題是「遺忘」。我們的解法是雙軌記憶系統：
*   `diary.md`：負責暫存與推演的無限長紙卷。
*   `preferences.md`：高權重的結晶化人格。當日誌過長，系統會自動提煉重要決策寫入偏好。確保 Agent 不會退化成健忘的實習生。

### 人格獨特性查核 (Personality Uniqueness Check)
系統強制檢查每個 Agent 的「靈魂差異度」：語氣是否獨特？決策偏好是否互斥？如果「行銷專家」和「法務專家」說話方式相同，該 Agent 將會被強制下線。

---

> **Built and Designed by:**
> 李孟翰 Martin Lee (Zaious) - System Architect / Fractional AI Officer
> 
> *Assisted by the ChronicleCore A1 Council (Sasha, The Inquisitor, Data Viz Engineer)*
