# Contributing to Meta-Agent for Claude Code

First off, thank you for considering contributing to Meta-Agent for Claude Code! It's people like you that make this tool better for everyone in the Claude Code community.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Guidelines](#development-guidelines)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)
- [Community](#community)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/your-username/meta_agent_for_claude_code.git
   cd meta_agent_for_claude_code
   ```
3. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear and descriptive title**
- **Steps to reproduce** the behavior
- **Expected behavior** description
- **Actual behavior** description
- **Claude Code version** you're using
- **Additional context** (screenshots, error messages, etc.)

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please provide:

- **Use case** - Why is this enhancement needed?
- **Proposed solution** - How should it work?
- **Alternatives considered** - What else did you think about?
- **Additional context** - Any examples from other projects?

### 🎯 Contributing New Agents

When creating new meta-agents or support agents:

1. **Follow the standard format**:
   ```markdown
   ---
   name: agent-name
   description: Brief description (max 100 chars)
   model: haiku|sonnet|opus
   ---
   
   [Agent system prompt content]
   ```

2. **Implement the 4-phase workflow** for meta-agents:
   - Phase 1: Automatic analysis
   - Phase 2: Interactive requirements (wait for user input)
   - Phase 3: Planning with approval
   - Phase 4: Conditional execution

3. **Create bilingual versions** when applicable:
   - English version: `agent-name.md`
   - Chinese version: `agent-name-zh.md`

### 📝 Improving Documentation

Documentation improvements are always welcome:

- Fix typos or grammatical errors
- Clarify existing documentation
- Add missing examples
- Translate documentation
- Update outdated information

## Development Guidelines

### Agent Development Principles

1. **Single Responsibility**: Each agent should have one clear purpose
2. **Model Optimization**: Choose the appropriate model tier:
   - **Haiku**: Simple, repetitive tasks
   - **Sonnet**: Standard development tasks
   - **Opus**: Complex analysis and reasoning
3. **Interactive Design**: Meta-agents must be interactive, not fully automatic
4. **Error Handling**: Include graceful error handling and recovery
5. **Documentation**: Every agent needs clear usage examples

### File Organization

```
meta_agent_for_claude_code/
├── meta-agent*.md           # Core meta-agents (root level)
├── .claude/
│   └── agents/             # Support agents
│       ├── *.md            # Agent files
│       └── deprecated/     # Old versions
├── docs/                   # Additional documentation
├── examples/               # Usage examples
└── tests/                  # Test files (if applicable)
```

### Testing Your Changes

Before submitting:

1. **Validate agent structure** using the agent-validator:
   ```bash
   @agent-validator Check your-new-agent.md
   ```

2. **Test the workflow** in Claude Code:
   - Ensure all phases work correctly
   - Verify error handling
   - Check output quality

3. **Verify bilingual sync** if applicable:
   ```bash
   @bilingual-synchronizer Check your-agent.md
   ```

## Style Guidelines

### Markdown Style

- Use clear, concise language
- Include code examples in fenced blocks
- Use tables for structured data
- Add emoji sparingly for visual markers
- Keep line length reasonable (80-120 chars for readability)

### Agent Naming

- Use lowercase with hyphens: `agent-name-here`
- Be descriptive but concise
- Avoid generic names like `helper` or `assistant`
- Include domain if specialized: `react-component-generator`

### Writing Style

- **Active voice**: "The agent analyzes..." not "The code is analyzed by..."
- **Present tense**: "Creates" not "Will create"
- **Imperative mood** for instructions: "Run the command" not "You should run"
- **Clear examples**: Show, don't just tell

## Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: New feature or agent
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Formatting, missing semicolons, etc.
- **refactor**: Code restructuring
- **test**: Adding tests
- **chore**: Maintenance tasks

### Examples

```bash
feat(agents): add docker-compose-generator agent

fix(meta-agent): correct phase 2 waiting logic

docs(readme): add troubleshooting section

refactor(validator): improve YAML parsing performance
```

## Pull Request Process

1. **Update documentation** - Ensure README.md and CLAUDE.md reflect your changes
2. **Update CHANGELOG.md** - Add your changes under "Unreleased"
3. **Ensure all tests pass** - Run validation tools
4. **Request review** - Tag relevant maintainers
5. **Address feedback** - Make requested changes promptly
6. **Squash commits** - Keep history clean if requested

### PR Title Format

Use the same format as commit messages:
- `feat(agents): add kubernetes deployment agent`
- `fix(synchronizer): handle special characters in Chinese`
- `docs: improve installation instructions`

### PR Description Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement

## Testing
- [ ] Tested in Claude Code
- [ ] Validated agent structure
- [ ] Checked bilingual sync (if applicable)

## Checklist
- [ ] My code follows the project style guidelines
- [ ] I have updated the documentation
- [ ] My changes generate no new warnings
- [ ] I have added examples showing usage
```

## Community

### Getting Help

- **Discord**: Join our community server (link in README)
- **GitHub Discussions**: Ask questions and share ideas
- **Issue Tracker**: Report bugs or request features

### Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Given credit in relevant documentation

## 🙏 Thank You!

Your contributions make Meta-Agent for Claude Code better for everyone. We appreciate your time and effort in improving this project!

---

**Questions?** Feel free to open an issue or reach out to the maintainers.