# YoushowPTE MCP Server

Read-only MCP server for PTE Academic question types, public sample questions, test format and Australian score requirements. No API key required.

Hosted, read-only and public: no API key, no account, no install step.

| | |
| --- | --- |
| **Endpoint** | `https://pte.youshowedu.com/api/mcp` |
| **Transport** | streamable-http (POST, JSON-RPC 2.0, stateless, anonymous, CORS enabled) |
| **Authentication** | none |
| **Server card** | https://pte.youshowedu.com/.well-known/mcp/server-card.json |
| **Product** | https://pte.youshowedu.com |
| **MCP guide** | https://pte.youshowedu.com/mcp |

## Tools

| Tool | Description |
| --- | --- |
| `list_question_types` | List all 22 PTE Academic question types by skill, with bank size and a public practice page. |
| `search_questions` | Find public PTE sample questions by question type, skill, difficulty, prediction status or keyword. |
| `get_test_format` | Get the three-part PTE Academic test structure with official duration ranges and question types. |
| `get_score_requirements` | Look up Australian Competent, Proficient and Superior English thresholds plus Temporary Graduate visa 485 minimums. |

## Connect a client

### Claude Code

```bash
claude mcp add --transport http youshow-pte https://pte.youshowedu.com/api/mcp
```

### Cursor, VS Code, Windsurf or any other MCP client

Add a remote MCP server with the endpoint URL:

```
https://pte.youshowedu.com/api/mcp
```

### Verify the endpoint by hand

```bash
curl -X POST https://pte.youshowedu.com/api/mcp \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

## About

This repository holds the published metadata for the hosted MCP server behind
https://pte.youshowedu.com. The server itself is deployed and operated by the product team;
this repository exists so that MCP directories and registries can link to a
public source of truth.

- Product: https://pte.youshowedu.com
- MCP guide: https://pte.youshowedu.com/mcp
- Contact: official@youshowedu.com

## License

MIT
