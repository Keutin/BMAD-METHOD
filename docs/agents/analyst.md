---
title: Mary, Business Analyst
description: What Mary, the BMad Business Analyst, does, how to load her, her menu codes, and what each code reads and writes.
sidebar:
  order: 1
---

Mary helps you ideate, research, and analyze before you commit to a project. Her output is the evidence the Product Manager plans from.

:::note[Quick facts]
**Skill ID:** `bmad-agent-analyst` · **Phase:** analysis · **Codes:** `BP`, `MR`, `DR`, `TR`, `TS`, `CR`, `UV`, `CB`, `WB`, `PC`
:::

## How to Invoke

Load the agent, then type a code from her menu:

```bash
bmad-agent-analyst
```

On some platforms the skill name takes a `/` or `$` prefix. Every skill on her menu also runs on its own without loading Mary.

## Menu

| Code | Runs                   | What it does                                                          | Guide                                                                                         |
| ---- | ---------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `BP` | `bmad-brainstorming`   | Guided brainstorming session                                          | [Explore and Validate an Idea](../plan/explore-and-validate-an-idea.md)                       |
| `MR` | `bmad-deep-recon`      | Market analysis, competitive landscape, customer needs and trends     | [Research a Decision](../plan/research-a-decision.md)                                         |
| `DR` | `bmad-deep-recon`      | Industry domain deep dive, expertise and terminology                  | [Research a Decision](../plan/research-a-decision.md)                                         |
| `TR` | `bmad-deep-recon`      | Technical landscape, architecture patterns and implementation reality | [Research a Decision](../plan/research-a-decision.md)                                         |
| `TS` | `bmad-deep-recon`      | Choose between technologies, vendors or tools                         | [Research a Decision](../plan/research-a-decision.md)                                         |
| `CR` | `bmad-deep-recon`      | Competitive teardown of named competitors                             | [Research a Decision](../plan/research-a-decision.md)                                         |
| `UV` | `bmad-deep-recon`      | User-voice research: reviews, communities, jobs to be done            | [Research a Decision](../plan/research-a-decision.md)                                         |
| `CB` | `bmad-product-brief`   | Create or update a product brief                                      | [Define Requirements and a Specification](../plan/define-requirements-and-a-specification.md) |
| `WB` | `bmad-prfaq`           | Working Backwards PRFAQ challenge for a product concept               | [Define Requirements and a Specification](../plan/define-requirements-and-a-specification.md) |
| `PC` | `bmad-project-context` | Set up, refresh or audit the repository's agent instructions          | [Set and Maintain Project Context](../existing-codebases/set-and-maintain-project-context.md) |

Codes are scoped to the agent: `CR` is a competitive teardown for Mary and a code review for Amelia.

## Inputs and Outputs

For each code, what the skill reads, what it writes, and who picks the result up next.

![Mary's menu as inputs and outputs: BP brainstorming writes optional brainstorm files for the brief or PRD; the six deep-recon codes write research.md for the brief, PRD or architecture; CB product brief writes brief.md for the PRD; WB PRFAQ writes prfaq-project.md for the PRD; PC project context writes the AGENTS.md context block that every agent reads](/diagrams/bmad-agent-analyst.svg)

## Persona

| Trait               | Default                                                                      |
| ------------------- | ---------------------------------------------------------------------------- |
| Role                | Ideate, research and analyze before committing to a project                  |
| Identity            | Michael Porter's strategic rigor and Barbara Minto's Pyramid Principle       |
| Communication style | A treasure hunter's excitement for patterns, a consulting memo's structure   |
| Principles          | Findings grounded in evidence; precise requirements; every stakeholder heard |

## Customize Mary

Her name and title are fixed. Her persona, principles, facts and menu can be overridden without editing the installed files. See [Customize BMad](../customize/customize-bmad.md).
