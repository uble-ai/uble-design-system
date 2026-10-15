Tabela mista de texto e número: texto em Archivo `body-s`, números em mono alinhados à direita, cabeçalho em `label`, hover em `hover-tint`.

## Quando usar
Listas de clientes, documentos, seções, comparações de concorrentes: tudo que tem uma coluna de nome e algumas de atributo. Quando todas as colunas são número, use **Ledger**.

## Anatomia
- `body-s` (14px) para texto; células numéricas com classe `.n` em `data`, `tabular-nums`, `text`, alinhadas à direita.
- Cabeçalho em `label` `text-muted`, alinhado como a coluna, `padding 10px 8px`, borda `line`.
- Célula `padding 12px 8px`, borda inferior `line`, `text-soft`; o nome principal em `text` 600.
- Última linha sem borda. Hover de linha em `hover-tint` (só em tela).
- Fora de card, a tabela fica direta sobre `bg`; dentro de card, rola horizontalmente.

## O consumidor fornece
Colunas (quais são numéricas), linhas, qual coluna é o nome.

## Faça / não faça
- Faça: até 6 colunas; ordenação indicada no cabeçalho com seta em `text-muted`.
- Não faça: zebra; bordas verticais; texto centralizado; ícones de status coloridos sem texto; cabeçalho com fundo sólido.
