# CLARITY GATE CHECKLIST

> **Mandatory Gate** — Complete this checklist between Phase 2 (Documentation) and Phase 3 (Execution).
> If ANY item fails, fix the documentation before proceeding. Never skip this.

---

**Project:** [Project Name]  
**Date:** [YYYY-MM-DD]  
**Reviewer:** [Name]

---

## Foundation Checks

- [ ] **Actionability:** Does every section dictate a specific implementation detail?
- [ ] **Currency:** Is everything current (no outdated decisions)?
- [ ] **Single Source of Truth:** Is every decision recorded in only one place?
- [ ] **Decisions, Not Wishes:** Is every statement a decision, not a hope?
- [ ] **Prompt-Ready:** Would you put every section in an AI prompt?
- [ ] **No Future State:** Have you removed all "we will eventually" language?
- [ ] **No Fluff:** Have you removed all motivational/aspirational content?

---

## Document Architecture Checks (v3.3)

- [ ] **Document Type:** Is each document clearly Strategic, Implementation, or Reference?
- [ ] **Anti-patterns Placement:** Are anti-patterns in implementation docs only?
- [ ] **Test Cases Placement:** Are test specs in implementation/testing docs only?
- [ ] **Error Handling Placement:** Is the error matrix in implementation docs only?
- [ ] **Deep Links:** Do ALL documents have deep links (not vague references)?
- [ ] **No Duplication:** Do strategic docs point to (not duplicate) implementation details?

---

## Quality Threshold

- [ ] **AI Coder Score:** Does documentation score 9+/10 on understandability?

### AI Coder Understandability Quick Test

Ask yourself: "If I gave this doc to an AI with no other context, would it produce correct code?"

| Score | Meaning |
|-------|---------|
| 10/10 | AI could implement with zero questions |
| 9/10 | AI might ask 1 clarifying question |
| 7-8/10 | AI would need 2-3 clarifications |
| <7/10 | **FAIL** — Documentation incomplete |

---

## Gate Result

- [ ] **PASS** — All items checked, proceed to Phase 3
- [ ] **FAIL** — Items below need fixing before Phase 3

### Items Requiring Fix

| Item | Issue | Owner | ETA |
|------|-------|-------|-----|
| | | | |

---

## Sign-off

**Approved by:** _______________  
**Date:** _______________

---

*For the complete AI Coder Understandability scoring rubric and document architecture templates, see [Appendix C](../manifesto/Appendix_C_Advanced_v3.3.md).*

---

*Template from [Stream Coding](https://github.com/frmoretto/stream-coding) by Francesco Marinoni Moretto — CC BY 4.0*
