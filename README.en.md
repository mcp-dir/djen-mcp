# DJEN (Diário de Justiça)

### DJEN (Diário de Justiça) for Claude, ChatGPT and AI agents

Brazil's National Electronic Court Gazette (CNJ/DJEN), judicial publications and notifications. Search by bar number (OAB), lawyer name, case number, court and date; each result includes the full text and certificate link. No credentials; hosted by the platform. (It is the court gazette, not a case-law database.)

- 📊 **3 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `DJEN (Diário de Justiça)`, URL `https://api.mcp.ai/p_djen`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=djen&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9kamVuIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=djen&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_djen%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_djen
```

---

## 3 tools

| Tool | Description |
|---|---|
| `djen_search_comunicacoes` | Busca publicações/intimações no Diário de Justiça Eletrônico Nacional (DJEN) por OAB, nome de advogado, número de processo, tribunal e data. |
| `djen_processos_por_parte` | DESCOBERTA por NOME de parte (grátis, sem captcha): busca o DJEN por quem figura no processo e agrupa por número — devolve a lista de processos da pessoa/empresa, com partes e tribunal. |
| `djen_get_certidao` | Retorna a URL da certidão (PDF) de uma comunicação do DJEN pelo seu hash (campo `hash` retornado na busca). |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_djen` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
