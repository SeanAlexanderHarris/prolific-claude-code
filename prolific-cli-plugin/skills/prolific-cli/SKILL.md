---
name: use-prolific-cli
description: Run the Prolific CLI
---

# Use Prolific CLI

This skill provides comprehensive guidance for using the Prolific CLI to manage research studies, participants, and data collection workflows.

### Prerequisites

This skill assumes the user has:
1. **Prolific CLI installed** on their local machine (see https://github.com/prolific-oss/cli)
2. **PROLIFIC_TOKEN environment variable set** with a valid API token
3. **Enabled Claude Code** to execute bash commands

This skill does NOT install the CLI itself - it provides expertise on using the CLI tool that must already be installed and authenticated on the user's machine.

### Best Practices

- **ALWAYS run `prolific --help` first** to see current available commands and syntax
- Use `--help` flag with any command to see available options (e.g., `prolific studies --help`)
- Review carefully before publishing studies
- If a command fails with "unknown command", check the help output for the correct command name

## When to Use This Skill

Use this skill when users need to:
- Set up or configure the Prolific CLI
- Create, manage, or publish research studies
- Handle participant recruitment and screening
- Export or analyze study data
- Troubleshoot CLI operations or authentication issues
- Automate research workflows using command-line tools

## How Claude Should Use This Skill

When helping users with Prolific CLI operations:

1. **Verify Installation First**: Check if the CLI is available by running `prolific --version`
2. **Check Help Output**: Run `prolific --help` or `prolific [command] --help` to verify current syntax
3. **Use Bash Tool**: Execute Prolific CLI commands using the Bash tool (e.g., `prolific studies list`)
4. **Create Config Files**: Use Write/Edit tools to create YAML/JSON study configuration files
5. **Check Environment**: Verify `PROLIFIC_TOKEN` is set if authentication errors occur
6. **Provide Context**: Explain what each command does before and after execution

### Example Workflow

When user asks: "Create a study with 100 participants aged 18-65"

1. Run `prolific --help` to verify CLI is available
2. Use Write tool to create a study configuration YAML file
3. Use Bash tool to run: `prolific study create -t study-config.yaml`
4. Parse the output and confirm success or help debug errors

Always verify commands with `--help` flag as the CLI may have been updated.