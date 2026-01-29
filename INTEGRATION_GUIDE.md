# Integration Guide

This document explains how developers should connect
real systems to the Agentic Ops Framework.

## Where to Plug Code

### 1. Signals
External events should update `state/current_state.json`
or trigger the loop runner.

### 2. Evaluation
Replace rule-based evaluation with:
- LLM calls
- Metrics engines
- Anomaly detectors

Inputs and outputs must remain stable.

### 3. Actions
Each action must:
- Be idempotent
- Be traceable
- Write execution feedback

No action may decide or classify.

### 4. Feedback
Every executed action must result in a case record.

## Forbidden Patterns
- Direct execution without decision map
- Hidden autonomy
- Agents triggering other agents directly

All coordination happens through the loop.
