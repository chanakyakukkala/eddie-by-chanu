# Eddie — HousingWire SEC Filing Monitor

A product and workflow system designed to monitor SEC filings from selected companies and deliver real-time alerts to internal teams through Slack.

## The problem

Teams tracking public companies often rely on manual checking, fragmented tools, or delayed updates to stay on top of filings. That creates a few problems:

- important filings can be missed or noticed too late
- monitoring across multiple companies becomes repetitive and inefficient
- teams lack a single dashboard for filing activity, alert status, and monitoring health
- internal workflows depend too heavily on manual effort

I wanted to design a system that reduced that friction and made SEC filing monitoring more reliable, visible, and actionable.

## The solution

Eddie is a filing monitoring system built to track SEC activity for specified companies and route alerts into existing team workflows.

The product includes:

- real-time monitoring of SEC filings by company and CIK
- company management for adding, editing, and enabling monitored entities
- Slack alerting for newly detected filings
- a dashboard for monitoring status and filing history
- database-backed storage and real-time updates with Supabase

The goal was to create a workflow that felt operationally lightweight for users while still supporting a reliable monitoring pipeline behind the scenes.

## Key product decisions

- **Slack-first alerting**  
  Instead of asking users to check another tool constantly, alerts are pushed into an existing collaboration channel.

- **CIK-based company setup**  
  Monitoring is anchored on SEC-native identifiers to make company tracking accurate and scalable.

- **Dashboard visibility**  
  Users need confidence that the system is running, what was detected, and whether alerts were delivered successfully.

- **Extensible backend foundation**  
  The structure supports additional alerting logic, more notification channels, and deeper filing categorization over time.

## Core features

- SEC filing monitoring for active companies
- company management by CIK and ticker
- filing detection and deduplication
- Slack notifications for new filings
- real-time dashboard and filing history
- secure storage with Supabase

## Workflow

1. Users add companies to monitor using CIK numbers
2. The system checks SEC EDGAR for new filings
3. New filings are detected against stored records
4. Alerts are generated and sent to Slack
5. Dashboard history and monitoring status update in real time

## Why this matters

This product is useful for editorial, research, and market-monitoring workflows where speed and visibility matter. Instead of waiting for someone to manually notice a filing, teams get a structured and repeatable way to stay informed.

## My role

I approached this as a product and systems design exercise across:

- problem framing
- workflow design
- feature definition
- data and alert logic
- dashboard thinking
- operational usability

## Impact

This project demonstrates how a relatively focused workflow tool can:

- reduce manual monitoring effort
- improve timeliness of information capture
- make alerting more consistent
- centralize visibility across filings, companies, and delivery status

## What I’d improve next

- smarter filing prioritization by form type and company importance
- user-level alert preferences and channel routing
- better filtering and search across filing history
- system health monitoring and failure recovery workflows
- analytics on alert usefulness and user engagement

## Screenshots

<img width="1371" height="957" alt="image" src="https://github.com/user-attachments/assets/38712142-6c4f-48a1-8d77-1e97a0b00101" />
<img width="1371" height="957" alt="image" src="https://github.com/user-attachments/assets/fa7df723-ea41-44d5-900e-a13cdd387bba" />
<img width="1207" height="768" alt="image" src="https://github.com/user-attachments/assets/2be36683-c7b5-4c10-b6f4-b1e133241a12" />



## Notes

This is a showcase repository focused on product design, workflow, and system architecture. The underlying implementation remains private.
