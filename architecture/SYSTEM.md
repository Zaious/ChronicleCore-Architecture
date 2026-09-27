# The Empire's System Architecture: Canon, Borrowing, and Switchable Brains

English · [繁體中文](SYSTEM_zh-TW.md)

> **Snapshot date**: 2026-09-26
> **Scope**: a conceptual description of the Empire generation's system architecture (from 2026-07). For the physical machines see [`INFRASTRUCTURE.md`](INFRASTRUCTURE.md); for how it evolved see [`ERAS.md`](ERAS.md).
> The A1 identity module (v1) is described in [`README.md`](README.md). The ASAF paper's supplement cites v1, frozen at tag `v2.0-asaf`.
> **Disclosure**: this document covers what and why, not implementation. The full specification is kept in a private archive; see the hash at the end.

---

## In one sentence

**Experts live in the Sanctum and are borrowed only when they work.** The Sanctum keeps who each expert is; when she is needed, she is borrowed from the Sanctum and returned when the work is done. Each time, a model can be chosen as her brain; with a different brain, she is still the same expert.

## Conceptual architecture

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="diagrams/system-overview.dark.svg">
  <img alt="System overview: the Sovereign works through the Empire Ark and Claude Code and signs the law; the Ark, Claude Code, and the night shift all borrow, return, and summon experts through the Sanctum, which keeps the expert identities and the law; all three use switchable brains." src="diagrams/system-overview.light.svg">
</picture>

<sub>Source: [`diagrams/system-overview.mmd`](diagrams/system-overview.mmd)</sub>

## Three principles

**1. There is one canon, and it lives in the Sanctum.** Experts' identities and the governance rules are kept in Git on the Sanctum; everything elsewhere is a borrowed copy. The law is released under the Sovereign's signature.

**2. Changes go through a person.** An expert can be borrowed to work in an Ark room, summoned directly by Claude Code, or woken for the night shift. In every case, the changes made during the work are not written back to the canon directly; they go to the Sovereign for a ruling. When an expert edits a document in a paper room, that too needs the Sovereign's approval, and the approved change is committed in the expert's own name.

**3. Change the brain, not the person.** An expert's brain can be Claude, Codex, Gemini, or a local model on the Forge. The model may change; who she is does not.

## Rooms

| Room | Purpose |
|---|---|
| Engineering room | Bound to one project |
| Paper room | Bound to the literature library, for academic writing |
| Residence | One per expert, bound to no project |

## Identity module v2

In the A1 generation, an expert was one `SKILL.md` plus a few persona files. The Empire generation splits an expert apart on one principle: **one file, one form of governance**. Content is stored separately according to who may change it, how fast, and whether changes must be logged, in roughly three kinds:

- **Sealed**: only the Sovereign may change it.
- **Process-bound**: it can change only through a defined process.
- **Self-editable**: the expert may change it herself, but must leave a record.

Memory can only be appended to, never rewritten. None of this relies on good behaviour; the Git server enforces the rules when changes are pushed.

---

The full specification (detailed version of 2026-09-26) is kept in a private archive. SHA-256: `06a40b43af0422cdd0538bdca610a9778ecf4db40ea45f1efd588d56e21b1d48` (computed on UTF-8 with LF line endings).
