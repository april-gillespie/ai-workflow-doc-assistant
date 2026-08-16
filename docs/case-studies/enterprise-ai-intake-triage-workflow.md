# Enterprise AI Intake and Triage Workflow

**Status:** Documentation-first MVP using fictional data  
**Implementation:** Prompt, sample input, sample output, and architecture documentation  
**Focus:** Structured intake, routing support, and human review

## Summary

This project explores how inconsistent support or operations requests can be converted into structured triage proposals.

Each proposal includes a summary, category, priority, missing information, recommended next action, confidence, sensitivity flags, and a reason for human review. The workflow supports a reviewer; it does not assign ownership, approve access, or make final business decisions.

## Problem

Requests often arrive through forms, email, chat, shared inboxes, and informal handoffs. They may be incomplete, inconsistent, or unclear.

Before routing a request, a person may need to:

- Determine the category
- Identify missing details
- Judge urgency
- Recommend an owner or next action
- Detect sensitive content
- Decide whether escalation is required

The repetitive structure makes AI assistance useful, but the judgment and risk require human review.

## Public Artifacts

- [Fictional intake tickets](../../sample_inputs/enterprise_intake_tickets.json)
- [Reusable triage prompt](../../prompts/enterprise_triage_prompt_v1.md)
- [Sample triage results](../../sample_outputs/enterprise_triage_results_v1.json)
- [Architecture notes](../architecture/enterprise-ai-triage-architecture.md)

## Workflow

```text
Request
  -> intake and basic validation
  -> AI-assisted structured proposal
  -> human review queue
  -> correction and approval
  -> routing, response draft, or escalation
  -> audit record
```

## Output Schema

The proposed record includes:

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

## Human Review

Before operational use, a reviewer confirms:

- Category and priority
- Missing information
- Recommended next action
- Routing recommendation
- Privacy or sensitivity flags
- Need for escalation
- Whether the output is appropriate to store or share

## Evaluation Criteria

| Criterion | Review question |
| --- | --- |
| Category accuracy | Is the request classified correctly? |
| Priority reasonableness | Is the urgency supported by the request? |
| Missing information | Does the proposal identify what is needed? |
| Routing usefulness | Would the recommended owner know what to do next? |
| Human-review fit | Are uncertain or high-risk cases escalated? |
| Privacy handling | Are sensitive details flagged appropriately? |
| Consistency | Do similar inputs produce comparable structures? |

## My Contribution

I defined the fictional scenario, workflow boundaries, output schema, review criteria, prompt structure, sample inputs and outputs, and architecture documentation.

AI tools assisted drafting and artifact generation. I reviewed the structure, limitations, and public materials and retained responsibility for the final design decisions.

## Implementation Boundaries

This is a documentation-first MVP, not a deployed application. It does not currently include a live API, database, review interface, authentication, production monitoring, or system integration.

A real deployment would require identity and access controls, secure retention policies, logging, compliance review, evaluation against labeled examples, and integration with approved systems.

## Public-Work Boundaries

All visible tickets and outputs are fictional. The project does not reproduce employer systems, customer data, internal materials, proprietary configurations, confidential prompts, or private implementation details.
