# Extension Points

Developers may extend the system only through the following points:

1. Add new evaluation logic under `evaluation/`
2. Add new actions under `actions/`
3. Improve feedback analysis under `feedback/`

The following MUST NOT be changed:
- Loop order
- Decision map semantics
- State contract

Breaking these rules breaks the system.
