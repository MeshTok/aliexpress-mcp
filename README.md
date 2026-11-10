# aliexpress-mcp

> **AliExpress MCP server & REST gateway — give any AI agent shopping capability.** Free hosted, no signup, registered in the official MCP Registry.

Search 7,000+ live AliExpress products, compare prices, get attributed affiliate buy links — via MCP (Streamable HTTP) or plain REST. Hosted for you: nothing to deploy, nothing to maintain.

## Quick start (MCP client)

```json
{
  "mcpServers": {
    "baydeep": { "url": "https://mcp.baydeep.com/mcp" }
  }
}
```

Works in Claude, Cursor, Cline, and any MCP-capable client. 4 tools are keyless and work immediately.

## Quick start (REST / curl)

```bash
# keyless shelf search — no signup
curl "https://api.baydeep.com/v1/shelf?q=air%20fryer&page_size=5"

# mint a free API key (unlocks live search + attributed links) — never expires
curl -X POST https://api.baydeep.com/v1/trial -H "Content-Type: application/json" -d '{}'
```

## Tools

| Tool | Key | Purpose |
|---|---|---|
| `catalog_overview` | keyless | Catalog contents, counts, how-to |
| `shelf_search` | keyless | Search stocked products + fares |
| `shelf_item` | keyless | Item detail by goods_id |
| `flight_search` | keyless | Flight fares by IATA city/date (Aviasales) |
| `search_products` | key | Live AliExpress search (target currency) |
| `hot_products` | key | Live trending products |
| `product_detail` | key | Detail for up to 10 ids |
| `convert_link` | key | Attribute any aliexpress URL to your account |
| `affiliate_orders` | key | Your attributed orders + tracking fields |
| `categories` | key | AliExpress category tree |
| `mint_free_key` | — | Self-serve key minting |

## What your agent gets

- **Product search** across a live, daily-refreshed catalog (7,000+ SKUs, 155 category pages)
- **Price comparison** — sort by price / sales / latest, price filters
- **Flight deals** — 190 fares across 40 routes, filterable by city and date
- **Attributed buy links** — `convert_link` turns any aliexpress.com URL into a tracked affiliate link
- **Order tracking** — `affiliate_orders` returns purchases driven by your agent

## Links

- Documentation: https://baydeep.com/docs/
- Developer console (free key): https://baydeep.com/console/
- Consumer storefront: https://leapbest.com
- Source: https://github.com/MeshTok/baydeep
- Official MCP Registry: `io.github.MeshTok/baydeep`

## Related

- [awesome-shopping-agents](https://github.com/MeshTok/awesome-shopping-agents) — curated list of open-source shopping agents
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — general MCP server directory
