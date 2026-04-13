# YouWire MCP Server

> **Compliance call recording intelligence for Japan**

YouWire MCP is a [Model Context Protocol](https://modelcontextprotocol.io) server that connects Claude directly to the YouWire compliance call recording platform. It enables AI-powered search, transcription retrieval, and analysis of business call recordings across all communication channels used in Japanese enterprises.

**Developed by**: [Geekfeed Inc.](https://www.geekfeed.co.jp)  
**Product site**: [https://www.youwire.jp](https://www.youwire.jp)  
**Support**: support@youwire.jp  
**Documentation**: [https://geekfeedjapan.github.io/youwire-mcp-public-docs](https://geekfeedjapan.github.io/youwire-mcp-public-docs)

---

## What YouWire Captures

YouWire records and transcribes business conversations across every channel:

- **Mobile calls** — All four major Japanese carriers (NTT Docomo, KDDI, SoftBank, Rakuten Mobile)
- **Landline calls** — All SIP-based PBX systems
- **Microsoft Teams Phone** — Compliance recording via YouWire CRBot
- **Web conferencing** — Zoom, Google Meet, and other platforms
- **In-person meetings** — Via mobile recording app

With YouWire MCP, Claude can search, retrieve, and analyze these recordings — enabling compliance review, operator coaching, sales intelligence, and more.

---

## Quick Start

### Requirements

- An active **YouWire subscription** (contact sales@youwire.jp)
- Your organization's MCP server URL: `https://[your-organization].youwire.jp/mcp`

### Connect to Claude

1. Go to [claude.ai/customize/connectors](https://claude.ai/customize/connectors)
2. Click **+ Add custom connector**
3. Enter your YouWire MCP URL
4. Complete the **OAuth 2.1 authentication** with your YouWire credentials
5. Start asking Claude about your call recordings

---

## Available Tools

| Tool | Type | Description |
|---|---|---|
| `searchRecordings` | Read | Search recordings by date, keyword, group, direction |
| `getRecordingDetails` | Read | Full transcript and metadata for a specific recording |
| `getCallStatistics` | Read | Call volume and duration statistics |
| `listTagCategories` | Read | Available compliance tag categories |
| `getUserPermissions` | Read | Your access level and permissions |
| `addTag` | Write | Add a compliance tag to a recording |
| `updateTag` | Write | Update an existing tag |
| `deleteTag` | Write | Remove a tag from a recording |

---

## Example Prompts

```
"Search for incoming calls last week where 'キャンセル' was mentioned."

"Summarize the 5 longest calls from the sales team this month."

"I'm visiting ABC Corp tomorrow — what did we discuss in our last call?"

"Show all calls tagged as TODO older than 7 days."
```

---

## Authentication

YouWire MCP uses **OAuth 2.1 + PKCE** with Dynamic Client Registration (DCR).

| RFC | Description |
|---|---|
| OAuth 2.1 | Authorization Code Flow with PKCE |
| RFC 7636 | PKCE |
| RFC 8414 | Authorization Server Metadata |
| RFC 7591 | Dynamic Client Registration |
| RFC 9728 | Protected Resource Metadata |
| RFC 7009 | Token Revocation |

---

## Documentation

Full documentation is available at:  
👉 **[https://geekfeedjapan.github.io/youwire-mcp-public-docs](https://geekfeedjapan.github.io/youwire-mcp-public-docs)**

---

## License

© 2026 Geekfeed Inc. All rights reserved.
