# DJEN (Diário de Justiça)

### DJEN (Diário de Justiça) para Claude, ChatGPT e agentes de IA

Diário de Justiça Eletrônico Nacional (CNJ), publicações e intimações judiciais. Busca por OAB, nome de advogado, número de processo, tribunal e data; cada resultado traz o texto completo e o link da certidão. Sem credencial; hospedado pela plataforma. (Diário de Justiça, não é base de jurisprudência/ementas.)

- 📊 **3 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `DJEN (Diário de Justiça)` e **URL** `https://api.mcp.ai/p_djen`.

### Cursor

[➕ Instalar DJEN (Diário de Justiça) no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=djen&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9kamVuIn0=)

### VS Code (Copilot Chat)

[➕ Instalar DJEN (Diário de Justiça) no VS Code](vscode:mcp/install?name=djen&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_djen%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_djen
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Busque publicações da OAB 21076/SP nos últimos 7 dias
Tem intimação para o processo 0208428-37.2007.8.26.0100?
Publicações do TST de hoje sobre determinado advogado
```

---

## 3 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `djen_search_comunicacoes` | Busca publicações/intimações no Diário de Justiça Eletrônico Nacional (DJEN) por OAB, nome de advogado, número de processo, tribunal e data. |
| `djen_processos_por_parte` | DESCOBERTA por NOME de parte (grátis, sem captcha): busca o DJEN por quem figura no processo e agrupa por número — devolve a lista de processos da pessoa/empresa, com partes e tribunal. |
| `djen_get_certidao` | Retorna a URL da certidão (PDF) de uma comunicação do DJEN pelo seu hash (campo `hash` retornado na busca). |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_djen`.


---

## Suporte

- 📧 [djen@mcp.ai](mailto:djen@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/djen-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_djen` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
