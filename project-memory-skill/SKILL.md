---
name: project-memory
description: Use this skill when the user wants to organize a project's important background, key decisions, current status, and next steps so the work can be picked up again after long chats, group discussions, or a gap in time. This skill helps the agent maintain a short, clear, recoverable single-project document and ask the human to clarify anything important that is still unclear.
---

# Project Memory

Use this skill to maintain a durable document for a single project. The goal is not to preserve the full history. The goal is to keep a short, reliable project record that helps the agent and the user quickly get back into context later.

## When to use

Use this skill in situations like these:

- The user wants to get a project's background, goals, and current status into a clear shape before continuing work.
- The user wants to turn a recent chat, group discussion, or thread into project information that will still matter later.
- The user wants to quickly recover the important context of a project after some time has passed.
- The user wants to add a new decision, constraint, todo, file location, or other important detail to the project's materials.
- The user wants the agent to keep project information organized as the conversation continues instead of re-understanding everything from scratch each time.
- The user wants to leave a clear restart point, handoff note, or reminder for the next time this project resumes.
- The agent notices that the project background, goal, confirmer, or document location is unclear and needs to ask the human before continuing.

This skill is for one project at a time. Do not turn it into a multi-project system unless the user explicitly asks for that.

## Core rules

- Only record information that is likely to matter later.
- Treat the project document as a recovery artifact, not a meeting transcript or activity log.
- When the project document cannot be located or read, first ask the user to confirm where it is stored and what the actual path or link is; once known, record that in the `Document Info` section.
- Prefer updating existing content instead of appending duplicate notes.
- Keep the document short, scannable, and stable.
- Treat project background as a high-value, mostly stable anchor.
- Use SMART thinking when recording goals, even if the final goal is written as a short paragraph rather than split into five fields.
- When people-related attribution matters, record the `Owner` and the `Confirmed by`.
- If a key detail is ambiguous, conflicting, or missing, ask the human immediately before writing it as fact.

## What to record

Usually worth recording:

- stable project identity
- why the project exists
- the current goal and what counts as success
- the current phase and latest meaningful status
- decisions that will affect later work
- constraints that limit later choices
- important files, documents, and commands
- high-value todos that affect progress
- notes that help resume the project later

Usually not worth recording:

- raw and sprawling brainstorm content
- repetitive status chatter
- temporary guesses that were never confirmed
- details that can be cheaply recovered from code or files later
- every small action taken during the session

## Ask immediately when unclear

Pause and ask the human if any of these are unclear:

- the project document cannot be located or read, or its storage method and path are unclear
- the project background has multiple plausible interpretations
- the goal is too vague to record with SMART discipline
- the success condition is missing
- an important decision has no clear reason or no clear confirmer
- a possible constraint has not been confirmed
- ownership matters but there is no clear `Owner`

Ask only the minimum necessary questions. Do not turn clarification into a long interview. Resolve the ambiguity, then update the document.

## Document format

Unless the user explicitly asks for a different format, use this structure:

```md
# Project Memory

## Document Info
- Storage type:
- Path or link:

## Project Identity
- Name:
- Owner / stakeholders:
- One-sentence description:

## Project Background
- Why this project exists:

## Goal

## Current State
- Current phase:
- Completed:
- Next expected step:

## Key Decisions
- Item:
- Why this decision was made:
- Owner:
- Confirmed by:

## Constraints

## Important References
- File name:
- File path / link:

## Todo Items
- Item:
- Owner:
- Needs to be done before:

## Recovery Notes
- Read this first when resuming:
- Critical context to reload:
- Easy-to-forget details:
```

## Section guidance

### Document Info

This section describes where the project document itself lives, not the project content. Before maintaining the project document, if the document cannot be located or read, first confirm:

- where the document is stored
- whether it is in a cloud document tool or a local file
- what the actual link or path is

If this information is unclear, ask first. Do not guess the storage location.

### Project Identity

Keep this short and stable. It should help someone immediately recognize what the project is.

### Project Background

Record the stable context behind the project. Focus on why the project exists, what value it is meant to create, and which background facts will continue to shape future understanding. Do not use this section for short-term updates.

### Goal

Record the goal using SMART thinking:

- make it as specific as possible
- make it measurable when possible
- keep it realistic for the project
- keep it relevant to the background
- include a time expectation when known

If one or more of these are missing and the gap affects the quality of the document, ask the human.

### Current State

Record only the latest meaningful state. Do not turn this section into a running log.

### Key Decisions

Each entry should explain:

- what was decided or confirmed
- why it was decided
- who confirmed it

If the item is important but `Confirmed by` is unclear, ask before writing it into durable project information.

### Constraints

Only record constraints that affect decisions, scope, delivery, or quality. If a constraint is still speculative, do not write it as fact unless it is clearly marked as unresolved elsewhere.

### Important References

Only record file paths, links, and document names that are worth coming back to later.

### Todo Items

Keep only meaningful todos. Do not let this section fill up with trivial, short-lived, or low-value tasks.

### Recovery Notes

This section should help a future session restart quickly. Keep it short, direct, and actionable.

## Update workflow

When maintaining the project document:

1. Check where the project document is stored and get the actual path or link.
2. Read the current document.
3. Identify the durable project context that changed or was added.
4. Ask clarifying questions if key information is still unclear.
5. Update the relevant sections instead of blindly appending.
6. Remove stale or duplicate content when replacing it.
7. Keep the final document concise and easy to scan.

## Output behavior

When the user asks to manage project information, do one of these:

- create a new project document using the standard format
- turn the current chat, group discussion, or user updates into document-ready changes and merge them into the right sections if the document already exists
- ask targeted clarification questions before writing

The document itself should stay clean and direct. Avoid process-heavy language inside it.
