# AI Workflow Portfolio

Practical AI workflow design for enterprise adoption, evaluation, and human-reviewed operations.

I design workflows that turn unstructured inputs—such as emails, transcripts, documents, screenshots, observations, and operational requests—into structured, reviewable outputs that fit the way people actually work.

This repository contains sanitized and fictional public artifacts documenting the underlying problem-solving, architecture, evaluation, privacy, and adoption decisions behind those workflows.

The goal is not to present AI as a replacement for human judgment. The goal is to show how AI can help organize confusing inputs, make patterns easier to see, and support better decisions when a person remains in the review loop.

This repository is personal work created outside of my employer. It does not include employer work product, customer information, internal materials, proprietary processes, confidential data, or employer-owned content.

## Why This Matters

Many practical problems are not caused by a lack of information. They are caused by information being scattered, inconsistent, unclear, visual, repetitive, or hard to review quickly.

This portfolio explores how AI can help in those situations when the workflow has clear inputs, outputs, review steps, privacy boundaries, evaluation criteria, and limitations.

The emphasis is practical usefulness: better summaries, clearer decisions, reusable prompts, documented processes, human-reviewed outputs, and workflows designed for adoption.

## Intended Audience

This repository may be useful for people interested in:

- AI-assisted workflow design
- AI solutions engineering portfolio examples
- Enterprise AI adoption
- Technical enablement and technical communication
- Human-AI collaboration
- Knowledge capture and workflow modernization
- Small business process improvement
- Decision-support systems with human validation
- Practical prompt engineering

## Current Status

This portfolio is actively growing. The current focus is documenting practical workflow examples before expanding into more technical prototypes, sample materials, and lightweight automation.

Planned improvements include:

- Stronger architecture documentation
- Expanded workflow diagrams
- Prompt versioning and evaluation criteria
- More sample inputs and outputs
- Lightweight Python examples for data cleanup and categorization
- Clearer before-and-after case study artifacts
- Labeled test sets and simple evaluation rubrics
- Review queues, audit trails, and approval metrics

## Start Here: Featured Projects

These are the best starting points for a quick portfolio review.

### 1. AI-Assisted Customer Feedback Capture and Synthesis

A sanitized reconstruction inspired by a real enterprise workflow challenge: sustaining high-quality customer-feedback capture across email and meeting transcripts without adding repetitive documentation work to engineers.

This is the strongest AI solutions and adoption example because it shows stakeholder discovery, multi-source workflow design, deterministic automation, LLM-assisted interpretation, human review, privacy controls, domain-expert evaluation, measurable operational value, and a clear path toward integrated deployment.

- [Customer feedback capture and synthesis case study](docs/case-studies/ai-assisted-customer-feedback-capture.md)

### 2. Expert-Governed AI Tool Evaluation

A sanitized case study showing how a controlled workflow can support evaluation of an AI-powered tool by generating first-pass QA reviewer comments while preserving completed review work, workbook controls, and final expert judgment.

This is the strongest AI evaluation example because it shows expert-governed QA, scoped automation, review integrity, controlled workbook updates, and validation against unintended changes.

- [Expert-governed AI tool evaluation case study](docs/case-studies/expert-governed-ai-tool-evaluation.md)

### 3. Enterprise AI Intake and Triage Workflow

A documentation-first enterprise workflow showing how messy support or operations requests can be converted into structured, human-reviewed triage records.

This is the strongest enterprise architecture example because it shows intake logic, structured extraction, priority handling, routing recommendations, privacy flags, human review, APIs, records, auditability, and review-queue thinking.

- [Enterprise intake and triage case study](docs/case-studies/enterprise-ai-intake-triage-workflow.md)
- [Enterprise triage architecture notes](docs/architecture/enterprise-ai-triage-architecture.md)
- [Fictional sample intake tickets](sample_inputs/enterprise_intake_tickets.json)
- [Reusable triage prompt](prompts/enterprise_triage_prompt_v1.md)
- [Sample triage results](sample_outputs/enterprise_triage_results_v1.json)

### 4. Voice-to-Agent Inbox Cleanup Workflow

A case study showing how an external AI voice-capture tool can act as the intake layer for a task-specific AI assistant connected to a real application.

This demonstrates external AI tool integration, voice-to-action workflow design, specialized AI handoff, connected application use, reversible boundaries, and completion reporting.

- [Voice-to-agent inbox cleanup case study](docs/case-studies/voice-to-agent-inbox-cleanup-workflow.md)

### 5. Visual Timeline Synthesis for Decision Support

A workflow for converting selected screenshots from a timestamped visual record into a structured timeline, rough observational estimates, uncertainty notes, and practical next-step recommendations.

This is the strongest multimodal example because it shows a full workflow pattern: messy visual input, structured timeline, human review, uncertainty language, and practical decision support.

- [Part 1: Decision-support workflow](docs/use-cases/visual-timeline-synthesis-decision-support.md)
- [Part 2: Pattern validation through iterative runs](docs/use-cases/visual-timeline-synthesis-pattern-validation.md)
- [Reusable prompt pattern](prompts/visual_timeline_synthesis_prompt_v1.md)

### 6. AI-Assisted Home Network Diagnostic Case Study

A case study showing how screenshots and location-based testing can turn a vague household internet complaint into a structured technical diagnosis and cost-aware recommendation.

