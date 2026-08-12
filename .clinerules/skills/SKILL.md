# {{LANGUAGE}} Skills Index

This directory contains the official skills for the {{LANGUAGE}} curriculum.

Each skill file covers a single topic area and serves as an authoritative reference.

## How to Populate Skills

When instantiating this template for a specific language:

1. Research the official documentation for the target language
2. Create one markdown file per topic area
3. Each skill should be self-contained and comprehensive
4. Place the files in this directory

## Skill File Naming Convention

Use kebab-case, descriptive names:

```
variables-and-types.md
control-flow.md
functions.md
error-handling.md
concurrency.md
testing.md
```

## Skill File Template

Each skill file should follow this structure:

```markdown
# {{TOPIC_NAME}}

## Overview
Brief description of the topic and its importance in {{LANGUAGE}}.

## Core Concepts
- Key concept 1 with explanation
- Key concept 2 with explanation

## Syntax and Examples
Code examples demonstrating correct usage.

## Best Practices
- Do this
- Avoid that

## Common Pitfalls
- Pitfall 1 and how to avoid it

## Official References
Links to official documentation.
```

## Required Skill Topics

At minimum, every language course should include skills for:

| Category | Topics |
|---|---|
| **Fundamentals** | syntax, types, variables, operators |
| **Control Flow** | conditionals, loops, comprehensions |
| **Functions** | definitions, parameters, return values, closures |
| **Data Structures** | built-in collections, custom types |
| **Error Handling** | exceptions, result types, error patterns |
| **Modules** | imports, exports, package management |
| **OOP/Functional** | classes, protocols, patterns (as applicable) |
| **Concurrency** | threads, async/await, goroutines (as applicable) |
| **Testing** | unit tests, integration tests, mocking |
| **Tooling** | linters, formatters, package manager |
| **Ecosystem** | popular libraries, frameworks |
| **Performance** | profiling, optimization techniques |

## Source Priority

1. Official language documentation (always first)
2. Language specification documents
3. Well-maintained community guides
4. Framework-specific documentation

## Maintenance

Skills should be reviewed and updated when:

- The language releases a new major version
- Best practices evolve
- New features are introduced
- Deprecated patterns are identified