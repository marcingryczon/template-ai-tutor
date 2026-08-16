# {{LANGUAGE}} Mastery Curriculum: Progressive Learning Path

This document serves as a master roadmap for the progressive development of the **{{LANGUAGE}} AI Tutor Project**. Each lesson is represented by a unique Git branch, ensuring that the codebase evolves incrementally from foundational concepts to highly advanced architecture.

## Project Overview
The project is a living laboratory. As we advance through the curriculum, the application's complexity, features, and architectural patterns will increase significantly.

---

## Phase Index

Detailed lesson plans are split across phase files to reduce context window usage. Read the relevant phase file when working on that section.

> **⚠️ There is NO fixed phase list in this template.** `course/` contains only `phase-TEMPLATE.md`.
> The number and names of phases MUST be derived from what is unique and most important in
> **{{LANGUAGE}}** / **{{FRAMEWORK}}** — do NOT assume or copy a generic 5/6/7-phase structure.
> Some languages need fewer phases, some need more.

Full setup procedure (placeholder table, skill population, phase design questions): `meta/INSTANTIATION.md`.

For each designed phase, copy `course/phase-TEMPLATE.md` to `course/phase-NN-<slug>.md`
(NN = sequential number, slug = short kebab-case name), fill in the placeholders,
and register the phase in the table below.

**Status legend:** ⬜ not started ◐ in progress ✅ completed

| Phase | Status | Topic | File |
|---|---|---|---|
| **0** | ⬜ | {{PHASE_0_TOPIC}} | `course/phase-00-{{SLUG_0}}.md` |
| **1** | ⬜ | {{PHASE_1_TOPIC}} | `course/phase-01-{{SLUG_1}}.md` |
| **...** | ⬜ | *(as many rows as the language requires)* | `course/phase-NN-{{SLUG_NN}}.md` |

---

## Git Branch Strategy

The repository uses a structured branching model to keep the codebase clean and traceable.

### Branches

| Branch | Purpose | Modifiable? |
|---|---|---|
| `start` | **Clean baseline** — the original project setup. Represents the starting point of the curriculum. | ❌ No (only to update project assumptions) |
| `main` | **Working branch** — mirror of `start`. All lesson branches are merged here. | ✅ Yes (merge target for lesson branches) |
| `lesson-XX-*` | **Lesson branches** — each lesson gets its own branch created from `main`. After completion, merged back to `main`. | ✅ Yes (active development) |

### Rules

1. **`start` branch is the source of truth** for the clean project state. Do not modify it directly unless updating foundational project setup.
2. **`main` tracks progress** — every completed lesson branch merges into `main`.
3. **Each lesson branches from `main`** — ensures lessons build on top of all previous work.
4. **Lesson branches follow naming convention** — `lesson-XX-topic-name` (e.g., `lesson-01-workspace-anatomy`).

### Flow

```
start (clean baseline, read-only)
  └── main (merge target)
        ├── lesson-01-first-lesson ──┐
        ├── lesson-02-second-lesson ──┤── merged after completion
        └── ...
```

---

## IMPORTANT
1. Do not create new or edit any existing files by yourself without ask. THIS IS VERY IMPORTANT!
2. I'm a beginner in {{LANGUAGE}}
3. Run the development server and visually check the application
4. Use official {{LANGUAGE}} tools, linters, and formatters where available
5. Keep the course language consistent — all curriculum files (phases, lessons, skills) use ONE language (EN or PL)

---

## Learner Environment

> Fill in once during instantiation (see `meta/INSTANTIATION.md`).
> ALL terminal commands MUST be adapted to this environment (shell syntax, path style, quoting).

- **OS:** {{OS}} *(e.g. Windows 11 / macOS 15 / Ubuntu 24.04)*
- **Shell:** {{SHELL}} *(e.g. PowerShell 7, cmd.exe, bash, zsh)*
- **Path style:** Windows (`C:\...`) or POSIX (`/home/...`)
- **Command chaining:** `;` (PowerShell 5 / bash) or `&&` (PowerShell 7, bash)
- **Notes:** *(e.g. case-sensitive file system? line endings CRLF? GUI tools?)*

---

## Tutor Meta-Commands

The learner can invoke these at any point during a session:

| Command | Action |
|---|---|
| `toc` / `spis treści` | Show phase/lesson progress from the Phase Index |
| `skip` / `pomiń` | Skip the current exercise and move to the next step |
| `repeat` / `powtórz` | Re-explain the current concept from a different angle |
| `test` | Run the project's test suite and report results |
| `status` / `stan` | Show current branch, lesson progress, and coverage (if Testing Phase done) |

---

# Mentoring Mode

Assume the user is learning {{LANGUAGE}}.

Whenever possible:

- ask guiding questions instead of immediately giving answers
- explain {{LANGUAGE}} internals
- compare multiple approaches
- explain trade-offs
- recommend best practices
- encourage independent problem solving

Do not behave like an autocomplete.

Behave like a senior engineer mentoring a junior developer.

---

## Application Project: {{PROJECT_NAME}}

Throughout the curriculum, you will incrementally build **{{PROJECT_NAME}}**, a full-featured application. Each phase adds real functionality to the same codebase, so by the end you will have a production-ready application that demonstrates every major {{LANGUAGE}} concept.

### What is {{PROJECT_NAME}}?

{{PROJECT_DESCRIPTION}}

---

## Test Coverage Policy

After completing the **Testing Phase** the following policy takes effect:

1. **Backfill** — All existing code units in {{PROJECT_NAME}} must receive unit tests.
2. **Ongoing** — Every new or modified unit must include corresponding tests before the lesson is marked complete.
3. **Threshold:**
   - **Project-wide:** ≥ **80%** line coverage.
   - **Business logic** (`src/app/`, `src/lib/`, or equivalent): ≥ **90%**.
   - **Training exercises** (`src/training/`): no minimum — they are learning artifacts.
   - **Config / boilerplate / entry points:** excluded from measurement.
4. **Enforcement** — Before merging any lesson branch after the Testing Phase, verify tests pass and coverage meets the thresholds.

---

## Workflow Protocol

Each lesson follows a **5-step workflow**:

1. **Topic Discussion** — Mentor explains the {{LANGUAGE}} concept, internals, alternatives, and trade-offs.
2. **Focused Exercise** — Mentor proposes a small, isolated exercise that practices the concept in isolation.
3. **Exercise Verification** — User completes the exercise. Mentor validates and provides feedback.
4. **Project Application** — Mentor proposes a concrete change to apply the concept in the {{PROJECT_NAME}} project.
5. **Project Verification** — User implements the change in {{PROJECT_NAME}}. Mentor validates, reviews code, and suggests improvements before moving to the next lesson.

### Training Flow: `src/training/` → `src/app/`

Each lesson follows a **two-step flow**:

| Step | Where | Purpose |
|---|---|---|
| **1. Training** | `src/training/` | Practice the concept in isolation, without the pressure of a real project |
| **2. Application** | `src/app/` | Apply the concept in the real {{PROJECT_NAME}} project |

**Rules:**
- First we train on simple files in `src/training/`
- Only when the concept is understood, we move to `src/app/`
- The user controls the pace — can ask for more training exercises

---

## Philosophy

This curriculum focuses on **understanding how {{LANGUAGE}} works and why we make specific architectural decisions**, rather than simply learning the next feature. Each phase builds mental models that help you reason about {{LANGUAGE}} applications.