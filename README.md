# Roleta — Dia da Virada da Coordenação (Marcelia Fernandes / Midas da Educação)

Página de roleta de prêmios com a identidade visual do site
[midasdaeducacao.com.br/aviradacoordenacao](https://www.midasdaeducacao.com.br/aviradacoordenacao).

Motor da roleta idêntico ao do projeto da Gabriela (`../gabriela-valiosas-experience/`) —
toda a personalização fica no bloco `window.ROLETA_CONFIG` no topo do `index.html`.
Passo a passo de replicação: `../gabriela-valiosas-experience/REPLICAR.md`.

## Identidade extraída do site da cliente

| Item | Valor |
|---|---|
| Dourado | `#FFB600` (texto escuro `#242424` sobre ele) |
| Verde CTA | `#22CB5F`, border-radius 14px |
| Card escuro | `#171717`, borda dourada |
| Fundo | preto |
| Fontes | Roboto (títulos/texto), Open Sans (botões), DM Sans 800 (destaques de preço) |

Material de referência (screenshots, computed styles, assets originais): `reference/`.

## Configuração atual (14/07/2026)

- **Prêmios reais** (checkout Hotmart `Y106465997B`): Ingresso R$ 1 (`off=ydruh3h5`),
  50% de desconto (`off=1u4rmlqj`), 2 por 1 (`off=wvi454o7`). Pesos 20/45/35 —
  o melhor prêmio (R$ 1) cai menos; ajustar no `ROLETA_CONFIG` se a cliente quiser.
- **GTM**: `GTM-KQW3T4J9` (script + noscript). Obs.: o container dispara uma tag
  que procura um campo de formulário do site dela e loga um erro inofensivo no
  console desta página — nada a corrigir aqui.
- **UTMs**: a página repassa `utm_source/medium/campaign/content/term` e `src`
  recebidos do anúncio para o link do checkout (whitelist em `PARAMS_REPASSE`).

## ⚠️ Pendências — confirmar com a cliente

- **FB_PIXEL_ID** vazio — confirmar se a Marcelia usa Meta Pixel além do GTM.
- **Data do evento**: hardcoded "25 de Julho das 09h às 17h" (copiada do site atual).

## Deploy

- Repo: https://github.com/mysterione17/roleta-dia-da-virada (público — fonte é o
  `index.html` legível; o publicado é o `docs/` minificado gerado por `bash build.sh`).
- GitHub Pages servindo `main:/docs`, domínio `roleta.midasdaeducacao.com.br` (docs/CNAME).
- DNS: criar CNAME `roleta` → `mysterione17.github.io` na zona de midasdaeducacao.com.br
  (mesmo padrão de evento.gabrielafachini.com.br). Depois de propagar, ativar
  "Enforce HTTPS" (GitHub emite o certificado sozinho).
- Fluxo de publicação: editar `index.html` → `bash build.sh` → commit + push.
