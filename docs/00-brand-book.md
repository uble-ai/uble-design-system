> **UBLE recupera a receita que o checkout perdeu.** Tudo o que a UBLE publica, de site a memo, parte deste sistema. Leia esta página inteira antes de criar qualquer material; depois use as seções (Tom de voz, Logo, Movimento, Gráficos, Aplicações, Antipadrões) conforme o caso.

## Princípios

**01 · Luz, não tinta.** Flamingo (`flamingo`) é uma fonte de luz sobre um fundo escuro, nunca uma lata de tinta. Um destaque por tela: o número que importa, o estado ativo, o ponto onde a UBLE entra. Se há dois laranjas competindo, um deles está errado.

**02 · Dado como voz.** A UBLE vende confiança em números. Todo número vive em IBM Plex Mono (`num-xl`, `num-l`, `data`), com `tabular-nums`, alinhado à direita em tabelas. Tipografia de dado é o sotaque da marca.

**03 · Profundidade por luz, não por sombra.** Superfícies se separam por transparência, borda de 1px e desfoque (`glass-card`, `line`, `blur-glass`), não por sombras pesadas. Sombra existe em três lugares (`shadow-panel`, `shadow-dock`, `glow-flamingo`) e em mais nenhum.

**04 · A cor conta a história do produto.** Em qualquer gráfico, `flamingo` é o que a UBLE recuperou, `shark` é a perda e o que não é UBLE, `success` é só status. Essa regra nunca é quebrada, porque é a tese da empresa desenhada.

**05 · Palco e documento.** O tema escuro (`dark`) é o palco: site, dataroom, decks projetados, capas, social. O tema claro (`light`) é o documento: proposta, relatório, memo, e-mail, impressão. Mesmos tokens, valores diferentes. Nunca misture os dois numa mesma peça, exceto capa escura em documento claro.

## Linguagem visual

A identidade não vem de cor vibrante em volume; vem do equilíbrio entre três coisas, nesta proporção aproximada de área:

| Parte | Tema escuro | Tema claro | Função |
|---|---|---|---|
| **Fundo** (≈70%) | `bg` #07090C e `surface` #151A21 | `bg` #EFEEEB e `surface` #F7F6F3 | Calma, espaço, foco. Nunca preto puro, nunca branco puro. |
| **Texto e linha** (≈25%) | `text` #EFEEEB, `text-soft`, `text-muted`, `line` | `text` #10161F, `text-soft`, `text-muted`, `line` | Hierarquia por escala e peso, não por cor. |
| **Flamingo** (≈5%) | `flamingo` #FD542D | `flamingo` em blocos; `flamingo-text` #B83516 em texto | O único acento. Marca o que importa. |

