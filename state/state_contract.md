# State Contract

This document defines the required structure of the system state.

Any system reading or writing state must comply.

## Required Fields
- status
- current_state
- open_cases
- last_evaluated_at
- human_in_the_loop_required

Breaking this contract invalidates the loop.
