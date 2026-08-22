# Design Loop Workflow

## Purpose

Execute the Universal Design Loop against the current web project.

The goal is to continuously improve the actual running application through
inspection, implementation, browser verification, evaluation, and controlled
iteration.

Do not stop merely because the application builds or the requested code has
been written.

---

# UNIVERSAL DESIGN LOOP

EXECUTE IN THIS ORDER:

1. INITIALIZE
2. DETECT MODE
3. LOAD REQUIREMENTS
4. DISCOVER SKILLS
5. RESEARCH
6. BUILD DESIGN QUALITY BAR
7. DESIGN SYNTHESIS
8. COUNCIL REVIEW WHEN NECESSARY
9. DECOMPOSE WORK
10. IMPLEMENT
11. BROWSER VERIFY
12. GAUNTLET CRITIC
13. IDENTIFY LARGEST GAP
14. FIX LARGEST GAP
15. REGRESSION CHECK
16. REPEAT
17. FINAL QUALITY GATE
18. GRAPHIFY UPDATE
19. FINALIZE

# DESIGN INTELLIGENCE PHASE

Before beginning major implementation:

1. Determine the operating mode.
2. Load the skill registry.
3. Identify relevant specialist skills.
4. Ask the user for reference websites when appropriate.
5. Ask the user for competitor references when appropriate.
6. If references are unavailable, perform independent research.
7. Inspect real websites using available browser tools.
8. Analyze references section by section.
9. Score references using DESIGN_RUBRIC.json.
10. Update REFERENCE_ATLAS.json.
11. Update SECTION_LIBRARY.json.
12. Select the strongest relevant patterns.
13. Create a design synthesis.
14. Evaluate template risk.
15. If template risk is too high, repeat research/synthesis.
16. Update DESIGN_CONSTITUTION.md with the project-specific direction.
17. Only then proceed to architecture and implementation.

Do not skip this phase for a new project unless the user explicitly asks for
implementation without research.

# COUNCIL PHASE

Use `COUNCIL_PROTOCOL.md` when the project reaches a strategic decision that
would benefit from independent specialist perspectives.

Do not invoke Council for routine work.

# DECOMPOSITION PHASE

Before parallelizing:

1. load `DECOMPOSITION_PROTOCOL.md`
2. identify coupled systems
3. classify work units
4. parallelize only low-coupling work
5. keep high-coupling work sequentially owned

# GAUNTLET PHASE

After a meaningful implementation milestone:

1. load `GAUNTLET_PROTOCOL.md`
2. load `QUALITY_BAR.json`
3. load `CRITIC_PROTOCOL.md`
4. inspect the real browser output
5. inspect relevant references
6. perform independent critique
7. compare current implementation against the quality bar
8. determine CURRENT WINS / REFERENCE WINS / INCONCLUSIVE
9. identify the largest remaining quality gap
10. create the next focused objective
11. fix it
12. re-run browser verification
13. perform regression verification
14. update state
15. repeat until the Gauntlet exit conditions are satisfied

# FINAL QUALITY GATE

Do not finish merely because requirements are implemented.

Confirm:

- functional requirements
- design constitution
- agency quality standard
- visual quality
- responsive quality
- accessibility
- technical quality
- performance
- regression status
- Gauntlet result
- Graphify synchronization

---

# 1. INITIALIZE

First load:

- `design-loop/SKILL.md`
- `design-loop/DESIGN_CONSTITUTION.md`
- `design-loop/REQUIREMENTS.md`
- `design-loop/STATE.json`
- `design-loop/ISSUES.json`
- `design-loop/PROGRESS.md`
- `design-loop/DECISIONS.md`

If one of these files does not exist:

- create it using the appropriate structure
- do not invent project requirements
- record missing information as `UNKNOWN` or `NOT PROVIDED`

Determine:

- project framework
- package manager
- development command
- build command
- test command
- lint/typecheck commands
- browser/testing tools available
- current application status

