# Design and Engineering Decisions

## Purpose

This document records important decisions made during development.

The purpose is to preserve reasoning across:

- iterations
- sessions
- model changes
- agent changes
- developer changes
- refactoring
- design revisions

The Design Loop should read this document before making major architectural, visual, or UX decisions.

Do not repeatedly reconsider a settled decision without new evidence.

---

## Decision Rules

A decision should be recorded when it materially affects:

- design language
- typography
- color system
- layout strategy
- component architecture
- responsive behavior
- interaction behavior
- animation strategy
- data architecture
- API architecture
- framework architecture
- performance strategy
- accessibility strategy
- security
- deployment
- dependencies
- major technical tradeoffs

Small implementation details do not need to be recorded.

---

## Decision Statuses

Use:

```text
PROPOSED
ACCEPTED
REJECTED
SUPERSEDED
REVISIT
```

---

## Decision Template

Copy this structure for every important decision.

```
DEC-001 — <Decision Title>

Date:          <date>
Iteration:     <iteration>
Category:      <design / ux / architecture / technical / responsive / performance / accessibility / security / deployment>
Status:        ACCEPTED

Context:
<what problem or situation led to the decision>

Options Considered:
Option A — <description>
Option B — <description>
Option C — <description if applicable>

Decision:
<what was chosen>

Reasoning:
<why it was chosen>

Evidence:
<screenshots, tests, measurements, requirements, references, or other evidence>

Tradeoffs:
Advantages:
  <advantage>
Disadvantages:
  <disadvantage>

Consequences:
<what this decision means for the rest of the project>

Affected Areas:
<page>
<component>
<system>

Revisit Condition:
<what future evidence would justify reconsidering this decision>
```

---

# INITIAL PROJECT DECISIONS

## DEC-001 — Design System Ownership

Status: **ACCEPTED**

**Decision:** The project-specific design constitution is the source of truth for visual consistency.

**Reasoning:** Repeated AI iterations can cause visual drift. A persistent constitution provides stable rules across iterations and across different AI agents.

**Consequences:** Major visual changes must either follow the constitution or explicitly update it.

---

## DEC-002 — Browser Output Is the Visual Source of Truth

Status: **ACCEPTED**

**Decision:** Rendered browser output is more authoritative than assumptions made from source code.

**Reasoning:** The code can appear correct while the actual rendered application contains:

- layout defects
- responsive problems
- font issues
- overflow
- runtime errors
- broken assets

**Consequences:** Visual verification must use the running application when browser tooling is available.

---

## DEC-003 — Verification Before Completion

Status: **ACCEPTED**

**Decision:** A task cannot be considered complete solely because code has been written.

**Reasoning:** Code generation is not equivalent to product verification.

**Consequences:** Important changes require appropriate validation.

---

## DEC-004 — Specialized Evaluation

Status: **ACCEPTED**

**Decision:** Visual, UX, responsive, technical, accessibility, and performance concerns should be evaluated separately where practical.

**Reasoning:** A single "looks good" evaluation can miss important problems.

**Consequences:** The loop should collect specialized evidence rather than relying on one general judgement.

---

## DEC-005 — Deterministic Tools Over Subjective Judgement

Status: **ACCEPTED**

**Decision:** When a deterministic tool can verify a property, use that tool instead of relying solely on an AI opinion.

**Examples:** Use:

- build output for build correctness
- tests for functional behavior
- browser inspection for rendering
- Lighthouse or equivalent for measured performance
- accessibility tooling where available

**Consequences:** LLM evaluation should supplement objective checks rather than replace them.

---

## DEC-006 — One Primary Objective Per Iteration

Status: **ACCEPTED**

**Decision:** Each loop iteration should have one primary improvement objective.

**Reasoning:** Changing too many unrelated things at once makes cause and effect difficult to understand and increases regression risk.

**Consequences:** The loop prioritizes the highest-value issue and solves it coherently before moving to the next.

---

## DEC-007 — Regression Protection

Status: **ACCEPTED**

**Decision:** An iteration that improves one area while materially damaging another should not automatically be accepted.

**Reasoning:** AI-generated changes can unintentionally break previously correct behavior.

**Consequences:** Accepted states must be preserved and compared against future iterations.

---

## DEC-008 — Agent Independence

Status: **ACCEPTED**

**Decision:** The design-loop methodology must remain independent from any specific AI agent.

**Reasoning:** The same project may be worked on with:

- Claude Code
- Codex
- Antigravity
- OpenClaw
- other coding agents

**Consequences:**

- Project memory remains inside `design-loop/`.
- Agent-specific integrations should be thin adapters.

---

## DEC-009 — No Fabricated Evidence

Status: **ACCEPTED**

**Decision:** The system must never claim that a test, screenshot, performance measurement, or verification step occurred when it did not.

**Consequences:** Unavailable checks must be recorded as `NOT VERIFIED`.

---

# DESIGN DECISIONS

Add major project-specific design decisions below.

## DEC-010 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED
- Revisit condition: NOT PROVIDED

---

# UX DECISIONS

## DEC-011 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED

---

# RESPONSIVE DECISIONS

## DEC-012 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED

---

# TECHNICAL DECISIONS

## DEC-013 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED

---

# PERFORMANCE DECISIONS

## DEC-014 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED

---

# ACCESSIBILITY DECISIONS

## DEC-015 — &lt;Title&gt;

Status: PROPOSED

- Context: NOT PROVIDED
- Decision: NOT PROVIDED
- Reasoning: NOT PROVIDED
- Evidence: NOT PROVIDED
- Consequences: NOT PROVIDED

---

# REJECTED DECISIONS

Use this section to record ideas that were intentionally rejected when the reason matters.

## REJ-001 — &lt;Title&gt;

- Proposal: &lt;what was proposed&gt;
- Reason Rejected: &lt;reason&gt;
- Evidence: &lt;evidence&gt;
- Do Not Reconsider Unless: &lt;condition&gt;

---

# SUPERSEDED DECISIONS

When an old decision is replaced, do not delete it.

Record:

```
DEC-<OLD-ID> — SUPERSEDED
Superseded by: DEC-<NEW-ID>
Reason: <reason>
Date: <date>
```

---

# DECISION REVIEW

Periodically review decisions when:

- the product direction changes
- major technical constraints change
- new evidence contradicts an old decision
- accessibility requirements change
- performance requirements change
- the design constitution changes

Do not revisit decisions merely because the current agent has a different personal preference.

---

# GAUNTLET DECISIONS

Record important decisions resulting from independent quality evaluation.

---

## G-DEC-001 — <Title>

### Context

<what the Gauntlet discovered>

### Reference

<reference>

### Current Problem

<problem>

### Decision

<decision>

### Reasoning

<reasoning>

### Evidence

<evidence>

### Tradeoff

<tradeoff>

### Revisit Condition

<condition>

---

# END OF DECISIONS
