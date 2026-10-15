# Logo

A marca da UBLE é um wordmark: quatro letras em caixa alta, geométricas, pesadas, sem símbolo. A simplicidade é a identidade; não adicione ícone, tagline colada ou efeito.

## As duas versões

| Arquivo | Tinta | Use sobre |
|---|---|---|
| `assets/Logos/uble-wordmark-ink.svg` | preta (#000000 no arquivo; aplique `text` via filtro ou recolorindo o path) | fundos claros: `bg` e `surface` do tema claro, branco de impressão |
| `assets/Logos/uble-wordmark-canvas.svg` | branca (#FFFFFF no arquivo) | fundos escuros: `bg` e `surface` do tema escuro, blocos `flamingo` em social |

Os dois SVGs vêm do Illustrator original do designer (viewBox 1000×1000, o wordmark centrado). Ao usar como `<img>`, recorte o espaço em volta com `object-fit` ou ajuste o viewBox para `0 0 800 220` aproximadamente; nunca redesenhe o path.

## Versão tipográfica (só em interface)

Quando o SVG não couber (barra de navegação, assinatura de e-mail, favicon tipográfico), componha o nome em `wordmark` (Archivo Black, espaçamento -0,03em) com um ponto final em `flamingo`: **UBLE.** É a forma usada no dataroom. O ponto é a única licença permitida.

## Espaço e tamanho

- Área de respiro: a altura do U em todos os lados. Nada entra nessa zona, nem texto, nem borda de card.
- Tamanho mínimo: 72px de largura em tela, 18mm em impressão. Abaixo disso use a versão tipográfica.
- Escale sempre proporcionalmente. Nunca estique, incline ou aplique contorno.

## Cor

- Sobre claro: tinta (`text` do tema claro, #10161F) ou preto do arquivo.
- Sobre escuro: canvas (`text` do tema escuro, #EFEEEB) ou branco do arquivo.
- Sobre Flamingo (avatar de social, capa de LinkedIn): branco. É a única situação em que branco toca Flamingo em tamanho grande.
- Nunca em Flamingo sobre claro, nunca em gradiente, nunca em cinza médio.

## Onde cada forma cabe

| Contexto | Forma |
|---|---|
| Capa de deck, página de site, proposta | SVG, canto superior esquerdo, altura de 22 a 28px no site e de 10mm na capa |
| Barra de navegação, dock, rodapé | Tipográfica `UBLE.` a 22px |
| Avatar de LinkedIn e redes | `assets/Logos/avatar-flamingo.png`: wordmark branco centrado em bloco Flamingo |
| Favicon | Pendente: o favicon atual está cortado (wordmark no canto, fundo branco). Gere um novo a partir do avatar Flamingo em 32, 96 e 180px |
| Assinatura de e-mail | Tipográfica, 16px, seguida do cargo em `body-s` |

## Com outras marcas

Em material de parceiro (Wake, VTEX, Mais Correios), o wordmark da UBLE e o logo do parceiro ficam na mesma linha, separados por um divisor vertical de 1px em `line`, com a mesma altura visual. UBLE à esquerda quando o material é nosso; à direita quando o material é do parceiro.
