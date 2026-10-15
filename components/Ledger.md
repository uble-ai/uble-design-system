Tabela de valores em IBM Plex Mono com `tabular-nums`, cabeçalho em `label`, perdido em `shark-text`, linha de total em `flamingo-text` sem borda.

## Quando usar
Qualquer tabela em que a coluna principal é dinheiro ou percentual: fechamento mensal, proposta de preço, unit economics, tabela de mercado. Para listas com texto longo, use **Table**.

## Anatomia
- Fonte `data` (13,5px), `tabular-nums`, `border-collapse: collapse`.
- Cabeçalho: `label` em `text-muted`, alinhado à direita (primeira coluna à esquerda), `padding 10px 8px`, borda inferior `line`.
- Célula: `padding 12px 8px`, borda inferior `line`, `text-soft`, alinhada à direita; primeira coluna à esquerda.
- Coluna "perdido" ou "sem UBLE" em `shark-text`. Coluna "recuperado" em `text` (ou `flamingo-text` quando for a conclusão).
- Linha de total: `flamingo-text`, peso 500, sem borda inferior, `padding-top 16px`.
- Linha projetada: sufixo " · projetado" em `label` `text-muted` na primeira célula.
- Dentro de um **Card** com padding reduzido (20 a 24px); em telas estreitas o card rola horizontalmente.

## O consumidor fornece
Colunas, linhas, qual coluna é perda, qual linha é total, quais são projeção.

## Faça / não faça
- Faça: formato brasileiro, vírgula alinhada pela fonte mono, no máximo 5 colunas.
- Não faça: zebra; borda vertical; vermelho para perda; verde para recuperado; total em negrito 700; célula centralizada.
