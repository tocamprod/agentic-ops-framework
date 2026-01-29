# Decision Map

This module defines what actions are allowed based on the evaluated system state.

It acts as a guardrail between reasoning and execution.

## States

### State A — Healthy
Allowed actions:
- log_state

Human approval required: false

---

### State B — Warning
Allowed actions:
- log_state
- notify_internal_summary

Human approval required: false

---

### State C — Degraded
Allowed actions:
- log_state
- notify_internal
- request_human_review

Human approval required: true

---

### State D — Critical
Allowed actions:
- log_state
- notify_internal
- notify_client
- escalate

Human approval required: true
