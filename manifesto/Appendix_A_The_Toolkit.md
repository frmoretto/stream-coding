# APPENDIX A: THE TOOLKIT
*"Methodology without tools is just philosophy. Here are the essential frameworks you need to execute Phases 1-3."*

> **AI Enforcement:** These templates work standalone, but for AI-enforced discipline, use them with [`SKILL.md`](https://github.com/frmoretto/stream-coding) in your editor's system prompt.

---

## 1. THE STRATEGIC BLUEPRINT TEMPLATE

**When to use:** Phase 1 (Strategic Thinking). This document must be 100% complete before you write a single line of code.

```markdown
# STRATEGIC BLUEPRINT: [Project Name]

## 1. THE CORE
* **Problem:** [Specific, painful, measurable problem]
* **User:** [Precise persona—e.g., "Solo SaaS Founders," not "Developers"]
* **Value Prop:** [One sentence: How you solve it differently]

**Implementation Implication:** [How this constrains technical decisions]

## 2. ECONOMIC ENGINE
* **Pricing Model:** [e.g., Freemium / Seat-based]
* **Unit Economics:** [Cost per user vs. Revenue per user]
* **Distribution:** [How you get your first 10 and first 100 users]

**Implementation Implication:** [How this affects architecture—e.g., "Client-side processing to minimize server costs"]

## 3. TECHNICAL ARCHITECTURE
* **The "Big Decision":** [The one architectural choice that defines the system]
* **Stack Rationale:** [Why these tools specifically?]
* **Data Model:** [Core entities and their relationships]

**Implementation Implication:** [Specific technical constraints this creates]

## 4. EXECUTION SCOPE
* **MVP Must-Haves:** [3-5 features only]
* **Explicitly Deferred:** [What you are NOT building yet—and why]
* **Risks:** [Top 3 risks and mitigation strategies]

**Implementation Implication:** [What this means for Phase 2 specifications]

## 5. REFERENCES

### Implementation Details Location
| Content Type | Location |
|--------------|----------|
| Anti-patterns | [Technical Spec, Section #] |
| Test Case Specifications | [Testing Doc, Section #] |
| Error Handling Matrix | [Error Handling Doc, Section #] |

*Replace `#` with actual section numbers and add markdown anchor links.*

### Schema References
| Topic | Location | Anchor |
|-------|----------|--------|
| [Topic] | [Path] | [Anchor] |

*This document provides strategic overview. Technical documents provide implementation specifications.*
```

---

## 2. THE ARCHITECTURE DECISION RECORD (ADR)

**When to use:** Whenever you make a significant technical choice (e.g., "PostgreSQL vs. Firebase," "Monolith vs. Microservices").

```markdown
# ADR-001: [Decision Title]
**Status:** Accepted | **Date:** [YYYY-MM-DD]

## Context
[What is the problem we are trying to solve? What are the constraints?]

## Decision
[We will use X.]

## Rationale
[Why X? What specific advantage does it give us?]

## Alternatives Considered
* **Option A:** [Why we rejected it]
* **Option B:** [Why we rejected it]

## Consequences
* **Positive:** [What we gain]
* **Negative:** [What trade-offs we accept]

## Implementation Implication
[Exactly how this affects the codebase—file structure, naming, patterns]
```

---

## 3. THE CLARITY GATE CHECKLIST

**When to use:** The mandatory gate between Phase 2 (Docs) and Phase 3 (Code). Never skip this.

### Foundation Checks
- [ ] **Actionability:** Does every section dictate a specific implementation detail?
- [ ] **Currency:** Is everything current (no outdated decisions)?
- [ ] **Single Source of Truth:** Is every decision recorded in only one place?
- [ ] **Decisions, Not Wishes:** Is every statement a decision, not a hope?
- [ ] **Prompt-Ready:** Would you put every section in an AI prompt?
- [ ] **No Future State:** Have you removed all "we will eventually" language?
- [ ] **No Fluff:** Have you removed all motivational/aspirational content?

### Document Architecture Checks (v3.3)
- [ ] **Document Type:** Is this clearly Strategic, Implementation, or Reference?
- [ ] **Anti-patterns Placement:** Are anti-patterns in implementation docs only?
- [ ] **Test Cases Placement:** Are test specs in implementation/testing docs only?
- [ ] **Error Handling Placement:** Is the error matrix in implementation docs only?
- [ ] **Deep Links:** Do ALL documents have deep links (not vague references)?
- [ ] **No Duplication:** Do strategic docs point to (not duplicate) implementation details?

### Quality Threshold
- [ ] **AI Coder Score:** Does documentation score 9+/10 on understandability?

**If ANY item fails:** Fix before proceeding to Phase 3.

*For the complete AI Coder Understandability scoring rubric and document architecture templates, see Appendix C.*

---

## 4. THE 7 PHASE 1 QUESTIONS

**When to use:** Phase 1 completion check. All 7 must be answered with specificity before proceeding to Phase 2.

| # | Question | ❌ Reject | ✅ Require |
|---|----------|-----------|------------|
| 1 | What exact problem? | "Help users manage tasks" | "[Persona] achieves [outcome] in [context]" |
| 2 | Success metrics? | "Users save time" | "100 users, 25% conversion, 3 months" |
| 3 | Why will you win? | "Better UI" | Structural advantage (architecture, data, model) |
| 4 | Architecture decision? | Let AI decide | Human decides with trade-off analysis |
| 5 | Tech stack rationale? | "I like Node.js" | "Node—team expertise, ship fast" |
| 6 | MVP features? | 10+ "must-haves" | 3-5 essential, rest explicitly deferred |
| 7 | What are you NOT building? | "We'll see" | Explicit exclusions with rationale |

**Phase 1 is complete when:** All 7 answered at "Require" level, documented, and approved.

---

## 5. QUICK REFERENCE: DOCUMENT TYPES

| Type | Purpose | Contains | Examples |
|------|---------|----------|----------|
| **Strategic** | WHAT and WHY | Decisions + Pointers to implementation | Blueprint, PRD |
| **Implementation** | HOW | Anti-patterns, Test Cases, Error Matrix, Deep Links | Tech Spec, API Spec, Module Spec |
| **Reference** | Lookup | Data definitions, configurations | Schema Reference, Glossary |

**The Rule:** Strategic docs point. Implementation docs contain. Never duplicate.

*For complete document architecture guidelines and templates, see Appendix C.*

---

**END OF APPENDIX A**

---

← [Chapter 5: The Perpetual Stream](./Chapter_05_The_Perpetual_Stream.md) | [Appendix B: References →](./Appendix_B_References.md)
