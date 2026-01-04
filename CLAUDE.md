# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the "awesome-claude" repository - a curated collection of resources, tools, and information related to Claude and Claude Code.

## Repository Structure

Currently, this is a minimal repository with only configuration files:
- `.claude/settings.json` - Claude Code settings for commit and PR attribution

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

This is a content repository (likely for documentation/resources), not a code project. There are no build, test, or compilation steps required.

For content contributions:
- Add new resources to appropriate sections
- Ensure links are valid and descriptions are accurate
- Follow markdown formatting conventions
- Maintain alphabetical or logical ordering within sections
