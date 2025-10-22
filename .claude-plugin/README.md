# Prolific Claude Code Plugin

This plugin provides Claude skills for working with the Prolific CLI research platform.

## Available Skills

### 1. prolific-cli-skill (Claude Code)
Location: `skill/prolific-cli-skill.md`

For use with **Claude Code CLI** where direct bash command execution is available. This skill provides instructions and best practices for using the Prolific CLI directly through bash commands.

**Use when:**
- Working in Claude Code CLI environment
- Direct terminal access is available
- Need to execute Prolific CLI commands automatically

### 2. prolific-cli-desktop (Claude Desktop)
Location: `claude-desktop-skill/`

For use with **Claude Desktop app on macOS** where direct bash execution is restricted. This skill uses a Python bridge script to enable Prolific CLI operations.

**Use when:**
- Working in Claude Desktop application
- Cannot execute bash commands directly
- Need to generate commands for manual execution

**Structure:**
```
claude-desktop-skill/
├── SKILL.md              # Skill definition and usage
├── reference.md          # Technical documentation
└── scripts/
    ├── prolific_bridge.py    # Python bridge to CLI
    └── example_workflow.py   # Automation examples
```

## Setup

### Claude Code Skill
No additional setup required. The skill provides instructions for using the Prolific CLI that should already be installed at `/Users/seanharris/go/bin/prolific`.

### Claude Desktop Skill

1. Ensure Python 3 is installed
2. Make bridge script executable:
   ```bash
   chmod +x .claude-plugin/claude-desktop-skill/scripts/prolific_bridge.py
   ```
3. Test the bridge:
   ```bash
   python3 .claude-plugin/claude-desktop-skill/scripts/prolific_bridge.py --version
   ```

## Usage Examples

### With Claude Code
```
User: "List all my Prolific studies"
Claude: [Executes] prolific studies list
```

### With Claude Desktop
```
User: "List all my Prolific studies"
Claude: "Run this command in your terminal:
python3 .claude-plugin/claude-desktop-skill/scripts/prolific_bridge.py studies list"
```

## Prerequisites

- **Prolific CLI** installed (https://github.com/prolific-oss/cli)
- **Valid Prolific API credentials** configured
- **Python 3** (for Claude Desktop skill only)

## Configuration

To use a different Prolific CLI installation path, update:
- Claude Code skill: No changes needed (uses PATH)
- Claude Desktop skill: Edit `PROLIFIC_CLI_PATH` in `claude-desktop-skill/scripts/prolific_bridge.py`

## Marketplace Configuration

This directory contains the marketplace configuration for publishing to Claude Code marketplace.

**Files:**
- `marketplace.json` - Marketplace listing configuration

The marketplace configuration defines marketplace name, owner information, plugin listings and metadata, sources and locations, tags for discoverability, and license information.

## Publishing

To publish to the marketplace, submit this configuration according to the Claude Code marketplace publishing guidelines.

## Support

For issues or questions:
- Prolific CLI: https://github.com/prolific-oss/cli
- Claude Documentation: https://docs.claude.com
