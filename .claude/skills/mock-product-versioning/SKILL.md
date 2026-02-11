---
name: Mock Product Versioning
description: Version and manage mock products and prototypes enabling iteration and client collaboration
---

# Mock Product Versioning

## Purpose

Systematically version and manage mock products, prototypes, and design iterations. Enable clients to review designs, provide feedback, and collaborate on iterative refinement while maintaining complete version history.

## When to Use This Skill

Use this skill when:
- Creating initial design mockups
- Iterating designs based on feedback
- Presenting design options to clients
- Managing design changes throughout project
- Archiving design evolution
- Handing off designs to development

## Mock Product Types

### Interactive Prototypes
- **Figma prototypes**: Clickable mockups with interactions
- **InVision prototypes**: Screen flows with hotspots
- **Adobe XD prototypes**: Interactive wireframes and designs

### Static Mockups
- **High-fidelity designs**: Pixel-perfect visual designs
- **Wireframes**: Low-fidelity layout structures
- **Design comps**: Photoshop or Sketch compositions

### Demo Applications
- **Frontend demos**: Working HTML/CSS/JS demonstrations
- **CodePen/CodeSandbox**: Interactive component demos
- **Static site generators**: Jekyll, Hugo, Next.js previews

## Versioning Strategy

### Version Number Format
`{Major}.{Minor}.{Iteration}-{Status}`

Examples:
- `1.0.0-draft`: Initial draft mockup
- `1.1.0-review`: Internal design review version
- `2.0.0-client`: Presented to client for feedback
- `2.1.0-revised`: Revised based on client feedback
- `3.0.0-approved`: Client approved design
- `3.0.0-final`: Final design for development handoff

### Version Increment Rules
- **Major** (1.0.0 → 2.0.0): Significant design direction change, major redesign
- **Minor** (1.0.0 → 1.1.0): Refinements, additional screens, component updates
- **Iteration** (1.0.0 → 1.0.1): Small tweaks, color adjustments, copy changes

### Status Tags
- `draft`: Work in progress, not ready for review
- `review`: Under internal design review
- `client`: Presented to client
- `revised`: Updated based on feedback
- `approved`: Client approved
- `final`: Ready for development handoff

## Mock Product Metadata

Track essential information:

```
Mock ID: {unique identifier}
Title: {mock product name}
Version: {version number}
Status: {draft/review/client/revised/approved/final}
Designer: {primary designer}
Created: {date}
Last Modified: {date}
Client Reviewed: {date}
Approved: {date}
Related Requirements: {requirement IDs}
Previous Version: {link to previous version}
File Location: {Figma link or file path}
Notes: {design rationale, feedback summary}
```

## Organization Structure

Organize mocks by project and version:

```
mocks/
├── {client-name}/
│   ├── {project-name}/
│   │   ├── wireframes/
│   │   │   ├── homepage-v1.0.0-draft.fig
│   │   │   ├── homepage-v1.1.0-review.fig
│   │   │   └── homepage-v2.0.0-client.fig
│   │   ├── high-fidelity/
│   │   │   ├── homepage-v1.0.0-draft.fig
│   │   │   ├── homepage-v2.0.0-client.fig
│   │   │   ├── homepage-v2.1.0-revised.fig
│   │   │   └── homepage-v3.0.0-approved.fig
│   │   ├── prototypes/
│   │   │   ├── user-flow-v1.0.0-draft.fig (prototype)
│   │   │   └── user-flow-v2.0.0-client.fig (prototype)
│   │   └── version-history.md
```

## Design Iteration Workflow

### Step 1: Create Initial Draft
- Design initial mockup based on requirements
- Version: `1.0.0-draft`
- Document design decisions and rationale

### Step 2: Internal Design Review
- Present to Design Director and peers
- Gather feedback and critique
- Iterate and refine
- Version: `1.1.0-review`

### Step 3: Client Presentation
- Package mockup for client review
- Present design with rationale
- Gather client feedback
- Version: `2.0.0-client`

### Step 4: Incorporate Feedback
- Analyze client feedback
- Prioritize changes
- Implement revisions
- Version: `2.1.0-revised`

### Step 5: Client Approval
- Present revised design
- Obtain client sign-off
- Archive approved version
- Version: `3.0.0-approved`

