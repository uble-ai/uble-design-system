Atmosfera de fundo do tema escuro: três manchas desfocadas que derivam devagar e uma grade de 72px mascarada. Substitui os anéis das capas antigas.

## Quando usar
Fundo de página de site, dataroom, capa de deck e de social (congelada), capa escura de proposta. Não em painéis densos de dado nem em documento claro no miolo.

## Anatomia
- Container `position: fixed; inset: 0; z-index: 0; pointer-events: none; aria-hidden`.
- Mancha 1: 52vw, canto superior esquerdo, `aurora-flamingo`, deriva 22s. Mancha 2: 46vw, direita, `aurora-shark`, 26s. Mancha 3: 30vw, centro, Flamingo a 18%, 30s em `alternate-reverse`. Todas com `blur-aurora` e `opacity-aurora`.
- Grade: linhas de 1px em `line` a cada `space-18` (72px), com `mask-image` radial (elipse 70% × 55% em 50% 20%) para sumir abaixo da dobra; `opacity-grid`.
- No tema claro, manchas a 0,3 e grade a 0,35.
- Com `prefers-reduced-motion`, as manchas param no lugar.
- O h1 do hero da capa (e só ele) pode usar o gradiente de texto Flamingo → `flamingo-soft` → Shark a 100°.

## Equivalente estático
Exporte este componente uma vez em 1920×1080 (e 1080×1350 para social) como PNG e use como fundo em deck, proposta e social. Nunca recrie manchas à mão em ferramenta de slide.

## Faça / não faça
- Faça: uma aurora por página; conteúdo em `z-index: 1`.
- Não faça: aurora atrás de tabela densa; mais de três manchas; manchas de outras cores; aurora no miolo claro de documento.
