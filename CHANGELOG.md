# Changelog

All notable changes to the Meta-Agent for Claude Code project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial release of Meta-Agent Collection for Claude Code
- Core meta-agents:
  - `meta-agent` - Creates new customized agent collections
  - `meta-agent-zh` - Chinese version of meta-agent
  - `meta-agent-updater` - Updates existing agent collections
  - `meta-agent-updater-zh` - Chinese version of updater
  - `meta-agent-unified` - Combined creation and update capabilities
  - `meta-agent-unified-zh` - Chinese version of unified agent
- Support agents (14 specialized agents):
  - `agent-template-generator` - Creates new meta-agent variants
  - `agent-validator` - Validates agent file structure
  - `bilingual-synchronizer` - Synchronizes English/Chinese versions
  - `model-assignment-optimizer` - Optimizes model tier selection
  - `prompt-quality-analyzer` - Analyzes and improves prompts
  - `claude-md-updater` - Maintains CLAUDE.md documentation
  - `agent-catalog-manager` - Manages agent inventory
  - `workflow-validator` - Validates interactive workflows
  - `pattern-extractor` - Identifies successful patterns
  - `feature-gap-analyzer` - Finds missing capabilities
  - `git-hook-manager` - Sets up git hooks for validation
  - `quick-agent-selector` - Interactive agent selection tool
  - `readme-generator` - Generates README documentation
- Comprehensive documentation:
  - README.md with usage examples
  - CONTRIBUTING.md with contribution guidelines
  - CODE_OF_CONDUCT.md for community standards
  - CLAUDE.md for Claude Code instructions
- MIT License for open source use
- .gitignore for common development files

### Features
- 4-phase interactive workflow for all meta-agents
- Bilingual support (English and Chinese)
- Automatic model tier optimization (Haiku/Sonnet/Opus)
- YAML frontmatter format for agent definitions
- Comprehensive validation and quality checks

## [1.0.0] - 2024-XX-XX (Planned)

### Planned Features
- GitHub Actions integration for CI/CD
- Automated testing suite
- Web-based agent builder interface
- Additional language support (Japanese, Spanish, French)
- Agent marketplace for community contributions
- Performance metrics and analytics
- Cloud-based agent storage option

## Version History

### Pre-release Development
- 2024-01 - Initial concept and prototype
- 2024-02 - Core meta-agent development
- 2024-03 - Bilingual support implementation
- 2024-04 - Support agents creation
- 2024-05 - Documentation and open source preparation

## How to Update

To update to the latest version:

1. Pull the latest changes:
   ```bash
   git pull origin main
   ```

2. Review the changelog for breaking changes

3. Update your existing agents if needed:
   ```bash
   @meta-agent-updater Update my agents to latest version
   ```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute to this project.

## Support

For questions, issues, or feature requests:
- Open an [issue](https://github.com/liqiongyu/meta_agent_for_claude_code/issues)
- Join the [discussions](https://github.com/liqiongyu/meta_agent_for_claude_code/discussions)

---

[Unreleased]: https://github.com/liqiongyu/meta_agent_for_claude_code/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/liqiongyu/meta_agent_for_claude_code/releases/tag/v1.0.0