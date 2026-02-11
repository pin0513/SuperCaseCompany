---
name: Traceability Requirements
description: Mandatory traceability practices ensuring accountability from client needs to final deliverables
---

# Traceability Requirements

## Applicability

Applies to: All team members involved in requirements, design, development, and delivery

## Core Principle

Every deliverable must trace back to a client need or business requirement. Every requirement must trace forward to implementation and testing. No orphaned work. No untraceable decisions.

## Mandatory Traceability Links

### Level 1: Client Need → Requirement
**Who**: Requirements Analyst, Requirements Director
**When**: During requirements capture
**What to track**:
- Client meeting/discussion where need was expressed
- Date and participants
- Exact client statement or request
- Business justification
- Priority and urgency

**Example**:
```
Requirement ID: REQ-042
Client Need: "We need customers to save items for later purchase"
Source: Client workshop on 2026-02-18, documented in meetings/2026-02-18-feature-discussion.md
Stated By: Client Product Manager
Business Value: Reduce cart abandonment, increase conversion
Priority: High
```

### Level 2: Requirement → Specification
**Who**: Requirements Director, Design Director, Tech Director
**When**: During design and technical specification
**What to track**:
- Which requirements each specification addresses
- Design decisions and rationale
- Technical approach and alternatives considered
- Assumptions and constraints

**Example**:
```
Specification ID: WISHLIST-SPEC-1.0
Addresses: REQ-042 (Save items for later)
Approach: Authenticated wishlist stored in database
Design Decision: Heart icon to add to wishlist (per UX best practices)
Technical Decision: Separate wishlist table vs. cart_items flag (chose separate table for scalability)
Assumptions: Users must be logged in to use wishlist
```

### Level 3: Specification → Design
**Who**: Design team (Page Designer, Frontend Designer, etc.)
**When**: During design mockup creation
**What to track**:
- Which specifications each design addresses
- Design rationale and user research
- Interaction patterns and states
- Accessibility considerations

**Example**:
```
Design ID: WISHLIST-UI-v2.0
Implements: WISHLIST-SPEC-1.0
Screens: Product detail page (wishlist button), Wishlist page, Account menu (wishlist link)
Interaction: Heart icon (unfilled → filled on click), tooltip "Add to wishlist"
States: Default, hover, loading, added, error
Accessibility: ARIA label "Add to wishlist", keyboard accessible
```

### Level 4: Design → Implementation
**Who**: Software Engineer, Frontend/Backend Tech Experts
**When**: During development
**What to track**:
- Which designs each code module implements
- File/module locations
- Dependencies and integrations
- Technical decisions during implementation

**Example**:
```
Implementation:
Implements Design: WISHLIST-UI-v2.0
Frontend Files:
- components/WishlistButton.tsx
- pages/Wishlist.tsx
- hooks/useWishlist.ts
Backend Files:
- api/wishlist/routes.ts
- services/wishlist.service.ts
- models/wishlist.model.ts
Database: wishlists table, wishlist_items table
Dependencies: Authentication service, product catalog API
```

### Level 5: Implementation → Tests
**Who**: QA Expert, Software Engineer
**When**: During testing
**What to track**:
- Which implementations each test verifies
- Test coverage (unit, integration, E2E)
- Test cases and scenarios
- Acceptance criteria validation

**Example**:
```
Test Suite: Wishlist Tests
Tests Implementation: Wishlist feature (components, services, API)
Unit Tests:
- TC-042-001: WishlistButton component renders correctly
- TC-042-002: Add item to wishlist API succeeds
- TC-042-003: Remove item from wishlist API succeeds
Integration Tests:
- TC-042-010: Complete add-to-wishlist flow (UI → API → DB)
- TC-042-011: Wishlist persists across sessions
E2E Tests:
- TC-042-020: User adds product to wishlist, views wishlist page, moves to cart
Acceptance Criteria Validated:
✓ REQ-042: Users can save items for later purchase
```

### Level 6: Tests → Deliverable
**Who**: Virtual Team Lead, Dimension Leads
**When**: At deliverable completion
**What to track**:
- Which tests validate each deliverable
- Test results and coverage
- Known issues and limitations
- Acceptance status

**Example**:
```
Deliverable: Wishlist Feature v1.0
Validated By: Test suite TC-042-* (all passing)
Test Coverage: 94% (exceeds 80% requirement)
Known Issues: None
Acceptance Status: REQ-042 Complete
Delivered: 2026-03-15
Approved By: Client Product Manager
```

## Traceability Matrix Maintenance

### Matrix Structure
Maintain in spreadsheet or traceability tool:

| Req ID | Client Need | Discussion Ref | Spec | Design | Code Files | Tests | Deliverable | Status |
|--------|-------------|----------------|------|--------|------------|-------|-------------|---------|
| REQ-042 | Save items for later | 2026-02-18 workshop | WISHLIST-SPEC-1.0 | WISHLIST-UI-v2.0 | WishlistButton.tsx, wishlist.service.ts | TC-042-* | Wishlist Feature v1.0 | Complete |

### Update Responsibilities

| Phase | Owner | Update Required |
|-------|-------|-----------------|
| Requirements capture | Requirements Analyst | Add requirement row, link to client need |
| Specification | Requirements/Design/Tech Director | Link specification to requirements |
| Design | Design team | Link designs to specifications |
| Implementation | Software Engineer | Link code to designs and specs |
| Testing | QA Expert | Link tests to implementation and requirements |
| Delivery | Virtual Team Lead | Update status to Complete, link deliverable |