---

# 2. DETERMINE CURRENT PHASE

Read `STATE.json`.

Possible phases:

- `initialization`
- `baseline`
- `implementation`
- `visual_review`
- `ux_review`
- `responsive_review`
- `technical_review`
- `regression_check`
- `completed`

Continue from the current state.

Do not unnecessarily restart completed phases.

---

# 3. INSPECT THE PROJECT

Before modifying anything:

- inspect repository structure
- inspect relevant source files
- inspect existing components
- inspect routes
- inspect styling
- inspect assets
- inspect existing tests
- inspect API/data dependencies
- inspect current design system

Identify:

1. what already works
2. what is incomplete
3. what is broken
4. what visually conflicts with the design constitution
5. what requirements are not yet satisfied

Do not rewrite working functionality without a reason.

---

# 4. ESTABLISH BASELINE

If this is the first run:

1. start the application
2. open the application in the browser
3. verify the initial state
4. capture screenshots
5. check console errors
6. check failed network requests
7. run available build/test/lint/type checks
8. check important interactions
9. test important responsive sizes

Save evidence in:

```text
design-loop/screenshots/000/
design-loop/evaluations/000.json
```

Update:

- `design-loop/STATE.json`
- `design-loop/ISSUES.json`
- `design-loop/PROGRESS.md`

Do not begin visual refinement before establishing a useful baseline when
a baseline is possible.

---

# 5. IDENTIFY THE HIGHEST-VALUE NEXT TASK

Read:

- requirements
- design constitution
- current issues
- previous evaluation
- previous accepted state

Choose the single highest-impact unresolved problem.

Priority order:

- `P0` → Critical
- `P1` → Major
- `P2` → Moderate
- `P3` → Polish

If multiple issues have the same priority, choose the one that:

- affects the largest part of the product
- affects core user flows
- produces the largest visual/UX improvement
- reduces future rework

Do not randomly choose tasks.

---

# 6. DEFINE THE ITERATION OBJECTIVE

Before editing, state internally:

```text
Iteration:
<current iteration>

Primary objective:
<one problem>

Evidence:
<why the problem exists>

Expected improvement:
<what should become better>

Potential regression risks:
<what might break>
```

Only then modify the project.

---

# 7. IMPLEMENT THE CHANGE

Implement the smallest coherent change that addresses the selected objective.

Rules:

- preserve existing functionality
- reuse existing components when appropriate
- follow the design constitution
- avoid unrelated refactoring
- avoid unnecessary dependencies
- avoid speculative features
- maintain existing architecture unless evidence requires a change

After implementation, perform basic code validation.

---

# 8. RUN THE APPLICATION

Start or restart the development environment when necessary.

Use the project's actual commands.

Do not invent commands.

Wait until the application is actually available.

If the application fails to start:

- inspect the error
- fix the startup problem
- re-run the application
- do not proceed to visual evaluation until the application is accessible

---

# 9. BROWSER VERIFICATION

Open the actual running application.

Verify:

- page rendering
- navigation
- important interactions
- buttons
- forms
- menus
- dialogs
- animations
- loading states
- error states
- important API/data flows

Inspect:

- console errors
- runtime exceptions
- network failures
- broken assets
- broken routes

Record evidence.

Do not claim verification without actually performing it.

---

# 10. CAPTURE VISUAL EVIDENCE

Capture screenshots for the relevant pages and states.

At minimum, when applicable:

- Desktop: 1440px
- Tablet: 768px
- Mobile: 390px

Use additional sizes for responsive-critical applications.

Store screenshots in:

```text
design-loop/screenshots/<iteration>/
```

Use descriptive filenames.

Example:

- `homepage-desktop.png`
- `homepage-tablet.png`
- `homepage-mobile.png`
- `dashboard-desktop.png`
- `mobile-menu-open.png`
- `checkout-error.png`

---

# 11. VISUAL REVIEW

