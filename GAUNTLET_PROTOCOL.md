# Gauntlet Quality Engine

## Purpose

The Gauntlet Quality Engine is the adversarial quality-control layer of the
Universal Design Loop.

Its purpose is to prevent the builder from declaring its own work successful
without independent evidence.

The engine continuously asks:

> Is the current implementation actually good enough when compared against
> the strongest relevant quality bar?

The Gauntlet Quality Engine must not replace the Universal Design Loop.

It operates inside the Universal Design Loop.

The relationship is:

Universal Design Loop:
determines what to build, how to build it, how to manage the project, and when
the project is technically complete.

Gauntlet Quality Engine:
determines whether the current result is actually competitive with the
established quality bar.

---

# 1. CORE LOOP

The Gauntlet loop is:

BUILD
→ RENDER
→ CAPTURE
→ FRESH CRITIC
→ REFERENCE COMPARISON
→ IDENTIFY LARGEST GAP
→ FIX LARGEST GAP
→ VERIFY
→ REGRESSION CHECK
→ REPEAT

Do not replace this with:

BUILD
→ SAME AGENT SAYS "LOOKS GOOD"
→ DONE

---

# 2. INDEPENDENT CRITIC PRINCIPLE

The builder should not be the final authority on whether its own work is good.

Whenever practical, the critic must receive fresh context.

The critic should receive:

- the current rendered result
- relevant screenshots
- relevant reference screenshots
- project requirements
- Design Constitution
- quality rubric
- comparison instructions

The critic should not rely on:

- the builder's explanation
- the builder's confidence
- the builder's statement that something is complete
- the builder's justification for a design choice

The actual artifact is the source of truth.

---

# 3. QUALITY BAR

Every important visual project should have a defined quality bar.

The quality bar may consist of:

- user-provided references
- competitor references
- industry-leading references
- discovered design references
- section-specific reference winners
- project-specific Design Constitution requirements

The quality bar should represent the strongest relevant standard that can
reasonably be achieved.

Do not choose a poor reference merely because it is easy to beat.

---

# 4. REFERENCE A/B COMPARISON

For important visual decisions, compare:

CURRENT IMPLEMENTATION
versus
REFERENCE

The critic should determine:

CURRENT WINS
REFERENCE WINS
INCONCLUSIVE

Do not rely only on a numerical score.

A project can score highly against a rubric and still lose an important
visual comparison against a much stronger reference.

---

# 5. SECTION-LEVEL GAUNTLET

Do not only compare entire websites.

Compare individual sections when appropriate.

Examples:

- hero
- navigation
- property showcase
- product showcase
- testimonials
- pricing
- gallery
- CTA
- footer
- mobile navigation
- interactive map
- 3D scene
- animation sequence

A single website may therefore use:

Hero:
Reference A

Property section:
Reference C

Testimonials:
Reference B

Mobile navigation:
Reference D

The final product must synthesize these patterns into a coherent original system.

---

# 6. LARGEST-GAP PRINCIPLE

After every important evaluation, identify the single largest meaningful gap.

Do not immediately fix twenty small problems.

Example:

Current implementation:

- typography gap: moderate
- spacing gap: minor
- hero composition gap: major
- footer gap: minor

The next objective should be:

hero composition.

The critic must answer:

> What is the biggest remaining difference between the current product and
> the quality bar?

---

# 7. HIGH-LEVERAGE FIX

Each Gauntlet iteration should attempt to fix the highest-leverage issue.

A high-leverage issue is one that:

- affects many users
- affects a major visual section
- strongly affects perceived quality
- affects multiple components
- prevents the design from feeling distinctive
- causes downstream problems
- creates a large gap compared with the quality bar

Do not prioritize a tiny shadow adjustment when the entire hero composition
is weak.

---

# 8. FRESH CRITIC

The critic should receive a fresh evaluation context whenever practical.

Do not pass the builder's internal reasoning into the critic unless it is
specifically necessary.

The critic should judge the output that actually exists.

---

# 9. ADVERSARIAL REVIEW

The critic is not being asked:

"Can you find some things to improve?"

