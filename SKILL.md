---
name: stream-coding
description: Documentation-first development methodology. The goal is AI-ready documentation - when docs are clear enough, code generation becomes automatic. Triggers on "Build", "Create", "Implement", "Document", or "Spec out". Version 3.3 adds 10/10 AI Coder requirements with document-type-aware placement (Anti-patterns, Test Cases, Error Handling in implementation docs; Deep Links in all docs).
---

# Stream Coding v3.3: Documentation-First Development

## ⚠️ CRITICAL REFRAME: THIS IS A DOCUMENTATION METHODOLOGY, NOT A CODING METHODOLOGY

**Version 3.3 Paradigm Shift:** The goal of Stream Coding is NOT faster coding. The goal is **AI-ready documentation**. When documentation is clear enough, code generation becomes automatic.

**The Insight:**
> "If your docs are good enough, AI writes the code. The hard work IS the documentation. Code is just the printout."

**v3.3 Addition:** Documents must score 10/10 on AI Coder Understandability. This requires mandatory sections placed in the CORRECT document type (see Section: Document Type Architecture).

---

## CHANGELOG

| Version | Changes |
|---------|---------|
| 3.0 | Initial Stream Coding methodology |
| 3.1 | Clearer terminology, mandatory Clarity Gate |
| 3.3 | +4 mandatory sections with **document-type-aware placement** |
| 3.3.1 | Corrected time allocation (40/40/20), added Phase 4, added Rule of Divergence |

---

## THE STREAM CODING TRUTH

```
Messy Docs → Vague Specs → AI Guesses → Rework Cycles → 2-3x Velocity
Clear Docs → Clear Specs → AI Executes → Minimal Rework → 10-20x Velocity
```

**Why Most "AI-Assisted Development" Fails:**
- People feed AI messy docs
- AI generates code based on assumptions
- Code doesn't match intent
- Endless revision cycles
- Result: Marginally faster than manual coding

**Why Stream Coding Achieves 10-20x:**
- Documentation is clarified FIRST
- AI has zero ambiguity
- Code matches intent on first pass
- Minimal revision
- Result: Documentation time + automatic code generation

---

## 🆕 DOCUMENT TYPE ARCHITECTURE (v3.3 Critical Addition)

**The Insight:** Not all documents need all v3.3 sections. Putting implementation details in strategic documents violates single-source-of-truth.

### Document Types

| Type | Purpose | Examples |
|------|---------|----------|
| **Strategic** | WHAT and WHY | Master Blueprint, PRD, Vision docs, Business cases |
| **Implementation** | HOW | Technical Specs, API docs, Module specs, Architecture docs |
| **Reference** | Lookup | Schema Reference, Glossary, Configuration |

### v3.3 Section Placement Matrix

| Section | Strategic Docs | Implementation Docs | Reference Docs |
|---------|---------------|---------------------|----------------|
| **Deep Links (References)** | ✅ Required | ✅ Required | ✅ Required |
| **Anti-patterns** | ❌ Pointer only | ✅ Required | ❌ N/A |
| **Test Case Specifications** | ❌ Pointer only | ✅ Required | ❌ N/A |
| **Error Handling Matrix** | ❌ Pointer only | ✅ Required | ❌ N/A |

### Why This Matters

**Wrong (violates single-source-of-truth):**
```
Master Blueprint
├── Strategy content
├── Anti-patterns ← WRONG: duplicates Technical Annex
├── Test Cases ← WRONG: duplicates Testing doc
└── Error Matrix ← WRONG: duplicates Error Handling doc
```

**Right (single-source-of-truth):**
```
Master Blueprint (Strategic)
├── Strategy content
└── References
    └── Pointer: "Anti-patterns → Part 07, 08, 18"

Technical Annex (Implementation)
├── Implementation details
├── Anti-patterns ← CORRECT: lives with specs
├── Test Cases ← CORRECT: lives with specs
└── Error Matrix ← CORRECT: lives with specs
```

### Strategic Document Template

```markdown
## [N]. REFERENCES

All cross-references use deep links.

**v3.3 Implementation Details Location:**
| Content Type | Location |
|--------------|----------|
| Anti-patterns | [Part XX: Relevant Annex] |
| Test Case Specifications | [Part XX: Testing] |
| Error Handling Matrix | [Part XX: Error Handling] |

*This document provides strategic overview. Technical documents provide implementation specifications.*

### [N].1 Schema References
| Topic | Location | Anchor |
|-------|----------|--------|
| ... | ... | ... |

### [N].2 Technical References
| Topic | Document | Section |
|-------|----------|---------|
| ... | ... | ... |
```

### Implementation Document Template

