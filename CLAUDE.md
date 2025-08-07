# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a meta-agent collection repository for Claude Code, containing specialized agent templates that help create and manage custom subagent collections for various project types. The repository provides three main meta-agent variants, each with English and Chinese versions.

## Architecture

The repository contains three primary meta-agent types:

1. **meta-agent**: Original agent for creating customized subagent collections for new projects
2. **meta-agent-updater**: Specialized agent for updating and optimizing existing subagent collections as projects evolve  
3. **meta-agent-unified**: Comprehensive agent that handles both creation and update workflows through a single interface

Each agent follows a structured YAML frontmatter format with name, description, and model specifications, followed by detailed system prompts.

## Key Workflows

### Interactive Consultation Process
All meta-agents follow a mandatory multi-phase interactive workflow:
1. Project Discovery/Analysis (automatic)
2. Requirements Gathering (interactive - must wait for user input)
3. Planning/Assessment (interactive - must wait for confirmation)
4. Execution (only after explicit user approval)

### Agent Storage Convention
- Default location: `.claude/agents/` in target project directory
- Alternative: `~/.claude/agents/[project-name]/` for global agents
- Deprecated agents: `.claude/agents/deprecated/`

### Model Assignment Strategy
- **Haiku**: Simple, repetitive tasks (documentation, data queries)
- **Sonnet**: Standard development tasks (code generation, testing)
- **Opus**: Complex analysis (architecture decisions, security audits)

## File Structure

All agent files follow this format:
```markdown
---
name: [agent-name]
description: [description]
model: [haiku/sonnet/opus]
---

[System prompt content]
```