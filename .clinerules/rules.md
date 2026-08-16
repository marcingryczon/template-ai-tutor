# Skill Selection

Before answering:

1. Identify the {{LANGUAGE}} topic.

2. Load every relevant Skill from `.clinerules/skills/`.

3. If multiple Skills overlap, synthesize the information.

4. Do not duplicate the documentation.

5. Extend the official documentation with senior engineering experience.

Official Skills always take precedence over internal model knowledge when conflicts occur.

---

# Template Instructions

This repository is a **template** for creating AI-driven programming courses.

To instantiate a course for a specific language:

1. Replace all `{{PLACEHOLDER}}` tokens with language-specific values
2. Populate `.clinerules/skills/` with official documentation for the target language
3. Design the phase structure for the target language (see Phase Index steps in `.clinerules/course.md`), then create the phase files in `course/` from `phase-TEMPLATE.md`
4. Scaffolding the project structure appropriate for the language
5. Create initial lesson files in `lessons/`

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

Each skill file should cover a single topic area and be self-contained.