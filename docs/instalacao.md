# Instalação detalhada

IBAMA: Certificado de Regularidade é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_ibama_certificado_regularidade`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_ibama_certificado_regularidade` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_ibama_certificado_regularidade` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_ibama_certificado_regularidade` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.ibama_certificado_regularidade` (ou `servers.ibama_certificado_regularidade` no VS Code) do config do cliente e reinicie.
