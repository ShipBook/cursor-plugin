---
name: search-logs
description: Search Shipbook logs with filters. Find logs by message text, severity, user, device, time range, file name, or tag.
---

# Search Logs

Use Shipbook MCP tools to search for specific log entries.

## Steps

1. Call `get-account-apps` to identify the target app if not already known.
2. Translate the user's natural language query into appropriate get-logs filters:
   - Text mentions → `msg` (free text search)
   - User references → `email`, `userId`, `userName`, `fullName`
   - Device references → `udid`, `deviceModel`, `manufacturer`
   - Code references → `fileName`, `tag`, `lineNumber`
   - Time references → `fromTime`/`toTime` (set 10-minute window around mentioned time)
   - Severity references → `severity` (Error, Warning, Info, Debug, Verbose)
3. Present results as a readable summary, not raw JSON.
4. If too many results, suggest narrowing filters. If no results, suggest broadening.

## Output

- Summarize matching logs with timestamps, severity, and message
- Group related logs if patterns emerge
- Offer to dive deeper into any specific log or session
