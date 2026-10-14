<div align="center">

# MeshArc

**A web crawler and scraping API that records what changed between crawls.**

Turn any site into clean markdown, crawl it on a schedule, and get the pages that were added, changed or removed — in your database, your vector store, or your AI assistant.

[Website](https://mesharc.dev) · [Docs](https://mesharc.dev/docs) · [MCP server](https://mesharc.dev/mcp) · [Pricing](https://mesharc.dev/pricing) · [Start free](https://mesharc.dev/signup)

</div>

---

### What it does

- **Scrape** a page to markdown, text, HTML, links, structured fields or a screenshot.
- **Crawl** a whole site, or **map** what its sitemaps declare before fetching anything.
- **Search** the web and read each result's page in the same call.
- **Watch** a site over time: scheduled runs and a change record — pages added, removed and modified, field by field.
- **Deliver** to webhooks, Slack and other chat apps, or straight into 18 destinations: Postgres, BigQuery, Snowflake, S3, Pinecone, Qdrant and more.

You pay only for pages that were read: blocked pages, 404s and unchanged pages cost nothing.

### Use it from your AI assistant

The hosted MCP server needs no API key — you sign in and approve once.

```bash
claude mcp add --transport http mesharc https://mcp.mesharc.dev/mcp
```

Works with Claude Code, Claude Desktop, Cursor, Windsurf and any client that speaks MCP over HTTP. [Setup for each client →](https://mesharc.dev/mcp)

### Use it from code

```bash
pip install mesharc      # Python 3.10+
npm install mesharc      # Node 20+
```

```python
from mesharc import MeshArc

arc = MeshArc()  # reads MESHARC_API_KEY
page = arc.scrape("https://example.com/pricing")
print(page["markdown"])
```

### Repositories

| Repository | What it is |
|---|---|
| [mesharc-python](https://github.com/mesharc-org/mesharc-python) | Python client for the MeshArc API, with the MCP server |
| [mesharc-node](https://github.com/mesharc-org/mesharc-node) | Node client for the MeshArc API, with TypeScript types |
| [mesharc-mcp](https://github.com/mesharc-org/mesharc-mcp) | The MCP server, packaged for directories and self-run setups |

All open-source code here is MIT-licensed.

### Get in touch

Questions and feature requests: open an issue on the relevant repository, or write to [hello@mesharc.dev](mailto:hello@mesharc.dev). Security reports: [security@mesharc.dev](mailto:security@mesharc.dev) — see [mesharc.dev/legal/security](https://mesharc.dev/legal/security).
