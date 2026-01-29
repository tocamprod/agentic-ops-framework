> This document defines the operational loop.
> It is the source of truth for execution order and system behavior.
> Conceptual descriptions live in `overview.md`.
> Capability mappings live in `loop_mapping.md`.

# Operational Intelligence Loop

This system is designed as a continuous reasoning loop, not a linear workflow.

The loop continuously evaluates operational signals, system knowledge, and past outcomes to decide the next best action.

## Core Loop States

1. Signal  
An operational event, anomaly, or error is detected from a client pipeline.

2. Sense  
The system interprets raw signals and structures the incident context.

3. Reason  
The system analyzes the incident, searches for similar past cases, and builds understanding.

4. Propose  
One or more possible resolutions are generated.

5. Decide  
The system determines whether human approval is required or if the case qualifies for autonomous action.

6. Act or Wait  
- If approved or validated, an action may be executed.
- Otherwise, the system waits for human input.

7. Learn  
The outcome is documented and stored as organizational knowledge.

The loop then restarts, using accumulated knowledge to improve future decisions.