This demonstrates evidence-based troubleshooting, structured observation, technical communication, and practical recommendation design.

- [Home network diagnostic case study](docs/case-studies/home-network-diagnostic-ai-assisted.md)

### 7. AI-Assisted Resume Transformation Workflow

A case study showing how multiple resume versions and a small amount of supplemental context can be consolidated into targeted career assets and role recommendations.

This demonstrates information synthesis, audience-aware rewriting, structured decision support, and human-reviewed content transformation.

- [Resume transformation case study](docs/case-studies/resume-transformation-workflow.md)

### 8. Small Business Website Completion Workflow

A case study showing how AI-assisted content standardization can help a small business owner complete repetitive website work while preserving brand voice and presentation style.

This demonstrates workflow modernization, content standardization, and practical small-business process support.

- [Small business website completion workflow](portfolio/small-business-website-completion/README.md)

### 9. Supporting Prompt Prototype: Documentation Quality Review

A reusable prompt prototype for checking documentation for clarity, completeness, consistency, and usability.

This is included as a supporting artifact rather than the lead project. It demonstrates prompt structure, review criteria, and reusable evaluation patterns.

- [Documentation review prompt](prompts/review_prompt_v1.md)
- [Sample review output](sample_outputs/review_feedback_v1.md)

## What This Repository Demonstrates

This portfolio is designed to show practical AI workflow design, especially for roles involving AI solutions, technical communication, enablement, workflow modernization, or human-centered decision support.

Key demonstrated skills include:

- Enterprise customer feedback capture and synthesis
- Adoption-oriented workflow design
- Hybrid deterministic automation and LLM workflows
- Qualitative domain-expert evaluation
- Expert-governed AI tool evaluation
- AI evaluation QA workflow design
- Controlled automation in structured review artifacts
- AI-assisted workflow design
- Human-in-the-loop review and validation
- External AI tool integration as a workflow intake layer
- Voice-to-action workflow design
- Specialized AI assistant handoff based on task type
- Connected application workflow design
- Prompt design for practical workflows
- Enterprise-style intake and triage workflow design
- Structured extraction from unstructured requests
- Routing, prioritization, and review-queue thinking
- Architecture documentation for API, database, audit, and human-review boundaries
- Multimodal analysis using screenshots and visual evidence
- Information synthesis from fragmented inputs
- Uncertainty handling and limitation-setting
- Decision-support documentation
- Evidence-based troubleshooting
- Reusable process design
- Documentation modernization
- Technical communication for non-ideal, real-world inputs
- Translating unstructured context into organized recommendations
- Practical evaluation through repeated observation and feedback loops

## General Workflow Pattern

Most examples in this repository follow a similar pattern:

1. Start with incomplete, unstructured, inconsistent, visual, or repetitive inputs.
2. Define the desired output and decision context.
3. Understand the needs and behavior of the people expected to use the workflow.
4. Separate deterministic automation from language or judgment tasks.
5. Apply a structured AI-assisted workflow where it adds value.
6. Route the task to the appropriate specialized assistant, prompt pattern, or connected system when needed.
7. Generate organized documentation, recommendations, summaries, or next actions.
8. Review the output with human judgment.
9. Identify uncertainty, limitations, privacy concerns, and failure modes.
10. Refine and evaluate the process so it can be repeated more consistently.

## Repository Map

| Location | Purpose |
| --- | --- |
| [`docs/case-studies/`](docs/case-studies/) | Longer case studies that show a problem, workflow, output, and practical value |
| [`docs/use-cases/`](docs/use-cases/) | Focused AI workflow use cases and reusable patterns |
| [`docs/architecture/`](docs/architecture/) | Architecture notes for enterprise-style workflow concepts |
| [`prompts/`](prompts/) | Reusable prompt patterns and prompt prototypes |
| [`sample_inputs/`](sample_inputs/) | Sanitized or fictionalized inputs for workflow testing |
| [`sample_outputs/`](sample_outputs/) | Example outputs generated from prompts or workflow patterns |
| [`portfolio/`](portfolio/) | Portfolio-ready project writeups and applied workflow examples |
| [`docs/architecture_overview.md`](docs/architecture_overview.md) | Early architecture notes for human-in-the-loop document workflows |
| [`docs/workflow_diagram.md`](docs/workflow_diagram.md) | Workflow structure and process notes |
| [`portfolio-linkedin-summary.md`](portfolio-linkedin-summary.md) | LinkedIn-safe project description and posting language |

## Privacy and Confidentiality Policy

This repository is intentionally sanitized for public sharing.

No employer work product, customer information, internal materials, proprietary processes, confidential data, or employer-owned content is included.

No customer, employer, proprietary, confidential, or personally identifiable information is included.

When an example is inspired by a real situation, the visible details are changed, simplified, anonymized, generalized, or replaced with synthetic content before being shared publicly.

Raw source materials such as private screenshots, household images, private documents, customer materials, or identifying records are not included. The public artifacts document the workflow pattern and problem-solving approach, not the private source material.

## Repository Direction

The long-term goal is to build this into a practical portfolio showing how AI can be used to create repeatable enterprise, personal, small business, technical, and operational workflows, not just one-off generated content.

The emphasis is on structured thinking, workflow design, human validation, privacy-aware documentation, adoption, evaluation, and practical usefulness.