### Update Timing
- **Real-time**: Update matrix as work progresses
- **Checkpoint reviews**: Verify completeness at milestones
- **Deliverable completion**: Final validation before client delivery

## Traceability for Changes

When requirements change:

### Change Impact Analysis Process
1. **Identify change**: What requirement is changing?
2. **Trace forward**: What downstream items are affected?
   - Specifications → Designs → Code → Tests → Deliverables
3. **Assess impact**: Effort, timeline, cost implications
4. **Communicate**: Inform all affected teams
5. **Update traceability**: Mark affected items for revision
6. **Track completion**: Verify all affected items updated

### Change Tracking Example
```
Change Request: REQ-042 Update
Original: "Users can save items for later purchase"
Changed To: "Users can save items for later AND share wishlists with others"

Impact Analysis:
- WISHLIST-SPEC-1.0 → Update required (add sharing functionality)
- WISHLIST-UI-v2.0 → Update required (add share button and share modal)
- Implementation → Additional code required (sharing service, permissions)
- Tests → Additional test cases required (sharing scenarios)
- Timeline Impact: +2 weeks
- Cost Impact: +15%

Affected Teams Notified:
✓ Design Director (2026-02-22)
✓ Tech Director (2026-02-22)
✓ Virtual Team Lead (2026-02-22)

Traceability Matrix Updated:
- REQ-042: Status changed to "In Revision"
- New row: REQ-042-B (Wishlist sharing)
- Linked items marked for update
```

## Traceability Tools

### Recommended Tools
- **Spreadsheet**: Google Sheets, Excel (simple projects)
- **Jira**: Issue linking, requirements management
- **Azure DevOps**: Work item linking, backlogs
- **Specialized**: Helix RM, Jama, Polarion (enterprise)

### Tool Requirements
Must support:
- Bidirectional linking (forward and backward traceability)
- Change history and audit trail
- Export and reporting
- Search and filtering
- Access control and permissions

## Traceability Verification

### Periodic Audits
Conduct traceability audits at:
- **Major milestones**: Verify all requirements have downstream links
- **Before client delivery**: Ensure all deliverables trace to requirements
- **Project completion**: Validate complete traceability chain

### Audit Checklist
- [ ] Every requirement has a client need source
- [ ] Every requirement links to specification(s)
- [ ] Every specification links to design(s)
- [ ] Every design links to implementation
- [ ] Every implementation has test coverage
- [ ] Every deliverable traces to requirement(s)
- [ ] No orphaned requirements (no downstream links)
- [ ] No orphaned deliverables (no upstream links)
- [ ] Change history is documented
- [ ] Traceability matrix is current

### Gap Resolution
When gaps found:
1. **Identify**: What's missing?
2. **Root cause**: Why wasn't it traced?
3. **Remediate**: Add missing links
4. **Prevent**: Update process to avoid recurrence

## Documentation Requirements

### In Requirements Documents
Every requirement must include:
```
Requirement ID: REQ-xxx
Title: {Brief description}
Source: {Client meeting/email/workshop} on {date}
Stated By: {Client role}
Business Value: {Why this matters}
Acceptance Criteria: {How to verify}
Priority: {Critical/High/Medium/Low}
Status: {Proposed/Approved/In Progress/Complete}
Related Requirements: {Dependencies}
```

### In Design Documents
Every design must reference:
```
Design ID: {identifier}
Implements: {Requirement IDs or Specification IDs}
Rationale: {Why designed this way}
Alternatives Considered: {Other options and why not chosen}
Assumptions: {What we assume to be true}
Constraints: {Limitations or boundaries}
```

### In Code
Code must include traceability comments:
```typescript
/**
 * Wishlist Button Component
 *
 * Implements: REQ-042 (User wishlist functionality)
 * Design: WISHLIST-UI-v2.0
 *
 * Displays heart icon button to add/remove items from wishlist.
 * Shows loading state during API calls and error state on failure.
 */
export const WishlistButton: React.FC<Props> = ({ productId }) => {
  // Implementation
}
```

### In Test Cases
Tests must reference requirements:
```
describe('Wishlist Functionality - REQ-042', () => {
  it('TC-042-001: should add item to wishlist', () => {
    // Test implementation
  });

  it('TC-042-002: should persist wishlist across sessions', () => {
    // Test implementation
  });
});
```

## Benefits of Traceability

### For Project Management
- Impact analysis for changes
- Progress tracking against requirements
- Verification of complete coverage
- Audit trail for accountability

### For Quality Assurance
- Verification that all requirements are tested
- Identification of gaps in test coverage
- Validation of deliverables against requirements

### For Client Relationships
- Transparency into what was delivered and why
- Justification for scope and timeline
- Accountability for commitments
- Foundation for change management

### For Learning
- Understanding of decisions and rationale
- Knowledge transfer for new team members
- Retrospective analysis
- Process improvement insights

## Success Criteria

Traceability succeeds when:
- Every deliverable traces to a client need
- Every requirement is implemented and tested
- Changes can be analyzed for full impact quickly
- No orphaned work exists
- Audit trail supports accountability
- Knowledge is preserved for future reference
- Overhead is manageable and valuable
