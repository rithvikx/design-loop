# Design Constitution

## Purpose

This document defines the visual, interaction, UX, responsive, accessibility,
and implementation principles that govern the project.

It is the source of truth for design quality.

The Design Loop must use this document when:

- creating new interfaces
- modifying existing interfaces
- evaluating visual quality
- making responsive decisions
- choosing between competing design directions
- reviewing component consistency
- deciding whether a change is an improvement
- detecting design drift

The Design Loop must not silently violate these rules.

If a significant rule needs to change, record the reason in:

`design-loop/DECISIONS.md`

and update this document intentionally.

---

# DESIGN INTELLIGENCE OVERRIDE

The Design Constitution may be informed by external research, competitors,
user-provided references, and selected design sections.

However, references are not automatically copied.

The final constitution must represent a synthesized and project-specific design
direction.

The Design Loop should prefer:

USER REFERENCES

> PROJECT REQUIREMENTS
>
> COMPETITIVE INSIGHTS
>
> DESIGN RESEARCH
>
> DESIGN SYNTHESIS
>
> AGENCY QUALITY STANDARD

The goal is not to reproduce another website.

The goal is to understand successful design decisions and create a stronger,
original result appropriate for the current product.

---

# 1. PROJECT DESIGN IDENTITY

## Product Personality

Define the emotional and visual personality of the product.

Examples:

- premium
- editorial
- cinematic
- minimal
- modern
- technical
- sophisticated
- playful
- trustworthy
- bold
- calm
- luxurious
- utilitarian

Current direction:

NOT YET DEFINED

---

## Primary Emotional Goal

When a user sees and uses the product, the interface should communicate:

NOT YET DEFINED

Examples:

- confidence
- trust
- excitement
- exclusivity
- clarity
- simplicity
- sophistication
- speed
- innovation

---

## Design Positioning

The interface should feel:

NOT YET DEFINED

Compared with competing products, the project should aim to be:

NOT YET DEFINED

The design should avoid looking like:

NOT YET DEFINED

---

# 2. DESIGN PRINCIPLES

These principles take priority over individual visual preferences.

## Principle 1 — Clarity Before Decoration

Visual elements should help the user understand:

- what the page is about
- where they are
- what they can do
- what action matters most

Decoration must never compete with core communication.

---

## Principle 2 — Strong Visual Hierarchy

Every important page should have a clear hierarchy.

The user should be able to identify:

1. primary message
2. supporting information
3. primary action
4. secondary actions
5. supporting details

Do not give every element equal visual weight.

---

## Principle 3 — Intentional Whitespace

Whitespace should be intentional.

Do not:

- compress unrelated sections
- create unnecessarily large gaps
- use whitespace inconsistently
- fill empty space merely because it exists

Whitespace should support:

- hierarchy
- rhythm
- readability
- focus
- perceived quality

---

## Principle 4 — Consistency Without Monotony

Repeated UI patterns should feel related.

However, visual consistency does not mean every section must look identical.

Use a consistent underlying design language while allowing:

- hierarchy variation
- layout variation
- content-specific composition
- deliberate visual emphasis

---

## Principle 5 — Design With Evidence

Visual decisions should be based on:

- the project requirements
- the design constitution
- reference material
- browser output
- user experience
- actual implementation constraints

Do not make changes simply because a model "likes" them.

---

# 3. VISUAL LANGUAGE

## Overall Visual Style

Current style:

NOT YET DEFINED

---

## Visual Density

Preferred density:

NOT YET DEFINED

Possible values:

- sparse
- balanced
- dense
- information-rich

The interface should avoid becoming:

NOT YET DEFINED

---

## Composition

Preferred composition principles:

NOT YET DEFINED

Examples:

- strong editorial layouts
- asymmetrical composition
- centered layouts
- grid-based composition
- full-bleed imagery
- modular cards
- large typographic sections

---

## Shape Language

Preferred shape language:

NOT YET DEFINED

Examples:

- sharp corners
- subtle radius
- large rounded corners
- mixed radius system
- geometric
- organic

Do not introduce arbitrary corner-radius values.

Use a consistent radius scale.

---

# 4. TYPOGRAPHY

## Typography Goals

Typography must create hierarchy before decorative effects are introduced.

The hierarchy should clearly distinguish:

- display text
- page titles
- section headings
- subheadings
- body text
- labels
- metadata
- captions
- actions

---

## Font Families

Display:

NOT YET DEFINED

Body:

NOT YET DEFINED

Monospace / technical:

NOT YET DEFINED

---

## Font Weight Rules

Primary heading:

NOT YET DEFINED

Secondary heading:

NOT YET DEFINED

Body:

NOT YET DEFINED

Labels:

NOT YET DEFINED

Do not introduce arbitrary font weights without reason.

---

## Typography Scaling

Desktop display size:

NOT YET DEFINED

Tablet display size:

NOT YET DEFINED

Mobile display size:

NOT YET DEFINED

Body size:

NOT YET DEFINED

Small text:

NOT YET DEFINED

---

## Line Height

