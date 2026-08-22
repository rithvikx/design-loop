# Task Decomposition and Coupling Protocol

## Purpose

Determine how the Design Loop should divide work between specialist skills or
agents.

This handles the important lesson from the Gauntlet research:

**Don't throw a bunch of agents at tightly coupled work.**

The system must avoid uncontrolled parallelism.

---

# 1. DECOMPOSITION PRINCIPLE

First understand the product.

Then determine the smallest meaningful units that can be:

- implemented
- evaluated
- improved
- verified

independently.

The units should be meaningful to the actual product, not arbitrary files.

---

# 2. POSSIBLE UNITS

Depending on the project:

- page
- section
- component
- user journey
- interaction
- animation
- data flow
- API feature
- responsive system
- 3D scene
- visual subsystem

---

# 3. COUPLING ANALYSIS

For every proposed work unit, classify it:

LOW COUPLING
MEDIUM COUPLING
HIGH COUPLING

---

# 4. LOW COUPLING

Examples:

- independent marketing sections
- isolated content components
- separate static pages
- independent research tasks

These may be parallelized when safe.

---

# 5. MEDIUM COUPLING

Examples:

- cards sharing a design system
- page sections sharing typography
- related responsive components

Parallel work may be allowed with controlled boundaries.

---

# 6. HIGH COUPLING

Examples:

- global design tokens
- typography system
- navigation + responsive navigation
- shared component architecture
- animation timeline
- 3D lighting + materials + scene composition
- database schema + dependent APIs
- payment architecture
- major state management

These should normally be owned sequentially by one lead or tightly coordinated
team.

---

# 7. PARALLELIZATION RULE

Never parallelize merely because more agents are available.

Parallelize only when:

- responsibilities are distinct
- files/components are sufficiently isolated
- changes are unlikely to conflict
- evaluation can be performed independently

---

# 8. SEQUENTIAL OWNERSHIP

When work is highly coupled:

1. assign one owner
2. let the owner inspect the whole system
3. implement the change
4. evaluate it
5. integrate it
6. run regression checks
7. then move to the next coupled task

---

# 9. SPECIALIST SELECTION

The decomposition layer should work with the Skill Registry.

Example:

3D website:

- 3D specialist
- WebGL specialist
- motion specialist
- frontend specialist
- performance specialist

Do not invoke specialists that do not materially contribute.

---

# 10. GAUNTLET INTEGRATION

After a specialist completes a meaningful unit:

run independent evaluation when the unit affects important product quality.

Do not allow each specialist to declare its own work successful without
verification.

---

# 11. RECOMPOSITION

After independent work:

1. integrate
2. run the application
3. run cross-system QA
4. evaluate visual consistency
5. evaluate technical consistency
6. run Gauntlet

A set of individually good sections can still form a poor whole.

---

# END OF DECOMPOSITION PROTOCOL
