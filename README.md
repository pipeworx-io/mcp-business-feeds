# mcp-business-feeds

Business Feeds MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 932+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `list_feeds` | List the curated business & industry feeds (id, title, category, source). Optionally filter by category (business, economics, marketing, real-estate) or keyword. Pass an id to read_feed. |
| `read_feed` | Read a curated business & industry feed by its id (from list_feeds). Returns normalized items (title, link, published, summary). Optionally filter items by keyword. |
| `fetch_feed` | Fetch and normalize any RSS / Atom / RDF feed by URL. CF-robust: fetches directly and falls back to a proxy if the source blocks the gateway. Use list_feeds first for curated sources. |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "business-feeds": {
      "url": "https://gateway.pipeworx.io/business-feeds/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 932+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Business Feeds data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [All tools and guides](https://github.com/pipeworx-io/examples)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
