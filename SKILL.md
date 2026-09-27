---
name: customer-insight-synthesizer
description: synthesize customer interview notes, transcripts, research docs, google drive files, and asana tasks into product insights focused on pain points. use when the user asks to summarize customer interviews, identify pain points, extract product opportunities, compare interview themes, turn customer feedback into product recommendations, or create follow-up actions in asana. use google drive when interview notes or research docs may live there, and use asana when product tasks, feature requests, or follow-up work should be checked or drafted.
---

# Customer Insight Synthesizer

## Overview

Transform customer interview notes into product insights with a strong bias toward evidence-backed pain points, product opportunities, and actionable follow-up. Use Google Drive as the primary source for interview notes and research documents, and Asana as the primary source for related product work, existing feature requests, and follow-up tasks.

## Workflow

1. Clarify the research scope only when it is missing and blocks useful work:
   - customer, segment, persona, product area, time period, or interview set
   - whether the user wants a single-interview summary or cross-interview synthesis
   - whether to draft Asana follow-up tasks or only recommend them
2. Gather source material:
   - If the user pasted interview notes, analyze them directly.
   - If the user references files, customers, projects, folders, or research topics, search Google Drive for interview notes, transcripts, call summaries, research docs, and tagged feedback.
   - Search Asana for related tasks, feature requests, bugs, roadmap items, previous customer requests, or open follow-ups tied to the same customer, persona, product area, or pain point.
3. Extract pain points:
   - Identify explicit complaints, blockers, inefficiencies, confusion, risk, unmet goals, repeated workarounds, switching costs, and emotional frustration.
   - Separate observed evidence from interpretation.
   - Preserve short customer quotes when available.
4. Cluster findings:
   - Group pain points into themes.
   - Merge duplicates and note how many interviews or sources support each theme.
   - Distinguish high-frequency issues from high-severity but low-frequency issues.
5. Translate into product insights:
   - For each theme, state the product implication, user need, affected workflow, and opportunity.
   - Connect to existing Asana work when relevant.
   - Flag whether an opportunity appears new, already tracked, blocked, or needs validation.
6. Prioritize:
   - Score each pain point using severity, frequency, business impact, confidence, and product fit.
   - Do not overstate certainty when the evidence is thin.
7. Produce the report using the default template in `references/report-template.md`.

## Google Drive Guidance

When using Google Drive:

- Search broadly first, then narrow using customer name, product area, interview date, persona, and terms like `interview`, `notes`, `transcript`, `research`, `feedback`, `pain point`, `discovery`, and `customer call`.
- Prefer original notes and transcripts over secondhand summaries.
- For long-running research docs, check dates inside the content before treating material as current.
- Track which interviews or files support each theme.
- Cite documents when citations are available.

## Asana Guidance

When using Asana:

- Search for related tasks using customer names, product areas, pain point keywords, feature request phrases, and known internal project names.
- Link pain points to existing tasks when possible.
- Do not create or modify Asana tasks unless the user explicitly asks.
- When drafting tasks, use this structure:
  - title: concise user pain or opportunity
  - problem: evidence-backed description
  - customer evidence: quotes or file references
  - proposed next step: discovery, design, engineering review, bug triage, or roadmap consideration
  - priority rationale: severity, frequency, impact, confidence

## Pain Point Analysis Rules

- Treat pain points as problems users experience, not feature requests users propose.
- Convert feature requests into underlying needs. Example: "export to CSV" may indicate reporting, audit, migration, or collaboration pain.
- Keep confidence calibrated:
  - high: repeated across multiple interviews or strongly supported by detailed evidence
  - medium: clearly stated once or supported by Asana history
  - low: inferred, ambiguous, or based on weak evidence
- Mark contradictions clearly when customers disagree.
- Avoid turning every complaint into a roadmap recommendation. Some findings may be onboarding, support, pricing, documentation, or positioning issues.

## Output Requirements

Use `references/report-template.md` as the default report structure. Adapt sections only when the user asks for a different format.

Always include:

- executive summary
- prioritized pain points
- evidence
- product insight or opportunity
- Asana connections or suggested follow-ups
- open questions / validation gaps

For each pain point, include:

- theme name
- who experiences it
- user goal being blocked
- evidence
- severity
- frequency
- confidence
- product implication
- recommended next action

## Resource Loading

Read `references/report-template.md` when producing a final synthesis report.
Read `references/pain-point-taxonomy.md` when the notes are messy, broad, or difficult to classify.
