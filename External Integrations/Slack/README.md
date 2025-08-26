# Slack Integration with TheHive

This topic explains how **Slack** integrates with **TheHive**.

## About Slack
Slack is a team collaboration platform offering channels, direct messaging, file sharing, and a rich app ecosystem for workflows and incident response.

## Responders
Cortex responders for Slack perform automated actions directly from TheHive.
| Responder | Purpose |
| --- | --- |
| Slack_CreateChannel | Creates a Slack channel for a TheHive case, invites participants, and optionally posts a case summary and/or case description. |

Find the complete list of Slack responders and their configuration details in the [Cortex Neurons documentation](https://thehive-project.github.io/Cortex-Analyzers/responders/Slack/) as well as its [source code](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/responders/Slack).

## Next steps
* [slack-case-assignee-change.md](use-cases/slack-case-assignee-change.md)
* [slack-notifier-alert-creation.md](use-cases/slack-notifier-alert-creation.md)