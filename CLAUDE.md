# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the "awesome-claude" repository - a curated collection of resources, tools, and information related to Claude and Claude Code.

## Repository Structure

This repository contains:
- `.claude/settings.json` - Claude Code settings for commit and PR attribution
- `.claude/commands/` - Custom slash commands for development workflow
  - `completed-review.md` - Code review for bugs, documentation, quality, and performance
  - `add-test.md` - Create test code for new functions and update test documentation
  - `update-claude.md` - Update CLAUDE.md when significant code changes occur
  - `git-msg.md` - Generate concise, descriptive git commit messages
  - `git-show.md` - Review git commits or branch differences with detailed analysis

## Custom Slash Commands

This repository includes specialized slash commands to streamline development workflow:

### Code Quality & Review
- `/completed-review` - Comprehensive code review analyzing bugs, documentation, code quality, and performance
- `/add-test` - Generate unit tests for new functions, verify execution, and update test documentation

### Git Workflow
- `/git-msg` - Analyze staged/unstaged changes and generate conventional commit messages
  - Follows format: `<type>: <description>` (e.g., `feat:`, `fix:`, `chore:`)
  - Analyzes change patterns to determine appropriate commit type
  - Enforces 50-72 character limit and imperative mood
- `/git-show [target]` - Review commits or branch differences with intelligent analysis
  - `/git-show` - Review latest commit (HEAD)
  - `/git-show <commit-hash>` - Review specific commit
  - `/git-show <branch>` - Compare current state vs branch
  - Highlights critical changes: security concerns, breaking changes, performance impacts

### Maintenance
- `/update-claude` - Automatically update this CLAUDE.md file when significant architectural or workflow changes occur

These commands are invoked by typing them in Claude Code (e.g., `/git-msg` after staging changes).

## Git Configuration

The repository has custom commit attribution settings configured in `.claude/settings.json`:
- Custom commit attribution footer (currently empty string)
- Custom PR attribution footer (currently empty string)

When these are empty, the default Claude Code attribution is used. To customize:
```json
{
    "attribution": {
        "commit": "Your custom commit footer",
        "pr": "Your custom PR footer"
    }
}
```

## Development Workflow

This is a content repository for Claude and Claude Code resources. Development is enhanced by custom slash commands.

### Recommended Git Workflow

1. **Make changes** to documentation or resources
2. **Stage changes**: `git add <files>`
3. **Generate commit message**: `/git-msg` - Auto-generates conventional commit messages
4. **Commit**: `git commit -m "<generated-message>"`
5. **Review changes**: `/git-show` - Analyze what was committed
6. **Update documentation**: `/update-claude` - Update CLAUDE.md if workflow or structure changed

### Content Contribution Guidelines

- Add new resources to appropriate sections
- Ensure links are valid and descriptions are accurate
- Follow markdown formatting conventions
- Maintain alphabetical or logical ordering within sections
- Use `/completed-review` before committing significant changes
