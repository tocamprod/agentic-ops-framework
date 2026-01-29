# Case Record Schema

This document defines how resolved cases are stored.

Each case represents a learning unit.

## Required Fields

- case_id
- client_id
- detected_signal
- classified_state (A | B | C | D)
- proposed_solution
- executed_action
- human_approval (true | false)
- outcome (success | failure)
- timestamp

## Optional Fields

- related_cases
- confidence_score
- notes

Cases with repeated successful outcomes
may qualify for autonomous execution.
