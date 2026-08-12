# {{LANGUAGE}} AI Tutor — Course Template

> **This is a template for creating an AI-driven programming course for any language or framework.**

## How to Use This Template

Copy this folder and give the following command to an LLM:

```
Create a course for [LANGUAGE/FRAMEWORK]
```

The LLM will use the templates in this repository to generate a complete, structured curriculum.

---

## What This Template Provides

### `.clinerules/` — AI Tutor Configuration

| File | Purpose |
|---|---|
| `course.md` | Master curriculum roadmap — defines phases, branching strategy, mentoring mode, and project description |
| `rules.md` | Skill selection policy and template instantiation instructions |
| `agents/senior.md` | AI persona definition — senior engineer mentor for the target language |
| `skills/SKILL.md` | Guide for populating official language/framework documentation as Skills |

### `course/` — Curriculum Phases

Each phase file defines a group of related lessons:

| File | Covers |
|---|---|
| `phase-00-fundamentals.md` | Workspace setup, syntax, types, mental model |
| `phase-01-core-concepts.md` | Functions, control flow, modules, error handling |
| `phase-02-data-structures.md` | Collections, custom types, memory management |
| `phase-03-advanced-patterns.md` | Language-specific advanced features |
| `phase-04-testing.md` | Testing frameworks, strategies, policies |
| `phase-05-production.md` | Deployment, optimization, production readiness |
| `phase-TEMPLATE.md` | Reusable template for creating additional phases |

> **⚠️ This sample course structure is NOT final.** It is a generic starting point that **must be adapted** to the target language or framework. The LLM should review, rename, split, merge, or replace phases so they match the actual learning progression of the language. Some languages may need fewer phases, others may need more. The phase names, lesson topics, and ordering should all be tailored to what matters most for that specific language.

### `lessons/` — Individual Lesson Files

Detailed lesson content with exercises, explanations, and project applications.

### `src/` — Project Structure

| Directory | Purpose |
|---|---|
| `src/training/` | Isolated exercises for practicing concepts |
| `src/app/` | The main tutorial application |
| `src/types/` | Domain type definitions |
| `src/lib/` | Shared utilities |

---

## Key Principle: Lessons Must Reflect the Language

**The lessons in the `course/` phases should reflect the most important elements of the target language or framework.**

When instantiating this template for a specific language:

1. **Identify the core concepts** — What makes this language/framework unique? What must every developer understand?
2. **Structure phases around those concepts** — Each phase should cover a critical area of the language or framework
3. **Progress from fundamentals to advanced** — Start with basics, build up to architecture and production patterns
4. **Include the ecosystem** — Cover not just the language but its tooling, testing, and deployment

### Example: What to emphasize per language

| Language | Key Elements to Cover |
|---|---|
| **Python** | Indentation, dynamic typing, decorators, generators, virtual environments, pip, pytest |
| **Rust** | Ownership, borrowing, lifetimes, pattern matching, Cargo, clippy |
| **Go** | Goroutines, channels, interfaces, error handling, `go mod`, standard library |
| **React** | Components, JSX, hooks, state management, virtual DOM, reconciliation |
| **Angular** | Components, signals, DI, RxJS, standalone APIs, change detection |

---

## Placeholders

Replace these tokens when instantiating the template:

| Placeholder | Example Values |
|---|---|
| `{{LANGUAGE}}` | Python, Rust, Go, JavaScript |
| `{{FRAMEWORK}}` | Django, Actix-web, Gin, React |
| `{{PACKAGE_MANAGER}}` | pip, cargo, go mod, npm |
| `{{BUILD_COMMAND}}` | `python runserver`, `cargo run`, `go run` |
| `{{PROJECT_NAME}}` | TaskFlow, NoteApp, BlogEngine |
| `{{PROJECT_DESCRIPTION}}` | Description of the tutorial application |
| `{{TEST_FRAMEWORK}}` | pytest, cargo test, go test |
| `{{LINTER}}` | flake8, clippy, golangci-lint |
| `{{EXTENSION}}` | .py, .rs, .go |

---

## Curriculum Design Guidelines

### Phase Structure

Each phase should:
- Focus on a single theme or area of the language
- Contain 3-5 lessons that build on each other
- Include training exercises and project applications for each lesson
- End with clear completion criteria

### Lesson Structure

Each lesson should:
- Have a clear objective
- Cover specific topics with depth
- Include a training exercise (isolated practice)
- Include a project application (real code integration)
- Follow the 5-step workflow: Discussion → Exercise → Verify → Apply → Verify

### Progressive Complexity

The curriculum should follow this progression:

```
Phase 0: Setup & Fundamentals      →  "What is this language?"
Phase 1: Core Concepts             →  "How do I write code?"
Phase 2: Data & Structures         →  "How do I model data?"
Phase 3: Advanced Patterns         →  "How do I write good code?"
Phase 4: Testing                   →  "How do I verify it works?"
Phase 5: Production                →  "How do I ship it?"
```

---

## Git Branch Strategy

The course uses a structured branching model:

- **`start`** — Clean baseline (read-only)
- **`main`** — Working branch (merge target)
- **`lesson-XX-topic`** — Individual lesson branches

Each lesson branches from `main`, gets implemented, and merges back.

---

## Philosophy

This curriculum focuses on **understanding how the language works and why we make specific architectural decisions**, rather than simply learning features. Each phase builds mental models that help developers reason about applications in that language.