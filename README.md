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

## ⚠️ Pendências — confirmar com a cliente

- **Prêmios**: os 4 atuais são placeholders plausíveis (ingresso R$14, kit grátis,
  50% off, ingresso+kit). Trocar labels, pesos e links no `ROLETA_CONFIG`.
- **WhatsApp**: os links usam `wa.me/5500000000000` (placeholder). Trocar pelo número real.
- **Tracking**: `FB_PIXEL_ID` e `GA4_ID` vazios — pedir os IDs da Marcelia.
- **Data do evento**: hardcoded "25 de Julho das 09h às 17h" (copiada do site atual).
- **Deploy**: sem repositório remoto/domínio definidos ainda.
