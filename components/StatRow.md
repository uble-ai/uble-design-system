Fileira de números-chave em cards, em bento: o primeiro número ocupa duas colunas, só um deles é Flamingo.

## Quando usar
Logo após o `lede` de uma seção de site, no slide de tração do deck, no topo de um relatório. Três a cinco números; mais que isso vira tabela.

## Anatomia
- Grid de 5 colunas iguais, gap `space-4`, margem superior `space-14`. O primeiro card tem `grid-column: span 2`.
- Cada card é um **Card** com padding `22px 24px`.
- Número em `num-xl` (clamp 28 a 40px), `text`; `flamingo-text` apenas no número principal (o que a UBLE recuperou ou o que o título afirma).
- Rótulo em `body-s`, `text-soft`, 8px abaixo; negrito em `text` para a palavra-chave.
- Fonte do dado em `caption` abaixo da fileira, obrigatória.
- Abaixo de 980px: uma coluna, o span some.

## O consumidor fornece
De 3 a 5 pares número + rótulo, qual é o principal, e a fonte.

## Faça / não faça
- Faça: formato brasileiro (R$ 2,4M; 9,94%); rótulo que diga o que o número é e o período.
- Não faça: dois Flamingos; número sem rótulo; número sem fonte; ícone ao lado do número; contador animado.
