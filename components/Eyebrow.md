Pílula em IBM Plex Mono que abre seção de deck, dataroom e capítulo de proposta: número em `flamingo-text`, rótulo em `text-soft`. Em site e landing page é opcional e nunca leva número.

## Quando usar
- **Deck, dataroom, proposta, relatório:** acima de todo `display-l` ou `display-m`, numerado. Esses materiais são lidos em ordem, e o número diz onde o leitor está. É o primeiro elemento do esqueleto `eyebrow → display → dek → lede → blocos`.
- **Site e landing page:** opcional e sem número. Quem visita um site rola e pula, não lê em sequência, e uma seção numerada com rótulo faz a página parecer uma apresentação. Use no máximo um por página, no topo, para dizer o que a página é ("Cases", "Calculadora"), ou acima de um CTA. As seções abrem direto no título.

## Anatomia
- Container: `padding 6px 12px`, borda 1px `line`, raio `radius-pill`, fundo `glass-card` (ou `surface` em mídia estática).
- Número ou data: `eyebrow`, cor `flamingo-text`, peso 500.
- Rótulo: `eyebrow`, cor `text-soft`, caixa alta com espaçamento 0,14em.
- Gap de 10px entre número e rótulo.

## O consumidor fornece
O número (`01`, `2.3`, `Out/26`) e o rótulo (até 4 palavras). O número é opcional em apêndices e capas, e proibido em site e landing page.

## Faça / não faça
- Faça: em deck e documento, um eyebrow por seção, sempre à esquerda, 22px acima do título. Em site, um por página, no topo.
- Não faça: eyebrow sem título abaixo; dois eyebrows na mesma tela; eyebrow em cor sólida Flamingo; rótulo com mais de 4 palavras; eyebrow numerado em seção de site.
