---
title: John, Product Manager
description: What John, the BMad Product Manager, does, how to load him, his menu codes, and what each code reads and writes.
sidebar:
  order: 2
---

John turns the product vision into a validated PRD, then into epics and stories development can execute. When the plan meets reality mid-sprint, he steers the change.

:::note[Quick facts]
**Skill ID:** `bmad-agent-pm` · **Phase:** planning and solutioning · **Codes:** `PRD`, `CE`, `IR`, `CC`
:::

## How to Invoke

Load the agent, then type a code from his menu:

```bash
bmad-agent-pm
```

On some platforms the skill name takes a `/` or `$` prefix. Every skill on his menu also runs on its own without loading John.

## Menu

| Code  | Runs                            | What it does                                                         | Guide                                                                                                  |
| ----- | ------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| `PRD` | `bmad-prd`                      | Create, update or validate a PRD                                     | [Define Requirements and a Specification](../plan/define-requirements-and-a-specification.md)          |
| `CE`  | `bmad-create-epics-and-stories` | Break requirements into the epics and stories that drive development | [Break Work into Stories and Track It](../plan/break-work-into-stories-and-track-it.md)                |
| `IR`  | `bmad-sprint-planning`          | Implementation readiness gate: are the plans complete and aligned?   | [Break Work into Stories and Track It](../plan/break-work-into-stories-and-track-it.md)                |
| `CC`  | `bmad-correct-course`           | Decide how to proceed when a significant change surfaces mid-sprint  | [Break Work into Stories and Track It](../plan/break-work-into-stories-and-track-it.md#correct-course) |

`IR` opens sprint planning; you can stop after the gate or continue into tracking. Winston offers the same code.

## Inputs and Outputs

For each code, what the skill reads, what it writes, and who picks the result up next.

![John's menu as inputs and outputs: PRD reads the brief, research and PRFAQ and writes prd.md for UX, architecture and epics; CE reads the PRD, architecture and UX and writes epics.md; IR checks readiness and writes implementation-readiness.md only on FAIL; CC writes a sprint change proposal routed to the PM, Architect or Developer](/diagrams/bmad-agent-pm.svg)

## Persona

| Trait               | Default                                                                                  |
| ------------------- | ---------------------------------------------------------------------------------------- |
| Role                | Translate product vision into a validated PRD, epics and stories                         |
| Identity            | Thinks like Marty Cagan and Teresa Torres; writes with six-pager discipline              |
| Communication style | A detective's relentless "why?"; direct, data-sharp, no fluff                            |
| Principles          | PRDs come from user interviews; ship the smallest thing that validates; user value first |

## Customize John

His name and title are fixed. His persona, principles, facts and menu can be overridden without editing the installed files. See [Customize BMad](../customize/customize-bmad.md).
