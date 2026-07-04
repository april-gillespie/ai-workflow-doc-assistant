# Course Audio Note Workflow — Supervised Machine Learning

Date: 2026-07-03

## Summary

This note documents a workflow experiment while progressing through DeepLearning.ai's **Supervised Machine Learning: Regression and Classification** course. The goal was to test whether lightweight audio notes can capture useful technical insights while rewatching course material, especially when fatigue makes traditional note-taking less effective.

The main question is whether the resulting summary has enough information density to justify the raw recording size, particularly when long recordings include silence while course videos play.

## Core Thesis

Audio capture may be useful as a second-pass technical learning workflow when the durable artifact is the structured AI-generated summary, not the raw recording itself.

For this use case, the audio file is best treated as temporary source material. The retained artifact should be a concise, human-reviewed note that captures the concepts, workflow observations, open questions, and next steps.

## Course Concepts Captured

### Supervised learning

Supervised learning uses training data that includes example inputs and the expected answers. The model learns from labeled examples.

Two primary supervised learning categories reviewed were:

- **Regression:** predicting continuous numeric outputs.
- **Classification:** predicting discrete categories or labels.

### Unsupervised learning

Unsupervised learning works with unlabeled data and focuses on finding structure or patterns.

Examples reviewed included:

- **Clustering:** grouping similar data points.
- **Anomaly detection:** identifying unusual data points or outliers.
- **Dimensionality reduction:** representing data with fewer numbers while preserving useful structure.

### Jupyter Notebooks

The course uses Jupyter Notebooks as the primary hands-on environment. This is familiar because of prior Python-for-engineers coursework.

Key environment note:

- `Shift + Enter` runs a code cell.

The hands-on notebook work requires a computer. The mobile recording workflow can support reflection and capture, but it does not replace the computer-based coding environment.

## Workflow Observations

### What worked

- Audio notes allowed thoughts to be captured as they came up during course review.
- The method reduced the pressure to produce polished written notes while tired.
- The resulting AI summary made it easier to separate durable insights from raw spoken observations.
- The workflow captured both technical content and process-level observations.

### What did not work cleanly

- Long recordings may contain a low ratio of spoken content to silence.
- Raw audio files may become unnecessarily large if recorded continuously during video playback.
- The value of the method depends on whether the AI summary is accurate, concise, and useful after human review.
- Mobile capture helps with reflection, but the course itself still requires a computer for Jupyter work.

## Storage and Documentation Decision

The best long-term approach is:

1. Record only when useful observations come up, rather than capturing long silent stretches.
2. Generate a structured AI summary from the recording.
3. Human-review the summary for accuracy and usefulness.
4. Keep the Markdown note as the durable artifact.
5. Delete the raw audio when it no longer has independent value.

This preserves the learning signal while avoiding unnecessary storage bloat.

## Signal-to-Noise Evaluation

This workflow is worth continuing if future notes meet at least one of these criteria:

- They clarify a technical concept.
- They capture a useful analogy or mental model.
- They identify a blocker, tool constraint, or next action.
- They connect course content to AI workflow design, evaluation, documentation, or portfolio development.

If a recording only restates obvious course content without adding reflection or next steps, the summary should not be kept as a standalone artifact.

## Portfolio Relevance

This is a supporting documentation artifact rather than a finished machine learning project.

It demonstrates:

- Technical learning documentation.
- AI-assisted knowledge capture.
- Human-reviewed summarization.
- Workflow evaluation.
- Storage and information-density trade-off analysis.
- Practical boundaries between mobile capture and computer-based technical work.

## Next Steps

- Continue the DeepLearning.ai course from a computer.
- Complete the hands-on Jupyter Notebook exercises.
- Use audio notes selectively during review, not continuously during passive video watching.
- Keep course notes only when they add technical understanding, workflow insight, or portfolio-relevant reflection.
