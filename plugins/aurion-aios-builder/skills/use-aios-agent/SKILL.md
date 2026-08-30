---
name: use-aios-agent
description: Find, inspect, invoke, schedule, continue training, or request archival of an active Aurion AIOS employee from Claude, ChatGPT, Codex, or Cursor.
---

# Use an AIOS Agent

Use the signed-in account's active AIOS employees as the source of truth.

1. Call `list_available_agents` and match the user's request to one employee. If ambiguous, show a short candidate list instead of guessing.
2. Call `get_agent_capabilities` for the selected Agent and collect only missing required inputs.
3. Call `invoke_agent` with a stable idempotency key.
4. Poll `get_agent_run` until a terminal state. Never report QUEUED or RUNNING as completed.
5. Return the actual result and any real blocker plainly.

If the user wants to teach or revise an employee, switch to the `build-aios-agent` workflow and pass the existing `agentId` to `start_agent_build`; AIOS resumes that employee's durable training session.

Runtime restrictions, budgets, and tool allowlists still apply. A tool mentioned in training is not connected until AIOS reports it available. Scheduling and archival use their dedicated tools and must be described according to the returned state, never as completed before AIOS confirms it.
