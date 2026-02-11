---
name: Project Context Protocol
description: Mandatory protocol for all members and directors to verify project context, delivery directories, and client management system before executing any task
---

# Project Context Protocol

## Applicability

Applies to: **All team members** (CEO, Customer Success Director, all dimension directors, all specialists)

## Core Principle

**Before executing any task, MUST verify: Is this TALK or OFFICIAL? Where are the directories? Where should outputs go?**

---

## Mandatory Pre-Task Checklist

When you receive any instruction, **STOP and answer these questions FIRST**:

### Question 1: TALK or OFFICIAL?

| Mode | Description | When to Use | Record Required |
|------|-------------|-------------|-----------------|
| **TALK** | Informal discussion, brainstorming, Q&A | Client just asking questions, exploring ideas, no commitment | ❌ No formal record |
| **OFFICIAL** | Formal project, deliverables expected, billable | Client confirmed engagement, expects deliverables, willing to pay | ✅ Full project records |

**How to determine**:
- Has client provided project name/code? → OFFICIAL
- Has client confirmed budget/timeline? → OFFICIAL
- Does client expect formal deliverables? → OFFICIAL
- Just chatting, no commitment yet? → TALK

**Example**:
```
Client: "我想了解一下做排班系統大概要多少錢？"
→ TALK mode (just exploring)

Client: "好，那就開始做吧，專案代號是 RESTAURANT-CHAIN-001"
→ OFFICIAL mode (confirmed engagement)
```

---

### Question 2: Where is the PROJECT DIRECTORY?

**If OFFICIAL mode**, project directory MUST exist:

```
projects/{CLIENT-NAME}-{PROJECT-CODE}/
```

**Directory structure**:
```
projects/RESTAURANT-CHAIN-001/
├── context/                          ← Project background & client info
│   ├── client-profile.md            ← Client company info, contacts
│   ├── project-charter.md           ← Project objectives, scope, timeline
│   └── stakeholders.md              ← Key stakeholders, decision makers
├── requirements/                     ← Requirements discovery
│   ├── interviews/                  ← Interview transcripts
│   │   ├── 01_first_contact_2026-02-11.md
│   │   ├── 02_pain_point_dive_scheduling_2026-02-12.md
│   │   └── ...
│   ├── verbatim_record.md           ← All client quotes (verbatim)
│   ├── requirement_spec_v1.0.md     ← Formal requirements specification
│   └── traceability_matrix.xlsx    ← Requirement traceability
├── design/                          ← Design outputs
│   ├── mockups/                     ← UI/UX mockups (Figma, sketches)
│   ├── design_proposal_v1.0.pdf    ← Design proposal for client
│   └── design_approval_2026-02-18.md ← Client approval record
├── development/                     ← Development outputs
│   ├── code/                        ← Source code (if applicable)
│   ├── architecture/                ← Architecture diagrams, decisions
│   ├── test-reports/                ← QA test reports
│   └── demo-feedback_2026-03-05.md ← Client demo feedback
├── delivery/                        ← Final deliverables
│   ├── final-report.pdf            ← Final project report
│   ├── user-manual.pdf             ← User manuals
│   ├── deployment-guide.pdf        ← Deployment instructions
│   └── handoff-checklist.md        ← Handoff checklist (signed)
└── client-records/                  ← Client management system
    ├── interactions/                ← All client interactions
    │   ├── 2026-02-11_kickoff_meeting.md
    │   ├── 2026-02-18_design_review.md
    │   └── 2026-03-05_demo_feedback.md
    ├── decisions/                   ← All decisions made
    │   ├── 2026-02-20_scope_change.md
    │   └── 2026-02-25_timeline_adjustment.md
    ├── issues/                      ← Issues and resolutions
    │   └── 2026-03-01_bug_report.md
    └── project-log.md               ← Master project log
```

---

### Question 3: Where should OUTPUT go?

**Determine output location based on task type**:

| Task Type | Output Location | Example |
|-----------|-----------------|---------|
| **Requirements Interview** | `requirements/interviews/` | `01_first_contact_2026-02-11.md` |
| **Design Mockup** | `design/mockups/` | `scheduling-ui-v1.0.fig` |
| **Design Proposal** | `design/` | `design_proposal_v1.0.pdf` |
| **Architecture Decision** | `development/architecture/` | `ADR-001-database-choice.md` |
| **Test Report** | `development/test-reports/` | `test-report-2026-03-05.md` |
| **Client Meeting Notes** | `client-records/interactions/` | `2026-02-18_design_review.md` |
| **Final Deliverable** | `delivery/` | `final-report.pdf` |

**Before starting work, confirm**:
```
I will work on: {task description}
Output will be saved to: {full path}
Is this correct?
```

---

### Question 4: Is CLIENT MANAGEMENT record needed?

**If OFFICIAL mode, ALWAYS record**:

#### Client Interaction Record

Every interaction with client must be recorded in `client-records/interactions/`:

