---
name: create-skill
description: Guides the creation of new agent skills, ensuring they follow best practices, correct structure, and provide high-quality instructions.
---

# Agent Skill Creation Guide

Use this skill when you are asked to create a new agent skill or modify an existing one.

## Core Structure
Every agent skill MUST be placed in a dedicated folder under the `.junie/skills/` directory (e.g., `.junie/skills/<skill-name>/`).
The folder MUST contain a `SKILL.md` file.

```text
.junie/skills/
└── <skill-name>/
    ├── SKILL.md              # Required: Main skill documentation
    ├── scripts/              # Optional: Executable scripts
    ├── templates/            # Optional: Code or doc templates
    └── checklists/           # Optional: Detailed checklists
```

## `SKILL.md` Requirements
1. **Frontmatter:** The file MUST start with a YAML frontmatter block containing a `name` and a concise, clear `description`. The description is crucial as it helps Junie determine when to invoke the skill.
2. **Title:** A clear markdown header (e.g., `# <Skill Name>`).
3. **Usage Context:** A brief explanation of when to use this skill.
4. **Instructions:** Specific, actionable instructions.

### Example Frontmatter
```markdown
---
name: your-skill-name
description: A brief, clear description of what this skill does and when it should be used.
---
```

## Best Practices for Writing Skills
- **Be Specific & Actionable:** Provide clear, concrete, and detailed instructions. Avoid vague statements. Use imperatives (e.g., "Use the AAA pattern").
- **Show, Don't Just Tell:** Include code blocks showing the exact patterns, formats, or commands you expect.
- **Reference Project Files:** Point to existing files in the project that serve as good examples or references.
- **Use Checklists:** For complex processes, provide a checklist to ensure all steps are followed.
- **Modularity:** If a skill is complex, break it down by placing scripts in a `scripts/` folder or large templates in a `templates/` folder, and reference them in `SKILL.md`.
