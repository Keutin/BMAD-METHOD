---
title: Amelia, Senior Software Engineer
description: What Amelia, the BMad Developer, does, how to load her, her menu codes, and what each code reads and writes.
sidebar:
  order: 5
---

Amelia runs the implementation loop: plan the sprint, build each story test-first, review it, and close the epic with a retrospective.

:::note[Quick facts]
**Skill ID:** `bmad-agent-dev` · **Phase:** implementation · **Codes:** `BD`, `QA`, `CR`, `SP`, `ER`
:::

## How to Invoke

Load the agent, then type a code from her menu:

```bash
bmad-agent-dev
```

On some platforms the skill name takes a `/` or `$` prefix. Every skill on her menu also runs on its own without loading Amelia.

## Menu

| Code | Runs                         | What it does                                                  | Guide                                                                                   |
| ---- | ---------------------------- | ------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `BD` | `bmad-build`                 | Implement a feature, fix or story                             | [Build a Change](../build/build-a-change.md)                                            |
| `QA` | `bmad-qa-generate-e2e-tests` | Generate API and end-to-end tests for existing features       | [Test Completed Work](../build/test-completed-work.md)                                  |
| `CR` | `bmad-code-review`           | Review code changes across several quality facets             | [Review a Change](../build/review-a-change.md)                                          |
| `SP` | `bmad-sprint-planning`       | Generate or update the sprint plan that sequences the stories | [Break Work into Stories and Track It](../plan/break-work-into-stories-and-track-it.md) |
| `ER` | `bmad-retrospective`         | Evidence-based review of a completed epic                     | [Finish an Epic](../build/finish-an-epic.md)                                            |

The `QA` code runs the lightweight test generator; the full Test Architect is a separate module.

## Inputs and Outputs

For each code, in loop order, what the skill reads, what it writes, and who picks the result up next.

![Amelia's menu as inputs and outputs: SP writes sprint-status.yaml from epics.md; BD builds a story into a spec file and code; QA writes API and E2E tests; CR reviews the diff and marks the story done; ER writes the epic retrospective and action items](/diagrams/bmad-agent-dev.svg)

## Persona

| Trait               | Default                                                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------- |
| Role                | Implement approved stories test-first and ship working, verified code                              |
| Identity            | Kent Beck's TDD and the Pragmatic Programmer's precision                                           |
| Communication style | Ultra-succinct; speaks in file paths and acceptance-criteria IDs                                   |
| Principles          | Nothing is done without passing tests; red, green, refactor; no workflow metadata in code comments |

## Customize Amelia

Her name and title are fixed. Her persona, principles, facts and menu can be overridden without editing the installed files. See [Customize BMad](../customize/customize-bmad.md).
