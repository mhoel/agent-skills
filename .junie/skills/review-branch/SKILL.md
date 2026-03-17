---
name: review-branch
description: Reviews changes made to the current git branch when comparing with the main branch.
---

# Branch Review Skill

Use this skill when asked to review changes made on a Git branch compared to the main branch.

## Prerequisites
- Ensure you have fetched the latest changes from the remote repository.
- Ensure you are on the branch to be reviewed.

## Review Steps
1. **Gather Changes:** Run `git diff main...HEAD` (or `git diff origin/main...HEAD` depending on the setup) to see all the changes introduced by the current branch.
2. **Review Code Quality:** Analyze the diff for:
    - Potential bugs and logical errors.
    - Code readability and maintainability.
    - Consistency with existing code style and patterns.
    - Missing or inadequate tests.
    - Missing documentation for new features or APIs.
3. **Provide Feedback:** Summarize your findings in a structured format, highlighting both positive aspects and areas for improvement. Provide actionable recommendations for any issues found.

## Best Practices
- Focus on the *diff* specifically.
- Group your feedback logically (e.g., by file or by type of issue).
- Include specific line numbers or code snippets when referencing problems.
