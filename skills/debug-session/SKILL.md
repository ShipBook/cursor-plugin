---
name: debug-session
description: Debug a specific user session in ShipBook. Finds logs for a user by email, device ID, or user ID, then traces the full session to understand what happened.
---

# Debug User Session

Use ShipBook MCP tools to debug what happened in a specific user's session.

## Steps

1. Call `get-account-apps` to identify the app.
2. Call `get-logs` filtered by the user identifier provided (email, userId, userName, udid) with severity=Error to find problems.
3. If errors are found, take the `session` ID from the error log and call `get-logs` again without severity filter to get the full session timeline.
4. If no errors are found, broaden the search (remove severity filter, adjust time range) to find the user's activity.
5. Use `minOrderId`/`maxOrderId` to navigate through long sessions.

## Output

- Reconstruct the user's session timeline chronologically
- Highlight any errors or warnings encountered
- Identify the sequence of events leading to any issues
- Suggest fixes if the problem is identifiable from the logs
