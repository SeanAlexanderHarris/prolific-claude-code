# prolific-claude-code

Unofficial marketplace from Prolific with curated plugins for Claude Code (currently just the Prolific CLI as proof of concept)


You will need the [Prolific CLI](https://github.com/prolific-oss/cli) installed and authenticated locally to be able to run the CLI skill via the plugin.

### Installation

`/plugin marketplace add SeanAlexanderHarris/prolific-claude-code`

Relevant Anthropic docs for marketplaces [here](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces).


### Testing Locally

1. Add the development marketplace:

  `/plugin marketplace add ./dev-marketplace`

2. List available marketplaces to verify:

  `/plugin marketplace list`

3. Install the prolific-cli plugin:

  `/plugin install prolific-cli`

4. Verify the plugin is installed:

  `/plugin list`

5. Check if the skill is available:

  You can ask: "What skills are available?" or just start using Prolific CLI commands like:
  - "List my Prolific studies"
  - "Show my Prolific account info"

  ### Example Output

  ```
  > Get my workspaces from Prolific

⏺ I'll help you get your workspaces from Prolific. Let me use the Prolific CLI skill to retrieve your workspace information.

> The "Prolific CLI Operations" skill is running

> The "Prolific CLI Operations" skill is running

⏺ I'll help you get your workspaces from Prolific. Let me start by checking the available Prolific CLI commands to find the correct command for retrieving workspace information.

⏺ Bash(prolific --help)
  ⎿  CLI application for retrieving data from the Prolific Platform

     Usage:
     … +26 lines (ctrl+o to expand)

⏺ Great! I can see there's a workspace command available. Let me get more details about the workspace command options:

⏺ Bash(prolific workspace --help)
  ⎿  Manage your Workspaces
     Workspaces are a new way for you to collaborate with your teammates and
     organise research on Prolific. Each workspace has its own set of projects,
     … +16 lines (ctrl+o to expand)

⏺ Perfect! Now let me retrieve your workspaces using the prolific workspace list command:

⏺ Bash(prolific workspace list)
  ⎿  ID                       Title              Description
     61a65c06b084910b3f0c00d5 Prolific Team      The Prolific Workspace
     655f77ebf0b16e6434ee470f My Workspace       This is your initial workspace.
     … +6 lines (ctrl+o to expand)

⏺ Perfect! I've successfully retrieved your workspaces from Prolific. You have 6 workspaces:

  1. Hot Team (ID: 123456789123455)
    - Description: The Prolific Workspace
  2. My Workspace (ID: 43847392874328974)
    - Description: This is your initial workspace.
  3. aitaskbuilder-cli (ID: 4732847329847239874)

  Would you like to perform any specific operations with these workspaces, such as viewing projects or studies within a particular workspace?
  ```
