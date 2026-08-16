# AI Workflow Portfolio

**Documentation-first case studies for practical, human-reviewed AI workflows.**

[Professional portfolio →](https://april-gillespie-ai-portfolio.aprilgillespie.chatgpt.site/)

## Overview

This repository shows how I frame ambiguous problems, define workflow boundaries, structure unorganized inputs, design human review, and evaluate AI-assisted outputs.

It is a solution-design portfolio, not a production software application. The public artifacts include case studies, architecture notes, reusable prompts, and synthetic sample inputs and outputs.

## My Role

I selected the problems, defined constraints and success criteria, directed the workflow and architecture decisions, reviewed the outputs, and refined the public artifacts. AI tools assisted drafting and implementation; I retained responsibility for scope, verification, and final decisions.

## Featured Case Studies

| Case study | Status | Evidence |
| --- | --- | --- |
| [Customer Feedback Capture and Synthesis](docs/case-studies/ai-assisted-customer-feedback-capture.md) | Generalized workflow case study | Multi-source intake, structured records, human approval, evaluation criteria |
| [Expert-Governed AI Tool Evaluation](docs/case-studies/expert-governed-ai-tool-evaluation.md) | Sanitized evaluation case study | Scoped automation, file-integrity validation, final expert authority |
| [Enterprise AI Intake and Triage](docs/case-studies/enterprise-ai-intake-triage-workflow.md) | Documentation-first MVP using fictional data | [Architecture](docs/architecture/enterprise-ai-triage-architecture.md), [sample input](sample_inputs/enterprise_intake_tickets.json), [prompt](prompts/enterprise_triage_prompt_v1.md), [sample output](sample_outputs/enterprise_triage_results_v1.json) |
| [Documentation Quality Review](prompts/review_prompt_v1.md) | Reusable prompt prototype | Defined review criteria and [sample feedback](sample_outputs/review_feedback_v1.md) |

Additional workflow examples remain available under [case studies](docs/case-studies/), [use cases](docs/use-cases/), and [portfolio examples](portfolio/).

## Design Pattern

Most examples use the same controlled pattern:

1. Define the problem, user, and decision context.
2. Separate deterministic processing from language or judgment tasks.
3. Convert inconsistent inputs into a structured proposal.
4. Preserve source context and flag uncertainty or sensitive content.
5. Require human review before an operational decision or source-of-truth update.
6. Evaluate quality, limitations, and adoption fit before expanding automation.

## Capabilities Demonstrated

- Workflow and solution architecture
- Structured extraction from unstructured information
- Human-in-the-loop review design
- AI evaluation and QA support
- Privacy, uncertainty, and approval boundaries
- Synthetic test data and reusable prompt design
- Technical communication for mixed audiences
- Adoption-oriented process design

## Repository Map

| Location | Contents |
| --- | --- |
| [`docs/case-studies/`](docs/case-studies/) | Detailed problem, workflow, evaluation, and limitation writeups |
| [`docs/use-cases/`](docs/use-cases/) | Focused workflow patterns |
| [`docs/architecture/`](docs/architecture/) | Enterprise-style architecture notes |
| [`prompts/`](prompts/) | Reusable prompt prototypes |
| [`sample_inputs/`](sample_inputs/) | Fictional or sanitized test inputs |
| [`sample_outputs/`](sample_outputs/) | Example structured outputs |
| [`portfolio/`](portfolio/) | Supporting applied workflow examples |

## Public-Work Boundaries

The documentation and synthetic artifacts in this repository were created independently for public demonstration. Some generalized workflow patterns are informed by professional experience, but the repository does not reproduce employer systems or include employer work product, customer information, internal materials, proprietary configurations, confidential prompts, or private source data.

AI-generated outputs are treated as proposals. Human review remains responsible for factual verification, approval, and final decisions.