Evaluate the new state against:

- the requirements
- the design constitution
- reference designs
- the previous accepted iteration

Review:

- composition
- hierarchy
- spacing
- alignment
- typography
- colors
- imagery
- component consistency
- visual rhythm
- interaction states
- motion
- responsive composition

Identify concrete problems.

Do not simply say:

> "Looks good."

Produce structured findings.

Example:

```json
{
  "category": "visual",
  "severity": "P1",
  "location": "homepage/hero",
  "problem": "Hero content is visually unbalanced.",
  "evidence": "Heading occupies too little visual weight compared with the image.",
  "recommended_action": "Increase heading scale and adjust hero composition."
}
```

---

# 12. UX REVIEW

Evaluate the application as a real user.

Check:

- can the user understand what to do?
- is the primary action obvious?
- is navigation understandable?
- are interactive elements discoverable?
- is feedback provided after actions?
- are errors understandable?
- are forms usable?
- are mobile interactions practical?
- are loading/empty/error states meaningful?

Record problems in `ISSUES.json`.

---

# 13. RESPONSIVE REVIEW

Check relevant viewport sizes.

Focus on:

- overflow
- clipping
- broken grids
- typography scaling
- navigation behavior
- image sizing
- button sizing
- spacing
- touch interaction
- content ordering

A desktop success does not mean the responsive implementation is successful.

---

# 14. TECHNICAL REVIEW

Run available deterministic checks:

- build
- tests
- lint
- typecheck
- route checks
- integration checks
- runtime checks

If a deterministic tool can verify something, prefer it over subjective model judgement.

Record failures as issues.

---

# 15. ACCESSIBILITY REVIEW

Check when tools and project scope allow:

- semantic structure
- keyboard navigation
- focus visibility
- accessible labels
- heading hierarchy
- contrast
- alt text
- form accessibility
- touch target usability
- reduced motion

Record material failures.

---

# 16. PERFORMANCE REVIEW

When practical, inspect:

- image sizes
- JavaScript bundle size
- loading behavior
- unnecessary requests
- layout shifts
- expensive animations
- blocking resources

Use measurements when possible.

Never fabricate a performance score.

---

# 17. CALCULATE ITERATION SCORE

Score the current state:

```text
Visual Quality:        30%
UX:                    20%
Responsive Quality:    15%
Technical Quality:     15%
Performance:           10%
Accessibility:         10%
```

Calculate an overall score from actual evidence.

Example:

```json
{
  "iteration": 7,
  "visual": 92,
  "ux": 94,
  "responsive": 89,
  "technical": 97,
  "performance": 91,
  "accessibility": 93,
  "overall": 92.2
}
```

Save the result to:

```text
design-loop/evaluations/<iteration>.json
```

---

# 18. UPDATE ISSUE TRACKING

For every detected problem:

- create a new issue if it does not exist
- update an existing issue if it already exists
- do not create duplicates
- assign priority
- record the iteration where it was first detected
- record the latest iteration where it remains unresolved

Use:

- `P0` = critical
- `P1` = major
- `P2` = moderate
- `P3` = polish

---

# 19. REGRESSION CHECK

Compare the current iteration with the last accepted iteration.

Check:

- functionality
- visual quality
- UX
- responsiveness
- accessibility
- technical stability

Determine:

- `IMPROVED`
- `NO MATERIAL CHANGE`
- `REGRESSION`

If there is a material regression:

- identify the change that caused it
- repair the regression
- re-run verification
- if necessary, restore the last accepted state

Never accept a lower-quality state merely because one metric improved.

---

# 20. ACCEPT OR REJECT THE ITERATION

Accept the iteration when:

- the primary objective was successfully addressed
- no critical regression exists
- important functionality remains intact
- verification passes
- the new state is equal to or better than the previous accepted state

When accepted:

- update `STATE.json`
- update `PROGRESS.md`
- record important decisions
- save the accepted iteration number

