---
name: Deliverable Management
description: Track, version, and manage project deliverables ensuring quality, traceability, and client collaboration
---

# Deliverable Management

## Purpose

Systematically track, version, and manage all project deliverables including documents (PDF, DOCX, PPTX), mock products, design assets, and code artifacts. Ensure deliverables are traceable, versioned, and accessible for client collaboration and iteration.

## When to Use This Skill

Use this skill when:
- Creating or updating project deliverables
- Presenting deliverables to clients
- Tracking deliverable versions and changes
- Managing deliverable approval workflows
- Organizing deliverables for project handoff
- Archiving completed project deliverables

## Deliverable Categories

### Documents
- Requirements specifications
- Design proposals and mockups
- Technical architecture documents
- Project plans and timelines
- Contracts and agreements
- Meeting minutes and decision logs

### Mock Products
- Interactive prototypes (Figma, InVision)
- Wireframes and design comps
- Demo applications
- Proof-of-concept implementations

### Design Assets
- UI/UX designs
- Brand guidelines and style guides
- Visual assets (logos, icons, images)
- Marketing materials

### Code Artifacts
- Source code repositories
- Deployment packages
- API documentation
- Database schemas

## Deliverable Lifecycle

### 1. Creation
- Assign owner and contributors
- Define deliverable scope and format
- Set target completion date
- Establish quality criteria

### 2. Review
- Conduct internal review
- Gather feedback from stakeholders
- Iterate based on feedback
- Obtain internal approval

### 3. Client Presentation
- Package deliverable for client review
- Present deliverable with context
- Gather client feedback
- Document client decisions

### 4. Iteration
- Incorporate client feedback
- Version deliverable appropriately
- Track changes and rationale
- Re-present updated deliverable

### 5. Approval
- Obtain client sign-off
- Archive approved version
- Update project status
- Prepare for next deliverable

### 6. Handoff
- Package deliverables for downstream teams
- Provide context and specifications
- Ensure access and permissions
- Confirm receipt and understanding

## Versioning Standards

### Version Number Format
`{Major}.{Minor}.{Patch}-{Status}`

Examples:
- `1.0.0-draft`: First draft version
- `1.1.0-review`: Internal review version
- `2.0.0-client`: Presented to client
- `2.0.1-approved`: Client approved with minor changes
- `3.0.0-final`: Final approved version

### Version Increment Rules
- **Major** (1.0.0 → 2.0.0): Significant changes, restructuring, major scope change
- **Minor** (1.0.0 → 1.1.0): Moderate changes, additions, refinements
- **Patch** (1.0.0 → 1.0.1): Small fixes, typos, minor clarifications

### Status Tags
- `draft`: Work in progress
- `review`: Under internal review
- `client`: Presented to client for review
- `approved`: Client approved
- `final`: Final deliverable, no further changes

## Deliverable Metadata

Track essential information for each deliverable:

```
Deliverable ID: {unique identifier}
Title: {deliverable name}
Category: {document/mock/design/code}
Version: {version number}
Status: {draft/review/client/approved/final}
Owner: {responsible person}
Contributors: {list of contributors}
Created: {date}
Last Modified: {date}
Client Reviewed: {date}
Approved: {date}
Related Requirements: {requirement IDs}
Related Deliverables: {linked deliverables}
File Location: {path or URL}
Notes: {important context}
```

## Organization Structure

Organize deliverables by client and project:

```
deliverables/
├── {client-name}/
│   ├── {project-name}/
│   │   ├── requirements/
│   │   │   ├── requirements-spec-v1.0.0-draft.pdf
│   │   │   ├── requirements-spec-v2.0.0-approved.pdf
│   │   │   └── traceability-matrix-v1.0.0-final.xlsx
│   │   ├── design/
│   │   │   ├── mockups-v1.0.0-client.fig
│   │   │   ├── mockups-v2.0.0-approved.fig
│   │   │   └── style-guide-v1.0.0-final.pdf
│   │   ├── technical/
│   │   │   ├── architecture-v1.0.0-review.pdf
│   │   │   └── api-spec-v1.0.0-approved.yaml
│   │   └── project-docs/
│   │       ├── project-plan-v1.0.0-approved.docx
│   │       └── final-report-v1.0.0-final.pdf
```

## Quality Standards

All deliverables must meet:
- **Completeness**: All required sections/content included
- **Accuracy**: Information is correct and validated
- **Clarity**: Content is clear and understandable
- **Consistency**: Formatting and terminology are consistent
- **Professionalism**: Polished presentation quality
- **Traceability**: Linked to requirements and decisions

## Collaboration Features

### Client Review Sessions
- Schedule review meetings
- Present deliverables with context
- Document client feedback in real-time
- Track action items and decisions

### Iterative Refinement
- Incorporate feedback systematically
- Maintain version history
- Document change rationale
- Re-present updated versions

### Approval Workflow
- Define approval criteria
- Route for internal approvals first
- Present to client for final approval
- Archive approved versions

## Tools and Platforms

Leverage collaboration tools:
- Document management: Google Drive, SharePoint, Dropbox
- Design collaboration: Figma, InVision, Miro
- Code repositories: GitHub, GitLab, Azure DevOps
- Project management: Asana, Trello, Jira

## Success Criteria

Deliverable management succeeds when:
- All deliverables are properly versioned and tracked
- Deliverables are easily accessible to authorized users
- Version history provides clear change audit trail
- Client feedback is systematically incorporated
- Approvals are documented and archived
- Deliverable quality consistently meets standards
- Handoffs between teams are smooth and complete

## Example Usage

**Scenario**: Requirements specification deliverable

```
Create Deliverable:
- Title: "E-commerce Platform Requirements Specification"
- Owner: Requirements Director
- Contributors: Requirements Analyst, Market Researcher
- Version: 1.0.0-draft
- Target: 2026-02-20

Internal Review:
- Reviewers: Requirements Consultant, Design Director
- Feedback incorporated
- Version: 1.1.0-review

Client Presentation:
- Presented: 2026-02-25
- Feedback: Add payment gateway requirements, clarify mobile app scope
- Version: 2.0.0-client

Iteration:
- Updates: Added payment section, mobile app details
- Version: 2.1.0-client

Approval:
- Client approved: 2026-03-01
- Version: 2.1.0-approved
- Archive and mark as baseline

Handoff:
- To: Design Director for mock development
- Package: Requirements spec + traceability matrix
- Status: Design phase initiated
```
