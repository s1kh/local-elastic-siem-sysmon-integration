# Local Elastic SIEM with Sysmon Integration

## Overview
Deployment and configuration of a local Security Information and Event Management
(SIEM) environment using the Elastic Stack, with Microsoft Sysmon providing detailed
endpoint telemetry and Elastic Agent/Fleet forwarding logs for centralized analysis.

## My Contribution
Individual project. I deployed, configured, and validated the entire pipeline
end-to-end.

## Objectives
- Stand up a working local SIEM for real-time system visibility
- Generate detailed endpoint telemetry (process creation, network activity)
- Centralize log collection and confirm detection capability with a proof of concept

## Environment
| Component | Details |
|---|---|
| SIEM Platform | Elastic Stack 9.3.3 (Elasticsearch + Kibana) |
| Log Source | Microsoft Sysmon v15.20 |
| Log Shipping | Fleet-managed Elastic Agent |

## Work Performed
- Installed Elasticsearch and Kibana locally and completed initial setup
- Initialized a Fleet server for centralized Elastic Agent management
- Installed and verified Microsoft Sysmon for detailed Windows event logging
- Installed and enrolled an Elastic Agent, verifying a "Healthy" status in Fleet
- Validated end-to-end log ingestion in Kibana Discover across multiple log
  sources (Sysmon operational logs, Windows security logs, agent health)
- Ran a proof-of-concept test (executing and tracking a command through to its
  indexed log) to confirm real-time detection capability

## Results
- Achieved real-time, centralized visibility into endpoint activity
- Confirmed the pipeline could ingest, parse, and visualize security-relevant
  events within seconds

## Documentation
See [`docs/Deployment of a Centralized SIEM.pdf`](./docs/Deployment of a Centralized SIEM.pdf) for the full written report, including setup steps and
supporting screenshots.

## Disclaimer
Deployed locally for educational purposes; no production or organizational data
was involved.
