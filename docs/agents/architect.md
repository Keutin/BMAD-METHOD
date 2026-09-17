---
title: Winston, System Architect
description: What Winston, the BMad System Architect, does, how to load him, his menu codes, and what each code reads and writes.
sidebar:
  order: 4
---

Winston converts the PRD and UX into the architecture decisions that keep separately built parts consistent, then checks the plans are ready for implementation.

:::note[Quick facts]
**Skill ID:** `bmad-agent-architect` · **Phase:** solutioning · **Codes:** `CA`, `IR`
:::

## How to Invoke

Load the agent, then type a code from his menu:

```bash
bmad-agent-architect
```

On some platforms the skill name takes a `/` or `$` prefix. Every skill on his menu also runs on its own without loading Winston.

## Menu

| Code | Runs                   | What it does                                                              | Guide                                                                                   |
| ---- | ---------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `CA` | `bmad-architecture`    | Produce the architecture spine: the invariants that keep units consistent | [Design UX and Architecture](../plan/design-ux-and-architecture.md)                     |
| `IR` | `bmad-sprint-planning` | Implementation readiness gate: are the plans complete and aligned?        | [Break Work into Stories and Track It](../plan/break-work-into-stories-and-track-it.md) |

`IR` opens sprint planning; you can stop after the gate or continue into tracking. John offers the same code.

## Inputs and Outputs

For each code, what the skill reads, what it writes, and who picks the result up next.

![Winston's menu as inputs and outputs: CA reads the PRD or spec, UX and existing code and writes ARCHITECTURE-SPINE.md for the epics; IR checks readiness and writes implementation-readiness.md only on FAIL](/diagrams/bmad-agent-architect.svg)

## Persona

| Trait               | Default                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------- |
| Role                | Convert the PRD and UX into architecture decisions that keep implementation on track        |
| Identity            | Martin Fowler's pragmatism and Werner Vogels's cloud-scale realism                          |
| Communication style | Calm and pragmatic; answers with trade-offs, not verdicts                                   |
| Principles          | Rule of Three before abstraction; boring technology; developer productivity is architecture |

## Customize Winston

His name and title are fixed. His persona, principles, facts and menu can be overridden without editing the installed files. See [Customize BMad](../customize/customize-bmad.md).
