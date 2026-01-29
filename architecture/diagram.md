# Agentic Ops – Operational Loop Diagram

```mermaid
flowchart TD
    Signal[Signal / Event]
    State[State<br/>Persistent Memory]
    Evaluation[Evaluation<br/>Classify State]
    Decision[Decision Map<br/>Allowed Actions]
    Human[Human-in-the-Loop]
    Actions[Actions<br/>Side Effects]
    Feedback[Feedback & Memory]
    
    Signal --> State
    State --> Evaluation
    Evaluation --> Decision

    Decision -->|Human Required| Human
    Human -->|Approved| Actions
    Human -->|Rejected| Feedback

    Decision -->|No Human Required| Actions

    Actions --> Feedback
    Feedback --> State
    State --> Signal

