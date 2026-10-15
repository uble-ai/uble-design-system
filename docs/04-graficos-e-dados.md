# Gráficos e dados

Um gráfico da UBLE deve ser lido em três segundos: onde estava a perda, onde a UBLE entrou, quanto voltou. A cor faz esse trabalho sozinha, por isso a semântica é fixa.

## Semântica de cor (inegociável)

| Token | Significa | Exemplos |
|---|---|---|
| `flamingo` | o que a UBLE recuperou | série "recuperado", barra de uplift, linha de receita recuperada, total do ledger |
| `shark` | a perda, e tudo que não é UBLE | série "perdido", "recusado", concorrente, mercado, baseline sem UBLE |
| `text-soft` | contexto principal | faturamento total, volume de pedidos |
| `text-muted` | contexto secundário, eixos, legendas, linhas de referência | média do segmento, meta |
| `success` | nunca em gráfico financeiro | só o ponto "online" e indicadores de status |
| `danger` | nunca em gráfico financeiro | só erro de formulário |

Quando houver mais de duas séries de dado, a terceira vai em `text-soft` e a quarta em `text-muted`. Nunca uma quinta: divida o gráfico. Hachura em 45° (`repeating-linear-gradient` de `text-soft` a 22%) marca projeção ou dado parcial, com legenda "projetado".

## Anatomia

- Título do gráfico em `heading`; a conclusão no título, não a descrição ("Recuperação cresce 2,3x após o 3º mês", não "Recuperação por mês").
- Eixos e legendas em `label` (`text-muted`, caixa alta, espaçamento 0,12em). Valores em `data`, com `tabular-nums`.
- Grade do gráfico em `line`, só horizontal, nunca vertical. Sem borda em volta da área de plotagem.
- Barras com raio `radius-xs` no topo; linhas de 2px; pontos de 6px só no último valor ou no valor em destaque.
- Um único destaque por gráfico: o valor que a frase do título afirma, em `flamingo` com rótulo direto no dado. O resto fica em `shark` e cinzas.
- Fonte do dado em `caption` logo abaixo, sempre ("Fonte: dados proprios UBLE, jan-set 2026, 13 clientes").

## Formas

- **Comparação antes/depois**: duas barras lado a lado, `shark` antes e `flamingo` depois. É o gráfico mais usado da UBLE; não o reinvente.
- **Série temporal**: linha, `flamingo` para recuperado e `shark` para perdido, mesma escala, mesmo eixo. Área preenchida só sob a linha Flamingo, a 14% (`flamingo-tint`).
- **Composição**: barras empilhadas horizontais, nunca pizza. Pizza é proibida.
- **Funil de pagamento**: a trilha (checkout → gateway → adquirente → emissor → recusa → UBLE → pago), em linha, não em funil de marketing.
- **Tabela**: cabeçalho em `label`, números alinhados à direita em `data`, linha de total em `flamingo-text` sem borda inferior. Veja os componentes **Ledger** e **Table**.

## Stat e bento

Um número-chave por card: valor em `num-xl`, rótulo em `body-s` `text-soft`. O número em `text`; em `flamingo` só quando for o que a UBLE recuperou ou o resultado que o título da seção afirma. Em uma fileira de stats, no máximo um Flamingo. O primeiro card ocupa duas colunas (bento) quando é o número principal.

## O que evitar

Gradientes em barras, sombra em gráfico, 3D, rótulo de dado em todos os pontos, eixo Y que não começa em zero numa barra, cor por categoria sem significado, legenda à direita (use abaixo), gráfico sem fonte.
