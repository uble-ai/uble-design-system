Índice lateral retrátil de leitura sequencial: 60px colapsado (só números), 272px expandido, com progresso em Flamingo e grupos em Shark.

## Quando usar
Narrativas longas lidas em ordem: dataroom, documentação, relatório web com muitas seções, painel com várias visões. Não em landing page nem em site de poucas páginas. Oculto abaixo de 1000px (vira menu em folha).

## Anatomia
- `position: fixed`, 16px da esquerda, 92px do topo, 20px do fundo; raio `radius-xl`; fundo `glass-panel` com `blur-glass` e `saturate(140%)`; borda `line`; `shadow-dock`.
- Topo: botão de fixar (32px, raio `radius-sm`, chevron que gira 180°) e contador "07 / 27 seções" em `label` (visível só expandido). Barra de progresso de 2px em `flamingo` sempre visível.
- Item: 30px de altura; número em `label` centrado em 58px; título em `body-s` que aparece com fade e `translateX(-6px → 0)` ao expandir.
- Estados: não visitado `text-dim`; visitado `text-muted`; atual `text` com número em `flamingo-text`, barra esquerda de 3px `flamingo` com `box-shadow 0 0 12px`. Hover `hover-tint`.
- Grupo: `label` 10px em `shark-text`; colapsado vira um traço de 20px em Shark a 40%.
- Largura transita em `duration-dock` com `ease-uble`. Fixado persiste em `localStorage`.

## O consumidor fornece
Lista de grupos e seções (número, título, URL), seção atual, seções visitadas.

## Faça / não faça
- Faça: um item é um link real, com nome acessível mesmo colapsado.
- Não faça: ícones por seção; dock em páginas curtas; dock e menu superior mostrando as mesmas coisas de forma diferente (o dock é sequencial, o menu é por grupo).