When rejected:

- record the reason
- identify the regression/problem
- repair or revert
- repeat verification

---

# 21. CONTINUE THE LOOP

After accepting an iteration:

- reload `ISSUES.json`
- identify the next highest-value issue
- increment the iteration
- repeat the process

The loop is:

```text
SELECT
→ IMPLEMENT
→ RUN
→ BROWSE
→ CAPTURE
→ EVALUATE
→ SCORE
→ REGRESSION CHECK
→ ACCEPT/REJECT
→ SELECT NEXT ISSUE
```

---

# 22. STOP CONDITIONS

Stop when all of the following are true:

- all critical requirements are satisfied
- no P0 issues remain
- no material P1 issues remain
- build passes
- major user flows work
- responsive behavior is acceptable
- visual quality meets the configured target
- no material regression exists

Default target:

```text
Overall score >= 95
```

The project may stop earlier when the user explicitly requests it.

Do not continue making changes merely to create more iterations after the product
has reached its target.

---

# 23. PLATEAU DETECTION

Do not loop indefinitely.

If two or more consecutive iterations produce negligible improvement:

- stop superficial tweaking
- inspect the root cause
- reconsider the implementation strategy
- check whether the issue is actually subjective
- determine whether further changes are worth the regression risk

If meaningful progress cannot be demonstrated, stop and document the limitation.

---

# 24. ANTI-THRASHING

Never repeatedly modify the same component without learning from previous attempts.

When an issue survives two iterations:

- review previous changes
- review previous evaluations
- inspect the component architecture
- identify the underlying cause
- change the strategy if necessary

Record failed approaches in `DECISIONS.md` when they are significant.

---

# 25. STATE MANAGEMENT

After EVERY iteration update:

- `design-loop/STATE.json`
- `design-loop/ISSUES.json`
- `design-loop/PROGRESS.md`

Update `DECISIONS.md` when a meaningful product/design/architecture decision
is made.

State must always describe the latest actual project condition.

---

# 26. EVIDENCE RULE

Never fabricate evidence.

If something could not be checked, write:

```text
NOT VERIFIED
```

Examples:

- browser unavailable
- screenshot unavailable
- performance tooling unavailable
- accessibility tooling unavailable

Do not silently assume success.

---

# 27. PLATFORM INDEPENDENCE

This workflow must work with any compatible AI coding agent.

Examples:

- Claude Code
- Codex
- Antigravity
- OpenClaw
- Gemini-based coding agents
- other agentic IDEs

Use the platform's available tools for:

- file operations
- terminal commands
- browser interaction
- screenshots
- testing

Do not change the underlying workflow logic just because the agent platform changes.

---

# 28. GRAPHIFY FINALIZATION

After the implementation has reached an accepted final state:

1. Run Graphify update using the available Graphify integration.
2. Prefer an incremental update.
3. Verify that the graph updated successfully.
4. Update STATE.json.
5. Update PROGRESS.md.
6. Record the Graphify synchronization in the final report.
7. Only then mark the project complete.

If Graphify is unavailable, record NOT VERIFIED instead of claiming success.

---

# 29. FINAL REPORT

When the loop completes, produce:

```text
DESIGN LOOP COMPLETE

Iterations:
<number>

Final Score:
<number>/100

Visual:
<number>

UX:
<number>

Responsive:
<number>

Technical:
<number>

Performance:
<number>

Accessibility:
<number>

Issues Resolved:
<number>

Issues Remaining:
<number>

Build:
PASS / FAIL

Tests:
PASS / FAIL / NOT VERIFIED

Browser Verification:
PASS / FAIL / NOT VERIFIED

Responsive Verification:
PASS / FAIL / NOT VERIFIED

Accessibility:
PASS / FAIL / NOT VERIFIED

Known Limitations:
<list>

Final State:
<summary>
```

Be honest about remaining issues and unverified areas.

---

