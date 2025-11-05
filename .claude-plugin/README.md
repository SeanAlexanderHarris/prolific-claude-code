# Prolific Claude Code Marketplace

This marketplace provides a Claude plugin for working with the Prolific CLI research platform.

## Plugin Structure

```
.claude-plugin/
├── marketplace.json              # Marketplace configuration
└── plugins/
    └── prolific-cli/            # Prolific CLI plugin
        ├── .claude-plugin/
        │   └── plugin.json      # Plugin metadata
        └── skills/
            └── prolific-cli.md  # Skill definition
```

## Available Plugin: prolific-cli

The `prolific-cli` plugin provides a skill for working with the Prolific CLI tool. This skill enables Claude Code to help users manage research studies, participants, and data collection workflows.

**Key Features:**
- Execute Prolific CLI commands directly through Claude Code
- Manage research studies and participant recruitment
- Export and analyze study data
- Automate research workflows

## Setup

No additional setup required beyond:
1. **Prolific CLI** installed on your system (https://github.com/prolific-oss/cli)
2. **Valid Prolific API credentials** configured
3. **Claude Code** with plugin support enabled

## Usage

Once installed, the skill will automatically activate when you ask Claude Code to perform Prolific-related tasks:

```
User: "List all my Prolific studies"
Claude: [Executes] prolific studies list
```

## Installation

Add this marketplace to Claude Code:

```
/plugin marketplace add SeanAlexanderHarris/prolific-claude-code
```

Then install the prolific-cli plugin:

```
/plugin install prolific-cli
```

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
