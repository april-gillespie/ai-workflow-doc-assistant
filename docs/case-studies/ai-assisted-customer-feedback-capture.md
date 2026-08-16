# AI-Assisted Customer Feedback Capture and Synthesis

**Status:** Generalized professional case study  
**Public implementation:** Not included  
**Focus:** Knowledge capture, workflow adoption, and human-reviewed AI

## Summary

This case study presents a generalized workflow pattern for converting fragmented customer feedback from email and meeting transcripts into structured records for expert review.

The design goal is not autonomous record creation. It is to reduce repetitive drafting while keeping a qualified reviewer responsible for every record that enters the source of truth.

## Problem

Customer feedback often arrives through normal conversations rather than a dedicated intake process. The information may be valuable but difficult to reuse because it is scattered across long threads, transcripts, and informal handoffs.

A practical workflow must balance several needs:

| Stakeholder | Need |
| --- | --- |
| Engineers | Lower-friction documentation after customer interactions |
| Reviewers | Traceable proposals that can be checked against the source |
| Product and business teams | Consistent records that support comparison and synthesis |
| Customers | No additional reporting burden |

The central adoption challenge is fitting structured capture into existing work behavior without sacrificing accuracy.

## Workflow

```text
Authorized email or transcript source
  -> collection and normalization
  -> relevant-content segmentation
  -> LLM-assisted extraction
  -> proposed structured record
  -> expert comparison with the source
  -> correction, approval, or rejection
  -> approved tracker entry
```

Deterministic automation handles routing, field normalization, status tracking, and other predictable operations. Language-model assistance handles summarization and proposed extraction from inconsistent language. Human review remains the approval boundary.

## Key Design Decisions

### Prioritize trustworthy capture over artificial completeness

Some fields require context that cannot be inferred safely. The workflow proposes core information and leaves specialist fields for human completion when needed.

### Separate orchestration from interpretation

Rules-based processing is appropriate for known formats and routing. Constrained language-model processing is better suited to interpreting long conversations, provided that the output remains a reviewable proposal.

### Protect the source of truth

Generated content never becomes a final record automatically. The reviewer compares it with the original source, corrects unsupported statements, and approves or rejects the proposal.

## Review Criteria

The reviewer checks:

- Factual consistency with the source
- Preservation of the customer issue and requested outcome
- Exclusion of unrelated internal discussion
- Completeness of technically important context
- Correct categorization
- Unsupported or invented content
- Sensitive information requiring removal or different handling

## Safeguards

- Use only authorized systems and the minimum necessary content.
- Preserve the original source for verification.
- Keep proposed and approved records as separate states.
- Require human approval before a source-of-truth update.
- Screen for sensitive information before broader use.
- Use synthetic examples for public documentation and testing.

## Evaluation Approach

A domain-expert review can assess factual accuracy, omission rate, unsupported claims, classification quality, and usefulness for downstream review.

A more mature evaluation would use a labeled test set and track approval rate, correction rate, omission rate, unsupported-claim rate, processing time, review time, and consistency across similar inputs.

## My Contribution

My work included identifying the adoption problem, mapping stakeholder and input needs, testing rules-based and LLM-assisted approaches, defining the human-review boundary, evaluating output quality using domain expertise, and refining the workflow around user behavior.

AI tools supported drafting and technical experimentation. I retained responsibility for the problem definition, constraints, review criteria, verification, and final workflow decisions.

## Public-Work Boundaries

This public document was created independently and contains generalized process descriptions only. It does not include employer systems, customer information, internal materials, proprietary configurations, confidential prompts, private source data, or implementation details.

The intended benefits described here are workflow-design objectives, not claims from a controlled production benchmark.
