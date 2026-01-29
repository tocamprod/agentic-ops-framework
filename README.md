# Agentic Ops Framework

This repository defines an operational, loop-based architecture
for agentic systems with human-in-the-loop governance.

## Core Principles
- This is a loop, not a workflow
- Decisions are separated from execution
- Human approval is explicit and enforceable
- Autonomy is earned through evidence

## High-Level Loop

Signal  
→ State  
→ Evaluation  
→ Decision Map  
→ Actions  
→ Feedback / Memory  
→ Loop

## Repository Structure

- `state/`  
  Persistent system memory (source of truth)

- `evaluation/`  
  System reasoning and state classification

- `decision_map/`  
  Allowed actions per system state

- `actions/`  
  Side effects (notifications, adjustments, etc.)

- `feedback/`  
  Learning, case memory, autonomy enablement

- `runner/`  
  Loop execution logic

- `architecture/`  
  Conceptual and operational documentation

## note

If you are implementing or extending this system:
- Do NOT change the loop order
- Do NOT execute actions outside the decision map
- All new capabilities must integrate through existing modules

See `architecture/overview.md` to get started.

