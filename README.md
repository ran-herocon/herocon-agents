# HeroCon Agents

Scheduled Claude Code agents that run autonomously on behalf of HeroCon's team.

## Agents

| Agent | Folder | What it does |
|---|---|---|
| PMM Competitive Intelligence | [`agents/pmm/`](agents/pmm/) | Discovers net-new competitors daily, tracks known rivals weekly, posts to Slack + Notion |

## How it works

Each agent is a Claude Code remote routine registered via the `/schedule` skill. Routines run on a cron schedule, have access to Slack and Notion MCP servers, and post results autonomously — no human in the loop.

To trigger a routine manually, use the RemoteTrigger API with the routine ID listed in the agent's README.

## Adding a new agent

1. Create a new folder under `agents/<name>/`
2. Write a `README.md` (config: routine IDs, cron, model, Slack channel, Notion DB)
3. Write the routine prompt(s) as `.md` files
4. Register via `/schedule` in a Claude Code session
5. Add the agent to the table above

## Stack

- **Runtime:** Claude Code remote routines (`claude-sonnet-4-6`)
- **Integrations:** Slack MCP, Notion MCP
- **Scheduling:** Cron via Claude Code `/schedule`
