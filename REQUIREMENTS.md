# PROJECT REQUIREMENTS

## Purpose

This document defines what the application must accomplish.

Requirements are divided into:

1. Product requirements
2. Functional requirements
3. UX requirements
4. Visual requirements
5. Responsive requirements
6. Accessibility requirements
7. Technical requirements
8. Performance requirements
9. Integration requirements
10. Security requirements
11. Deployment requirements
12. Acceptance criteria

The Design Loop must use this document to determine whether the project is
actually complete.

Do not invent requirements that have not been provided or reasonably inferred
from the existing product.

When information is unavailable, mark it as:

NOT PROVIDED

---

# 1. PRODUCT OVERVIEW

## Product Name

NOT PROVIDED

## Product Type

NOT PROVIDED

Examples:

- marketing website
- e-commerce website
- SaaS application
- dashboard
- portfolio
- booking platform
- marketplace
- internal tool
- mobile web application

## Product Goal

NOT PROVIDED

## Target Users

NOT PROVIDED

## Primary User Problem

NOT PROVIDED

## Primary User Action

NOT PROVIDED

## Business Goal

NOT PROVIDED

---

# 2. SCOPE

## In Scope

Add all functionality that must be implemented.

- NOT PROVIDED

## Out of Scope

Explicitly list functionality that should not be implemented during this
project.

- NOT PROVIDED

Do not expand the scope merely because additional features appear useful.

---

# 3. CORE USER JOURNEYS

Define the important journeys.

## User Journey 1

Name:

NOT PROVIDED

Expected flow:

1. NOT PROVIDED
2. NOT PROVIDED
3. NOT PROVIDED

Success condition:

NOT PROVIDED

---

## User Journey 2

Name:

NOT PROVIDED

Expected flow:

1. NOT PROVIDED
2. NOT PROVIDED
3. NOT PROVIDED

Success condition:

NOT PROVIDED

---

## User Journey 3

Name:

NOT PROVIDED

Expected flow:

1. NOT PROVIDED
2. NOT PROVIDED
3. NOT PROVIDED

Success condition:

NOT PROVIDED

---

# 4. FUNCTIONAL REQUIREMENTS

## Authentication

Required:

NOT PROVIDED

Requirements:

- sign in
- sign out
- registration
- password reset
- session handling

Mark unused functionality explicitly as:

NOT REQUIRED

---

## Navigation

Required routes:

- NOT PROVIDED

Navigation behavior:

NOT PROVIDED

---

## Forms

Required forms:

- NOT PROVIDED

Each important form must define:

- required fields
- validation
- submission behavior
- success behavior
- error behavior
- loading behavior

---

## Data

Required data:

NOT PROVIDED

Data sources:

NOT PROVIDED

---

## Search

Required:

NOT PROVIDED

Search behavior:

NOT PROVIDED

---

## Filtering

Required:

NOT PROVIDED

Filtering behavior:

NOT PROVIDED

---

## CRUD

Required resources:

NOT PROVIDED

Operations:

- Create
- Read
- Update
- Delete

---

## Notifications

Required notification behavior:

NOT PROVIDED

---

## Other Functional Requirements

- NOT PROVIDED

---

# 5. PAGE / SCREEN REQUIREMENTS

## Page 1

Name:

NOT PROVIDED

Purpose:

NOT PROVIDED

Required sections:

- NOT PROVIDED

Required actions:

- NOT PROVIDED

Required states:

- loading
- empty
- error
- success
- NOT PROVIDED

---

## Page 2

Name:

NOT PROVIDED

Purpose:

NOT PROVIDED

Required sections:

- NOT PROVIDED

Required actions:

- NOT PROVIDED

Required states:

- NOT PROVIDED

---

# 6. UX REQUIREMENTS

The interface must:

- make the primary action obvious
- communicate system state
- provide meaningful feedback
- handle errors clearly
- maintain navigation context
- support expected user workflows
- prevent avoidable user errors
- avoid unnecessary friction

Project-specific UX requirements:

- NOT PROVIDED

---

# 7. VISUAL REQUIREMENTS

Reference materials:

- NOT PROVIDED

Required visual direction:

NOT PROVIDED

Required:

- typography
- spacing
- visual hierarchy
- imagery
- layout
- colors
- responsive composition
- interaction states

Project-specific visual requirements:

- NOT PROVIDED

---

# 8. RESPONSIVE REQUIREMENTS

The product must work across:

- desktop
- laptop
- tablet
- mobile

Primary target viewport sizes:

- 1440px
- 1280px
- 1024px
- 768px
- 390px

Additional target sizes:

NOT PROVIDED

The interface must not have unintended:

- horizontal scrolling
- clipping
- broken grids
- inaccessible controls
- unreadable text
- navigation failures

---

# 9. ACCESSIBILITY REQUIREMENTS

Required accessibility level:

NOT PROVIDED

Minimum expectations:

- semantic HTML
- keyboard navigation
- visible focus
- appropriate labels
- accessible names
- readable contrast
- heading hierarchy
- meaningful alt text
- usable touch targets

Additional requirements:

- NOT PROVIDED

---

# 10. TECHNICAL REQUIREMENTS

## Frontend

Framework:

NOT PROVIDED

Language:

NOT PROVIDED

Styling:

NOT PROVIDED

Component library:

NOT PROVIDED

---

## Backend

Framework:

NOT PROVIDED

Runtime:

NOT PROVIDED

Database:

NOT PROVIDED

---

## APIs

Required APIs:

- NOT PROVIDED

Authentication:

NOT PROVIDED

---

## Package Manager

