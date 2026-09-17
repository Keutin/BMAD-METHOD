---
title: Glossary
description: The abbreviations, IDs, section names, statuses and keys that appear inside the files BMad skills write, grouped by the file you find them in.
sidebar:
  order: 2
---

Use this page to decode what you read inside a BMad file: an `FR-3` in a PRD, an `AD-2` in the architecture spine, a `review` status in `sprint-status.yaml`. Terms are grouped by the file that carries them, and alphabetized within each group. For where each file lands and which agent writes it, see [Where Files Land](./skills-and-agents.md#where-files-land).

![A glossary card for each kind of BMad file, coloured by the agent that writes it: abbreviations, shared terms, product brief and PRFAQ, research, PRD, UX design, architecture spine, epics and stories, sprint status, spec, Build story file, code review, retrospective, sprint change proposal, project context, and brainstorming and forge, each term with a short meaning; the tables below give the full definitions](/diagrams/bmad-glossary.svg)

## Abbreviations

| Term             | Definition                                                                                                                                                   |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **AC**           | Acceptance criteria: the checkable conditions a story or change must meet. Files spell the heading out as *Acceptance Criteria* and do not number the items. |
| **AD-n**         | *Architecture spine.* A numbered architecture decision. IDs only go up and are never reused.                                                                 |
| **CAP-n**        | *Spec.* A numbered capability in `SPEC.md`, each with its intent and how success shows.                                                                      |
| **E2E**          | End-to-end: tests that drive the running product the way a user does, written by `bmad-qa-generate-e2e-tests`.                                               |
| **FR-n / FRn**   | Functional requirement. The PRD numbers them `FR-1`; `epics.md` extracts them as `FR1`, without the hyphen.                                                  |
| **I/O**          | Input and output, as in the *I/O & Edge-Case Matrix* of a Build story file.                                                                                  |
| **MVP**          | Minimum viable product: the smallest scope worth shipping, drawn as In and Out lists in the PRD.                                                             |
| **NFR / NFRn**   | Non-functional requirement: a quality such as speed or security. The PRD keeps them as prose; `epics.md` numbers them `NFR1`.                                |
| **PRD**          | Product requirements document, written by `bmad-prd`.                                                                                                        |
| **PRFAQ**        | Press release plus frequently asked questions: Amazon's Working Backwards format, run by `bmad-prfaq`.                                                       |
| **SM-n / SM-Cn** | *PRD.* A success metric, and a counter-metric that must not be optimized at its expense.                                                                     |
| **UJ-n**         | *PRD.* A numbered key user journey.                                                                                                                          |
| **UX**           | User experience, captured by `bmad-ux` in `DESIGN.md` and `EXPERIENCE.md`.                                                                                   |
| **UX-DRn**       | *Epics.* A UX design requirement extracted from the UX files into `epics.md`.                                                                                |

## Shared Across Files

| Term                        | Definition                                                                                                                                                 |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`addendum.md`**           | Depth you gave that does not fit the main document, kept next to a brief or PRD.                                                                           |
| **Companion**               | A file that must be read alongside a spec, listed in its `companions:` frontmatter.                                                                        |
| **HALT**                    | The point where a skill stops and waits. In unattended runs it comes with a final status and the blocking condition.                                       |
| **Lock**                    | *Forge idea.* A point you settled that will not be reopened; `forged-idea.md` is built from locks.                                                         |
| **`.memlog.md`**            | Append-only memory of a run, one line per decision, change, assumption or event. The final document is distilled from it.                                  |
| **Output paths**            | `output_folder`, `planning_artifacts`, `implementation_artifacts` and `project_knowledge` in `_bmad/config.toml`; `{project-root}` is the repository root. |
| **`review-{slug}.md`**      | The full findings of one reviewer lens, kept in the run folder.                                                                                            |
| **`status: draft / final`** | Frontmatter lifecycle of a PRD, UX pair or architecture spine.                                                                                             |

## Product Brief and PRFAQ

Found in `brief.md`, `prfaq-{project}.md`.

| Term                          | Definition                                                                                                                                                       |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coaching notes**            | *PRFAQ.* Hidden notes kept per stage, fed into the distillate.                                                                                                   |
| **Distillate**                | *PRFAQ.* `prfaq-{project}-distillate.md`: short bullet notes the PRD reads instead of the full document.                                                         |
| **Stage**                     | *PRFAQ.* The last finished stage, used to resume: 1 Ignition, 2 Press Release, 3 Customer FAQ, 4 Internal FAQ, 5 Verdict.                                        |
| **Verdict ratings**           | *PRFAQ.* How strong the concept is: *Forged in steel*, *Needs more heat* or *Cracks in the foundation*.                                                          |
| **What Makes This Different** | *Brief.* The section that says why this solution beats the alternatives, next to The Problem, The Solution, Who This Serves, Success Criteria, Scope and Vision. |

## Research

Found in `research/{type}-{topic}-{date}/`.

| Term                 | Definition                                                                                                           |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **`brief.md`**       | The research prompt, written ready to paste into another tool.                                                       |
| **Claim status**     | Where a finding stands after checking: verified, unverified, disputed or overturned.                                 |
| **Confidence**       | How far a finding can be trusted: high, medium or low.                                                               |
| **Digest**           | One research assistant's filtered findings for a round, under `digests/`, each with its source, date and confidence. |
| **Freshness bar**    | How many months a kind of claim stays current before it needs a newer source.                                        |
| **Red team**         | An optional skeptic pass that looks for evidence against the conclusion.                                             |
| **`ref=[n]`**        | An inline citation pointing to a row in the numbered source appendix.                                                |
| **Two-source class** | A kind of claim that needs two independent sources before it counts as verified.                                     |

## PRD

Found in `prds/prd-{project}-{date}/prd.md`.

| Term                   | Definition                                                                                                                                                  |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`[ASSUMPTION: …]`**  | An inline guess, listed again in the Assumptions Index at the end of the PRD.                                                                               |
| **Cross-Cutting NFRs** | An optional section for qualities that apply to every feature.                                                                                              |
| **Glossary**           | The only domain nouns the PRD may use. Using a synonym counts as a defect.                                                                                  |
| **Jobs To Be Done**    | What the target user is trying to get done, under Target User.                                                                                              |
| **Non-Goals**          | What the product deliberately will not do. `[NON-GOAL for MVP]` marks one inline.                                                                           |
| **`[NOTE FOR PM]`**    | An inline callout for the product manager to resolve.                                                                                                       |
| **Validation report**  | `validation-report.md`: each dimension rated strong, adequate, thin or broken, findings rated critical to low, and an overall grade from Excellent to Poor. |

## UX Design

Found in `ux-designs/ux-{project}-{date}/`.

| Term                       | Definition                                                                                                                                                              |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Accessibility Floor**    | *EXPERIENCE.md.* The behavioural accessibility minimum; visual contrast lives in DESIGN.md.                                                                             |
| **`DESIGN.md`**            | The look: Brand & Style, Colors, Typography, Layout & Spacing, Elevation & Depth, Shapes, Components, and Do's and Don'ts, with tokens referenced as `{path.to.token}`. |
| **`EXPERIENCE.md`**        | The behaviour: Foundation, Information Architecture, Voice and Tone, Component Patterns, State Patterns, Interaction Primitives, Accessibility Floor and Key Flows.     |
| **Foundation**             | *EXPERIENCE.md.* The form factor and UI system the experience is built on.                                                                                              |
| **Interaction Primitives** | *EXPERIENCE.md.* The basic interactions the product's flows are built from.                                                                                             |
| **Key Flows**              | *EXPERIENCE.md.* The main journeys, each with a named protagonist and a climax beat.                                                                                    |
| **`.working/`**            | Drafts, mockups and wireframes before they are promoted into the two main files.                                                                                        |

## Architecture Spine

Found in `architecture/architecture-{project}-{date}/ARCHITECTURE-SPINE.md`.

| Term                              | Definition                                                                                                |
| --------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **`[ADOPTED]`**                   | Marks an AD that records a decision already made rather than a new one.                                   |
| **Altitude**                      | The scope the spine covers: initiative, feature or epic.                                                  |
| **Binds / Prevents / Rule**       | The three fields of every AD: what it constrains, what failure it prevents, and the rule builders follow. |
| **Capability → Architecture Map** | Where each product capability lives in the architecture.                                                  |
| **Consistency Conventions**       | Naming, format and pattern choices that keep separately built parts alike.                                |
| **Deferred**                      | Decisions consciously left for later.                                                                     |
| **Design Paradigm**               | The overall architectural style the decisions follow.                                                     |
| **Inherited Invariants**          | ADs from a parent spine, kept with their original IDs and read-only.                                      |
| **Purpose**                       | Who the spine is for: build-substrate, discussion, report or deck.                                        |
| **Stack**                         | Name and version of each key technology, marked SEED: verified when written, then owned by the code.      |
| **Structural Seed**               | The starting layout of folders and modules.                                                               |

## Epics and Stories

Found in `planning-artifacts/epics.md`.

| Term                          | Definition                                                                        |
| ----------------------------- | --------------------------------------------------------------------------------- |
| **As a / I want / So that**   | The user-story sentence each story opens with.                                    |
| **FR Coverage Map**           | Which epic covers each extracted requirement, as `FR1: Epic 1 - …`.               |
| **Given / When / Then / And** | The format of each acceptance criterion.                                          |
| **inputDocuments**            | Frontmatter list of the planning files the epics were built from.                 |
| **Requirements Inventory**    | Every FR, NFR, additional and UX requirement extracted before epics are designed. |
| **stepsCompleted**            | Frontmatter record of finished steps, used to resume.                             |
| **`Story N.M`**               | Story M of epic N.                                                                |

## Sprint Status

Found in `implementation-artifacts/sprint-status.yaml`.

| Term                     | Definition                                                                                                                                               |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`action_items`**       | Follow-ups raised by retrospectives: open, in-progress or done.                                                                                          |
| **`development_status`** | The map of every epic, story and retrospective key to its status.                                                                                        |
| **epic-N**               | An epic key. Status: backlog, in-progress or done.                                                                                                       |
| **epic-N-retrospective** | An epic's retrospective key. Status: optional or done.                                                                                                   |
| **N-M-slug**             | A story key, such as `2-3-digest-delivery`; a letter suffix (`2-6a-…`) marks a split story. Status: backlog, ready-for-dev, in-progress, review or done. |
| **`project_key`**        | Prefix for an external tracker; `NOKEY` when there is none.                                                                                              |
| **Readiness gate**       | The check before sprint planning: PASS, CONCERNS or FAIL. A FAIL can be saved as `implementation-readiness.md`.                                          |
| **`story_location`**     | Where story files live.                                                                                                                                  |
| **`tracking_system`**    | Where status is tracked; `file-system` by default.                                                                                                       |

## Spec

Found in `specs/spec-{slug}/`.

| Term                  | Definition                                                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **`done_checkpoint`** | *stories.yaml.* When true, the dispatching loop pauses after the story completes, before anything else runs.                                |
| **`id: SPEC-{slug}`** | The spec's identifier in `SPEC.md` frontmatter.                                                                                             |
| **`invoke_dev_with`** | *stories.yaml.* Free text appended verbatim to the prompt that dispatches the story to the dev skill.                                       |
| **`sources`**         | Documents fully absorbed into the spec, listed for audit only; downstream skills do not read them.                                          |
| **`spec_checkpoint`** | *stories.yaml.* When true, a human reviews the story spec between planning and implementation.                                              |
| **`stories.yaml`**    | The spec split into stories: `id`, `title`, `description`, `spec_checkpoint`, `done_checkpoint`, `invoke_dev_with`. It has no status field. |
| **Success signal**    | The moment the world has changed, concrete enough to test or demonstrate; not a dashboard number.                                           |

## Build Story File

Found in `implementation-artifacts/spec-{slug}.md`.

| Term                         | Definition                                                                             |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| **`## Auto Run Result`**     | *bmad-build-auto.* The outcome of an unattended run, with deferred items and warnings. |
| **Boundaries & Constraints** | What the change must always do and must never do.                                      |
| **Code Map**                 | The files the change touches and why.                                                  |
| **`deferred-work.md`**       | Findings postponed by review, each with its source spec, summary and evidence.         |
| **`epic-N-context.md`**      | Context compiled from the planning files for one epic, read by every Build in it.      |
| **Frozen after approval**    | The intent section you approved; Build may not change it on its own.                   |
| **I/O & Edge-Case Matrix**   | Inputs, expected outputs and edge cases the change must handle.                        |
| **Review Triage Log**        | Every review finding and where it went: patch, defer, reject, intent_gap or bad_spec.  |
| **Route**                    | How Build runs the change: oneshot or full.                                            |
| **Spec Change Log**          | Changes made to the spec after work started, with the reason.                          |
| **Status**                   | draft, ready-for-dev, in-progress, in-review or done; unattended runs add blocked.     |
| **Type**                     | feature, bugfix, refactor or chore.                                                    |

## Code Review

Found in Story file and `deferred-work.md`.

| Term                                    | Definition                                                                               |
| --------------------------------------- | ---------------------------------------------------------------------------------------- |
| **`decision-needed`**                   | A finding only you can settle.                                                           |
| **Layer / lens**                        | One independent reviewer with its own angle, such as the blind hunter.                   |
| **patch / defer / reject**              | Triage buckets: fix in this change, record in `deferred-work.md`, or drop with a reason. |
| **`[Review][Patch] / [Review][Defer]`** | Task lines review adds to the story file for a fix now or a deferral.                    |
| **`review_mode`**                       | full when a spec exists to review against, no-spec otherwise.                            |

## Retrospective

Found in `epic-{N}-retro-{date}.md` or `RETROSPECTIVE.md`.

| Term                              | Definition                                                                            |
| --------------------------------- | ------------------------------------------------------------------------------------- |
| **Behavior verification**         | Evidence that the delivered behaviour matches what the epic promised.                 |
| **`criteria`**                    | Where acceptance criteria came from: declared in the plan, or profiled from the work. |
| **Disposition**                   | What to do with a gap: fix now, defer or accept as-is.                                |
| **epic-N-retro-item-n-slug**      | The ID of an action item, tracked in `sprint-status.yaml`.                            |
| **Previous-retro follow-through** | Whether the last retrospective's action items were done.                              |
| **`verdict`**                     | The acceptance decision: accepted, accepted-with-open-items or rejected.              |

## Sprint Change Proposal

Found in `planning-artifacts/sprint-change-proposal-{date}.md`.

| Term                       | Definition                                                                                           |
| -------------------------- | ---------------------------------------------------------------------------------------------------- |
| **Implementation Handoff** | The change scope and who carries out the approved change.                                            |
| **Recommended Approach**   | The path chosen from the checklist: direct adjustment, rollback, MVP review of the PRD, or a hybrid. |
| **Scope**                  | The size of the change: Minor, Moderate or Major.                                                    |

## Project Context

Found in The `<!-- bmad:context -->` block in `AGENTS.md`.

| Term                                | Definition                                                                                                        |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Known pitfalls**                  | Mistakes agents have made here, recorded so they are not repeated.                                                |
| **Ledger decision**                 | What happens to each existing instruction when context is adopted: retain, rewrite, relocate, automate or delete. |
| **Policy**                          | What the organization requires of every agent working in the repository.                                          |
| **Running and verifying**           | The commands that build, test and check the project, verified before they are written.                            |
| **`Verified {date} against {SHA}`** | The commit the block was last checked against.                                                                    |

## Brainstorming and Forge Idea

Found in `brainstorming/…` and `forge/{slug}/`.

| Term                       | Definition                                                                        |
| -------------------------- | --------------------------------------------------------------------------------- |
| **`brainstorm-intent.md`** | Only the discoveries you chose, written to feed the next skill.                   |
| **`forge-report.html`**    | The readable record of a forge session.                                           |
| **`forged-idea.md`**       | The hardened idea, written only when the outcome is HARDENED.                     |
| **Outcome**                | How a forge session ends: HARDENED, KILLED or CLARIFIED.                          |
| **Stance**                 | How brainstorming works with you: Facilitator, Creative Partner or Ideate for me. |
