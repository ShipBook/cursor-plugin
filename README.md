# ShipBook Plugin for Cursor

Connect [Cursor](https://cursor.com) to [ShipBook](https://shipbook.io)'s cloud logging platform via MCP (Model Context Protocol).

Search logs, investigate errors, and debug user sessions — all from within your IDE using AI.

**Prerequisites:** A [ShipBook](https://shipbook.io) account with at least one app. [Get started here](https://docs.shipbook.io).

## Features

### MCP Tools

| Tool | Description |
|------|-------------|
| **get-account-apps** | List all apps in your ShipBook account |
| **get-loglytics-errors** | Retrieve grouped/classified errors with occurrence counts |
| **get-logs** | Search logs with 20+ filters (severity, user, device, time, etc.) |

### AI Skills

Pre-built investigation workflows:

| Skill | Description |
|-------|-------------|
| **investigate-errors** | Diagnose errors using Loglytics data and session context |
| **debug-session** | Trace a user's session to understand what happened |
| **search-logs** | Search logs using natural language queries |

### Rules

Built-in AI guidance for optimal tool usage, including investigation workflows and best practices.

## Installation

### From Cursor Marketplace

Search for "ShipBook" in the Cursor marketplace and click Install.

### One-Click Install

<a href="cursor://anysphere.cursor-deeplink/mcp/install?name=shipbook&config=eyJ1cmwiOiJodHRwczovL2FwaS5zaGlwYm9vay5pby9tY3AiLCJhdXRoIjp7IkNMSUVOVF9JRCI6ImExZGI4ZGY1LWNlYjUtNDAxMy04YzM1LWFmOWU0NTdjNjliNSJ9fQ">
  <img src="https://cursor.com/deeplink/mcp-install-dark.svg" alt="Install ShipBook MCP in Cursor" height="32" />
</a>

## Authentication

The plugin uses **OAuth 2.1** for secure authentication. On first use, you will be redirected to ShipBook to log in and authorize access. Your credentials are never shared with Cursor.

## Usage Examples

- "Find errors in my app and suggest fixes"
- "What happened to the user with email test@example.com?"
- "Show me logs from the last hour with severity Error"
- "Investigate the most common crash in my iOS app"
- "Debug the session where user X reported a problem"
- "Fix the issues found in ShipBook Loglytics"

## Documentation

- [ShipBook MCP Documentation](https://docs.shipbook.io/mcp)
- [ShipBook Website](https://shipbook.io)

## License

MIT
