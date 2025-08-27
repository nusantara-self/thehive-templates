# Proofpoint Integration with TheHive

This topic explains how **Proofpoint** integrates with **TheHive**.

## About Proofpoint
Proofpoint is an email and cloud security platform that protects mail and collaboration tools from advanced threats and data loss. For incident response, it surfaces user-risk signals and rich telemetry (message traces, URL and attachment verdicts, click activity) and publishes TAP event streams (`messageDelivered`, `clicksPermitted`) plus APIs/webhooks that TheHive can consume for alerting and investigation.


## Alert ingestion
Proofpoint events can be ingested into TheHive through multiple methods, depending on your architecture and integration approach.

### Method 1: Native features
* [Alert ingestion for Proofpoint TAP alerts – Clicks Permitted](use-cases/alert-ingestion-clicksPermitted.md) – Ingest Proofpoint TAP clicksPermitted events as TheHive alerts to track and respond to users who clicked on malicious links that were not blocked by Proofpoint and may require investigation.
* [Alert ingestion for Proofpoint TAP alerts – Message Delivered](use-cases/alert-ingestion-messageDelivered.md) – Ingest Proofpoint TAP messagesDelivered events as TheHive alerts to track and respond to threats that have reached user mailboxes and may require investigation.

### Method 2: SIEM tools
If you ingest TheHive alerts via your SIEM, official **Splunk** or **Elastic** integrations can forward relevant TAP events and context:
- [Splunk apps](https://splunkbase.splunk.com/apps?page=1&author=proofpointsplunkintegrations)
- [Elastic integration](https://www.elastic.co/docs/reference/integrations/proofpoint_tap)

### Method 3: External scripts

You can build or use a connector that polls or subscribes to Proofpoint APIs/webhooks and creates **TheHive Alerts** in real time. Make sure to customize alerts title, description, tags, observables extraction, custom fields and TTPs as needed.

## Analyzers
Cortex analyzers enrich investigations in TheHive with contextual data from the product APIs.

| Analyzer | Purpose |
| --- | --- |
| ProofPoint_Lookup | Check URL, file, SHA256 against ProofPoint forensics. |

Find Proofpoint analyzers and their configuration details in the [Cortex Neurons documentation](https://thehive-project.github.io/Cortex-Analyzers/analyzers/Proofpoint/) as well as its [source code](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/analyzers/Proofpoint)
