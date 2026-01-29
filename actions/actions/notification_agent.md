# Notification Agent (Slack)

Purpose:
Send controlled notifications based on allowed actions.

## Inputs
- system_state (A, B, C, D)
- case_id
- message
- target (internal | client)

## Behavior
- Sends messages only if permitted by decision_map
- Logs notification result
- Never retries autonomously without loop re-evaluation

## Channels
- Internal: #ops-alerts
- Client-facing: #client-notifications