Display:

NOT YET DEFINED

Heading:

NOT YET DEFINED

Body:

NOT YET DEFINED

Compact metadata:

NOT YET DEFINED

---

## Typography Rules

Avoid:

- excessive font-size variation
- weak heading hierarchy
- excessively long text lines
- cramped paragraph spacing
- inconsistent capitalization
- arbitrary letter spacing

Typography must remain readable at every supported viewport.

---

# 5. COLOR SYSTEM

## Color Philosophy

The color system should communicate:

NOT YET DEFINED

---

## Primary Colors

Primary:

NOT YET DEFINED

Secondary:

NOT YET DEFINED

Accent:

NOT YET DEFINED

---

## Surface Colors

Primary background:

NOT YET DEFINED

Secondary background:

NOT YET DEFINED

Elevated surface:

NOT YET DEFINED

Muted surface:

NOT YET DEFINED

---

## Text Colors

Primary text:

NOT YET DEFINED

Secondary text:

NOT YET DEFINED

Muted text:

NOT YET DEFINED

Inverse text:

NOT YET DEFINED

---

## Border Colors

Default border:

NOT YET DEFINED

Strong border:

NOT YET DEFINED

Interactive border:

NOT YET DEFINED

---

## Semantic Colors

Success:

NOT YET DEFINED

Warning:

NOT YET DEFINED

Error:

NOT YET DEFINED

Information:

NOT YET DEFINED

---

## Color Rules

Do not introduce new colors merely to solve local styling problems.

Reuse the existing palette whenever appropriate.

A new color should be introduced only when:

- it provides a meaningful semantic purpose
- existing colors cannot solve the problem
- it is consistent with the project identity

---

# 6. SPACING SYSTEM

Use a predictable spacing system.

Preferred scale:

NOT YET DEFINED

Examples may include:

- 4
- 8
- 12
- 16
- 24
- 32
- 48
- 64
- 80
- 96
- 128

Do not randomly introduce:

- 17px
- 27px
- 43px
- 71px

unless there is a deliberate reason.

Spacing should communicate relationships.

Small spacing:
related elements.

Medium spacing:
related groups.

Large spacing:
separate content sections.

Very large spacing:
major compositional transitions.

---

# 7. LAYOUT SYSTEM

## Container

Maximum content width:

NOT YET DEFINED

Minimum side padding:

NOT YET DEFINED

---

## Grid

Desktop:

NOT YET DEFINED

Tablet:

NOT YET DEFINED

Mobile:

NOT YET DEFINED

---

## Section Rhythm

Major sections should have a consistent vertical rhythm.

Do not manually invent unrelated spacing for every section.

---

## Alignment

Preferred alignment:

NOT YET DEFINED

Possible patterns:

- left aligned
- centered
- mixed editorial alignment
- asymmetric alignment

Alignment should be intentional.

---

# 8. RESPONSIVE DESIGN

Responsive design is not simply shrinking the desktop interface.

When moving between breakpoints, the system should preserve:

- hierarchy
- readability
- usability
- visual identity
- interaction clarity

while allowing:

- layout restructuring
- content reordering
- navigation changes
- typography changes
- image crop changes
- component simplification

---

## Desktop

Primary target:

NOT YET DEFINED

---

## Tablet

Primary target:

NOT YET DEFINED

---

## Mobile

Primary target:

NOT YET DEFINED

---

## Responsive Rules

Avoid:

- horizontal scrolling unless intentionally required
- text becoming too small
- controls becoming difficult to tap
- desktop composition simply squeezed into mobile
- inconsistent spacing
- inaccessible navigation
- content disappearing without reason

---

# 9. COMPONENT DESIGN

Components should behave as part of a coherent system.

Important component families include:

- buttons
- navigation
- headers
- cards
- forms
- inputs
- dropdowns
- tabs
- modals
- alerts
- tables
- badges
- tooltips
- pagination
- footers

---

## Component Consistency

A component family should share:

- typography
- spacing
- radius
- states
- interaction behavior
- visual hierarchy

Do not create visually unrelated versions of the same component without a reason.

---

# 10. BUTTONS

## Primary Button

Purpose:

NOT YET DEFINED

Visual hierarchy:

NOT YET DEFINED

---

## Secondary Button

Purpose:

NOT YET DEFINED

Visual hierarchy:

NOT YET DEFINED

---

## Destructive Button

Purpose:

NOT YET DEFINED

Visual treatment:

NOT YET DEFINED

---

## Button States

Every important button should consider:

- default
- hover
- focus
- active
- disabled
- loading
- success/error where applicable

---

# 11. FORMS

Forms must prioritize clarity and error prevention.

Each important form should provide:

- clear labels
- clear input expectations
- visible focus
- helpful validation
- meaningful error messages
- loading state
- success state where appropriate

Avoid relying on placeholder text as the only label.

---

# 12. NAVIGATION

Navigation must make the user's location and available options understandable.

Consider:

- current page
- nested navigation
- mobile navigation
- active states
- keyboard interaction
- menu behavior

