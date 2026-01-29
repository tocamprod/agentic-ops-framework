# State Classification Logic

This document defines how the system classifies its current state.

## Input
- state/current_state.json

## Output
- One of: A, B, C, D

## State Definitions

### A — Healthy
- No open cases
- No anomalies detected
- human_in_the_loop_required = false

### B — Warning
- Minor issues detected
- No critical impact
- human_in_the_loop_required = false

### C — Degraded
- Active issues affecting operations
- Requires human review
- human_in_the_loop_required = true

### D — Critical
- System failure or blocking issue
- Immediate escalation
- human_in_the_loop_required = true
