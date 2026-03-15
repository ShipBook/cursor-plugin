---
name: investigate-errors
description: Investigate and diagnose errors in a ShipBook app. Retrieves grouped error data from Loglytics, finds specific error instances, and traces the full session context to identify root causes.
---

# Investigate Errors

Use ShipBook MCP tools to investigate errors in an application.

## Steps

1. Call `get-account-apps` to list available apps. Ask the user which app to investigate if not specified.
2. Call `get-loglytics-errors` with the appId to retrieve grouped error categories.
3. Present errors ranked by impact (occurrence count, affected devices/sessions).
4. For the most critical error (or the one the user asks about), use its `key` with `get-logs` to find specific instances.
5. Pick a representative error log and use its `session` ID to call `get-logs` without severity filter — this reveals the full session timeline leading up to the error.
6. Summarize findings: what happened, how often, which users/devices are affected, and suggest code fixes if the cause is identifiable.

## Output

- Present a prioritized list of errors with counts
- For investigated errors, show the chain of events leading to the crash/error
- Suggest concrete fixes when the root cause is visible in the logs
- If the user's codebase is open, offer to locate and fix the relevant code
