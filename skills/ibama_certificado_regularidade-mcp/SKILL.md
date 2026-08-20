---
name: ibama_certificado_regularidade-mcp
description: Skill da REST API do IBAMA: Certificado de Regularidade na MCP.AI: 1 endpoint em /api/ibama_certificado_regularidade. IBAMA: Certificado de Regularidade, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# IBAMA: Certificado de Regularidade — REST API skill

Você tem acesso à **IBAMA: Certificado de Regularidade** REST API na MCP.AI.

> IBAMA: Certificado de Regularidade, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/ibama_certificado_regularidade
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/ibama_certificado_regularidade/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/ibama_certificado_regularidade/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `ibama_certificado_regularidade_consultar`

IBAMA: Certificado de Regularidade, consulta em fonte oficial. _(POST /api/ibama_certificado_regularidade/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_ibama_certificado_regularidade` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
