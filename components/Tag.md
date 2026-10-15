Rótulo pequeno em mono caixa alta: tag informa (tipo, série, rótulo de projeção), chip filtra (estado ativo em `flamingo-tint`) e status mostra "online" com um ponto `success`.

## Quando usar
- Tag: tipo de documento, nome de série de gráfico (`flam` para recuperado, `shark` para perdido), rótulo "projetado".
- Chip: filtros de período, segmento, plataforma. Sempre em grupo, um ativo.
- Status: presença ou saúde ("Online agora", "Dados de hoje").

## Anatomia
- Tag: `padding 3px 9px`, borda `line`, raio `radius-pill`, estilo `label` com espaçamento 0,08em, `text-soft`. Variantes `flam` (`flamingo-text`, borda Flamingo a 40%) e `shark` (`shark-text`).
- Chip: `padding 6px 14px`, mesmo estilo; ativo = borda `flamingo`, fundo `flamingo-tint`, texto `text`; hover = borda Flamingo a 50%.
- Status: ponto 6px `success` com `box-shadow 0 0 10px` e texto `body-s` em `text-soft`. O texto é obrigatório (cor sozinha não comunica).

## O consumidor fornece
Texto curto (1 a 3 palavras), variante, e para chip o estado `aria-pressed`.

## Faça / não faça
- Faça: tag `flam` e `shark` com o mesmo significado dos gráficos.
- Não faça: tag preenchida de cor; tag verde ou vermelha para dinheiro; chip sem estado ativo visível; status sem texto.
