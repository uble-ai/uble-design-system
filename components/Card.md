Superfície padrão de conteúdo: vidro (`glass-card` + `blur-glass`) com borda de 1px em gradiente Flamingo → linha → Shark. Em mídia estática, `surface` sólido com borda `line-strong`.

## Quando usar
Qualquer bloco de conteúdo agrupado: documento, stat, tabela, gráfico, item de bento. Em grids de 2, 3 ou 4 colunas com gap `space-4`; cards da mesma linha esticam à mesma altura.

## Anatomia
- Padding `space-7` (26 a 28px), raio `radius-2xl`, `overflow: hidden`, `isolation: isolate`.
- Fundo `glass-card`; `backdrop-filter: blur(var(--blur-glass))`.
- Borda: pseudo-elemento `::before` com `padding: 1px`, gradiente a 140° de Flamingo a 55% → `line` (8% claro) aos 40% → Shark a 35%, máscara `content-box` com `mask-composite: exclude`.
- Conteúdo interno: eyebrow ou `label` → `heading` → `body-s` em `text-soft` → ação em `label` `shark-text` ou botão.
- Variante `.static`: fundo `surface`, borda `line-strong`, sem `::before`. Use em deck, proposta, e-mail, imagem.
- Hover (quando clicável): `translateY(-2px)` em 250ms. Nada de sombra.

## O consumidor fornece
O conteúdo e, para grids, o número de colunas. O card não tem título obrigatório.

## Faça / não faça
- Faça: mantenha um card por ideia; em stat rows, o primeiro ocupa duas colunas.
- Não faça: card dentro de card (o interno vira transparente); borda esquerda colorida; sombra pesada; fundo Flamingo; card com mais de uma ação primária.
