# Contributing to Local SEO Auditor

## How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-skill`)
3. Make your changes following the skill format below
4. Submit a pull request

## Skill File Format

Each skill lives in `skills/<skill-name>/SKILL.md` and follows this structure:

```markdown
---
name: skill-name
description: One-line description
version: 1.0.0
tags: [local-seo, relevant-tags]
related: [other-skill-1, other-skill-2]
---

# Skill Name

## When to Use This Skill
Trigger conditions and use cases.

## Discovery Phase
Questions to gather before starting.

## Assessment Framework
Checklist items, evaluation criteria, scoring rubrics.

## Implementation Guide
Step-by-step actions with code examples.

## Data Sources
### DFS MCP Tools
List of DataForSEO MCP tools used.
### User-Provided Data
What exports/reports to request from the user.

## Output Format
Structured output template.

## Cross-References
Links to related skills.
```

## Guidelines

- All skills must score findings against the three-channel model (Map Pack, Organic, AI Search)
- Include DFS MCP tool references where applicable
- Include direct API code fallbacks for environments without MCP
- Reference the knowledge base ranking factor weights
- Keep output formats consistent with the audit report template
