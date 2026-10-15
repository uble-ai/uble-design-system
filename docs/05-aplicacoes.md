# Aplicações por mídia

O sistema é um só, mas cada mídia tem um tema, um esqueleto e um conjunto de equivalentes. Esta tabela decide antes de qualquer arquivo ser aberto.

| Mídia | Tema | Vidro e aurora | Fontes | Esqueleto |
|---|---|---|---|---|
| Site e landing page | `dark` | Vivos | Google Fonts ou @fontsource | display-l → dek → lede → bento/cards; eyebrow só no topo da página, sem número |
| Dataroom | `dark` | Vivos | @fontsource | eyebrow numerado → display-l → dek → lede → bento/cards |
| Painel e produto | `dark` | Vivos, sem aurora em telas densas | @fontsource | dock lateral + topo fixo + cards |
| Deck projetado (pitch, comercial) | `dark` | Equivalente estático | Instaladas (Archivo, Archivo Black, IBM Plex Mono) | capa display-xl; slides eyebrow → display-m → 1 bloco |
| Proposta, relatório, business case | `light`, capa em `dark` | Nenhum | Instaladas | capa escura; miolo em documento claro, 980px |
| Memo, SOP, documento interno | `light` | Nenhum | Instaladas ou Archivo do Google Docs | heading → body; tabelas em `data` |
| E-mail | `light` | Nenhum | Fallback: Arial para texto, Courier New para dado | logo tipográfico, body 16px, um CTA |
| LinkedIn e social | `dark` ou bloco `flamingo` | Aurora congelada como imagem | Instaladas | wordmark canvas, display-l, uma frase |
| Impressão (brinde, papelaria) | `light` | Nenhum | Instaladas | wordmark ink, muito espaço |

## Site e landing page

- O site é navegado, não lido em ordem. Seções abrem direto no título (`display-l`), sem eyebrow e sem número.
- Eyebrow só no topo de cada página, para dizer o que ela é ("Cases", "Calculadora"), e acima do CTA final. Nunca numerado.
- Numeração só onde a ordem é informação real, como os passos de um processo ("Passo 1 · Conectar").

## Deck

- Capa: `bg` escuro, aurora congelada exportada em PNG como fundo (gerada uma vez a partir do componente **Aurora**), wordmark no canto superior esquerdo, título em `display-xl` até 3 linhas, data em `label`.
- Slide padrão: eyebrow numerado no topo à esquerda, título `display-m` com 28ch no máximo, um bloco de conteúdo (um gráfico, uma tabela, um bento de três cards ou um parágrafo `lede`). Nunca dois blocos competindo.
- Rodapé: `label` em `text-muted` com "UBLE · <nome do material>" à esquerda e número da página à direita.
- Cards: `surface` sólido com borda 1px `line-strong`, raio 20px (ou 18px quando a ferramenta limita).
- Fechamento: CTA único, no formato do botão primário (fundo `text`, texto `bg`, pílula), como o "Falar com o Diego" do dataroom. Flamingo só no ponto de status ao lado do rótulo.

## Proposta e relatório

- Capa escura (mesmas regras do deck), miolo claro.
- Corpo em `body` 16px, 70ch, `text` sobre `bg` claro (#EFEEEB). Para impressão em volume, `bg` pode ser branco; o resto não muda.
- Títulos de capítulo em `display-m`, subtítulos em `heading`. Eyebrow numerado antes de cada capítulo.
- Números no texto em `data` quando forem valores de tabela; no corpo corrido, `body` mesmo.
- Tabela de preços e de resultado como **Ledger** (claro): cabeçalho `label`, linhas `data`, total em `flamingo-text`.
- Destaque de conclusão: card `surface` claro com borda `line-strong`, nunca fundo laranja.

## E-mail

- Largura 600px, fundo `bg` claro, texto `text` claro, 16px Arial como fallback de Archivo.
- Logo tipográfico "UBLE." em Archivo Black 20px (fallback Arial Black), ponto em `flamingo`.
- Um CTA: botão com fundo `text` (#10161F) e texto `bg` (#EFEEEB), raio 999px, 14px 600. Link secundário em `flamingo-text`.
- Dados em tabela simples, Courier New como fallback da Plex Mono, alinhados à direita.
- Assinatura: nome em `heading` 14px, cargo em `caption`, telefone e site em `flamingo-text`.

## Social

- Avatar: `assets/Logos/avatar-flamingo.png`.
- Capa de página: `bg` escuro com aurora congelada, wordmark canvas à esquerda, uma frase em `display-l` à direita.
- Post com texto: `bg` escuro, eyebrow, uma frase em `display-l` com no máximo 12 palavras, wordmark no rodapé. Sem foto de banco de imagem; se houver pessoa, é alguém da UBLE.
- Post de dado: um número em `num-xl` escalado (até 160px) em `flamingo`, rótulo em `lede`, fonte em `caption`.
- Formatos: 1080×1080, 1080×1350 e 1200×627. Margem interna de 72px (`space-18`).
