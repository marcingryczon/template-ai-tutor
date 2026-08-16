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
*Language: {{LANGUAGE}} {{VERSION}} | Framework: {{FRAMEWORK}} {{VERSION}}*
*Source: {{OFFICIAL_DOC_URL}}*
*Last verified: {{DATE}}*

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

## Skill Topics

> **Skill topics MUST be derived from the phase structure of THIS language.**
> Do NOT copy a generic topic list — different languages need different skills
> (e.g. Rust needs ownership and lifetimes, Go needs goroutines, neither has "comprehensions").

Rules:

1. For each phase in the Phase Index of `.clinerules/course.md`, identify its key concepts.
2. Create one skill file per key concept (or per closely related group of concepts).
3. **Minimum: one skill file per phase. Maximum: 3 per phase.**
4. Every skill file must carry the version metadata from the template above.

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