```markdown
## [N]. ANTI-PATTERNS (DO NOT)

### [N].1 [Domain] Anti-patterns
| ❌ Don't | ✅ Do Instead | Why |
|----------|---------------|-----|
| ... | ... | ... |

## [N+1]. TEST CASE SPECIFICATIONS

### [N+1].1 Unit Tests
| Test ID | Component | Input | Expected Output | Edge Cases |
|---------|-----------|-------|-----------------|------------|
| ... | ... | ... | ... | ... |

### [N+1].2 Integration Tests
| Test ID | Flow | Setup | Verification | Teardown |
|---------|------|-------|--------------|----------|
| ... | ... | ... | ... | ... |

## [N+2]. ERROR HANDLING MATRIX

### [N+2].1 External Service Errors
| Error Type | HTTP Code | User Message | Log Level | Recovery |
|------------|-----------|--------------|-----------|----------|
| ... | ... | ... | ... | ... |

### [N+2].2 Business Logic Errors
| Error Type | Trigger | Message | Suggested Action |
|------------|---------|---------|------------------|
| ... | ... | ... | ... |

## [N+3]. REFERENCES (Deep Links)

### [N+3].1 Internal References
| Topic | Section | Anchor |
|-------|---------|--------|
| ... | ... | ... |

### [N+3].2 External Dependencies
| Dependency | Documentation | Version |
|------------|---------------|---------|
| ... | ... | ... |
```

---

## THE 4-PHASE METHODOLOGY

### Time Allocation (v3.3.1 Corrected)

| Phase | Time | Focus |
|-------|------|-------|
| Phase 1: Strategic Thinking | 40% | WHAT to build, WHY it matters |
| Phase 2: AI-Ready Documentation | 40% | HOW to build (specs so clear AI has zero decisions) |
| Phase 3: Execution | 15% | Code generation + implementation |
| Phase 4: Quality & Iteration | 5% | Testing, refinement, continuous improvement |

**The Counterintuitive Truth:** 80% of time goes to documentation. 20% to code. This is why velocity is 10-20x—not because coding is faster, but because rework approaches zero.

---

## PHASE 1: STRATEGIC THINKING (40% of time)

### The 7 Questions Framework

Before ANY documentation, answer these with specificity:

| # | Question | ❌ Reject | ✅ Require |
|---|----------|-----------|------------|
| 1 | What exact problem? | "Help users manage tasks" | "[Persona] achieves [outcome] in [context]" |
| 2 | Success metrics? | "Users save time" | "100 users, 25% conversion, 3 months" |
| 3 | Why will you win? | "Better UI" | Structural advantage (architecture, data, model) |
| 4 | Architecture decision? | Let AI decide | Human decides with trade-off analysis |
| 5 | Tech stack rationale? | "I like Node.js" | "Node—team expertise, ship fast" |
| 6 | MVP features? | 10+ "must-haves" | 3-5 essential, rest explicitly deferred |
| 7 | What are you NOT building? | "We'll see" | Explicit exclusions with rationale |

### Phase 1 Exit Criteria

- [ ] All 7 questions answered at "Require" level
- [ ] Strategic Blueprint document created
- [ ] Architecture Decision Records (ADRs) for major choices
- [ ] Zero ambiguity about WHAT you're building

---

## PHASE 2: AI-READY DOCUMENTATION (40% of time)

### The Clarity Test

Before moving to Phase 3, every spec must pass:

| Check | Question |
|-------|----------|
| **Actionable** | Does every section dictate a specific implementation detail? |
| **Current** | Is everything up-to-date (no outdated decisions)? |
| **Single Source** | Is every decision recorded in only one place? |
| **Decision, Not Wish** | Is every statement a decision, not a hope? |
| **Prompt-Ready** | Would you paste this directly into an AI prompt? |

### The 10/10 AI Coder Test (v3.3)

**Question:** "If I gave this document to a new developer (human or AI) with no other context, could they implement it correctly?"

| Score | Meaning | Action |
|-------|---------|--------|
| 10/10 | Zero questions needed | Ready for Phase 3 |
| 9/10 | 1 minor clarification | Fix, then proceed |
| 7-8/10 | Several gaps | Revise documentation |
| <7/10 | Major gaps | Stay in Phase 2 |

### The Clarity Gate (Mandatory)

**⛔ NEVER skip this gate.**

Before ANY code generation:

1. Run Clarity Test on every document
2. Score each document 1-10
3. Fix anything below 9/10
4. Re-score until all pass

**Why This Matters:** Every point below 10 = debugging hours later. A 7/10 document generates 7/10 code that needs 30% rework.

---

## PHASE 3: EXECUTION (15% of time)

