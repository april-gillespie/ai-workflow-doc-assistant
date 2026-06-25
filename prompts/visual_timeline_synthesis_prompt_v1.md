# Visual Timeline Synthesis Prompt v1

**Date captured:** June 25, 2026  
**Associated use case:** `docs/use-cases/visual-timeline-synthesis-decision-support.md`  
**Status:** Sanitized prompt pattern

## Purpose

This prompt pattern supports the creation of a structured timeline and decision-support summary from a set of timestamped screenshots or images.

It is designed for situations where the goal is to understand what appears to have happened over time, not to make clinical, legal, safety, or definitive claims.

## Prompt Template

```text
I am uploading a sequence of timestamped screenshots from a longer visual recording.

Please review the images in chronological order and create a concise decision-support report.

For each screenshot:
- Extract or record the visible timestamp if available.
- Describe only what is visually observable.
- Avoid guessing intent, health status, emotional state, or anything not visible.
- Use uncertainty language when the image is ambiguous.

Please produce:
1. A timestamped timeline of notable events.
2. A short summary of the overall pattern.
3. Rough observational estimates only if the evidence supports them.
4. A confidence note explaining the limitations of the estimate.
5. A practical takeaway or next action based on the observed pattern.

Important constraints:
- This is not a medical, diagnostic, legal, or clinical analysis.
- Do not identify people by name.
- Do not make definitive claims from a single screenshot.
- Separate observation from interpretation.
- Keep the report useful, concise, and easy for another person to review.
```

## Optional Follow-Up Prompt

```text
Now revise the report for a public portfolio artifact.

Remove private details, names, images, and household-specific context.
Reframe the example as a general workflow for converting fragmented timestamped visual evidence into a structured timeline and decision-support summary.
Keep the focus on inputs, process, human review, limitations, and practical value.
```

## Notes

This prompt is intentionally tool-agnostic. The workflow can be performed with any multimodal AI assistant capable of reviewing uploaded images and producing structured text.

Model/version details should be tracked privately when needed for reproducibility, but are not required in the public portfolio artifact unless the use case is specifically evaluating model performance.
