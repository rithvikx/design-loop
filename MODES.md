# Design Loop Modes

The Design Loop must determine which operating mode best matches the user's
intent before taking major action.

---

# CREATE MODE

Use when:

- building a new product
- building a new website
- creating a new application
- starting from a brief with no meaningful existing implementation

Flow:

INTAKE
→ RESEARCH
→ DESIGN SYNTHESIS
→ ARCHITECTURE
→ BUILD
→ VERIFY
→ REFINE

Research is mandatory unless the user explicitly requests no research.

---

# REBUILD MODE

Use when the user says:

- "I don't like the design."
- "Rebuild the UI."
- "Make it look completely different."
- "Keep the content but redesign it."
- "Start the frontend again."
- "I want a new visual direction."

Rules:

1. Preserve important content and required functionality.
2. Extract existing content and data.
3. Identify existing routes and user journeys.
4. Treat the current UI as a source of content/behavior, not as the desired
   visual direction.
5. Run new design research.
6. Generate a new design direction.
7. Build a new visual system.
8. Compare the result against the old version.
9. Avoid superficial modifications to the old design.

---

# REFINE MODE

Use when the user requests:

- polish
- better spacing
- improved typography
- more premium design
- stronger hierarchy
- visual improvements

Preserve the existing design direction unless evidence suggests it is flawed.

Do not unnecessarily rebuild the application.

---

# FIX MODE

Use for:

- broken UI
- broken responsive behavior
- functionality errors
- visual bugs
- runtime errors
- broken routes

Focus on correcting the existing system.

Do not redesign unrelated components.

---

# RESEARCH MODE

Use when the user asks:

- research competitors
- find design references
- analyze websites
- compare design styles
- identify better UI patterns

Do not begin implementation unless requested.

---

# AUDIT MODE

Use when the user asks:

- review the current website
- score the UI
- identify weaknesses
- perform a design audit
- evaluate accessibility
- evaluate responsiveness

Produce evidence and issues without unnecessarily changing the code.

---

# RESUME MODE

Use when:

- the previous session stopped
- the user reached a model/tool limit
- the agent was interrupted
- the user explicitly provides the configured resume keyword

Read:

- SESSION.json
- STATE.json
- PROGRESS.md
- ISSUES.json
- DECISIONS.md

Continue from the last confirmed checkpoint.

Do not restart completed work.

---

# MODE DETECTION

Interpret the user's intent rather than relying only on exact keywords.

Examples:

"Build me a real estate website."

→ CREATE

"The website is okay but I hate the design."

→ REBUILD

"Make this hero more premium."

→ REFINE

"The navbar is broken on mobile."

→ FIX

"Analyze competitors."

→ RESEARCH

"Tell me what's wrong with this website."

→ AUDIT

"Continue where you stopped."

→ RESUME

---

# MODE PRIORITY

If the request contains multiple intentions:

1. determine the primary mode
2. preserve existing user constraints
3. do not mix modes unnecessarily

Example:

"Keep the content but completely redesign the website using these references."

Primary mode:

REBUILD

Research is therefore part of the rebuild.

---

# GAUNTLET MODE

Use when:

- visual quality is the primary concern
- the current product is being compared to a reference
- the user asks for premium / agency-level quality
- a design section is clearly weaker than the reference
- the builder has completed a major visual milestone

Flow:

CURRENT OUTPUT
→ INDEPENDENT CRITIC
→ REFERENCE COMPARISON
→ LARGEST GAP
→ FIX
→ VERIFY
→ REPEAT

# REBUILD + GAUNTLET

When the user says the existing UI is not good enough:

REBUILD MODE

must include:

RESEARCH
→ NEW DESIGN DIRECTION
→ NEW QUALITY BAR
→ BUILD
→ GAUNTLET

# END OF MODES