NOT PROVIDED

---

## Environment

Development:

NOT PROVIDED

Production:

NOT PROVIDED

---

# 11. PERFORMANCE REQUIREMENTS

Expected:

- fast initial load
- optimized images
- minimal unnecessary JavaScript
- stable layout
- responsive interaction

Specific performance targets:

NOT PROVIDED

Do not fabricate measurements.

---

# 12. SECURITY REQUIREMENTS

Consider:

- authentication security
- authorization
- input validation
- XSS protection
- CSRF where relevant
- secure API handling
- secret management
- dependency security
- user data protection

Project-specific security requirements:

NOT PROVIDED

---

# 13. SEO REQUIREMENTS

Required:

NOT PROVIDED

Potential requirements:

- page titles
- metadata
- Open Graph
- structured data
- canonical URLs
- semantic HTML
- sitemap
- robots.txt

Only implement those that are actually relevant.

---

# 14. ANALYTICS REQUIREMENTS

Required:

NOT PROVIDED

Possible:

- page views
- conversion events
- user interactions
- form submissions

---

# 15. INTEGRATIONS

Required external systems:

- NOT PROVIDED

Examples:

- payment gateway
- CRM
- WhatsApp
- email
- maps
- analytics
- CMS
- authentication provider
- storage provider

---

# 16. CONTENT REQUIREMENTS

Content source:

NOT PROVIDED

Rules:

- do not invent real business information
- do not fabricate testimonials
- do not fabricate prices
- do not fabricate statistics
- do not fabricate reviews
- do not fabricate customer information

Placeholder content should be clearly identified when actual content is missing.

---

# 17. DEPLOYMENT REQUIREMENTS

Hosting:

NOT PROVIDED

Domain:

NOT PROVIDED

Build process:

NOT PROVIDED

Environment variables:

NOT PROVIDED

Deployment restrictions:

NOT PROVIDED

---

# 18. QUALITY REQUIREMENTS

The project should satisfy:

## Functional

All critical workflows work.

## Visual

The design follows the Design Constitution.

## UX

The interface is understandable and usable.

## Responsive

Important layouts work across supported viewport sizes.

## Accessibility

Important interactions are accessible.

## Technical

The application builds and does not contain unresolved critical runtime errors.

## Performance

No obvious performance defects exist.

---

# 19. ACCEPTANCE CRITERIA

The project is complete when:

- critical functionality works
- required pages exist
- required interactions work
- required APIs work
- build passes
- important tests pass
- no critical runtime errors remain
- responsive behavior is acceptable
- important accessibility requirements are satisfied
- visual quality satisfies the Design Constitution
- reference requirements are satisfied where applicable
- no material regressions remain

Default overall quality target:

95 / 100

---

# 20. REQUIREMENT STATUS

Each requirement should eventually have one of these states:

```text
NOT STARTED
IN PROGRESS
BLOCKED
IMPLEMENTED
VERIFIED
REJECTED
OUT OF SCOPE
```

Do not mark a requirement VERIFIED without evidence.

---

# 21. REQUIREMENT CHANGE POLICY

When requirements change:

- update this document
- identify affected pages/components
- identify potential regressions
- record the decision in DECISIONS.md
- update STATE.json
- re-evaluate affected areas

Do not silently change requirements during implementation.

---

# RESEARCH REQUIREMENTS

Before implementation, determine:

- whether the user has provided references
- whether the user has provided competitors
- whether independent competitor research is required
- whether industry design research is required

For a new project, design research should normally occur before implementation.

---

# DESIGN SYNTHESIS REQUIREMENTS

Before major implementation begins, the project should have:

- reference analysis
- section-level analysis
- design scoring
- selected reference patterns
- design direction
- originality strategy
- template-risk assessment

---

# SKILL REQUIREMENTS

The Design Loop should inspect available specialized skills and select those
relevant to the project.

The implementation should use the selected skills where available.

---

# GRAPHIFY REQUIREMENT

After the final accepted implementation state, Graphify should be updated when
available.

The final project state should be synchronized with the Graphify knowledge
graph before completion.

---

# REBUILD REQUIREMENT

When the user requests a redesign while keeping existing content:

- preserve content
- preserve required functionality
- preserve business/data requirements
- research a new design direction
- do not simply restyle the existing UI
- rebuild the visual system where appropriate

---

# INITIAL STATE

The Design Loop starts from:

- this REQUIREMENTS document
- the Design Constitution
- SKILL_REGISTRY.json
- AGENCY_QUALITY_STANDARD.md
- any user-provided references, requirements, or content

No decisions are assumed until explicitly made and recorded in SESSION.json

# FINAL OUTPUT REQUIREMENTS

Before accepting a project as complete, the Design Loop must produce:

- Final Design System
- Requirements Checklist
- Design Constitution
- Design Analysis Report
- Session JSON

These outputs form the complete project record.

# GAUNTLET REQUIREMENT

For high-quality design projects, establish a quality bar before final
implementation.

The quality bar should contain:

- user references where provided
- relevant competitor references
- strongest discovered references
- section-specific reference winners

The final implementation must pass independent quality review.

---

# AGENCY-LEVEL REQUIREMENT

The application must not be accepted merely because it resembles a polished
template.

The project should demonstrate:

- distinctive visual identity
- intentional art direction
- strong hierarchy
- product-specific composition
- meaningful interaction
- responsive excellence
- technical reliability

---

# GAUNTLET ACCEPTANCE

The project should not be considered complete while a material high-impact
quality gap remains between the current implementation and the established
quality bar.

---

END OF REQUIREMENTS
