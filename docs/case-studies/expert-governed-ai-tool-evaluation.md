# Expert-Governed AI Tool Evaluation

**Status:** Sanitized professional case study  
**Public implementation:** Source workbook and evaluation data not included  
**Focus:** Controlled automation, QA support, and expert authority

## Summary

This case study documents a controlled workflow for supporting evaluation of an AI-powered tool. The workflow generated first-pass QA comments for unfinished evaluation entries while preserving completed work and keeping final decisions under expert control.

AI-generated comments were treated as drafts. Factual verification, pass or fail decisions, and final acceptance remained with the reviewer.

## Problem

Structured AI evaluation can become repetitive when many entries require factual checks, consistent reviewer comments, and documented decisions. Automation can assist, but only if it changes the intended fields, preserves completed review work, and does not bypass expert judgment.

## Constraints

- Completed review entries must remain unchanged.
- Only the targeted reviewer-comment field may be updated.
- Existing workbook structure and review controls must be preserved.
- Generated comments are proposals, not final judgments.
- Final factual verification and acceptance remain with the expert reviewer.

## Method

1. Identify unfinished entries requiring first-pass comments.
2. Limit the workflow to the intended field and rows.
3. Preserve the original file.
4. Review the available question, context, model output, and reference material.
5. Generate concise draft QA comments.
6. Apply changes only to targeted entries.
7. Verify that completed work, unrelated fields, and review controls were unchanged.
8. Inspect the resulting workbook before returning it for expert review.

## Technical Challenge

Inconsistent row and cell formatting caused some target entries to be skipped during early validation. The update logic was adjusted to handle format variation without depending on one style pattern.

This made verification as important as generation. A successful workflow had to demonstrate that it changed only the intended content.

## Result

The workflow produced first-pass reviewer comments for the targeted unfinished entries while preserving completed reviewer work and existing controls.

The draft comments supported a more consistent first pass, but they did not replace factual verification, QA judgment, or final evaluation decisions. This public case study does not assert quantified ROI or production scale.

## My Contribution

I defined the update scope and review boundary, directed the AI-assisted drafting and file-update workflow, investigated skipped entries, refined the validation logic, and reviewed the resulting artifact for unintended changes.

AI tools assisted generation and implementation. I retained responsibility for constraints, verification, interpretation, and final acceptance.

## Capabilities Demonstrated

- Expert-governed AI evaluation
- Controlled automation in structured files
- Preservation of completed work
- Validation against unintended changes
- Debugging inconsistent workbook structures
- Clear separation between AI assistance and reviewer authority

## Public-Work Boundaries

This case study contains sanitized process descriptions only. It does not include the source workbook, evaluation content, proprietary tool details, employer materials, confidential data, or private implementation artifacts.
