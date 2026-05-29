# Greenhouse Docs MCP

A Model Context Protocol (MCP) server that makes 2,394 Greenhouse help articles searchable by AI assistants.

## Add to Claude Code

```json
"greenhouse-docs": {
  "type": "http",
  "url": "https://greenhouse-docs-mcp.netlify.app/mcp"
}
```

## Tools

- `search_greenhouse_docs` — keyword search across all articles
- `get_greenhouse_doc` — fetch a full article by slug
- `list_greenhouse_docs` — list all available articles

## Refresh the docs

```bash
python3.11 fetch.py           # re-fetch from Zendesk API
python3.11 build_docs.py      # rebuild docs.json
git add netlify/functions/docs.json && git commit -m "refresh docs"
git push
```