The critic is being asked:

> "Try to disprove the claim that this implementation is good enough."

Look specifically for:

- major visual mismatches
- weak hierarchy
- generic patterns
- template-like composition
- poor interaction
- responsive weaknesses
- weak art direction
- poor typography
- weak imagery
- lack of differentiation
- implementation compromises
- obvious quality gaps

---

# 10. DO NOT CHASE PIXEL PERFECTION BLINDLY

The purpose of the Gauntlet is not endless cosmetic tweaking.

A change should be pursued when it produces meaningful quality improvement.

Do not sacrifice:

- usability
- accessibility
- performance
- maintainability
- functionality

simply to achieve superficial visual similarity.

---

# 11. REGRESSION PROTECTION

After a successful fix:

compare the result against the latest accepted state.

A fix must not introduce material regressions.

Check:

- desktop
- tablet
- mobile
- interaction
- accessibility
- technical stability
- performance

If a regression is introduced:

REJECT OR REPAIR THE ITERATION.

---

# 12. COUPLING AWARENESS

Before assigning tasks to multiple agents, determine whether the tasks are
independent.

Use parallel execution when components can be evaluated and modified
independently.

Use sequential execution when changes are strongly coupled.

Examples of strongly coupled work:

- typography + hero composition
- lighting + 3D materials
- global spacing + all sections
- design tokens + component system
- navigation + responsive layout
- animation timing + scroll architecture

Do not create conflicts by allowing unrelated agents to simultaneously modify
highly coupled systems.

---

# 13. COUNCIL INTEGRATION

Council may be used when:

- multiple design directions are viable
- multiple references are competing
- a major redesign strategy is uncertain
- originality is uncertain
- the current result is controversial
- a high-impact visual decision requires multiple independent perspectives

Council is advisory.

The Design Loop remains the final orchestrator.

Do not invoke Council for every iteration.

---

# 14. WHEN TO RUN GAUNTLET

Gauntlet evaluation should occur:

- after the first meaningful implementation
- after major design changes
- after major section redesigns
- when the visual direction changes
- when a rebuild is completed
- when the user says they dislike the UI
- before final acceptance
- when progress appears to plateau

It does not need to run after every tiny code change.

---

# 15. STOP CONDITIONS

The Gauntlet loop may stop when:

- the major quality gaps are resolved
- the current implementation is competitive with the established quality bar
- remaining differences are minor or subjective
- additional changes create more regression risk than expected benefit
- the quality target is reached
- the user explicitly requests completion

Default recommendation:

Stop when there are no unresolved high-impact quality gaps.

Do not require literal superiority over every reference.

The goal is strong product quality, not blind imitation.

---

# 16. PLATEAU DETECTION

If multiple Gauntlet iterations produce little meaningful improvement:

1. stop superficial tweaking
2. reconsider the design strategy
3. reconsider the selected references
4. ask Council for strategic review when appropriate
5. consider rebuilding the affected section
6. consider switching the relevant specialist skill
7. determine whether the remaining difference is subjective

---

# 17. EVIDENCE

Every important Gauntlet judgement should reference actual evidence.

Examples:

- screenshot
- browser observation
- A/B comparison
- measured result
- test
- accessibility report

Never fabricate a Gauntlet score.

---

# 18. GAUNTLET RESULT

Every major Gauntlet review should produce:

```text
Quality Bar:
<description>

Current Result:
<description>

Comparison:
CURRENT WINS / REFERENCE WINS / INCONCLUSIVE

Largest Gap:
<description>

Severity:
P0 / P1 / P2 / P3

Recommended Fix:
<description>

Confidence:
LOW / MEDIUM / HIGH

Decision:
FIX / ACCEPT / REBUILD / ESCALATE

```

---

# 19. FINAL GAUNTLET GATE

Before final completion:

- Inspect the final application
- Compare against the strongest relevant reference
- Evaluate major sections
- Identify remaining high-impact gaps
- Determine whether any remaining issue justifies another iteration
- perform regression verification
- only then approve final completion

---

# END OF GAUNTLET PROTOCOL
