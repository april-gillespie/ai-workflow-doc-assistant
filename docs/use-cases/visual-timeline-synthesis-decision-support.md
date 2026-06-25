# Visual Timeline Synthesis for Decision Support

**Date captured:** June 25, 2026  
**Category:** Personal workflow / decision support  
**Status:** Use case documented

## Summary

This workflow converts selected screenshots from a timestamped visual recording into a coherent timeline, rough observational estimates, and practical next-step recommendations.

The source example is an overnight household camera recording used to understand a disrupted parent/toddler sleep period. The professional value of the workflow is broader: it demonstrates how AI can help turn fragmented visual evidence into a structured, human-reviewed decision-support artifact.

This is not a medical, diagnostic, surveillance, or clinical workflow. The output is intended to support practical human decision-making when the available evidence is incomplete and distributed across multiple images.

## Problem

Real-world evidence is often fragmented. A person may have screenshots, timestamps, photos, notes, or short clips, but not a clean written record of what happened.

In the source example, the parent had an overnight camera recording that showed repeated wake-ups, movement, and interruptions. Reviewing the full video manually would have been time-consuming. Individual screenshots were easier to capture, but they were not useful until they were organized into a coherent sequence.

This workflow addresses the gap between raw visual evidence and an actionable summary.

## Inputs

The workflow begins with a set of timestamped screenshots taken from a longer visual record.

Example screenshot triggers include:

- A visible start state
- A person or subject appearing awake, asleep, upset, active, or settled
- A meaningful change in position, posture, location, or behavior
- A visible interaction between people
- A large time gap between events
- A visible end state

Each screenshot should include a timestamp or be accompanied by one.

## Process

1. Arrange screenshots in chronological order.
2. Extract or record the timestamp from each screenshot.
3. Describe only what is visually observable in each frame.
4. Identify likely events, changes, and interruptions.
5. Convert the screenshot sequence into a plain-language timeline.
6. Make rough estimates only when the visual evidence supports them.
7. Clearly separate observation from interpretation.
8. State the uncertainty level of any estimate.
9. Add a practical takeaway that supports a real-world decision.
10. Review the output manually before relying on it or sharing it.

## Output

The output is a short decision-support report that includes:

- Timestamped timeline of notable events
- Brief description of what appears to be happening
- Rough estimates where appropriate
- Confidence or uncertainty notes
- Practical takeaway
- Suggested next action

## Example Output Structure

```text
10:47 PM — Subject appears settled. Observer is awake.
12:01 AM — Subject is sitting up. Observer appears asleep or very tired.
1:39 AM — Subject interacts with observer while observer appears asleep.
3:52 AM — Subject is active and moving around the space.
6:52 AM — Subject is awake and upset. Observer appears to wake up.

Rough estimate:
- Observer rest: approximately 3-4 hours total, fragmented.
- Subject rest: approximately 6-7 hours total, interrupted.

Confidence: Low to moderate. Estimate is based on selected screenshots, not continuous measurement.

Takeaway: The observer's rest appears significantly disrupted. A recovery block or alternate coverage may be appropriate.
```

## Workflow Metadata

This section captures implementation context without making the artifact dependent on a specific vendor, model, or version.

| Field | Description |
| --- | --- |
| Tool category | Multimodal AI assistant capable of reviewing uploaded images and generating structured text |
| Model/version | Not specified in the public artifact because model availability and naming change frequently; exact model/version can be tracked privately when needed |
| Input format | Selected timestamped screenshots from a longer visual recording |
| Output format | Timeline summary, rough observational estimates, uncertainty note, and practical next action |
| Prompting approach | Chronological review, observation-versus-interpretation separation, uncertainty language, and practical decision framing |
| Human review step | Manual check of timestamps, descriptions, privacy, tone, and estimate confidence |
| Risk controls | No raw screenshots, no identifying details, no clinical claims, no definitive estimates, and no replacement of human judgment |
| Reuse potential | Applicable to other fragmented visual records where the desired output is a timeline, summary, or decision-support note |

A sanitized prompt pattern for this workflow is documented separately in `prompts/visual_timeline_synthesis_prompt_v1.md`.

## Practical Value

This workflow turns a vague or subjective statement into a concrete timeline that another person can review quickly.

The value is not exact measurement. The value is making a pattern visible enough to support action.

Possible actions include:

- Assigning another person to cover the next time block
- Adjusting the next-day schedule based on observed disruption
- Comparing several events or nights to identify recurring patterns
- Deciding whether more formal tracking is needed
- Improving communication between people sharing responsibility for the outcome

## Human-in-the-Loop Review

A human reviewer should confirm that the generated timeline matches the screenshots and remove any overconfident language.

The reviewer should especially check:

- Whether timestamps were read correctly
- Whether the descriptions match what is visible
- Whether estimates sound more precise than the evidence supports
- Whether private or identifying details should be removed before sharing
- Whether the final takeaway is practical, fair, and proportionate

## Limitations

This workflow does not measure clinical sleep quality, health status, intent, emotional state, or exact duration of any event.

Screenshots only show selected moments. A person may appear asleep while awake, or appear active while still getting some rest. Time gaps may include events that were not captured.

All estimates should be treated as rough observational estimates, not definitive conclusions.

## Privacy and Safety Notes

No raw screenshots, video, child images, names, private household details, or sensitive personal information should be included in a public portfolio version of this workflow.

The shareable artifact should document the process, not expose the private source material.

## What This Demonstrates

This use case demonstrates practical AI-assisted workflow design:

- Turning fragmented visual inputs into a structured timeline
- Translating messy real-world context into usable documentation
- Supporting decisions without overclaiming certainty
- Preserving human judgment in the review loop
- Identifying practical actions from incomplete evidence
- Creating a repeatable process from a one-off situation

## Career Relevance

This workflow supports a broader professional narrative around AI solutions, workflow modernization, and human-centered decision support.

It demonstrates the ability to:

- Recognize practical AI use cases in unstructured situations
- Define inputs, outputs, constraints, and review steps
- Convert ambiguous evidence into an actionable summary
- Communicate limitations clearly
- Design workflows that support human decisions rather than replacing judgment

## Possible Improvements

Future versions could add:

- A standard screenshot capture checklist
- A reusable report template
- A confidence rating for each estimated window or event
- A simple template for comparing multiple events over time
- A context field for unusual conditions that may affect interpretation
- A follow-up field documenting what action was taken afterward
