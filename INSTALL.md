# Instalação rápida

Portal da Transparência: Cadastro de Expulsões da Administração Federal (CEAF) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_portal_transparencia_ceaf`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Portal da Transparência: Cadastro de Expulsões da Administração Federal (CEAF)` / `https://api.mcp.ai/p_portal_transparencia_ceaf`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "portal_transparencia_ceaf": { "type": "http", "url": "https://api.mcp.ai/p_portal_transparencia_ceaf" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=portal_transparencia_ceaf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wb3J0YWxfdHJhbnNwYXJlbmNpYV9jZWFmIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "portal_transparencia_ceaf": { "url": "https://api.mcp.ai/p_portal_transparencia_ceaf" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=portal_transparencia_ceaf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_portal_transparencia_ceaf%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "portal_transparencia_ceaf": { "type": "http", "url": "https://api.mcp.ai/p_portal_transparencia_ceaf" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_portal_transparencia_ceaf
```

Dúvidas? [portal_transparencia_ceaf@mcp.ai](mailto:portal_transparencia_ceaf@mcp.ai)
