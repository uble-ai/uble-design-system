# Antipadrões

O que a UBLE não faz, com o motivo. Se um material cai em qualquer item desta lista, ele não está pronto.

## Cor

- **Laranja dessaturado (#DC602E, #B84E25, #EC6630).** Apareceram em propostas e decks de 2026 como improviso para legibilidade no claro. A família oficial é `flamingo` (#FD542D) e `flamingo-text` (#B83516 no claro). Ao retocar esses arquivos, troque.
- **Flamingo como fundo de slide ou de seção inteira.** Flamingo é luz, não tinta. A exceção é o avatar e a capa de social.
- **Dois laranjas na mesma tela.** Um destaque por tela.
- **Verde para "recuperado" ou dinheiro.** `success` é status. Recuperado é `flamingo`.
- **Vermelho para perda em gráfico.** Perda é `shark`. Vermelho vira alarme e tira a leitura da tese.
- **Preto puro e branco puro.** `bg` escuro é #07090C; `bg` claro é #EFEEEB.
- **Gradientes azul-roxo, roxo, rosa.** Não existem na paleta. O painel de 2026 (#C111E0) e o battlecard (#4F8EF7, #A78BFA) estão fora do sistema.
- **Texto branco sobre Flamingo em tamanho de leitura.** 2,8:1. Use `on-flamingo`.

## Tipografia

- Space Grotesk, Inter, Space Mono, Roboto, Poppins, Montserrat. A UBLE usa Archivo Black, Archivo e IBM Plex Mono, e só isso.
- Título em caixa alta. Caixa alta só em `eyebrow` e `label`.
- Archivo Black abaixo de 26px ou em texto corrido.
- Número em fonte de texto. Todo número vive na Plex Mono com `tabular-nums`.
- Mais de 70ch por linha em texto corrido; mais de 15ch em `display-xl`.

## Superfície e layout

- Vidro dentro de vidro.
- Card com borda esquerda colorida como destaque.
- Card com sombra pesada em vez de borda `line`.
- Grade de três cards idênticos centralizados como seção de "benefícios".
- Herói centralizado com ilustração 3D ou foto de banco de imagem.
- Pílulas e botões em várias cores. Botão principal é `text` sobre `bg`; secundário é borda `line`; nada mais.
- Anéis e arcos circulares das capas antigas. Substituídos pela aurora e pela grade.
- Visual padrão do shadcn no lado público. Shadcn é aceitável só no admin.

## Dado e gráfico

- Pizza e rosca.
- Eixo Y que não começa em zero numa barra.
- Rótulo em todos os pontos.
- Gráfico sem fonte.
- Número sem fonte, projeção sem rótulo, estatística de enchimento ("+2 milhões de e-commerces") sem relação com a tese.
- Comissão multiplicada pela recuperação (conta duas vezes). Veja o registro de decisões do fundraising para a cadeia válida.

## Movimento

- Contador que sobe até o número, texto que se digita, parallax, loop de logos, scroll-jacking.
- Animar `width`, `height`, `top`, `left`.
- Ignorar `prefers-reduced-motion`.

## Conteúdo

- Travessão. Emoji em material da marca. Lorem ipsum. "Solução", "inovador", "disruptivo", "jornada".
- Promessa sem número ("transforme", "potencialize", "até X%" sem base declarada). Voz de vendas em material de fundraising.
- Misturar português e inglês no mesmo material.
