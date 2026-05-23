# PMM Competitive Intelligence Agent

Two scheduled Claude Code routines that monitor HeroCon's competitive landscape.

## Configuration

| Key | Value |
|---|---|
| Notion collection ID | `0f07780c-f6b5-4397-bd53-28e3a68c66eb` |
| Notion DB page URL | https://www.notion.so/edc7cceaf5f1417bae081e1919543ab3 |
| Slack channel | `C0B57P1C7MM` |
| Ran's Slack user ID | `U0B55G1TMEU` |
| Model | `claude-sonnet-4-6` |
| Discovery cron | `0 9 * * *` - daily 9am Asia/Jerusalem |
| Weekly cron | `0 9 * * 0` - Sunday 9am Asia/Jerusalem |

## Routines

| Routine | Routine ID | Prompt file | Job |
|---|---|---|---|
| `pmm-discovery` | `trig_01PLXZUNCco94iJxopJfDUmm` | `agents/pmm/discovery-prompt.md` | Find net-new competitors -> Slack + Notion |
| `pmm-weekly` | `trig_011nbtsY53cHhS7XyZr753nY` | `agents/pmm/weekly-prompt.md` | Track known rivals + weekly digest |

## Updating a prompt

1. Edit the relevant `.md` file in `agents/pmm/`
2. Re-register the routine via `/schedule` with the updated prompt text
3. Commit the change

## Known competitor seed list (initial)

- Paces
- UpCodes
- Autositu

## HeroCon design partners (customer overlap trigger)

- Haskell
- DPR
- Beck
- Copper Mill
