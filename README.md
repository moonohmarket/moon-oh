# Moonoh NYC & NJ Marketplace — Remote MCP Server

Official Model Context Protocol (MCP) server for **[Moonoh](https://moon-oh.com)** — search **39,762+ verified secondhand listings, curated NYC independent boutique items, and regional market price reports** across New York City (Manhattan, Brooklyn, Queens, The Bronx, Staten Island) and Northern New Jersey (Bergen & Hudson Counties).

## Endpoint & Transport

- **Remote MCP URL**: `https://moon-oh.com/api/mcp`
- **Transport**: Streamable HTTP (`POST` JSON-RPC 2.0, `GET` health/discovery)
- **Authentication**: None required (public read-only tools)
- **Website**: [https://moon-oh.com](https://moon-oh.com)

---

## Available Tools (Read-Only)

| Tool | Title | Description |
| :--- | :--- | :--- |
| `search_marketplace` | Search NYC & NJ Marketplace and Local Shops | Search 39,762 items (24,385 marketplace listings + 14,718 local shop items) by keyword, borough/neighborhood, or category. |
| `get_item_details` | Get Marketplace Item Details | Retrieve full structured item details (photos, price, condition, seller, neighborhood, and similar listings) by ID or Moonoh URL. |
| `get_price_report` | Get NYC & NJ Local Market Price Report | Get asking-price medians, IQR ranges, and category breakdowns across NYC boroughs and Northern NJ. |

---

## Quick Setup

### Cursor / Claude Desktop / Cline (`mcp.json`)

```json
{
  "mcpServers": {
    "moonoh-marketplace": {
      "type": "streamable-http",
      "url": "https://moon-oh.com/api/mcp"
    }
  }
}
```

### Example Prompts
- *"Search for secondhand dining tables in Manhattan under $150 on Moonoh."*
- *"What is the median asking price for furniture in Brooklyn and Queens?"*
- *"Get full details for Moonoh item `heykorean-674246`."*

---

## Support & Policies
- **Support**: [https://moon-oh.com/contact](https://moon-oh.com/contact)
- **Privacy Policy**: [https://moon-oh.com/privacy](https://moon-oh.com/privacy)
- **Terms of Service**: [https://moon-oh.com/terms](https://moon-oh.com/terms)
- **MCP Server Card**: [https://moon-oh.com/.well-known/mcp/server-card.json](https://moon-oh.com/.well-known/mcp/server-card.json)
