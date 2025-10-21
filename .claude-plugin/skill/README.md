# Prolific CLI Skill for Claude Code

This directory contains the skill definition that gives Claude Code expertise in working with the Prolific CLI.

## Files

- `prolific-cli-skill.md` - Comprehensive skill instructions and examples

## What This Skill Provides

The Prolific CLI skill enables Claude Code to:
- Execute Prolific CLI commands via bash
- Manage research studies and participants
- Export and analyze study data
- Work with AI Task Builder
- Handle authentication and configuration
- Troubleshoot common issues

## How It Works

When a user asks Claude Code to perform Prolific-related tasks, Claude Code uses this skill to:
1. Understand the user's intent
2. Verify CLI availability and syntax
3. Execute appropriate Prolific CLI commands
4. Parse and explain results
5. Help with error resolution

## Skill Capabilities

- **Study Management**: Create, list, publish, pause studies
- **Participant Operations**: View participants, manage submissions
- **Data Export**: Export study data in various formats
- **Workspace Management**: List and manage workspaces
- **Project Management**: Organize studies within projects
- **AI Task Builder**: Create and manage AI-powered studies

## Prerequisites

This skill assumes:
1. Prolific CLI is installed on the user's system
2. User has valid Prolific API credentials
3. Claude Code has permission to execute bash commands

## Usage

Once installed, simply ask Claude Code natural language questions like:
- "Show me my Prolific workspaces"
- "Create a study with 50 participants"
- "Export data from study xyz789"

Claude Code will automatically use this skill to help you accomplish these tasks.

## Best Practices

- The skill always checks CLI help output for current syntax
- Commands are explained before and after execution
- Errors are handled gracefully with helpful suggestions
- Configuration files are created when needed

## Customization

You can customize this skill by editing `prolific-cli-skill.md` to add:
- Custom workflows specific to your organization
- Additional command examples
- Organization-specific best practices
- Custom error handling procedures
