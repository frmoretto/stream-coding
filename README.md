# Stream Coding v3.4

**The 10-20x Methodology for AI-Accelerated Software Development**

> 📢 **v3.4 Update:** Complete 13-item Clarity Gate (was 5 items), scoring rubric, Documentation Audit. Re-download if using older version.

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
- Zero bugs in generated code, 21 minutes average per tested module

*Note: The case study focuses on backend intelligence modules—Stream Coding's sweet spot. For frontend, use the methodology for behavior (components, state, logic) and complement with AI design tools for visuals. See Chapter 4 for details.*

---

## Quick Start

### Option 1: claude.ai / Claude Desktop

1. Download [`stream-coding.zip`](stream-coding.zip)
2. Go to Settings → Features → Skills → Add
3. Upload the zip file
4. Ask Claude: *"Build a user authentication system"*

### Option 2: Claude Code

1. Copy `SKILL.md` to your project's skills folder
2. Claude Code will automatically detect and use it
3. Ask Claude: *"Build a user authentication system"*

### Option 3: Claude Projects

Add [`SKILL.md`](SKILL.md) to project knowledge. Claude will search it when needed, though Skills provide better integration.

### Option 4: Manual / Other LLMs

For Cursor, Windsurf, or other AI tools:
- Extract core principles (Phases, Document Types, Clarity Gate)
- Create a condensed version for `.cursorrules` or project settings
- Use the [templates](./templates) and [Clarity Gate Checklist](./templates/CLARITY_GATE_CHECKLIST.md) as reference

The methodology is tool-agnostic—only SKILL.md is Claude-optimized.

---

### Read the Manifesto

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

### Use the Templates

The [`/templates`](./templates) folder contains ready-to-use frameworks:

| Template | Purpose |
|----------|--------|
| [Strategic Blueprint](./templates/STRATEGIC_BLUEPRINT.md) | Answer the 7 Phase 1 Questions |
| [ADR Template](./templates/ADR_TEMPLATE.md) | Document architecture decisions with rationale |
| [Clarity Gate Checklist](./templates/CLARITY_GATE_CHECKLIST.md) | The mandatory Phase 2→3 gate |

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
✅ **Backend/business logic focused** (see Chapter 4 for frontend approach)

❌ Not for large enterprises (see GitHub Spec-Kit, Kiro, Gemini Conductor)  
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

## Related

**Clarity Gate** — Pre-ingestion verification for epistemic quality (originated from Stream Coding's Clarity Gate concept)  
[github.com/frmoretto/clarity-gate](https://github.com/frmoretto/clarity-gate)

**Source of Truth Creator** — Create epistemically calibrated documents  
[github.com/frmoretto/source-of-truth-creator](https://github.com/frmoretto/source-of-truth-creator)

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
