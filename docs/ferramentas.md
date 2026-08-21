# Ferramentas

DJEN (Diário de Justiça) expõe 3 ferramentas (todas somente leitura).

### 1. `djen_search_comunicacoes`
**Input**: `numero_oab` (opcional), `uf_oab` (opcional), `nome_advogado` (opcional), `nome_parte` (opcional), `numero_processo` (opcional), `sigla_tribunal` (opcional), `data_inicio` (opcional), `data_fim` (opcional), `meio` (opcional), `texto` (opcional), `pagina` (opcional), `itens_por_pagina` (opcional)

Busca publicações/intimações no Diário de Justiça Eletrônico Nacional (DJEN) por OAB, nome de advogado, número de processo, tribunal e data.

### 2. `djen_processos_por_parte`
**Input**: `nome_parte`, `sigla_tribunal` (opcional), `data_inicio` (opcional), `data_fim` (opcional), `itens_por_pagina` (opcional), `pagina` (opcional)

DESCOBERTA por NOME de parte (grátis, sem captcha): busca o DJEN por quem figura no processo e agrupa por número — devolve a lista de processos da pessoa/empresa, com partes e tribunal.

### 3. `djen_get_certidao`
**Input**: `hash`

Retorna a URL da certidão (PDF) de uma comunicação do DJEN pelo seu hash (campo `hash` retornado na busca).

## Prompts de exemplo

```
Busque publicações da OAB 21076/SP nos últimos 7 dias
Tem intimação para o processo 0208428-37.2007.8.26.0100?
Publicações do TST de hoje sobre determinado advogado
```
