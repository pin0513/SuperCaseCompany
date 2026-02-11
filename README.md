# Super Case Company Team

> A complete multi-agent team structure for a comprehensive B2B expert company

## Overview

Super Case Company is a comprehensive B2B expert company with 7 strategic dimensions, 55+ specialist agents, and executive leadership. The company delivers end-to-end solutions including IT consulting, industry expertise, and business services, covering requirements discovery, design, development, deployment, operational support, and industry-specific consulting.

## Team Structure

### Executive Leadership

**CEO (Chief Executive Officer)**
- Provides strategic leadership using five-pillar management framework (產銷人發財)
- Forms and oversees virtual teams for client engagements
- Makes strategic decisions and handles escalations
- Ensures company health across all dimensions

### Seven Strategic Dimensions

#### Dimension 1: Requirements Discovery & Market Intelligence
**Lead**: Requirements Director
**Specialists**:
- Requirements Analyst (materials organization, discussion records)
- Market Researcher (competitive analysis, market trends)
- SEO Specialist (search optimization)
- Segmented Marketing Expert (audience segmentation)
- Keyword Advertising Expert (paid search campaigns)
- Requirements Consultant (quality advisory)

#### Dimension 2: Sales & Supply Chain
**Lead**: Sales Director
**Specialists**:
- Sales Expert (business development, proposals)
- Warehouse Manager (fulfillment operations)
- Inventory Manager (inventory optimization)

#### Dimension 3: Mock System Design & Development
**Lead**: Design Director
**Specialists**:
- Frontend Designer (UI components)
- Graphic Designer (visual assets)
- Page Designer (layouts and flows)
- E-commerce Expert (e-commerce UX)
- Ad Designer (advertising creatives)
- Visual Designer (brand identity)
- OS Expert (platform-specific design)
- Frontend Tech Expert (frontend architecture)
- Backend Tech Expert (backend architecture)
- Security Expert (security architecture)

#### Dimension 4: System Development & Cloud Infrastructure
**Lead**: Tech Director
**Specialists**:
- Software Engineer (application development)
- QA Expert (testing and quality)
- Cloud Deployment Expert (GCP, Azure, AWS, Cloudflare)
- High-Concurrency Architect (scalability, performance)
- ERP System Expert (enterprise systems integration)

#### Dimension 5: Operations Management & Support
**Lead**: Operations Director
**Specialists**:
- Document & Asset Manager (knowledge management)
- Investment Expert (business investments)
- Finance Expert (financial planning)
- Customer Service Expert (support and satisfaction)
- UX Optimizer (experience optimization)
- HR Expert (talent management)
- Legal Expert (Taiwan legal compliance)
- Accounting Expert (financial reporting)

#### Dimension 6: Learning, Development & Innovation
**Lead**: Innovation Director
**Specialists**:
- Training Expert (learning programs)
- AI Training Consultant (AI capabilities)
- Domain Consultant (industry expertise)

#### Dimension 7: Industry Experts & Procurement
**Lead**: Industry Consulting Director
**Specialists**:
- Restaurant Industry Expert (shift scheduling, chain management, central kitchen)
- Breakfast Chain Expert (early morning ops, franchisee management)
- Beverage Shop Expert (customization, seasonal menu, mobile ordering)
- Raw Material Trading Expert (bulk orders, B2B, commodity pricing)
- Cold Chain Logistics Expert (temperature control, food safety, traceability)
- Coffee Shop Expert (barista skills, specialty coffee, third-place experience)
- Procurement Expert (supplier sourcing, import logistics, cost analysis)

## Working Model: Virtual Teams

SuperCase operates using **virtual team formation**:

1. **Project Request**: Client engagement received
2. **Analysis**: CEO analyzes requirements and scope
3. **Team Formation**: CEO selects appropriate dimension leads and specialists
4. **Execution**: Virtual team delivers project under team lead coordination
5. **Dissolution**: Team completes and specialists return to home dimensions

### Example Virtual Teams

**Discovery-Only Team**:
- Requirements Director (lead)
- Requirements Analyst
- Market Researcher
- Requirements Consultant

**E-commerce Project Team**:
- CEO (oversight)
- Requirements Director (requirements)
- Sales Director (inventory/supply chain)
- Design Director (lead) → E-commerce Expert, Page Designer, Visual Designer
- Tech Director (development) → Software Engineer, Cloud Deployment Expert
- Operations Director (support) → Finance Expert, Customer Service Expert

## Core Skills

### Virtual Team Formation (`/virtual-team-formation`)
Dynamically assemble cross-functional teams based on project needs

### Deliverable Management (`/deliverable-management`)
Track, version, and manage all project deliverables (documents, designs, code)

### Requirement Tracing (`/requirement-tracing`)
Maintain bidirectional traceability from client needs to final deliverables

