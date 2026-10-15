# UBLE Design System

Fonte de verdade da identidade visual e da voz da UBLE. Tudo o que a UBLE publica parte daqui: site, dataroom, painel, decks, propostas, relatorios, memos, e-mail e social.

A versao navegavel (com previews ao vivo e editor de tokens) e o artifact "UBLE Design System" no Claude, design system padrao da organizacao. Este repositorio e a copia versionada para consumo por codigo e por quem nao usa o Claude.

## Comece por aqui

1. Leia `docs/00-brand-book.md` inteiro. Depois `docs/05-aplicacoes.md` para a midia que voce vai produzir.
2. Em codigo, carregue `tokens/tokens.css` e use as variaveis e as classes de texto. Fontes: Archivo Black, Archivo 400/500/600 e IBM Plex Mono 400/500 (Google Fonts ou @fontsource).
3. Antes de entregar, passe em `docs/06-antipadroes.md`.

## Estrutura

| Pasta | O que tem |
|---|---|
| `tokens/` | `tokens.css` (pronto para `<link>`) e `tokens.json` (para ferramentas e para o artifact) |
| `docs/` | brand book, tom de voz (com prompt de sistema), logo, movimento, graficos e dados, aplicacoes por midia, antipadroes |
| `components/` | preview HTML e guia de cada componente-assinatura; abrem no navegador com `tokens.css` ao lado |
| `assets/logo/` | wordmark SVG para fundo claro (`ink`) e escuro (`canvas`), avatar Flamingo |
| `assets/favicon/` | conjunto completo + `head-snippet.html` para colar no `<head>` |
| `assets/aurora/` | fundo congelado para deck, proposta e social, em 6 formatos (escuro e claro) |
| `assets/social/` | capa de LinkedIn, 3 modelos de post (PNG) e os templates HTML editaveis |
| `plugin/` | `uble-brand.plugin` para o Claude (skills `uble-design-system` e `uble-voz`) |

## Consumo por URL (repo publico)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/<org>/uble-design-system@main/tokens/tokens.css">
```

Fixe uma tag (`@1.0.0`) em producao; `@main` so em ambiente de teste.

## Como mudar

1. Mude no artifact do Claude (editor de tokens ou pedindo ao Claude).
2. Exporte `tokens.css`, `tokens.json` e os `.md` para ca, atualize o `CHANGELOG.md`, suba a versao e crie a tag.
3. Regere o plugin e o knowledge do Lovable a partir dos mesmos arquivos.

Nenhum valor e editado direto aqui: o artifact e a fonte, o repo e o espelho versionado.
