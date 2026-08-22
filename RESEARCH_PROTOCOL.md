# Design Research Protocol

## Purpose

Before building a new product, the Design Loop must understand the visual
language, interaction patterns, information architecture, and competitive
landscape relevant to the requested product.

The purpose of research is not to copy another website.

The purpose is to identify high-quality patterns and synthesize them into an
original design direction appropriate for the project.

---

# 1. RESEARCH INTAKE

Before implementation, ask the user:

1. Do you have reference websites?
2. Do you have competitor websites?
3. Do you have Figma designs, screenshots, videos, or other visual references?
4. Are there websites whose visual language you specifically like?
5. Are there websites or design patterns you specifically dislike?

Do not block the project indefinitely waiting for references.

If the user has none, continue automatically into independent research.

---

# 2. USER-PROVIDED REFERENCES

User-provided references have highest priority.

For every provided URL:

1. open the website
2. inspect the actual interface
3. scroll through the page
4. identify meaningful sections
5. capture relevant screenshots
6. inspect navigation
7. inspect interactions
8. inspect responsive behavior when possible
9. record strengths
10. record weaknesses
11. score the reference

Do not rely only on search-result descriptions.

---

# 3. COMPETITOR DISCOVERY

If the product has a recognizable industry:

search for relevant competitors and strong reference websites.

Example categories:

real estate:

- real estate developers
- luxury property developers
- property marketplaces
- architectural property websites

ecommerce:

- premium ecommerce brands
- category leaders
- high-conversion stores

finance:

- fintech platforms
- banking products
- premium financial services

travel:

- hotel platforms
- premium resorts
- travel marketplaces

For every discovered website, decide whether it is:

- direct competitor
- indirect competitor
- design reference
- interaction reference
- information-architecture reference
- low-quality example
- irrelevant

---

# 4. DO NOT RESEARCH ONLY BY HOMEPAGE

A website must be evaluated section by section.

Potential sections include:

- announcement bar
- navigation
- hero
- trust/credibility
- brand story
- feature showcase
- product showcase
- property listings
- services
- statistics
- testimonials
- case studies
- gallery
- pricing
- comparison
- FAQ
- CTA
- footer

Add project-specific sections when necessary.

---

# 5. SECTION EXTRACTION

For every website, identify:

- section name
- position
- purpose
- visual structure
- information hierarchy
- typography
- spacing
- imagery
- interaction
- animation
- responsiveness
- strengths
- weaknesses

Example:

Hero:

Purpose:
Communicate the value proposition immediately.

Structure:
Large heading + supporting text + primary action + image.

Strength:
Strong visual hierarchy.

Weakness:
CTA visibility on mobile is weak.

---

# 6. SECTION SCORING

Each section receives a score.

Evaluate:

- visual quality
- hierarchy
- UX
- composition
- originality
- usability
- responsiveness
- brand suitability
- technical plausibility

Use the Design Rubric.

Do not score based purely on personal taste.

---

# 7. CROSS-SITE COMPARISON

After analyzing multiple websites:

identify the best-performing section for each important page section.

Example:

Best Hero:
Reference A

Best Navigation:
Reference C

Best Product Section:
Reference B

Best Testimonials:
Reference D

Best Mobile Experience:
Reference C

Best CTA:
Reference B

---

# 8. DESIGN SYNTHESIS

Do not copy an entire website.

Instead synthesize the strongest relevant patterns.

The system must answer:

- What makes the references successful?
- Which patterns are appropriate for this product?
- Which patterns are overused?
- Which patterns should be avoided?
- What can be combined?
- What should be redesigned from first principles?
- How can the final product have a distinctive identity?

---

# 9. ORIGINALITY REQUIREMENT

The final design must not simply become:

"Reference A + Reference B."

It must have its own:

- typography system
- color system
- composition
- spacing system
- imagery direction
- component treatment
- interaction language
- brand personality

References are inputs.

The final design is a synthesis.

---

# 10. TEMPLATE-RISK EVALUATION

Before implementation, estimate whether the planned design resembles a
generic AI/template website.

Look for:

- generic SaaS hero
- predictable 3-card layouts
- repetitive rounded cards
- excessive gradients
- excessive glassmorphism
- generic testimonial sections
- generic "trusted by" section
- identical CTA patterns
- predictable section rhythm
- overuse of pills
- weak art direction
- no distinctive composition

If template risk is high:

do not begin implementation.

Return to design synthesis.

---

# 11. RESEARCH STOP CONDITION

Research is complete when:

- important user references have been analyzed
- sufficient competitors have been analyzed
- relevant design references have been analyzed
- major page sections have reference evidence
- a section-level synthesis exists
- the design direction is documented
- template risk is acceptable

---

# 12. RESEARCH MEMORY

Store:

- URLs
- screenshots
- scores
- section analysis
- strengths
- weaknesses
- selected references
- rejected references
- synthesis decisions

inside:

`design-loop/research/`

and update:

`design-loop/REFERENCE_ATLAS.json`

---

# 13. RESEARCH INTEGRITY

Never claim a website was inspected if it was not actually opened.

Never invent:

- design scores
- competitor information
- website features
- visual properties
- performance characteristics

When something cannot be verified:

NOT VERIFIED

# QUALITY-BAR RESEARCH

When selecting references, do not ask only:

"Which website looks nice?"

Ask:

"Which website provides the strongest relevant quality bar for this particular
project?"

The strongest reference may differ by section.

Example:

Hero:
Reference A

Property showcase:
Reference C

Navigation:
Reference B

Mobile experience:
Reference D

The research system should therefore establish both:

1. an overall quality bar
2. section-specific quality bars

# GAUNTLET REFERENCE SELECTION

Before implementation, identify:

- primary quality reference
- secondary quality references
- section-specific references
- references that should NOT be copied
- known weaknesses of the references

The final reference set should challenge the builder rather than merely provide
visual inspiration.

---

# END OF RESEARCH PROTOCOL
