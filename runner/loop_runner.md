# Agentic Ops Loop Runner

This document defines how the operational loop is executed step by step.

This is not implementation code.
It is the canonical execution order.

---

## Loop Execution

### Step 1 — Load State
- Read `state/current_state.json`
- Load open cases and last evaluation

---

### Step 2 — Evaluate
- Apply rules from `evaluation/classify_state.md`
- Determine system state: A, B, C, or D

---

### Step 3 — Decide
- Consult `decision_map/README.md`
- Determine allowed actions
- Determine if human approval is required

---

### Step 4 — Human Gate (if required)
- Pause execution
- Await explicit human input
- Resume loop only after approval or rejection

---

### Step 5 — Execute Actions
- Trigger allowed actions from `actions/`
- Example: notification_agent

---

### Step 6 — Persist Feedback
- Update `state/current_state.json`
- Append execution result with timestamp

---

### Step 7 — Loop
- Wait for next signal or scheduled trigger
- Restart from Step 1