### Step 6: Development Handoff
- Prepare design specifications
- Export assets and resources
- Brief development team
- Version: `3.0.0-final`

## Client Collaboration Features

### Design Review Sessions
- Schedule review meetings
- Present mockups in context
- Walk through user flows
- Demonstrate interactions
- Document feedback in real-time

### Feedback Management
- Collect feedback systematically
- Categorize by priority (must-have, nice-to-have)
- Map feedback to requirements
- Track implementation status

### Version Comparison
- Show before/after comparisons
- Highlight changes between versions
- Explain design rationale
- Validate alignment with feedback

## Change Tracking

Document changes between versions:

```
Version 2.1.0-revised (changes from 2.0.0-client)
- Homepage: Updated hero image per client preference
- Navigation: Changed from hamburger to always-visible menu
- Color scheme: Adjusted primary color from blue to teal (#008080)
- Typography: Increased body font size from 16px to 18px
- Product cards: Added "Add to Cart" button to card footer
- Footer: Removed social media icons per client request

Client Feedback Addressed:
✓ "Hero image should be more aspirational" → Updated image
✓ "Navigation is hard to find" → Made navigation always visible
✓ "Colors feel too corporate" → Warmed up color palette
✓ "Text is too small" → Increased font sizes
✓ "Make add to cart more prominent" → Added to product cards
✗ "Add customer testimonials section" → Deferred to v3.0.0
```

## Design Handoff Package

When handing off to development:

```
Final Design Package v3.0.0-final:

1. Design Files:
   - Figma file (with developer mode enabled)
   - Exported PNG/SVG assets
   - Icon library
   - Image assets (optimized)

2. Design Specifications:
   - Style guide (typography, colors, spacing)
   - Component library documentation
   - Responsive breakpoints
   - Interaction specifications

3. Design Rationale:
   - Key design decisions and why
   - User research insights
   - Accessibility considerations

4. Requirements Traceability:
   - Mapping of designs to requirements
   - Coverage verification

5. Development Notes:
   - Technical constraints or considerations
   - Third-party libraries or dependencies
   - Browser compatibility requirements
```

## Quality Standards

Mock products must meet:
- **Alignment**: Designs align with requirements
- **Usability**: Designs follow UX best practices
- **Accessibility**: Designs meet WCAG guidelines
- **Consistency**: Designs use consistent patterns and styles
- **Fidelity**: Appropriate detail for design phase
- **Documentation**: Design decisions are documented

## Tools and Platforms

### Design Tools
- Figma (preferred for collaboration)
- Adobe XD
- Sketch
- InVision
- Framer

### Prototyping Tools
- Figma Prototype mode
- InVision
- Principle
- ProtoPie

### Version Control
- Figma version history
- Abstract (for Sketch)
- Git (for code-based designs)

## Success Criteria

Mock product versioning succeeds when:
- Design evolution is fully documented
- All versions are accessible and retrievable
- Client feedback is systematically incorporated
- Approved designs are clearly identified
- Development handoff is complete and clear
- Design rationale is preserved for future reference

## Example Usage

**Scenario**: E-commerce homepage design

```
v1.0.0-draft (2026-02-20):
- Initial wireframe based on requirements
- Basic layout structure
- Placeholder content
- Internal draft only

v1.1.0-review (2026-02-22):
- Refined layout based on peer feedback
- Added visual hierarchy
- Improved information architecture
- Presented to Design Director → Approved for client presentation

v2.0.0-client (2026-02-25):
- High-fidelity design
- Final colors, typography, imagery
- Interactive prototype
- Presented to client → Feedback received

Client Feedback:
1. Hero section needs stronger call-to-action
2. Product grid should show 4 columns instead of 3
3. Add customer review section
4. Change "Shop Now" to "Browse Products"

v2.1.0-revised (2026-02-28):
- Incorporated all client feedback
- Updated hero CTA design
- Adjusted grid to 4 columns
- Added reviews section
- Updated button text

v3.0.0-approved (2026-03-01):
- Presented revised design to client
- Client approved
- No further changes requested
- Archived as approved baseline

v3.0.0-final (2026-03-03):
- Prepared development handoff package
- Exported all assets
- Created design specification document
- Handed off to Tech Director
```