### Document Generation (`/document-generation`)
Create professional documents in PDF, DOCX, PPTX formats

### Mock Product Versioning (`/mock-product-versioning`)
Version and iterate design mockups and prototypes with client collaboration

### Client Collaboration (`/client-collaboration`)
Facilitate effective client engagement through structured communication and win-win solutions

### Shift Scheduling (`/shift-scheduling`)
Design shift scheduling systems for restaurants, breakfast shops, beverage shops, and service businesses

### Chain Management (`/chain-management`)
Design multi-location chain management systems with store manager dashboards and centralized oversight

### Central Kitchen Management (`/central-kitchen`)
Design central kitchen systems for food preparation, distribution, and quality control

### Procurement Management (`/procurement-management`)
Design procurement systems for supplier sourcing, import logistics, and cost analysis

## Key Principles

### 產銷人發財 (Five Pillars of Management)

Every decision considers:
1. **產 (Production)**: Can we deliver with quality?
2. **銷 (Sales)**: Does this fit our market positioning?
3. **人 (Human Resources)**: Do we have the right expertise?
4. **發 (R&D)**: Does this advance our capabilities?
5. **財 (Finance)**: Is this profitable and sustainable?

### Quality Standards

- All deliverables are client-ready before submission
- Mandatory review and approval process
- Complete traceability from requirements to delivery
- Professional formatting and branding

### Collaboration Protocols

- Structured handoffs between dimensions
- Transparent communication
- Proactive escalation of issues
- Win-win solution design

## Typical Project Workflow

```
1. Project Intake
   └─> CEO receives client engagement request

2. Requirements Phase
   └─> Requirements Director leads discovery
   └─> Requirements documented with traceability
   └─> CEO approves requirements

3. Design Phase (if applicable)
   └─> Design Director creates mockups
   └─> Client reviews and provides feedback
   └─> Iterative refinement until approval

4. Development Phase (if applicable)
   └─> Tech Director leads implementation
   └─> QA testing and cloud deployment
   └─> Security and performance validation

5. Delivery Phase
   └─> Final deliverables packaged
   └─> CEO approval
   └─> Client presentation and handoff
   └─> Retrospective and lessons learned
```

## Directory Structure

```
SuperCaseCompanyTeam/
├── CLAUDE.md                      # Team-wide instructions
├── README.md                      # This file
└── .claude/
    ├── agents/
    │   ├── ceo.md                # CEO (coordinator)
    │   ├── dimension-1-requirements/
    │   ├── dimension-2-sales/
    │   ├── dimension-3-design/
    │   ├── dimension-4-development/
    │   ├── dimension-5-operations/
    │   └── dimension-6-innovation/
    ├── skills/
    │   ├── virtual-team-formation/
    │   ├── deliverable-management/
    │   ├── requirement-tracing/
    │   ├── document-generation/
    │   ├── mock-product-versioning/
    │   └── client-collaboration/
    └── rules/
        ├── dimension-lead-protocol.md
        ├── virtual-team-protocol.md
        ├── deliverable-standards.md
        ├── traceability-requirements.md
        └── ceo-management-principles.md
```

## Getting Started

### For CEO

1. Receive client engagement request
2. Review requirements and determine scope
3. Use `/virtual-team-formation` to assemble appropriate team
4. Conduct kickoff with virtual team
5. Monitor progress and provide strategic guidance
6. Review and approve deliverables
7. Manage client relationship

### For Dimension Leads

1. Receive project assignment from CEO
2. Select and brief specialists from your dimension
3. Coordinate with other dimension leads on handoffs
4. Review specialist work for quality
5. Report status to CEO weekly
6. Escalate issues and blockers promptly
7. Support virtual team lead as needed

### For Specialists

1. Receive task assignment from dimension lead
2. Execute work to quality standards
3. Collaborate with virtual team members
4. Update progress regularly
5. Raise blockers early
6. Participate in reviews and retrospectives
7. Contribute to continuous improvement

## Success Metrics

- **Project Delivery**: >90% on-time, within budget
- **Quality**: <10% rework rate, >90% first-time acceptance
- **Client Satisfaction**: NPS >50, >85% retention
- **Team Performance**: Resource utilization 75-85%, high engagement
- **Business Growth**: Revenue growth, strong margins, repeat business

## Communication Language

Default language is **Traditional Chinese (繁體中文)**. Technical terms may remain in English with explanation on first use.

## Deployment Mode

**Subagent Mode**: Agents are invoked via the Task tool within a single Claude Code session. CEO manages all coordination and delegation.

---

**Version**: 1.0
**Created**: 2026-02-11
**Company**: Super Case Company
**Total Agents**: 47 (1 CEO + 6 Dimension Leads + 40 Specialists)
