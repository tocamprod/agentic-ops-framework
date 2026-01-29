# Evaluation Module

This module evaluates the current system state.

Responsibilities:
- Read current_state.json
- Analyze metrics and signals
- Classify the system into a discrete state (A, B, C, D)

This module MUST NOT:
- Trigger actions
- Send notifications
- Modify external systems
