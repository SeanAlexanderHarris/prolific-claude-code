---
name: Prolific CLI Operations
description: Comprehensive skill for working with the Prolific CLI tool to manage studies, participants, and research data. Use this skill when users need to interact with Prolific's research platform through command-line operations.
---

# Prolific CLI Operations

## Instructions

This skill provides comprehensive guidance for using the Prolific CLI to manage research studies, participants, and data collection workflows.

**IMPORTANT: Always start by running `prolific --help` to get the current overview of available commands and their correct syntax before attempting any operations. The CLI commands may differ from the examples below.**

### Core CLI Operations

1. **Authentication and Setup**
   - Use `prolific auth login` to authenticate with your Prolific account
   - Configure workspace settings with `prolific config`
   - Verify connection with `prolific whoami`

2. **Study Management**
   - List studies: `prolific studies list`
   - Create studies: `prolific studies create --config study-config.json`
   - View study details: `prolific studies show <study-id>`
   - Publish studies: `prolific studies publish <study-id>`
   - Pause/resume studies: `prolific studies pause|resume <study-id>`

3. **Participant Management**
   - View participants: `prolific participants list --study-id <study-id>`
   - Manage submissions: `prolific submissions list --study-id <study-id>`
   - Handle participant screening: `prolific participants screen --criteria <criteria>`

4. **Data Operations**
   - Export study data: `prolific data export --study-id <study-id> --format csv|json`
   - Download participant responses: `prolific data download --study-id <study-id>`
   - Generate reports: `prolific reports generate --study-id <study-id>`

5. **AI Task Builder Integration**
   - Create AI-powered studies: `prolific ai-task-builder create --template <template>`
   - Manage AI task configurations: `prolific ai-task-builder config`
   - Get dataset statistics: `prolific ai-task-builder stats --dataset <dataset-id>`

### Best Practices

- **ALWAYS run `prolific --help` first** to see current available commands and syntax
- Verify CLI version compatibility: `prolific --version`
- Use `--help` flag with any command to see available options (e.g., `prolific studies --help`)
- Test configurations in development mode before publishing studies
- Regularly backup study configurations using export commands
- Monitor participant progress with list and status commands
- If a command fails with "unknown command", check the help output for the correct command name

## Examples

### Basic Study Workflow
```bash
# Authenticate
prolific auth login

# List existing studies
prolific studies list

# Create a new study from configuration
prolific studies create --config my-study.json

# Publish the study
prolific studies publish <study-id>

# Monitor participants
prolific participants list --study-id <study-id>

# Export results when complete
prolific data export --study-id <study-id> --format csv
```

### AI Task Builder Workflow
```bash
# Create an AI-powered study
prolific ai-task-builder create --template standard-sample

# Check dataset statistics
prolific ai-task-builder stats --dataset my-dataset

# Configure AI task parameters
prolific ai-task-builder config --study-id <study-id>
```

### Data Analysis Pipeline
```bash
# Export all study data
prolific data export --study-id <study-id> --format json --output data/

# Generate comprehensive report
prolific reports generate --study-id <study-id> --include-demographics

# Download individual submissions
prolific submissions download --study-id <study-id> --status completed
```

## When to Use This Skill

Use this skill when users need to:
- Set up or configure the Prolific CLI
- Create, manage, or publish research studies
- Handle participant recruitment and screening
- Export or analyze study data
- Integrate AI Task Builder capabilities
- Troubleshoot CLI operations or authentication issues
- Automate research workflows using command-line tools