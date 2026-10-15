# Logos

Os arquivos oficiais da marca, vindos do Illustrator do designer original (mar/2025) e do kit de social (set/2024). Regras de uso na seção **Logo**.

| Arquivo | O que é | Tinta | Use sobre |
|---|---|---|---|
| `uble-wordmark-ink.svg` | Wordmark UBLE, viewBox 1000×1000 | preta no arquivo (#000); recolora para `text` do tema claro quando for inline | fundos claros (`bg` e `surface` claros, branco de impressão) |
| `uble-wordmark-canvas.svg` | Wordmark UBLE, viewBox 1000×1000 | branca no arquivo (#fff); recolora para `text` do tema escuro quando for inline | fundos escuros (`bg` e `surface` escuros) |
| `avatar-flamingo.png` | Avatar de redes sociais, 400×400 | wordmark branco centrado sobre bloco `flamingo` | LinkedIn, Instagram, WhatsApp Business |

Os dois SVGs são marcas de tinta única: via `<img>` eles não herdam cor, por isso existem as duas versões. Inline, use um só path e preencha com `currentColor`.

Pendente: favicon. O conjunto atual (`favicon/` no Drive) está cortado, com o wordmark no canto superior esquerdo sobre branco. Gere o novo a partir de `avatar-flamingo.png` em 32, 96 e 180px.
