# Enterprise AI Triage Architecture

**Related case study:** `docs/case-studies/enterprise-ai-intake-triage-workflow.md`  
**Status:** Conceptual architecture / documentation-first MVP

## Purpose

This document describes a vendor-neutral architecture for an AI-assisted enterprise intake and triage workflow.

The architecture is intentionally simple. It is designed to show enterprise software thinking without depending on proprietary systems, paid platforms, or employer-specific workflows.

## High-Level Flow

```text
Requester
  -> Intake channel
  -> Backend API
  -> Validation layer
  -> AI triage service
  -> Structured triage record
  -> Database
  -> Human review queue
  -> Routing / escalation / response draft
  -> Audit log and reporting
```

## Components

| Component | Purpose |
| --- | --- |
| Requester | Person submitting a support, training, access, documentation, or operations request |
| Intake channel | Web form, email parser, chat intake, or ticketing portal |
| Backend API | Receives the request, validates required fields, and creates an intake record |
| Validation layer | Checks whether required metadata exists before AI triage |
| AI triage service | Classifies the request, summarizes it, identifies missing information, and recommends routing |
| Database | Stores raw request metadata, structured triage result, review status, and audit fields |
| Human review queue | Allows a reviewer to approve, correct, reject, or escalate the AI-generated triage record |
| Routing layer | Sends reviewed records to the correct queue, owner, or next workflow step |
| Audit log | Records major actions, changes, review decisions, and timestamps |
| Reporting view | Tracks categories, priority trends, unresolved queues, missing information patterns, and review corrections |

## Example Data Model

### intake_ticket

| Field | Description |
| --- | --- |
| ticket_id | Unique ticket identifier |
| submitted_at | Submission timestamp |
| channel | Source channel such as web form, email, chat, or ticket portal |
| requester_type | Internal user, external customer, admin, trial user, etc. |
| account_type | Standard, trial, enterprise, or unknown |
| product_area | Initial product or workflow area if known |
| raw_request | Original request text |
| created_at | Record creation timestamp |

### triage_result

| Field | Description |
| --- | --- |
| result_id | Unique triage result identifier |
| ticket_id | Related intake ticket |
| category | AI-generated or reviewer-corrected category |
| priority | Low, medium, high, or urgent |
| summary | Short structured summary |
| missing_information | List of details needed to move forward |
| recommended_next_action | Suggested next action |
| confidence | Low, medium, or high |
| requires_human_review | Boolean flag |
| human_review_reason | Why review is needed |
| privacy_or_sensitivity_flags | Access, security, customer impact, privacy, or ambiguity flags |
| routing_recommendation | Suggested queue or owner |
| created_at | Triage creation timestamp |

### review_record

| Field | Description |
| --- | --- |
| review_id | Unique review identifier |
| ticket_id | Related intake ticket |
| reviewer_role | Role of reviewer, not necessarily personal identity |
| review_status | Pending, approved, corrected, rejected, escalated |
| reviewer_notes | Notes added during review |
| corrected_fields | Fields changed by the reviewer |
| reviewed_at | Review timestamp |

## Human-in-the-Loop Design

The workflow intentionally keeps humans in control of operational decisions.

AI can assist with:

- Summarizing raw requests
- Classifying ticket type
- Estimating priority
- Identifying missing information
- Suggesting routing
- Flagging privacy or sensitivity concerns

Humans remain responsible for:

- Access changes
- Customer communication
- Escalation decisions
- Security or privacy responses
- Priority overrides
- Final routing decisions
- Any action with business, customer, compliance, or security impact

## Role-Based Review Concept

A production version would use role-based permissions.

Example roles:

| Role | Allowed Actions |
| --- | --- |
| Intake reviewer | Review, correct, and route standard tickets |
| Support owner | Accept routed support tickets and update status |
| Admin reviewer | Approve account or access-related triage results |
| Security/privacy reviewer | Review data retention, privacy, and security-sensitive requests |
| Reporting viewer | View aggregate trends without accessing sensitive raw details |

## Privacy and Security Controls

A real deployment would need controls such as:

- Authentication and authorization
- Role-based access control
- Data minimization
- Input redaction for sensitive fields
- Audit logging
- Retention policy enforcement
- Encryption in transit and at rest
- Secure prompt and output logging rules
- Clear separation between raw request text and aggregate reporting
- Human review for security, privacy, customer-impacting, and access-control cases

## Failure Modes

Potential failure modes include:

- Incorrect category assignment
- Underestimated priority
- Overestimated urgency
- Missing privacy or security flag
- Overconfident output for an ambiguous request
- Inconsistent routing for similar tickets
- Hallucinated details not present in the request
- Reviewer overtrust of AI-generated output

## Mitigations

Mitigations include:

- Always requiring human review in the MVP
- Using structured JSON output
- Separating observation from recommendation
- Requiring missing information fields
- Capturing confidence levels
- Logging reviewer corrections
- Creating evaluation rubrics
- Comparing outputs against expected sample results
- Limiting AI to triage support rather than final operational action

## MVP Implementation Path

### Phase 1: Documentation MVP

- Case study
- Sample fictional intake data
- Reusable prompt
- Sample structured output
- Architecture notes

### Phase 2: Local Script

- Python script reads `sample_inputs/enterprise_intake_tickets.json`
- Script generates mock triage output
- Output is written to `sample_outputs/`
- No live AI service required

### Phase 3: API Prototype

- FastAPI endpoint accepts one ticket
- Endpoint returns a structured triage object
- Input validation added with Pydantic models
- Mock AI function remains replaceable

### Phase 4: Database Prototype

- SQLite or PostgreSQL stores tickets, triage results, and review records
- Add basic status fields such as pending, reviewed, corrected, and escalated

### Phase 5: Enterprise Readiness Additions

- Dockerfile
- GitHub Actions validation
- Basic automated tests
- Environment variable pattern for future AI provider integration
- Evaluation rubric for expected versus actual triage outputs

## What This Architecture Demonstrates

This architecture demonstrates enterprise software awareness without requiring a large application.

It shows:

- Where AI fits in a workflow
- Where AI should not make final decisions
- How structured records support review and reporting
- Why auditability matters
- How role-based review can reduce risk
- How sample data, prompts, outputs, and architecture docs can support a build plan
