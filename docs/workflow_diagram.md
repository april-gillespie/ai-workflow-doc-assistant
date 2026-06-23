# Workflow Diagram

## AI-Assisted Document Review Workflow

This document provides a high-level workflow diagram for the AI-assisted document review process.

The workflow is designed to keep AI assistance structured, reviewable, and subordinate to human judgment.

## Simple Flow

```text
Source Document
      ↓
Document Intake
      ↓
Structured Review Prompt
      ↓
AI-Assisted Analysis
      ↓
Structured Feedback Output
      ↓
Human Review Gate
      ↓
Final Decision
      ↓
Document Revision or Follow-Up Action
```

## Expanded Flow

```text
[1] Source Document
        |
        v
[2] Intake and Context Check
        |
        |-- Is the document in scope?
        |       |-- No  → Stop or redirect to appropriate reviewer
        |       |-- Yes → Continue
        v
[3] Apply Structured Review Prompt
        |
        v
[4] AI-Assisted Review
        |
        |-- Evaluate clarity
        |-- Evaluate completeness
        |-- Evaluate consistency
        |-- Identify missing assumptions
        |-- Identify usability issues
        |-- Flag items needing human or SME review
        v
[5] Generate Structured Feedback
        |
        |-- Overall assessment
        |-- Strengths
        |-- Areas for improvement
        |-- Recommendations
        |-- Human review notes
        |-- Escalation items
        v
[6] Human Review Gate
        |
        |-- Accept recommendation
        |-- Modify recommendation
        |-- Reject recommendation
        |-- Escalate to subject matter expert
        |-- Defer for later review
        v
[7] Final Decision
        |
        |-- Revise document
        |-- Request more information
        |-- Approve current version
        |-- Route for expert review
        v
[8] Updated Document or Action Plan
```

## Workflow Stages

### 1. Source Document

The workflow begins with a draft, sample, or existing document that needs review.

Examples may include:

- Technical documentation
- Workflow instructions
- Training material
- Standard operating procedures
- Onboarding content
- Synthetic sample documents

### 2. Intake and Context Check

Before review begins, the document should be checked for scope and context.

Key questions:

- What type of document is being reviewed?
- Who is the intended audience?
- What decision or action should the document support?
- Is the document appropriate for AI-assisted review?
- Does the document contain sensitive or confidential information?

Documents containing confidential, proprietary, customer, employer, or personally identifiable information should not be processed in this public portfolio workflow.

### 3. Structured Review Prompt

A structured prompt defines the reviewer role, evaluation criteria, and output format.

The prompt helps prevent vague or inconsistent feedback by giving the AI model a repeatable review structure.

Current prompt location: `prompts/review_prompt_v1.md`

### 4. AI-Assisted Analysis

The AI model reviews the document against defined criteria.

The review focuses on practical document quality factors such as:

- Clarity
- Completeness
- Consistency
- Usability
- Missing assumptions
- Actionability
- Audience fit
- Areas requiring human validation

### 5. Structured Feedback Output

The output should be organized so that a human reviewer can quickly act on it.

Recommended feedback categories:

- Overall assessment
- Strengths
- Areas for improvement
- Recommended changes
- Priority or severity
- Human review notes
- Subject matter expert review required

### 6. Human Review Gate

The human reviewer evaluates whether the AI feedback is accurate, useful, and appropriate.

The reviewer decides whether to:

- Accept the recommendation
- Modify the recommendation
- Reject the recommendation
- Escalate the issue
- Request more context
- Defer the item

### 7. Final Decision

The final decision remains with the human reviewer or document owner.

AI-generated feedback should not be treated as approval authority.

### 8. Updated Document or Action Plan

The workflow ends with either a revised document or a documented action plan.

Possible outcomes include:

- Updated document
- Review notes for later
- Escalation to a subject matter expert
- Request for missing context
- Prompt improvement notes
- No change needed

## Quality Gates

The workflow includes several quality gates:

| Gate | Purpose |
| --- | --- |
| Scope Check | Confirms the document is appropriate for this workflow. |
| Prompt Structure | Ensures review criteria are defined before analysis begins. |
| Feedback Formatting | Makes the AI output easier to review and compare. |
| Human Review | Prevents unsupported AI recommendations from being accepted automatically. |
| Final Decision | Keeps publication, approval, or revision authority with a person. |

## Key Principle

The workflow is not designed to automate judgment.

It is designed to make review work more structured, consistent, and easier to act on while preserving human control over final decisions.