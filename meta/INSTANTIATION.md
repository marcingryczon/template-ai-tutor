# Template Instantiation Procedure

> **One-time setup.** Run this procedure ONCE per language/framework, before the first lesson.
> Do NOT load this file during normal tutoring sessions.

This repository is a **template** for creating AI-driven programming courses.
Instantiation = replacing all placeholders, designing the phase structure,
populating skills, and scaffolding the project.

---

## Procedure

1. Replace all `{{PLACEHOLDER}}` tokens with language-specific values (table below),
   **including the Learner Environment section** (OS, shell, path style) in `.clinerules/course.md` —
   ask the learner for their OS and default shell if unknown.
2. Populate `.clinerules/skills/` with official documentation for the target language
   (see `.clinerules/skills/SKILL.md` for the skill file format and source priority).
3. **Design the phase structure for THIS language** — see the Phase Index steps in
   `.clinerules/course.md`. The number and names of phases MUST be derived from what is
   unique to the target language; there is no fixed phase list.
4. Copy `course/phase-TEMPLATE.md` to `course/phase-NN-<slug>.md` for each designed phase,
   fill in the placeholders, and register each phase in the Phase Index table.
5. Scaffold the project structure appropriate for the language under `src/`
   (`src/training/`, `src/app/`, `src/types/`, `src/lib/` or the language's equivalent layout).
6. Create initial lesson files in `lessons/` from `lesson-TEMPLATE.md`.
7. Run the **Post-Instantiation Verification Checklist** below. Only start Lesson 1 if ALL items pass.

---

## Placeholders

| Placeholder | Description | Example |
|---|---|---|
| `{{LANGUAGE}}` | Name of the programming language | Python, Rust, Go |
| `{{FRAMEWORK}}` | Primary framework (if applicable) | Django, Actix-web |
| `{{PACKAGE_MANAGER}}` | Package/dependency manager | pip, cargo, go mod |
| `{{BUILD_COMMAND}}` | Command to run the development server | `python manage.py runserver` |
| `{{PROJECT_NAME}}` | Name of the tutorial application | TaskFlow, NoteApp |
| `{{PROJECT_DESCRIPTION}}` | Description of the tutorial application | Multi-board Kanban task manager |
| `{{TEST_FRAMEWORK}}` | Primary testing framework | pytest, cargo test |
| `{{LINTER}}` | Primary linter/tool | flake8, clippy |
| `{{EXTENSION}}` | Primary file extension | .py, .rs |
| `{{OS}}` | Learner's operating system (Learner Environment) | Windows 11, macOS 15, Ubuntu 24.04 |
| `{{SHELL}}` | Learner's default shell (Learner Environment) | PowerShell 7, bash, zsh |

---

## Skill Sources

Prioritize official documentation as Skills:

| Language | Skill Source |
|---|---|
| Python | PEP 8, Python Docs, official tutorials |
| JavaScript/TypeScript | MDN, TypeScript Handbook |
| Rust | The Rust Book, Rust By Example |
| Go | Go Blog, Effective Go |
| React | Vercel React Best Practices |
| Angular | Angular.dev documentation |

Place official skills in `.clinerules/skills/` as markdown files.

---

## Post-Instantiation Verification Checklist

Before starting Lesson 1, verify ALL of the following:

- [ ] No `{{PLACEHOLDER}}` tokens remain — search: `grep -r "{{" .clinerules/ course/ lessons/ README.md`
- [ ] Phase structure designed (≥ 3 phases, each with 3+ lessons), derived from the target language
- [ ] Every phase file registered in the Phase Index of `.clinerules/course.md`
- [ ] Skills populated — at least one skill file per phase in `.clinerules/skills/`
- [ ] Every skill file has version metadata (language version, source URL, last-verified date)
- [ ] `.clinerules/agents/senior.md` contains no empty or placeholder sections
- [ ] `{{PROJECT_NAME}}` and `{{PROJECT_DESCRIPTION}}` set consistently in all files
- [ ] `src/training/` and `src/app/` directories exist
- [ ] Phase and lesson templates use the **same language** as the course (EN or PL, not mixed)
- [ ] **Learner Environment** filled in `.clinerules/course.md` (OS, shell, path style, command chaining)
- [ ] `start` branch created (clean baseline); `main` ready as merge target
- [ ] First lesson branch `lesson-01-<slug>` created from `main`

If any item fails, fix it before the first lesson.