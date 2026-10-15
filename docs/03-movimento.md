# Movimento

Movimento na UBLE existe para dar sequência à leitura, não para decorar. Tudo que se move obedece a uma curva, a um conjunto de durações e a uma regra de acessibilidade. As receitas abaixo vêm do dataroom e do painel, onde já estão em produção.

## As regras

1. **Uma curva.** `ease-uble` = `cubic-bezier(0.2, 0.7, 0.2, 1)`. Entrada rápida, pouso longo. A única exceção é `ease-linear`, para traços de SVG sendo desenhados.
2. **Saída mais rápida que entrada.** Página sai em `duration-exit` (320ms) e entra em `duration-enter` (700ms). Dropdown abre em 220 a 280ms e fecha em `duration-fast` (160ms).
3. **Só propriedades baratas.** Anime `transform`, `opacity`, `filter` e `clip-path`. Nunca `width`, `height`, `top`, `left`, `margin` ou `padding`. A exceção documentada é a largura do dock (`duration-dock`, 450ms), que é um elemento fixo e único na tela.
4. **Reduced motion é lei.** Com `prefers-reduced-motion: reduce`, toda animação e transição são removidas e cada elemento aparece no estado final. A aurora para. O pulso da trilha some.
5. **Mídia estática = estado final.** Em PDF, slide ou imagem, renderize o último quadro, nunca um quadro intermediário.

## Receitas

**Transição de página**
```css
.page       { animation: page-in var(--duration-enter) var(--ease-uble) both; }
.page.out   { animation: page-out var(--duration-exit) var(--ease-uble) both; }
@keyframes page-in  { from { opacity: 0; filter: blur(10px); transform: translateY(18px); } to { opacity: 1; filter: none; transform: none; } }
@keyframes page-out { to   { opacity: 0; filter: blur(8px);  transform: translateY(-10px); } }
```

**Revelação escalonada** (título, depois dek, depois blocos)
```css
.reveal > * { opacity: 0; transform: translateY(16px); animation: reveal var(--duration-reveal) var(--ease-uble) forwards; }
.reveal > :nth-child(1) { animation-delay: 100ms; }
.reveal > :nth-child(2) { animation-delay: 160ms; }
.reveal > :nth-child(3) { animation-delay: 220ms; }   /* +60ms por filho, teto em 520ms */
@keyframes reveal { to { opacity: 1; transform: none; } }
```

**Dropdown**
```css
.panel { opacity: 0; visibility: hidden; transform: translateY(-6px) scale(0.98); transform-origin: top left;
         transition: opacity var(--duration-fast) var(--ease-uble), transform 200ms var(--ease-uble), visibility 0s linear 200ms; }
.open .panel { opacity: 1; visibility: visible; transform: none;
         transition: opacity 220ms var(--ease-uble), transform 280ms var(--ease-uble), visibility 0s; }
```

**Hover de CTA**: `transform: translateY(-1px)` em 200ms e `box-shadow: var(--glow-flamingo)` em 300ms. Nada mais.

**Aurora**: cada mancha deriva em `translate` e `scale` por 22 a 44s, `alternate`, `infinite`, com `will-change: transform`. Três manchas, três durações diferentes, para o padrão nunca se repetir visivelmente.

**Traço de SVG** (trilha de pagamento): `stroke-dasharray` igual ao comprimento, `stroke-dashoffset` indo a 0 em `ease-linear` para a linha-base e em `ease-uble` para o caminho Flamingo. Nós aparecem com `opacity` em 500ms quando o traço chega neles. Um pulso de 4px em Flamingo percorre o caminho com `animateMotion` em 4,4s, para sempre.

**Gráficos**: entram com `opacity` e `scale(0.98)` → `1` em 600ms quando cruzam o viewport (IntersectionObserver), uma única vez.

## O que não fazer

Parallax, scroll-jacking, contadores que "sobem" até o número, texto que digita sozinho, loop de logos de clientes, animação em hover de tabela. Nada disso acrescenta leitura e tudo isso distrai do dado.
