---
name: Requirement Tracing
description: Maintain bidirectional traceability from client needs to deliverables enabling accountability and change management
---

# Requirement Tracing

## Purpose

Establish and maintain bidirectional traceability from client needs through requirements to design, implementation, testing, and final deliverables. Enable impact analysis, accountability, and comprehensive change management.

## When to Use This Skill

Use this skill when:
- Capturing initial client requirements
- Creating design specifications from requirements
- Implementing features based on requirements
- Validating deliverables against requirements
- Analyzing impact of requirement changes
- Conducting project retrospectives
- Responding to "why was this decided" questions

## Traceability Directions

### Forward Traceability
Track requirements forward to implementation:
- Client Need → Requirement → Design → Implementation → Test → Deliverable

### Backward Traceability
Trace deliverables back to origin:
- Deliverable → Test → Implementation → Design → Requirement → Client Need

## Traceability Matrix Structure

Maintain comprehensive linkages:

| Req ID | Client Need | Discussion Ref | Specification | Design | Implementation | Test | Deliverable | Status |
|--------|-------------|----------------|---------------|--------|----------------|------|-------------|---------|
| REQ-001 | User login | 2026-02-11 meeting | AUTH-SPEC-1.2 | LOGIN-UI-v2 | auth-service.ts | TC-001-005 | Login Page | Complete |
| REQ-002 | Mobile app | 2026-02-15 email | MOBILE-SPEC-2.1 | MOBILE-MOCK-v1 | mobile-app/* | TC-010-020 | iOS/Android App | In Progress |
| REQ-003 | Payment | 2026-02-20 workshop | PAYMENT-SPEC-3.1 | CHECKOUT-FLOW-v3 | payment-integration/* | TC-025-035 | Payment Module | Not Started |

## Requirement Identification

### Requirement ID Format
`REQ-{sequence}` or `{category}-{sequence}`

Examples:
- `REQ-001`: General requirement
- `FUNC-001`: Functional requirement
- `NFR-001`: Non-functional requirement
- `UI-001`: UI/UX requirement
- `INT-001`: Integration requirement

### Requirement Attributes
Each requirement tracks:
- **ID**: Unique identifier
- **Title**: Brief description
- **Source**: Where it originated (client need, discussion, regulatory)
- **Priority**: Critical / High / Medium / Low
- **Status**: Proposed / Approved / In Progress / Complete / Deferred
- **Owner**: Responsible person
- **Related Requirements**: Dependencies and relationships

## Traceability Linkages

### Level 1: Client Need to Requirement
Link documented client needs to formal requirements:
- Client interview: "We need mobile access" → REQ-002: Mobile application support
- Email request: "Payment via credit card" → REQ-003: Credit card payment integration

### Level 2: Requirement to Specification
Link requirements to detailed specifications:
- REQ-001 → AUTH-SPEC-1.2: Authentication and authorization specification
- REQ-002 → MOBILE-SPEC-2.1: Mobile application technical specification

### Level 3: Specification to Design
Link specifications to design artifacts:
- AUTH-SPEC-1.2 → LOGIN-UI-v2.0: Login page design mockup
- MOBILE-SPEC-2.1 → MOBILE-MOCK-v1.0: Mobile app prototype

### Level 4: Design to Implementation
Link designs to code artifacts:
- LOGIN-UI-v2.0 → auth-service.ts, login-page.tsx: Implementation files
- MOBILE-MOCK-v1.0 → mobile-app/src/*: Mobile codebase

### Level 5: Implementation to Test
Link code to test cases:
- auth-service.ts → TC-001, TC-002, TC-003: Unit and integration tests
- login-page.tsx → TC-004, TC-005: UI component tests

### Level 6: Test to Deliverable
Link tests to final deliverables:
- TC-001-005 → Login Page: Completed and tested deliverable
- TC-010-020 → Mobile App v1.0: Tested mobile application

## Change Impact Analysis

When requirements change, trace impact:

**Example**: Client changes REQ-002 from "iOS only" to "iOS and Android"

**Impact Analysis**:
1. Requirement: REQ-002 updated to include Android
2. Specification: MOBILE-SPEC-2.1 updated to cover Android
3. Design: MOBILE-MOCK-v1.0 updated for Android UI guidelines
4. Implementation: Additional Android codebase required
5. Test: Additional Android test cases (TC-015-020)
6. Deliverable: Android app added to deliverables
7. Timeline: +4 weeks for Android development
8. Budget: +30% for Android parallel development

## Documentation References

Link requirements to discussion records:
- Meeting minutes: `meetings/2026-02-11-kickoff.md#requirement-discussion`
- Email threads: `emails/2026-02-15-mobile-request.eml`
- Decision logs: `decisions/2026-02-20-payment-gateway-selection.md`

## Traceability Tools

Maintain traceability using:
- **Spreadsheet**: Traceability matrix in Excel/Google Sheets
- **Requirement Management Tools**: Jira, Azure DevOps, Helix RM
- **Documentation**: Cross-references in markdown documents
- **Code Comments**: Link requirements in code comments

## Quality Standards

Traceability succeeds when:
- Every requirement traces to a client need
- Every deliverable traces back to a requirement
- Changes can be analyzed for full impact
- Historical context is preserved and accessible
- Audit trail supports accountability
- Gaps and orphaned items are identified

## Workflow Integration

### Requirements Phase
1. Capture client need with reference
2. Create requirement with unique ID
3. Link requirement to client need source
4. Update traceability matrix

### Design Phase
1. Create design artifact
2. Link to requirements it addresses
3. Update traceability matrix
4. Verify all requirements have design coverage

### Development Phase
1. Implement feature
2. Link code to requirements and design
3. Update traceability matrix
4. Verify implementation coverage

### Testing Phase
1. Create test cases
2. Link to requirements and implementation
3. Update traceability matrix
4. Verify test coverage

### Delivery Phase
1. Package deliverable
2. Verify all requirements are delivered
3. Update traceability status
4. Archive traceability records

## Success Criteria

Requirement tracing succeeds when:
- All requirements have clear source and rationale
- All deliverables trace to requirements
- Impact of changes can be quickly assessed
- Gaps in coverage are identified early
- Project history supports learning and accountability
- Traceability overhead is manageable and valuable

## Example Usage

**Scenario**: Client requests payment feature

**Traceability Flow**:

```
1. Client Need (2026-02-18 workshop):
   "Users must be able to pay with credit card, Apple Pay, and Google Pay"
   → Documented in: meetings/2026-02-18-payment-discussion.md

2. Requirements:
   REQ-003: Credit card payment integration
   REQ-004: Apple Pay integration
   REQ-005: Google Pay integration
   → Documented in: requirements/payment-requirements-v1.0.pdf

3. Specifications:
   PAYMENT-SPEC-3.1: Payment gateway integration specification
   → References: REQ-003, REQ-004, REQ-005

4. Design:
   CHECKOUT-FLOW-v3: Checkout page with payment options
   PAYMENT-UI-v2: Payment method selection component
   → References: PAYMENT-SPEC-3.1

5. Implementation:
   payment-integration/stripe-service.ts
   payment-integration/apple-pay.ts
   payment-integration/google-pay.ts
   → References: CHECKOUT-FLOW-v3, PAYMENT-UI-v2

6. Tests:
   TC-025: Credit card payment flow
   TC-026: Apple Pay integration
   TC-027: Google Pay integration
   → References: payment-integration/*

7. Deliverable:
   Payment Module v1.0 (supports all three payment methods)
   → References: REQ-003, REQ-004, REQ-005 (Complete)

Traceability Matrix Updated:
All payment requirements marked Complete
All linkages documented
Client need satisfied and traceable
```