Navigation should not become visually impressive at the cost of usability.

---

# 13. IMAGERY

Images should be treated as design elements, not merely inserted into empty spaces.

Evaluate:

- composition
- crop
- aspect ratio
- resolution
- focal point
- relationship to surrounding text
- loading behavior

Do not use poor-quality images simply because they fill the correct dimensions.

---

# 14. ANIMATION AND MOTION

Motion must have a purpose.

Acceptable purposes include:

- feedback
- orientation
- hierarchy
- transition
- revealing content
- communicating state

Avoid animation for decoration alone when it harms usability.

---

## Motion Intensity

Preferred intensity:

NOT YET DEFINED

---

## Duration

Fast interaction:

NOT YET DEFINED

Normal transition:

NOT YET DEFINED

Complex transition:

NOT YET DEFINED

---

## Reduced Motion

Important animations should respect reduced-motion preferences where appropriate.

---

# 15. ACCESSIBILITY PRINCIPLES

Accessibility is part of quality, not a separate optional feature.

Prioritize:

- semantic HTML
- keyboard access
- visible focus
- readable contrast
- accessible names
- clear labels
- understandable error messages
- appropriate heading hierarchy
- meaningful alt text
- usable touch targets

---

# 16. UX PRINCIPLES

Every important screen should answer:

- Where am I?
- What can I do?
- What matters most?
- What happens when I act?
- What went wrong if something fails?
- What should I do next?

---

# 17. ERROR STATES

Errors should be:

- understandable
- actionable
- visible
- appropriately positioned

Avoid generic messages such as:

"Something went wrong."

unless there is genuinely no more useful information available.

---

# 18. LOADING STATES

Loading states should communicate that the system is working.

Use:

- skeletons
- progress indicators
- contextual loading states

when appropriate.

Avoid unnecessary global loading states.

---

# 19. EMPTY STATES

Empty states should explain:

- what is empty
- why it is empty
- what the user can do next

---

# 20. DESIGN ANTI-PATTERNS

Unless explicitly requested, avoid:

- generic AI-generated SaaS layouts
- excessive glassmorphism
- excessive gradients
- random neon accents
- unnecessary 3D elements
- excessive rounded cards
- excessive drop shadows
- decorative animation everywhere
- inconsistent spacing
- too many font sizes
- inconsistent buttons
- arbitrary colors
- visual noise
- large empty areas without compositional purpose
- design patterns copied without relevance

---

# 21. REFERENCE PRIORITY

When reference material exists, prioritize it in this order:

1. explicit user requirements
2. brand requirements
3. reference design intent
4. existing project design system
5. usability
6. accessibility
7. implementation convenience
8. personal stylistic preference

Do not prioritize model preference over explicit requirements.

---

# 22. DESIGN QUALITY STANDARD

A high-quality interface should demonstrate:

- strong hierarchy
- deliberate spacing
- consistent components
- coherent typography
- restrained visual language
- responsive behavior
- clear interactions
- useful feedback
- accessibility
- technical reliability
- absence of obvious visual defects

---

# 23. DESIGN DRIFT RULE

When making repeated changes, periodically compare the current implementation against this document.

If the visual language begins to drift:

1. identify the drift
2. determine why it happened
3. decide whether it is intentional
4. record the decision
5. restore consistency or update the constitution

Do not allow accumulated iterations to slowly redefine the design without an explicit decision.

---

# 24. PROJECT-SPECIFIC RULES

Add project-specific rules below.

## Rule A

NOT YET DEFINED

## Rule B

NOT YET DEFINED

## Rule C

NOT YET DEFINED

---

# 25. CONSTITUTION CHANGE POLICY

This document may change when:

- the user changes the product direction
- the brand changes
- the reference design changes
- usability testing reveals a better direction
- accessibility requirements demand a change
- technical constraints require a deliberate design adaptation

Changes must be intentional and recorded in:

`design-loop/DECISIONS.md`

---

# SKILL INTEGRATION

Before major design or implementation work, the Design Loop must inspect the
available skill registry and select relevant specialist skills.

The selected skill set should be recorded in SESSION.json.

Examples:

- UI/UX design
- frontend development
- animation
- accessibility
- responsive design
- 3D
- WebGL
- ecommerce
- mobile
- desktop
- backend
- security
- performance

Specialized skills should be used when their domain expertise materially
improves the task.

Do not invoke unrelated skills merely because they exist.

# QUALITY BAR RELATIONSHIP

This constitution defines the project's own design language.

External references are used to establish a quality bar, not to replace the
project's identity.

The final design must balance:

- reference quality
- brand identity
- product requirements
- usability
- accessibility
- originality
- technical feasibility

Do not blindly clone the strongest reference.

# GAUNTLET ORIGINALITY RULE

A section may lose a direct visual comparison to a reference while still being
accepted if:

- the difference is intentional
- the current implementation is equally strong or stronger in the context of
  the actual product
- the alternative design better serves the project
- the difference does not represent a material quality deficiency

---

# END OF DESIGN CONSTITUTION
