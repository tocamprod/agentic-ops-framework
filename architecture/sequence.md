# Agentic Ops – Loop Sequence Diagram

```mermaid
sequenceDiagram
    participant S as Signal Source
    participant ST as State Store
    participant E as Evaluation
    participant D as Decision Map
    participant H as Human
    participant A as Actions
    participant F as Feedback

    S->>ST: New signal / event
    ST->>E: Load current_state
    E->>D: Classified state (A/B/C/D)

    alt Human approval required
        D->>H: Request approval
        H-->>D: Approve / Reject
    end

    D->>A: Allowed actions
    A->>F: Execution result
    F->>ST: Update state & memory
