# Stream Coding

**The 10-20x Methodology for AI-Accelerated Software Development**

> *"Stream coding isn't about faster coding. It's about documentation so clear that code writes itself."*

---

## The Problem: The Velocity Mirage

AI tools promise 10x productivity. GitHub Copilot, Cursor, Claude Code—they make coding 55% faster.

**But projects still take the same time to ship.**

Why? Because faster typing doesn't solve:
- Strategic decisions AI can't make for you
- Context that gets lost between prompts
- Technical debt created at 10x speed

This gap between task velocity and project velocity is the **Velocity Mirage**.

---

## The Solution: Stream Coding

Stream Coding is a documentation-first methodology that makes AI-generated code deterministic.

**The 40/40/20 Split:**
- **40%** Strategic Thinking (Phase 1) — Solve hard problems before coding
- **40%** AI-Ready Documentation (Phase 2) — Specs so complete AI has zero decisions
- **20%** Execution + Quality (Phases 3-4) — Code streams out automatically

**Real Results (5Levels Case Study):**
- 7 production modules in 4.5 hours
- 46 intelligence endpoints (77 total backend API)
- Zero bugs, 21 minutes average per tested module

---

## Quick Start

### 1. Get the Skill

Drop [`SKILL.md`](./SKILL.md) into your AI editor as a system prompt:

- **Cursor:** Add to `.cursorrules`
- **Windsurf:** Add to project rules
- **Claude Projects:** Add to project knowledge

The Skill enforces Stream Coding discipline, it will refuse vague requests and steer you toward proper documentation.

### 2. Read the Manifesto

The [`/manifesto`](./manifesto) folder contains the complete methodology:

| Chapter | Topic |
|---------|-------|
| [Chapter 1](./manifesto/Chapter_01_The_10x_Promise.md) | The Velocity Mirage |
| [Chapter 2](./manifesto/Chapter_02_Why_AI_Cant_Deliver.md) | Why AI Tools Alone Fail |
| [Chapter 3](./manifesto/Chapter_03_The_Methodology_Gap.md) | The Missing Middle |
| [Chapter 4](./manifesto/Chapter_04_What_Is_Stream_Coding.md) | The 4-Phase Methodology |
| [Chapter 5](./manifesto/Chapter_05_The_Perpetual_Stream.md) | Day 2 & The Rule of Divergence |
| [Appendix A](./manifesto/Appendix_A_The_Toolkit.md) | Templates & Checklists |
| [Appendix B](./manifesto/Appendix_B_References.md) | Research & SDD Positioning |
| [Appendix C](./manifesto/Appendix_C_5Levels_Case_Study.md) | 5Levels Case Study (Git-Verified) |
| [Advanced Framework](./manifesto/advanced/Advanced_Framework_v3.3.md) | Document Architecture (v3.3) |

### 3. Use the Templates

The [`/templates`](./templates) folder contains ready-to-use frameworks:

- **Strategic Blueprint** — Answer the 7 Phase 1 Questions
- **ADR Template** — Document architecture decisions with rationale
- **Clarity Gate Checklist** — The mandatory Phase 2→3 gate

---

## The Core Insight

> **"When code fails, fix the spec—not the code."**

Traditional development iterates on code. Stream Coding iterates on documentation.

Every manual code edit without updating the spec creates **Divergence**—technical debt that breaks the stream. The methodology works because it treats code as a compiled output of documentation, not the source of truth.

---

## Who This Is For

✅ **Technical founders** building greenfield products  
✅ **Solo developers** and small teams (1-5 people)  
✅ **Anyone tired of AI-generated spaghetti code**

❌ Not for large enterprises (see GitHub Spec-Kit, Tessl, Kiro)  
❌ Not for hackathons or throwaway prototypes  
❌ Not for teams who can't commit to documentation-first

---

## Research Validation

Stream Coding aligns with industry research:

- **McKinsey (2025):** Top performers see 16-30% productivity gains through "end-to-end PDLC implementation" and "structured communication of specs"
- **DORA (2025):** 7.2% delivery instability increase for every 25% AI adoption *without foundational systems*
- **METR (2025):** Developers 19% slower with AI despite *feeling* 20% faster

The methodology isn't magic, it's systematic application of spec-driven development at founder scale.

---

## Contributing

Stream Coding is open source under CC BY 4.0. You're free to use, adapt, and share with attribution.

Found an improvement? Open an issue or PR.

---

## About

Created by [Francesco Marinoni Moretto](https://www.linkedin.com/in/francesco-moretto/) while building [5Levels](https://5levels.io), a LinkedIn relationship intelligence platform.

The methodology emerged from building 7 production modules in 4.5 hours, and documenting exactly how.

---

## License

[CC BY 4.0](./LICENSE) — Use freely with attribution.

*"Stream Coding methodology by Francesco Marinoni Moretto (github.com/frmoretto/stream-coding)"*

---

*In memory of my beloved father Guido*
