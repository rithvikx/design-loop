---
name: design-loop
description: >
  Universal design and development loop for AI coding agents. Use when
  building, rebuilding, refining, or visually improving websites and web
  applications. The skill requires the agent to inspect the real application,
  gather evidence through browser verification and screenshots, evaluate visual
  quality and engineering correctness, prioritize issues, make controlled
  changes, verify the result, detect regressions, and iterate until explicit
  acceptance criteria are satisfied.
---

# Universal Design Loop

You are operating inside the Universal Design Loop.

Your job is NOT simply to generate code.

Your job is to continuously improve the actual running application through
evidence-based iteration.

The fundamental loop is:

UNDERSTAND
→ INSPECT
→ PLAN
→ IMPLEMENT
→ RUN
→ BROWSE
→ CAPTURE
→ EVALUATE
→ PRIORITIZE
→ FIX
→ VERIFY
→ REGRESSION CHECK
→ ACCEPT OR ITERATE

---

# DESIGN LOOP EXECUTION MODEL

The Universal Design Loop consists of five major layers:

1. Design Intelligence
2. Specialist Skill Orchestration
3. Implementation
4. Gauntlet Quality Engine
5. Engineering Verification

The agent must not treat the project as a simple code-generation task.

The goal is:

RESEARCH
→ STRATEGY
→ BUILD
→ CRITIQUE
→ IMPROVE
→ VERIFY

# SKILL ORCHESTRATION

Before implementation:

1. load `SKILL_REGISTRY.json`
2. discover available skills
3. classify the project
4. select relevant specialist skills
5. record the selection in `SESSION.json`

Use specialized skills when they materially improve the result.

Do not invoke every available skill.

The agent must never invent a skill that does not exist.

# GAUNTLET REQUIREMENT

Important visual work must be evaluated independently of the builder.

When the Gauntlet Quality Engine is active:

- use fresh-context criticism when possible
- establish a quality bar
- compare current output against relevant references
- identify the largest remaining quality gap
- fix the largest gap
- verify
- repeat

The builder must not be the sole authority on quality.

# GRAPHIFY REQUIREMENT

After an accepted final implementation:

update Graphify using the available Graphify integration.

Prefer incremental updates.

Do not declare final project completion while a required Graphify update is
known to have failed.

If Graphify is unavailable:

record NOT VERIFIED.

# 1. CORE PRINCIPLE

Never assume the generated code represents the final quality of the product.

The real application is the source of truth.

You must inspect the running application whenever the environment allows it.

A task is not complete merely because:

- code was generated
- files were changed
- the build succeeds
- the page loads

The implementation must also satisfy the visual, UX, responsive,
technical, accessibility, and functional requirements.

---

# 2. INSPECT BEFORE MODIFYING

Before making significant changes:

- inspect the repository
- identify the framework
- identify the package manager
- identify the application entry point
- identify routes
- identify components
- identify styling architecture
- identify existing design tokens
- identify state/data architecture
- identify existing tests
- identify how the application is started
- inspect existing screenshots or references
- identify existing problems

Preserve working functionality.

Do not rewrite architecture without evidence that it is necessary.

Do not modify unrelated files.

---

# 3. LOAD PROJECT MEMORY

Before continuing work, read:

design-loop/STATE.json
design-loop/DESIGN_CONSTITUTION.md
design-loop/REQUIREMENTS.md
design-loop/ISSUES.json
design-loop/PROGRESS.md
design-loop/DECISIONS.md

These files represent project memory.

Do not restart reasoning from zero when previous iterations already contain useful
information.

---

# 4. DESIGN CONSTITUTION

The Design Constitution defines the visual language of the project.

You must respect:

- typography
- colors
- spacing
- layout
- component consistency
- visual hierarchy
- interaction principles
- animation principles
- responsive behavior
- prohibited design patterns

Do not introduce design drift.

If a significant design rule needs to change, record the decision in:

design-loop/DECISIONS.md

---

# 5. REQUIREMENTS

The requirements define what the product must accomplish.

Distinguish between:

Functional requirements
UX requirements
Visual requirements
Technical requirements

Never replace an explicit requirement with a personal design preference.

---

# 6. BROWSER-FIRST VERIFICATION

Whenever browser tooling is available:

1. start the application
2. open the application
3. wait for the page to settle
4. inspect the rendered result
5. inspect console errors
6. inspect failed network requests
7. interact with important controls
8. capture screenshots
9. repeat at important viewport sizes

The browser output is more authoritative than your assumptions about the code.

---

# 7. VISUAL EVALUATION

Evaluate:

- composition
- visual hierarchy
- spacing
- alignment
- typography
- color consistency
- imagery
- component consistency
- responsive behavior
- interaction states
- motion
- overall visual coherence

When references exist, compare the current implementation against them.

Do not merely say:

"Looks good."

Instead produce concrete observations.

Example:

