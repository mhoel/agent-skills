# Agent Skills

This repository contains custom agent skills designed to enhance the capabilities of autonomous AI agents (like Junie). 
These skills are modular sets of instructions, templates, and scripts that provide domain-specific guidance for various tasks.

## Purpose
This project is primarily intended for learning and exploring how to build, configure, and reuse custom agent skills. 

## Structure
- `.junie/skills/`: This directory contains the individual skill definitions. Each skill typically has its own folder containing a `SKILL.md` file (the main instructions) and any associated configuration files or scripts.

## Available Skills (Examples)
- **review-branch**: Reviews changes made to the current Git branch compared to the main branch.
- **bitbucket-review**: Reviews changes made in a Bitbucket Server or Data Center pull request using the REST API.
- **create-skill**: Guides the creation of new agent skills, ensuring they follow best practices and correct structure.

## Note on Privacy
Some skills may require sensitive configuration (like API keys or tokens). Ensure that sensitive files (e.g., `apikey`, `.junie/memory/`) are added to your `.gitignore` to prevent accidental exposure in public repositories.