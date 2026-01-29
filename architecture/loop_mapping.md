# Loop Capability Mapping

This document maps loop states to the system capabilities (agents) they can invoke.

The loop is the primary control structure. Agents are passive capabilities used when needed.

## Loop State → Capability Mapping

### Signal
- Observer Agent  
Purpose: Detect operational events or anomalies.

### Sense
- Observer Agent  
Purpose: Structure raw signals into incident context.

### Reason
- Diagnosis Agent  
Purpose: Analyze context and identify probable root causes.

### Propose
- Solution Agent  
Purpose: Generate resolution proposals and assess risk.

### Decide
- Decision Logic  
- Human-in-the-Loop (if required)  
Purpose: Determine whether autonomous action is allowed or human approval is required.

### Act / Wait
- Deployment Capability (conditional)  
Purpose: Execute approved actions or pause awaiting human input.

### Learn
- Documentation Agent  
Purpose: Store outcomes as organizational knowledge.

### Communicate
- Notification Agent  
Purpose: Inform stakeholders about incident resolution and status.