```markdown
# Client Interaction Record

**Date**: 2026-02-18
**Type**: Design Review Meeting
**Participants**:
- Client: {Client names and roles}
- Super Case Company: {Team member names and roles}
**Project**: RESTAURANT-CHAIN-001
**Phase**: Design

## Discussion Summary

{What was discussed}

## Client Feedback (Verbatim)

> "{Client's exact words}"

> "{Client's exact words}"

## Decisions Made

| Decision | Rationale | Impact |
|----------|-----------|--------|
| {Decision 1} | {Why} | {What changes} |

## Action Items

- [ ] {Who} to do {what} by {when}
- [ ] {Who} to do {what} by {when}

## Next Steps

{What happens next}

## Attachments

- {Link to design mockup}
- {Link to feedback document}
```

#### Decision Record

Important decisions must be recorded in `client-records/decisions/`:

```markdown
# Decision Record

**Date**: 2026-02-20
**Decision ID**: DEC-001
**Project**: RESTAURANT-CHAIN-001

## Decision

{What decision was made}

## Context

{Why this decision was needed}

## Client Request (Verbatim)

> "{Client's exact words}"

## Options Considered

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| A | {pros} | {cons} | {impact} |
| B | {pros} | {cons} | {impact} |

## Decision

Chose: **Option {A/B}**

Reason: {Why this option was chosen}

## Impact

- Scope: {How scope changes}
- Timeline: {How timeline changes}
- Cost: {How cost changes}

## Approval

- Client: {Approved by whom, when}
- Super Case Company: {Approved by CEO/CSD, when}
```

---

## Execution Protocol

### Step 1: Verify Mode

```
Member receives instruction:
"請設計排班系統的 UI"

Member MUST ask:
1. Is this TALK or OFFICIAL?
2. If OFFICIAL: What is the project code?
3. Where should I save my output?
```

### Step 2: Verify Project Directory

```
If OFFICIAL:
- Check if projects/{PROJECT-CODE}/ exists
- If NOT exist → Ask Customer Success Director to create it
- If exists → Proceed
```

### Step 3: Determine Output Location

```
Task: Design scheduling UI
Output type: Design mockup
Output location: projects/RESTAURANT-CHAIN-001/design/mockups/
Filename: scheduling-ui-v1.0.fig

Confirm before starting:
"I will save design mockup to:
 projects/RESTAURANT-CHAIN-001/design/mockups/scheduling-ui-v1.0.fig

 Is this correct?"
```

### Step 4: Record Client Interaction (if applicable)

```
If this task involves client feedback or decision:
- Create record in client-records/interactions/ or client-records/decisions/
- Follow the template above
- Update project-log.md
```

---

## TALK Mode vs OFFICIAL Mode

### TALK Mode (Informal)

**Characteristics**:
- Exploratory conversation
- No project code assigned yet
- No deliverable commitment
- Just providing information/advice

**What to do**:
- Answer questions directly
- Provide general guidance
- No need to create project directory
- No need to record in client management system

**Example**:
```
Client: "你們做排班系統大概要多久？"

Response:
"根據複雜度不同，通常 1-3 個月：
- 簡單版（單店，基本排班）：1 個月
- 進階版（多店，技能匹配，勞基法檢查）：2 個月
- 完整版（含分析報表、薪資整合）：3 個月

如果您確定要開始做，我們可以進入正式專案流程，
先做需求訪談，給您精確的時程與報價。"
```

### OFFICIAL Mode (Formal Project)

**Characteristics**:
- Client confirmed engagement
- Project code assigned (e.g., RESTAURANT-CHAIN-001)
- Deliverables expected
- Billable work
- Contract or verbal agreement

**What to do**:
1. Create project directory (if not exists)
2. Every output must be saved to correct location
3. Every client interaction must be recorded
4. Follow full project workflow

**Example**:
```
Client: "好，那就開始吧，專案代號是 RESTAURANT-CHAIN-001"

Response:
"收到！專案代號：RESTAURANT-CHAIN-001

我現在會：
1. 建立專案目錄：projects/RESTAURANT-CHAIN-001/
2. 開始需求訪談流程
3. 所有文件會存放在對應目錄
4. 每次與您的互動都會記錄

請問我們可以開始第一次需求訪談了嗎？"
```

---

## Client Management System

### Purpose

**Why we need this**:
- Track all client interactions and decisions
- Traceability (why we made certain choices)
- Knowledge retention (future team members can understand context)
- Dispute resolution (what was agreed upon)
- Continuous improvement (learn from past projects)

### What to Record

**ALWAYS record**:
- Client meetings (kickoff, review, demo, handoff)
- Client feedback (verbatim quotes)
- Decisions made (scope change, timeline adjustment)
- Issues raised (bugs, concerns, complaints)
- Approvals (design approval, milestone approval)

**DON'T record**:
- Internal team discussions (unless they impact client)
- Draft work (only record delivered outputs)

### Master Project Log

Every project must maintain `project-log.md`:

