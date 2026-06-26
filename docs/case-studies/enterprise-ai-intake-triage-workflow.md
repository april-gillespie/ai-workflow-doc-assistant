# Enterprise AI Intake and Triage Workflow

**Date captured:** June 26, 2026  
**Category:** Enterprise workflow / AI-assisted decision support  
**Status:** Documentation-first MVP  
**Related artifacts:**

- `sample_inputs/enterprise_intake_tickets.json`
- `prompts/enterprise_triage_prompt_v1.md`
- `sample_outputs/enterprise_triage_results_v1.json`
- `docs/architecture/enterprise-ai-triage-architecture.md`

## Summary

This case study documents a generic enterprise-style workflow for using AI to support intake triage.

The workflow starts with messy support or operations requests and converts them into structured triage records. Each record includes a summary, category, priority, missing information, recommended next action, confidence level, privacy or sensitivity flags, and whether human review is required.

The goal is not to automate support ownership or replace human judgment. The goal is to show how AI can reduce ambiguity, improve intake quality, and help teams route work more consistently when requests arrive in inconsistent formats.

This is a sanitized portfolio project. It is not based on employer systems, employer data, customer data, proprietary workflows, or confidential materials.

## Enterprise Problem

Enterprise teams often receive requests through many channels: forms, email, chat, shared inboxes, ticketing systems, customer portals, or informal handoffs.

Those requests are frequently incomplete, inconsistent, or unclear. A person may need to read the request, determine the category, identify missing details, judge urgency, route it to the correct team, and decide whether escalation is needed.

That work is repetitive but judgment-heavy. It is a good fit for AI assistance only when the workflow preserves human review, privacy boundaries, and clear limitations.

## Example Scenario

A fictional company receives internal and external support requests related to software access, installation, training, documentation, bug reports, and account administration.

The intake team needs a faster way to convert each request into a structured triage record before assigning the ticket.

## Workflow Goals

The workflow is designed to:

- Convert unstructured requests into structured records
- Classify request type
- Estimate priority without overclaiming certainty
- Identify missing information
- Recommend a next action
- Flag privacy or sensitivity concerns
- Preserve a human review step before routing or response
- Create an audit-friendly record of the triage result

## Inputs

The input is a collection of fictional intake tickets. Each ticket includes:

- Ticket ID
- Request channel
- Requester type
- Raw request text
- Submitted timestamp
- Optional metadata such as product area or account type

Sample data is stored in `sample_inputs/enterprise_intake_tickets.json`.

## AI-Assisted Processing Step

The AI triage step reads the raw request and produces a structured output.

Expected output fields include:

- `ticket_id`
- `category`
- `priority`
- `summary`
- `missing_information`
- `recommended_next_action`
- `confidence`
- `requires_human_review`
- `human_review_reason`
- `privacy_or_sensitivity_flags`
- `routing_recommendation`

The reusable prompt pattern is stored in `prompts/enterprise_triage_prompt_v1.md`.

## Human Review Step

A human reviewer checks the structured output before it is used for routing, escalation, or response.

The reviewer confirms:

- Whether the category is correct
- Whether the priority is reasonable
- Whether missing information was identified
- Whether the recommended next action is appropriate
- Whether privacy or sensitivity flags were applied correctly
- Whether the request needs escalation
- Whether the output is safe to store or share

## Output

The output is a structured triage result for each ticket. A sample output set is stored in `sample_outputs/enterprise_triage_results_v1.json`.

The output is intended to support a human workflow, not to operate as an autonomous decision system.

## Architecture Concept

The workflow can be represented as:

```text
Requester
  -> Intake form / email / chat / ticket portal
  -> Backend API
  -> AI triage service
  -> Structured triage record
  -> Database
  -> Human review queue
  -> Routing / escalation / response draft
  -> Audit log and reporting
```

The architecture notes are documented in `docs/architecture/enterprise-ai-triage-architecture.md`.

## Enterprise Concepts Demonstrated

This project demonstrates awareness of enterprise software patterns, including:

- Intake workflows
- Backend/API boundaries
- Database-backed records
- Structured data extraction
- Ticket routing logic
- Human review queues
- Audit trails
- Role-based review concepts
- Privacy and sensitivity flags
- Confidence and uncertainty handling
- Workflow evaluation criteria
- Vendor-neutral AI system design

## Evaluation Criteria

A triage output should be evaluated against practical criteria:

| Criterion | Question |
| --- | --- |
| Category accuracy | Did the output classify the request correctly? |
| Priority reasonableness | Is the urgency appropriate based on the request text? |
| Missing information | Did the output identify what is needed to move forward? |
| Routing usefulness | Would the recommended owner/team know what to do next? |
| Human review fit | Did the workflow flag cases that should not be automated? |
| Privacy handling | Were sensitive details flagged or protected? |
| Consistency | Would similar inputs receive similar outputs? |

## Limitations

This workflow does not make final business decisions, approve access, resolve tickets, diagnose production systems, or replace subject matter experts.

The AI output may be wrong, incomplete, or overconfident. Human review is required before any operational action.

The sample data is fictional and simplified. Real enterprise deployment would require stronger security controls, identity management, logging, data retention rules, access controls, compliance review, and integration with existing systems.

## What This Demonstrates

This case study extends the portfolio beyond personal workflows and into enterprise-style software thinking.

It demonstrates the ability to:

- Translate a messy operational problem into a structured AI-assisted workflow
- Define inputs, outputs, review steps, and system boundaries
- Design for human review rather than full automation
- Think in terms of APIs, records, routing, auditability, and privacy
- Create reusable prompt and data artifacts
- Communicate limitations clearly
- Build a documentation-first MVP before writing production code

## Future Build Phases

Future versions could add:

1. A Python script that reads sample tickets and writes mock triage results
2. A FastAPI endpoint for submitting a ticket and returning a structured triage record
3. A SQLite or PostgreSQL database schema for ticket and review records
4. A simple human review queue
5. A Dockerfile for local deployment
6. GitHub Actions checks for formatting and sample data validation
7. A lightweight evaluation rubric comparing expected and actual outputs

## Portfolio Positioning

A concise way to describe this project:

> Designed a sanitized enterprise-style AI intake and triage workflow that converts messy support requests into structured, human-reviewed triage records with category, priority, missing information, recommended next action, confidence, routing, and privacy flags. Documented the workflow, sample data, reusable prompt pattern, sample outputs, and architecture notes to demonstrate enterprise software thinking around AI-assisted decision support.