### The Generate-Verify-Integrate Loop

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│  1. GENERATE                                        │
│     Feed spec to AI → Receive code                  │
│                                                     │
│  2. VERIFY                                          │
│     Run tests → Check against spec                  │
│     Does output match spec exactly?                 │
│     - Yes → Continue                                │
│     - No → Fix SPEC first, then regenerate          │
│                                                     │
│  3. INTEGRATE                                       │
│     Commit → Update documentation if needed         │
│     (But prefer spec fixes over code patches)       │
│                                                     │
└─────────────────────────────────────────────────────┘
```

### The Golden Rule of Phase 3

> **"When code fails, fix the spec—not the code."**

If generated code doesn't work:
1. ❌ Don't patch the code manually
2. ✅ Ask: "What was unclear in my spec?"
3. ✅ Fix the spec
4. ✅ Regenerate

**Why:** Manual code patches create divergence between spec and reality. Divergence compounds. Eventually your spec is fiction and you're back to manual development.

---

## PHASE 4: QUALITY & ITERATION (5% of time)

### The Rule of Divergence (v3.3.1)

**Definition:** Divergence occurs when code and documentation don't match.

```
Every manual edit without updating the spec = Divergence debt
Divergence debt compounds like financial debt
Eventually: Spec becomes fiction, AI becomes useless
```

### Preventing Divergence

| Scenario | ❌ Wrong | ✅ Right |
|----------|----------|----------|
| Bug in generated code | Fix code manually | Fix spec, regenerate |
| Missing edge case | Add code patch | Add to spec, regenerate |
| Performance issue | Optimize code | Document constraint, regenerate |
| "Quick fix" needed | Just this once... | No. Fix spec. |

### When Manual Edits Are Acceptable

Only when:
1. **AND** the change is spec-conformant (doesn't deviate from intent)
2. **AND** you immediately update the spec to match
3. **AND** you document why regeneration wasn't practical

Even then, prefer regeneration. Manual edits are technical debt.

---

## TRIGGER BEHAVIOR

This methodology activates when the user says:
- "Build [feature]"
- "Create [component]"
- "Implement [system]"
- "Document [project]"
- "Spec out [feature]"

### Response Protocol

1. **Check Phase:** Where is this project in the 4-phase journey?

2. **If Phase 1 incomplete:**
   - "Before building, let's clarify strategy. [Ask 7 Questions]"

3. **If Phase 2 incomplete:**
   - "Before coding, let's ensure documentation is AI-ready. [Run Clarity Test]"

4. **If Phase 3 ready:**
   - "Documentation looks complete. Generating implementation..."

5. **If maintaining (Phase 4):**
   - "Is this change spec-conformant? Let's update docs first if needed."

---

## DOCUMENT TEMPLATES

### Strategic Blueprint Template

```markdown
# [PROJECT NAME] - Strategic Blueprint

## 1. Problem Statement
**Specific Problem:** [Measurable, painful problem]
**Target User:** [Precise persona]
**Success Looks Like:** [Concrete metrics]

## 2. Solution Overview
**Core Insight:** [Why this approach wins]
**Key Differentiator:** [Structural advantage]

## 3. Architecture Decisions
| Decision | Choice | Rationale | Trade-offs |
|----------|--------|-----------|------------|
| Database | [X] | [Why] | [Accepted downsides] |
| Framework | [X] | [Why] | [Accepted downsides] |

## 4. MVP Scope
**Must Have (v1.0):**
1. [Feature 1]
2. [Feature 2]
3. [Feature 3]

**Explicitly Deferred:**
- [Feature X] - Because [rationale]
- [Feature Y] - Because [rationale]

## 5. References
| Content Type | Location |
|--------------|----------|
| Anti-patterns | [Technical Spec, Section X] |
| Test Specifications | [Testing Doc, Section Y] |
| Error Handling | [Error Matrix, Section Z] |
```

### Architecture Decision Record (ADR) Template

```markdown
# ADR-[NUMBER]: [TITLE]

## Status
[Proposed | Accepted | Deprecated | Superseded]

## Context
[What is the situation? What forces are at play?]

## Decision
[What decision was made?]

## Rationale
[Why this choice over alternatives?]

## Consequences
**Positive:**
- [Benefit 1]
- [Benefit 2]

**Negative:**
- [Trade-off 1]
- [Trade-off 2]

## Alternatives Considered
| Option | Pros | Cons | Why Rejected |
|--------|------|------|--------------|
| [A] | ... | ... | ... |
| [B] | ... | ... | ... |
```

---

## QUICK REFERENCE

### Phase Checklist

- [ ] **Phase 1:** 7 Questions answered, Strategic Blueprint complete
- [ ] **Phase 2:** All specs pass Clarity Test (9+/10), Clarity Gate passed
- [ ] **Phase 3:** Generate-Verify-Integrate loop, fix specs not code
- [ ] **Phase 4:** Rule of Divergence enforced, specs match reality

### The Core Mantras

1. "Documentation IS the work. Code is just the printout."
2. "When code fails, fix the spec—not the code."
3. "Every manual edit without updating the spec = Divergence debt."
4. "A 7/10 spec generates 7/10 code that needs 30% rework."

### Time Reality Check

If you're spending more than 20% of time on coding/debugging:
- Your documentation isn't clear enough
- Go back to Phase 2
- The 40/40/20 split is not optional

---

## VERSION HISTORY

- **v3.3.1** (Current): Corrected time allocation (40/40/20), added Phase 4, added Rule of Divergence
- **v3.3**: Added document-type-aware placement, 10/10 AI Coder requirements
- **v3.1**: Clearer terminology, mandatory Clarity Gate
- **v3.0**: Initial Stream Coding methodology

---

*Stream Coding by Francesco Marinoni Moretto (github.com/frmoretto/stream-coding) — CC BY 4.0*