```markdown
# Project Log: RESTAURANT-CHAIN-001

## Project Overview

**Client**: ABC Restaurant Chain
**Project**: Scheduling System
**Start Date**: 2026-02-11
**Target End Date**: 2026-04-11
**Status**: In Progress

## Timeline

| Date | Event | Phase | Participants | Link |
|------|-------|-------|--------------|------|
| 2026-02-11 | Kickoff Meeting | Requirements | CEO, CSD, Client CEO | [meeting notes](client-records/interactions/2026-02-11_kickoff.md) |
| 2026-02-12 | Pain Point Interview | Requirements | Requirements Analyst, Client Operations Manager | [interview](requirements/interviews/02_pain_point_dive_scheduling_2026-02-12.md) |
| 2026-02-18 | Design Review | Design | CSD, Design Director, Client | [review notes](client-records/interactions/2026-02-18_design_review.md) |
| 2026-02-20 | Scope Change Request | Design | CSD, Client | [decision record](client-records/decisions/2026-02-20_scope_change.md) |
| 2026-03-05 | Demo Feedback | Development | CSD, Tech Director, Client | [demo feedback](development/demo-feedback_2026-03-05.md) |

## Key Decisions

| ID | Date | Decision | Impact | Status |
|----|------|----------|--------|--------|
| DEC-001 | 2026-02-20 | Add "View Monthly Hours" feature | +3 days timeline | ✅ Implemented |
| DEC-002 | 2026-02-25 | Integrate LINE notification | +5 days timeline, +10% cost | ✅ Approved by client |

## Current Status

**Phase**: Development
**Progress**: 70%
**Next Milestone**: Final Demo (2026-03-20)
**Blockers**: None
**Risks**: None

## Client Satisfaction

| Milestone | Client Rating | Feedback Summary |
|-----------|---------------|------------------|
| Requirements Confirmation | 9/10 | "Very thorough understanding" |
| Design Proposal | 8/10 | "Good, requested minor changes" |
| Development Demo | 9/10 | "Looks great, requested LINE integration" |
```

---

## Violation Scenarios

### Violation 1: Started work without verifying mode

```
❌ BAD:
Client: "請設計排班系統的 UI"
Member: {Immediately starts designing}

✅ GOOD:
Client: "請設計排班系統的 UI"
Member: "收到！請問：
        1. 這是正式專案（OFFICIAL）還是只是討論（TALK）？
        2. 如果是正式專案，專案代號是什麼？
        3. 設計稿要存放在哪個目錄？"
```

### Violation 2: Output saved to wrong location

```
❌ BAD:
Saves design mockup to: ~/Desktop/scheduling-ui.fig

✅ GOOD:
Saves design mockup to: projects/RESTAURANT-CHAIN-001/design/mockups/scheduling-ui-v1.0.fig
```

### Violation 3: Client interaction not recorded

```
❌ BAD:
Had design review meeting with client, discussed changes, but didn't record

✅ GOOD:
After design review meeting:
1. Create: client-records/interactions/2026-02-18_design_review.md
2. Record all client feedback (verbatim)
3. Record decisions made
4. Update project-log.md
```

### Violation 4: Assumed project directory structure

```
❌ BAD:
Member assumes directory exists and saves file there (fails silently)

✅ GOOD:
Member checks if directory exists:
- If NOT exist → Ask CSD to create it
- If exists → Proceed with save
```

---

## Responsibilities

### Customer Success Director

- Create project directory when new OFFICIAL project starts
- Ensure all members know the project code and directory structure
- Monitor that all client interactions are being recorded
- Review project-log.md weekly for accuracy

### All Members and Directors

- ALWAYS verify TALK vs OFFICIAL before starting work
- ALWAYS confirm output location before creating deliverables
- ALWAYS record client interactions in client-records/
- ALWAYS update project-log.md when milestone is reached

### CEO

- Assign project code when client confirms engagement
- Review project-log.md monthly for all active projects
- Ensure team follows this protocol

---

## Quick Reference

### Pre-Task Checklist

Before starting ANY task:

- [ ] Is this TALK or OFFICIAL?
- [ ] If OFFICIAL: What is the project code?
- [ ] Does project directory exist?
- [ ] Where should my output be saved?
- [ ] Do I need to record this in client-records/?

### Common Scenarios

| Scenario | Mode | Action |
|----------|------|--------|
| Client asks general questions | TALK | Answer directly, no record needed |
| Client confirms project engagement | OFFICIAL | Create project directory, start recording |
| Conducting requirements interview | OFFICIAL | Save to `requirements/interviews/`, record in verbatim_record.md |
| Client reviews design | OFFICIAL | Record in `client-records/interactions/` |
| Client requests scope change | OFFICIAL | Record in `client-records/decisions/` |
| Delivering final product | OFFICIAL | Save to `delivery/`, record in project-log.md |

---

## Benefits

**Why this protocol matters**:

1. **Traceability**: Every decision can be traced back to client request
2. **Accountability**: Clear record of who did what, when
3. **Knowledge Retention**: Future team can understand project history
4. **Dispute Prevention**: Clear record of what was agreed
5. **Quality**: Ensures nothing falls through the cracks
6. **Efficiency**: Everyone knows where to find things
7. **Professionalism**: Demonstrates organized, systematic approach

---

**Remember**: When in doubt, ASK. Better to clarify upfront than to redo work later.

---

**Version**: 1.0 | **Created**: 2026-02-11 | **Type**: Mandatory Protocol