Shark (`shark` #6C99A4) é o contraponto frio do Flamingo: aparece em séries secundárias de gráfico, rótulos de grupo e na mancha direita da aurora. Nunca é o acento principal.

O fundo escuro tem atmosfera: três manchas desfocadas (`aurora-flamingo` acima à esquerda, `aurora-shark` à direita, uma Flamingo fraca no centro; `blur-aurora`, deriva lenta de `duration-aurora`) e uma grade de 72px (`space-18`) em `line`, mascarada por um gradiente radial para sumir abaixo da dobra. Veja o componente **Aurora**. Os anéis e arcos circulares das capas de 2024 e 2025 estão aposentados; a aurora e a grade assumem a função.

## Cor

- Fundo de página em `bg`; cards e painéis em `surface`; dropdown, dock e modal em `surface-2`.
- Texto principal em `text`, secundário em `text-soft`, rótulos e notas em `text-muted`. `text-dim` é decorativo (`aria-hidden`) e nunca carrega informação.
- Links e texto laranja sempre em `flamingo-text`, nunca em `flamingo`. No tema claro o Flamingo puro dá 2,8:1 sobre o fundo e reprova; o token já resolve isso (#B83516, 5,1:1).
- Texto sobre preenchimento Flamingo é `on-flamingo` (tinta escura). Branco sobre Flamingo (2,8:1) só existe no avatar oficial, em tamanho de wordmark.
- Item ativo e chip selecionado: fundo `flamingo-tint`, texto `flamingo-text`, borda `flamingo` quando houver.
- Bordas e divisores só em `line`; em foco ou hover, `line-strong`. Nunca uma borda cinza sólida.
- Gradiente de texto só no h1 da capa: `flamingo` → `flamingo-soft` → `shark` a 100°. Em qualquer outro lugar, Flamingo é chapado.
- Estados: `success` para "online/ok" (um ponto de 6 a 7px com halo), `danger` para erro de formulário, `warning` raro. Nenhum deles entra em gráfico financeiro.

Pares verificados em ambos os temas (mínimo 4,5:1): `text`, `text-soft`, `text-muted`, `flamingo-text`, `shark-text`, `success`, `danger`, `warning` e `focus` sobre `bg` e `surface`; `on-flamingo` sobre `flamingo`.

## Tipografia

Três vozes, cada uma com um papel fixo:

- **Archivo Black** (`display`) para títulos e números gigantes em capa: `display-xl`, `display-l`, `display-m`, `display-s`. Peso 400 (a família só tem um), espaçamento negativo, entrelinha de 0,98 a 1,1. Largura máxima por estilo: 15ch, 20ch, 28ch. Nunca em caixa alta, nunca abaixo de 26px.
- **Archivo** (`body`) para tudo que se lê: `dek`, `lede`, `body`, `body-s`, `caption`, `heading`, `button`. Negrito 600 só em `heading`, `button` e trechos em destaque dentro de `lede`.
- **IBM Plex Mono** (`mono`) para tudo que se mede: `num-xl`, `num-l`, `data`, `code` e os rótulos em caixa alta `eyebrow` e `label`. Caixa alta existe apenas nesses dois estilos.

Hierarquia de uma seção, de cima para baixo: `eyebrow` (pílula) → `display-l` → `dek` em `text` → `lede` em `text-soft` → blocos. Esse esqueleto vale para slide, dataroom e capítulo de proposta. Em site e landing page a seção começa no `display-l`: o eyebrow aparece só no topo da página e nunca numerado (veja **Aplicações**).

Archivo é a fonte da UBLE desde o designer original (Figma, 2024). Space Grotesk, Inter e Space Mono apareceram em materiais de 2026 e estão descontinuadas; ao retocar esses materiais, troque pela família correta.

## Espaço e layout

- Grade de 4px; passos nomeados em `space-*`. Conteúdo em `measure` (1240px) no site; 980px em documento; gutter de `space-7` no desktop e `space-4` no mobile.
- Card: padding `space-7`, raio `radius-2xl`. Card compacto: `space-5` e `radius-lg`.
- Grids de cards com gap `space-4`; stat rows viram bento (o primeiro número ocupa duas colunas). Abaixo de 980px tudo empilha em uma coluna.
- Ritmo entre seções: `space-18` no site, `space-8` em documento. Margem acima de stat row `space-14`, acima de grid `space-11`, acima de tabela `space-6`.
- Alvos de toque de no mínimo 44px (`space-11`).

## Elevação, vidro e o equivalente estático

Vidro existe em quatro lugares, e só neles: barra superior rolada (`glass-nav` + `blur-glass`), dropdown e modal (`glass-panel` + `blur-panel` + `shadow-panel`), dock (`glass-panel` + `blur-glass` + `shadow-dock`) e card (`glass-card` + `blur-glass`). Nunca empilhe vidro dentro de vidro: um card dentro de um card é transparente.

O card tem borda de 1px em gradiente (`flamingo` a 55% → `line` a 40% do caminho → `shark` a 35%, a 140°), desenhada com `::before` e máscara. É o detalhe mais reconhecível do sistema; veja **Card**.

**Fora do navegador o vidro não existe.** Em PDF, PowerPoint, Google Slides, e-mail e imagem estática, aplique o equivalente:

| Elemento vivo | Equivalente estático |
|---|---|
| `glass-card` + `blur-glass` + borda gradiente | `surface` sólido + borda 1px `line-strong` |
| `glass-panel` | `surface-2` sólido + `shadow-panel` |
| Aurora animada + grade | Aurora congelada (exportada como imagem de fundo uma única vez) ou `bg` chapado com a grade |
| Gradiente de texto no h1 | `flamingo` chapado |
| Revelação escalonada | Estado final |

## Movimento

Uma curva (`ease-uble`), saída mais rápida que entrada (`duration-exit` 320ms, `duration-enter` 700ms), só `transform`, `opacity`, `filter` e `clip-path`. Com `prefers-reduced-motion: reduce`, nada se move e tudo está no estado final. Regras completas e receitas na seção **Movimento**.

## Logo e marca

O wordmark é a única marca: `assets/Logos/uble-wordmark-ink.svg` sobre fundos claros e `uble-wordmark-canvas.svg` sobre fundos escuros. Não existe símbolo isolado; não invente um. Área de respiro igual à altura da letra U em todos os lados. Em interface, o wordmark pode ser composto em `wordmark` (Archivo Black) com o ponto final em `flamingo`: **UBLE.** Regras completas na seção **Logo**.

## Iconografia e ilustração

- Ícones de interface: traço de 1,4 a 1,6px, cantos arredondados, cor herdada do texto (`currentColor`), 14 a 20px. Use um conjunto de linha fina consistente (Lucide serve); nunca ícones preenchidos, nunca emoji.
- Ilustração: diagramas em linha fina monocromática sobre o fundo, em `text-muted` para o que é estrutura e `flamingo` para o caminho da UBLE. O modelo é a **trilha de pagamento** do dataroom (checkout → gateway → adquirente → emissor → recusa, e a curva Flamingo que leva até "pago"). Sem fotos de banco de imagem, sem ilustração 3D, sem mascote.
- Os 11 ícones SVG do dashboard de 2024 (`Menu-*.svg`) não entram no sistema: são de uma geração anterior do produto.

## Gráficos e dados

`flamingo` = recuperado pela UBLE. `shark` = perda e o que não é UBLE. `text-soft` e `text-muted` = séries de contexto. `success` nunca entra. Eixos e legendas em `label`; valores em `data`; grade do gráfico em `line`. Regras completas e exemplos na seção **Gráficos e dados**.

## Conteúdo e voz

A voz se adapta ao contexto (investidor, cliente, parceiro, time), mas três coisas não mudam: a mais direta e clara possível, número com fonte, zero jargão de IA. Em português para time, clientes e parceiros; em inglês para investidores. Sem travessão, sem emoji. Regras por contexto, exemplos de "evite / prefira" e um prompt de sistema prontos na seção **Tom de voz**.

## Como consumir

- Site, dataroom, Lovable e qualquer HTML: carregue `tokens.css` e use as variáveis (`var(--flamingo)`, `var(--space-7)`, `var(--font-mono)`) e as classes de texto (`.display-l`, `.lede`, `.num-xl`). Fontes via Google Fonts: Archivo Black, Archivo 400/500/600, IBM Plex Mono 400/500 (o dataroom hospeda as mesmas via @fontsource por exigência de CSP).
- Deck, proposta, relatório: copie os valores hexadecimais dos tokens e aplique o equivalente estático da tabela acima. O esqueleto de seção (`eyebrow` → `display` → `dek` → `lede` → blocos) vale igual. No site, sem eyebrow por seção.
- Peça a um agente de IA que leia este README antes de produzir qualquer material da UBLE; os tokens, os componentes e a seção Tom de voz são o briefing.
