---
title: Sally, UX Designer
description: What Sally, the BMad UX Designer, does, how to load her, her menu code, and what it reads and writes.
sidebar:
  order: 3
---

Sally turns user needs and the PRD into a UX specification that informs the architecture and the implementation. Use her when the product has an interface whose look and behavior matter.

:::note[Quick facts]
**Skill ID:** `bmad-agent-ux-designer` · **Phase:** planning · **Codes:** `CU`
:::

## How to Invoke

Load the agent, then type a code from her menu:

```bash
bmad-agent-ux-designer
```

On some platforms the skill name takes a `/` or `$` prefix. `bmad-ux` also runs on its own without loading Sally.

## Menu

| Code | Runs      | What it does                                             | Guide                                                               |
| ---- | --------- | -------------------------------------------------------- | ------------------------------------------------------------------- |
| `CU` | `bmad-ux` | Capture the UX vision as `DESIGN.md` and `EXPERIENCE.md` | [Design UX and Architecture](../plan/design-ux-and-architecture.md) |

`DESIGN.md` records the look; `EXPERIENCE.md` records the behavior. The skill can lead the PRD, follow it, or stand alone.

## Inputs and Outputs

What the skill reads, what it writes, and who picks the result up next.

![Sally's menu as inputs and outputs: CU UX design reads the brief, PRD and your direction and writes DESIGN.md and EXPERIENCE.md for the architecture and the epics](/diagrams/bmad-agent-ux.svg)

## Persona

| Trait               | Default                                                                          |
| ------------------- | -------------------------------------------------------------------------------- |
| Role                | Turn user needs and the PRD into UX design specifications                        |
| Identity            | Don Norman's human-centered design and Alan Cooper's persona discipline          |
| Communication style | Paints pictures with words; an empathetic advocate for the user                  |
| Principles          | Every decision serves a real user need; start simple; data-informed but creative |

## Customize Sally

Her name and title are fixed. Her persona, principles, facts and menu can be overridden without editing the installed files. See [Customize BMad](../customize/customize-bmad.md).
