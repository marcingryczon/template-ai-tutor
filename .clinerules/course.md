# {{LANGUAGE}} Mastery Curriculum: Progressive Learning Path

This document serves as a master roadmap for the progressive development of the **{{LANGUAGE}} AI Tutor Project**. Each lesson is represented by a unique Git branch, ensuring that the codebase evolves incrementally from foundational concepts to highly advanced architecture.

## Project Overview
The project is a living laboratory. As we advance through the curriculum, the application's complexity, features, and architectural patterns will increase significantly.

---

## Phase Index

Detailed lesson plans are split across phase files to reduce context window usage. Read the relevant phase file when working on that section.

The lessons in this course should reflect the **most important elements of the {{LANGUAGE}} language or {{FRAMEWORK}} framework**. Each phase covers a critical area that every developer must master.

> **⚠️ The sample phase structure below is NOT final.** It is a generic starting point that **must be adapted** to the target language or framework. When instantiating this template, review, rename, split, merge, or replace phases so they match the actual learning progression. Some languages may need fewer phases, others may need more.

**Status legend:** ⬜ not started ◐ in progress ✅ completed

| Phase | Status | Topic | File |
|---|---|---|---|
| **0** | ⬜ | Workspace Setup & {{LANGUAGE}} Fundamentals | `course/phase-00-fundamentals.md` |
| **1** | ⬜ | Core {{LANGUAGE}} Concepts | `course/phase-01-core-concepts.md` |
| **2** | ⬜ | Data Structures & Collections | `course/phase-02-data-structures.md` |
| **3** | ⬜ | Advanced Patterns & {{LANGUAGE}} Features | `course/phase-03-advanced-patterns.md` |
| **4** | ⬜ | Testing | `course/phase-04-testing.md` |
| **5** | ⬜ | Production & Deployment | `course/phase-05-production.md` |

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
3. **Threshold** — Minimum code coverage is **90%** (measured per-file, not project-wide).
4. **Enforcement** — Before merging any lesson branch after the Testing Phase, verify tests pass and coverage meets the threshold.

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