{
"category": "visual",
"severity": "P1",
"location": "homepage/hero",
"problem": "Hero hierarchy is weak.",
"evidence": "Heading and CTA have insufficient visual separation.",
"recommended_action": "Increase heading scale and rebalance hero spacing."
}

---

# 8. UX EVALUATION

Evaluate:

- navigation clarity
- information architecture
- primary action discoverability
- interaction feedback
- loading states
- error states
- empty states
- form usability
- mobile usability
- keyboard usability
- focus visibility

Visual quality must never destroy usability.

---

# 9. RESPONSIVE EVALUATION

Whenever practical, verify:

- 1440px
- 1280px
- 1024px
- 768px
- 390px

Look for:

- horizontal overflow
- broken grids
- clipped content
- unreadable text
- collapsed navigation
- unusable buttons
- incorrect image ratios
- excessive spacing
- broken responsive typography

---

# 10. TECHNICAL EVALUATION

Use deterministic tools whenever available.

Check:

- build
- tests
- lint
- type checking
- runtime errors
- console errors
- failed API requests
- broken routes
- missing assets

Never claim that something passed unless it was actually checked.

---

# 11. ACCESSIBILITY

Whenever practical, check:

- semantic HTML
- heading hierarchy
- keyboard navigation
- focus visibility
- accessible names
- form labels
- color contrast
- alt text
- touch target usability
- reduced-motion behavior

---

# 12. PERFORMANCE

When tools are available, evaluate:

- page loading
- image sizes
- unnecessary JavaScript
- large bundles
- layout shifts
- render-blocking resources
- expensive animations

Use actual measurements.

Never invent performance numbers.

---

# 13. ISSUE PRIORITY

Classify problems as:

P0 = critical
P1 = major
P2 = moderate
P3 = polish

Examples:

P0:

- application does not load
- core functionality is broken
- runtime crash

P1:

- major layout problem
- broken mobile experience
- major visual mismatch
- important workflow unusable

P2:

- inconsistent spacing
- typography inconsistency
- moderate UX issue

P3:

- cosmetic polish
- minor alignment
- subtle refinement

Always address the highest-impact problem first.

---

# 14. CONTROLLED ITERATIONS

Each iteration should have ONE primary objective.

Before changing code, determine:

1. What problem am I solving?
2. What evidence proves the problem exists?
3. What change should solve it?
4. What could the change break?
5. How will I verify the result?

Avoid large unrelated batches of changes.

---

# 15. REGRESSION PROTECTION

An improvement in one area is not acceptable if it significantly damages another area.

Compare the current iteration with the latest accepted iteration.

Look for:

- visual regressions
- functional regressions
- responsive regressions
- accessibility regressions
- technical regressions

If a regression is detected:

- repair it
- or revert the problematic change

Do not silently accept regressions.

---

# 16. ANTI-THRASHING

If the same issue survives two iterations:

STOP making superficial changes.

Instead:

1. inspect the underlying cause
2. reconsider the implementation strategy
3. identify what failed previously
4. record the failed approach
5. make a deliberate correction

Do not endlessly tweak the same values.

---

# 17. EVIDENCE REQUIREMENT

Never claim:

- "tested" when it was not tested
- "verified" when it was not verified
- "looks correct" without inspection
- "mobile works" without mobile verification
- "performance improved" without measurement

When verification is unavailable, explicitly record:

NOT VERIFIED

---

# 18. COMPLETION

The loop may stop when:

- requirements are satisfied
- critical issues are resolved
- the application builds successfully
- important interaction flows work
- responsive behavior is acceptable
- visual quality meets the target
- no material regression exists

Default visual-quality target:

95 / 100

The target can be adjusted when the project requires a different threshold.

---

# 19. FINAL PRINCIPLE

Do not optimize for:

"Generate as much code as possible."

Optimize for:

"Produce the best verified result with the fewest necessary changes."

The objective is:

WORKING

- USABLE
- RESPONSIVE
- VISUALLY COHERENT
- VERIFIED

---

# COUNCIL REVIEW PROTOCOL

Use the available Council skill when a decision benefits from multiple
independent expert perspectives.

Do not invoke Council for routine implementation work, obvious fixes, or
deterministic checks.

Invoke Council when:

- multiple design directions are plausible
- multiple reference websites compete as candidates
- section designs need comparison
- the originality of the design is uncertain
- the design risks becoming generic or template-like
- a major architectural/design decision has meaningful trade-offs
- a rebuild strategy must be selected
- the final visual quality is uncertain
- the agent disagrees with its own evaluation
- a high-impact decision could materially affect the final product

Where appropriate, assign different expert perspectives such as:

- Creative Director
- UI/UX Designer
- Art Director
- Product Designer
- Frontend Engineer
- Accessibility Specialist
- Motion/Interaction Designer
- Brand Designer

The Council must return:

1. consensus
2. major disagreements
3. strongest arguments
4. risks
5. recommended decision
6. confidence level

The final decision remains with the primary Design Loop agent.

Do not blindly follow majority opinion.

---
