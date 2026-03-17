---
name: bitbucket-review
description: Review changes made in a Bitbucket Server or Data Center pull request using the REST API.
---

# Bitbucket PR Review Skill

Use this skill when asked to review changes made in a Bitbucket pull request. This skill relies on the Bitbucket Server REST API (e.g., v1.0 or v1002).

## Prerequisites
- A Bitbucket Server/Data Center instance URL.
- The Project Key, Repository Slug, and Pull Request ID.
- An authentication token or credentials capable of reading the PR diff.

## Review Steps
1. **Gather Changes:** Fetch the diff for the pull request using the Bitbucket REST API. For example, using `curl` or `Invoke-WebRequest` to hit:
   `GET /rest/api/1.0/projects/{projectKey}/repos/{repositorySlug}/pull-requests/{pullRequestId}/diff`
   (Adjust the API version or endpoint based on the instance's version and Bitbucket documentation).
2. **Review Code Quality:** Analyze the diff for:
    - Potential bugs and logical errors.
    - Code readability and maintainability.
    - Consistency with existing code style and patterns.
    - Missing or inadequate tests.
    - Missing documentation for new features or APIs.
3. **Provide Feedback:** Post comments directly on the appropriate lines in the pull request using the Bitbucket REST API. For example, send a `POST` request to `/rest/api/1.0/projects/{projectKey}/repos/{repositorySlug}/pull-requests/{pullRequestId}/comments` with a JSON payload specifying the `anchor` (file path, lineType, and line number). For general PR feedback, summarize findings in a structured format:
    - **Positive Aspects:** What was done well.
    - **Areas for Improvement:** General issues and recommendations.

## Best Practices
- Focus on the *diff* specifically, ignoring unchanged parts of the codebase unless relevant for context.
- Group your feedback logically (e.g., by file or by type of issue).
- Include specific line numbers or code snippets when referencing problems.
- If possible, fetch PR comments or metadata (via the `/activities` or `/comments` endpoints) to avoid duplicating existing feedback.
