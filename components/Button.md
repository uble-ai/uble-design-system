Três níveis de ação: primário (`text` sobre `bg`, pílula), secundário (borda `line-strong`) e ghost (só texto). Flamingo não é cor de botão.

## Quando usar
- Primário: a única ação principal da tela ("Falar com o Diego", "Entrar no data room"). Um por tela.
- Secundário: ação alternativa ("Ver documentos", "Baixar PDF").
- Ghost: navegação e utilidades (menu, fechar, filtro).
- Link inline (`flamingo-text`, sublinhado a 50%): fonte, referência, "saiba mais" dentro de texto.

## Anatomia
- Padding `9px 16px`, raio `radius-pill`, estilo `button` (14px/600 Archivo), gap 8px.
- Primário: fundo `text`, texto `bg`. Hover: `translateY(-1px)` em 200ms e `glow-flamingo` em 300ms.
- Ponto de status opcional no primário: 7px `success` com halo de 3px a 20%. Significa "alguém online"; não use como enfeite.
- Secundário: fundo transparente, borda `line-strong`, texto `text-soft`; hover `text` e borda `text-muted`.
- Ghost: texto `text-soft`, hover fundo `hover-tint`.
- Desabilitado: `opacity-disabled`.
- Altura mínima de 44px em telas de toque.

## O consumidor fornece
Rótulo (verbo + objeto, até 4 palavras, caixa normal), destino, e se há ponto de status.

## Faça / não faça
- Faça: um primário por tela; rótulo com verbo ("Ver", "Falar", "Baixar").
- Não faça: botão Flamingo chapado; botões em várias cores; rótulo em caixa alta; ícone de seta decorativa; dois primários lado a lado.
