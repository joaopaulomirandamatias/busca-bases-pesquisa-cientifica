# Busca em bases científicas: passo a passo (MirandasTech)

Manual em formato de slides (53) para buscar literatura científica na pós-graduação: por que mais de uma base, da pergunta aos conceitos e termos (método de Bramer), sintaxe que muda de base para base, o que registrar (PRISMA-S, PRESS, diário `BUSCA.md`), qual base para quê; as bases abertas uma a uma com passo a passo, filtros, exportação e limites (Portal de Periódicos da CAPES sem login e o caminho do CAFe, Google Acadêmico, IEEE Xplore, Semantic Scholar, PubMed e LILACS/BVS, arXiv, SciELO, BDTD/oasisbr/Catálogo de Teses, BASE, DOAJ e CORE, Unpaywall, Crossref) e as bases por assinatura (Scopus, Web of Science, ScienceDirect) e de descoberta por grafo (Dimensions, Lens, Connected Papers, ResearchRabbit); busca reprodutível por API com o OpenAlex (`buscar_openalex.py`), a mesma pergunta em seis APIs (`contar_bases.py`), verificação de acesso aberto pelo Unpaywall (`verificar_oa.py`); exportar para o Zotero, obter o PDF, snowballing, alertas, avaliar o periódico (Qualis na Sucupira, SJR, DOAJ, Think. Check. Submit., retratações), registrar no diário; erros comuns, checklist, glossário com popovers e referências. Capturas reais e datadas (09/09/2026) de todas as bases, sem login, e saídas reais dos scripts.

**Manual on-line:** https://busca.mirandastech.com.br/ · **PDF:** https://busca.mirandastech.com.br/manual.pdf

Manuais irmãos: **Revisão sistemática com PRISMA 2020** — https://prisma.mirandastech.com.br/ · **Zotero** — https://zotero.mirandastech.com.br/ · **Metodologia** — https://metodologia.mirandastech.com.br/ · **Gemini Notebook** — https://notebook.mirandastech.com.br/ · **Uso de IA na pesquisa** — https://manual.mirandastech.com.br/ · **Plugin Pesquisa (Claude e Codex)** — https://plugin.mirandastech.com.br/ · Hub: https://www.mirandastech.com.br/pesquisa

| Pasta | O que há |
|---|---|
| `manual/` | deck HTML autônomo, PDF, fonte do artefato e `fatos_verificados.md` (todas as fontes e chamadas de API conferidas em 09/09/2026) |
| `site/` | o que o servidor serve (`index.html`, `manual.pdf`) |
| `capturas/` | 35 capturas reais, 09/09/2026 (30 telas de bases e portais, 5 figuras de terminal com saídas reais) |
| `scripts/buscar_openalex.py` | busca reprodutível no OpenAlex com cursor; grava CSV, RIS (Zotero) e diário JSON |
| `scripts/contar_bases.py` | a mesma pergunta em OpenAlex, Crossref, PubMed, arXiv, DOAJ e Semantic Scholar |
| `scripts/verificar_oa.py` | acrescenta `is_oa`, `oa_status` e `pdf_url` (Unpaywall) a um CSV de DOIs |
| `scripts/gerar_deck.py` | regenera HTML e PDF a partir do fonte |
| `modelos/BUSCA.md` | diário de busca no padrão PRISMA-S |
| `skills/busca-bases-abertas/` | skill do agente (cópia sincronizada do plugin Pesquisa MirandasTech) |
| `Dockerfile` · `Caddyfile` · `railway.json` | deploy estático (Caddy) |
| `.github/workflows/verificar.yml` | CI: integridade do deck e capturas referenciadas |

## Os manuais juntos
Este manual cobre a **busca**: da pergunta ao diário. O que sai daqui entra no Zotero (`zotero-pesquisa-cientifica`) e segue para a triagem, o fluxograma e o relato do manual de revisão sistemática (`revisao-sistematica-pesquisa-cientifica`). No plugin **Pesquisa MirandasTech** (`pesquisa-mirandastech`), a skill `busca-bases-abertas` conduz a fase 4 «Busca e biblioteca» com os três scripts e o diário; ela nunca faz login em proxy ou CAFe e nunca registra uma busca que não foi executada.

## Como citar
MATIAS, J. P. M. *Busca em bases científicas: passo a passo.* MirandasTech, v1.0, set. 2026. CC BY 4.0.

## Declaração de uso de IA
Escrito com assistência de IA (Claude, Anthropic) na estruturação, redação, automação das capturas e execução dos scripts. Coberturas, limites de API, nomes de botões, planos e preços e referências conferidos nas fontes oficiais e em chamadas reais às APIs em 09/09/2026 (lista em `manual/fatos_verificados.md`); nenhuma busca foi feita com login. O autor responde integralmente pelo conteúdo. CAPES, Google, IEEE, Elsevier, Clarivate, OpenAlex, Crossref, Unpaywall, SciELO, IBICT e os demais serviços citados são marcas e projetos de terceiros; este manual não tem vínculo com eles.
