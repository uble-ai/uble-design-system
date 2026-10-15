Pílula em IBM Plex Mono que abre toda seção, slide ou capítulo: número em `flamingo-text`, rótulo em `text-soft`.

## Quando usar
Acima de todo `display-l` ou `display-m`: seção de site, slide de deck, capítulo de proposta. É o primeiro elemento do esqueleto `eyebrow → display → dek → lede → blocos`.

## Anatomia
- Container: `padding 6px 12px`, borda 1px `line`, raio `radius-pill`, fundo `glass-card` (ou `surface` em mídia estática).
- Número ou data: `eyebrow`, cor `flamingo-text`, peso 500.
- Rótulo: `eyebrow`, cor `text-soft`, caixa alta com espaçamento 0,14em.
- Gap de 10px entre número e rótulo.

## O consumidor fornece
O número (`01`, `2.3`, `Out/26`) e o rótulo (até 4 palavras). O número é opcional (apêndices e capas).

## Faça / não faça
- Faça: um eyebrow por seção, sempre à esquerda, 22px acima do título.
- Não faça: eyebrow sem título abaixo; dois eyebrows na mesma tela; eyebrow em cor sólida Flamingo; rótulo com mais de 4 palavras.
