# Tom de voz

A UBLE fala como alguém que já viu o dado antes de abrir a boca. A voz muda de registro conforme quem lê, mas é sempre **clara, direta e precisa**: clara porque o leitor entende na primeira leitura; direta porque ele decide em segundos; precisa porque tudo que afirmamos tem número e fonte.

## Os três princípios (valem em todo contexto)

**Clara.** Frases curtas. Um parágrafo, uma ideia. Termo técnico só quando necessário, e explicado na primeira vez. Nada de jargão de IA.

**Direta.** O "so what" vem primeiro; a explicação depois. Se dá para cortar, corte. Uma ação por mensagem.

**Precisa.** Nenhum número sem fonte. Nenhum adjetivo no lugar de um dado. "Recuperamos 9,94% das vendas perdidas, média simples entre clientes de e-commerce" vale mais do que "recuperação expressiva".

## A voz muda com o contexto

| Contexto | Quem lê | Como soa | Regra que só vale aqui |
|---|---|---|---|
| Fundraising (deck, dataroom, memo) | VC de seed, cético | Voz de investidor, nunca de vendas: tese, cálculo, risco nomeado antes do leitor | Inglês. Sinalizar o que o investidor atacaria |
| Comercial (proposta, deck, case, e-mail de venda) | CFO, head de e-commerce | Consultiva: o problema dele em número, o que a UBLE faz, o que ele ganha. Persuasiva sem promessa vazia | Resultado com fonte e período; "até X%" só com base declarada |
| Produto e suporte (painel, relatório, mensagem ao consumidor) | Operador da loja, consumidor final | Curta e resolutiva: o que aconteceu, o que fazer, uma ação | No fluxo de recuperação, fala em nome da loja, nunca "UBLE" |
| Parceiros (Wake, VTEX, PagBank) | CS e vendas do parceiro | Didática e prática: o que dizer ao cliente deles, com exemplo pronto | Logo e termos do parceiro conforme o guia dele |
| Interno (SOP, memo, Slack) | Time UBLE | Objetiva: decisão, motivo, dono, prazo | Pode ter informalidade; não pode ter ambiguidade |

Tratamento por "você" em todos os contextos. Nome de pessoa, não de departamento ("Falar com o Diego", não "Entre em contato com nossa equipe comercial").

## Evite / prefira

| Contexto | Evite | Prefira |
|---|---|---|
| Comercial | Transforme vendas perdidas em receita com a UBLE! | Pagamento recusado não é falta de interesse. |
| Comercial | Solução inovadora de recuperação inteligente | Recuperamos a venda depois que o emissor recusou o cartão. |
| Comercial | Aumente seu faturamento em até 20% | 9,94% das vendas perdidas recuperadas, média simples entre 13 clientes. |
| Comercial | Sem integração complexa | Sem trocar o gateway, sem projeto de integração, sem demanda para o seu time. |
| Fundraising | We are the leading recovery platform in LatAm | SOM of US$142M in Brazil; 13 paying customers closed by the founder. |
| Produto | Erro 403: usuário não autorizado. | Você não tem permissão para ver esta loja. |
| Produto | Processando solicitação. | Estamos buscando seus dados de setembro. |
| Interno | Nossa equipe entrará em contato | O Diego responde até amanhã. |

## Estrutura ideal de uma mensagem

1. **O fato.** O que aconteceu ou o que é. ("Sua loja perdeu R$ 184 mil em pagamentos recusados em setembro.")
2. **O porquê importa.** O impacto, em número. ("É 2,1% do faturamento, acima da média do segmento.")
3. **O próximo passo.** Uma ação, nunca duas. ("Veja quais recusas eram recuperáveis na página 3.")

## Regras de escrita

- Português brasileiro para time, clientes e parceiros. Inglês para investidores e documentos de fundraising. Nunca os dois no mesmo texto.
- Sem travessão (—). Use vírgula, ponto ou dois-pontos. O travessão soa como texto gerado por IA.
- Sem emoji em material da marca. Em Slack e WhatsApp, no máximo um por mensagem.
- Caixa alta só nos estilos `eyebrow` e `label`. Títulos em caixa normal.
- Números: vírgula decimal e ponto de milhar em português (R$ 184.320,00); formato inglês em material de investidor (US$ 142M). Percentual com uma casa quando houver comparação (9,9% vs 4,2%), duas quando for o número-chave (9,94%).
- Bases projetadas levam rótulo ("2026, projetado"). Entre duas leituras corretas de um dado, use a mais favorável e declare a escolha.
- Negrito só para o dado ou a conclusão, uma vez por parágrafo. Nunca para ênfase emocional.
- Evite expressões de IA: "sem firula", "direto ao ponto", "é sobre isso", "mais do que X, Y", "no final do dia", "robusto", "poderoso", "jornada".

## Vocabulário

**Use:** recuperação de pagamentos, venda perdida, pagamento recusado, receita recuperada, take rate, taxa de aprovação, emissor, adquirente, gateway, checkout, cliente (a loja), consumidor (quem compra).

**Evite:** solução, plataforma inovadora, inteligência artificial como adjetivo, parceria estratégica, sinergia, disruptivo, "nossa tecnologia proprietária" sem dizer o que ela faz.

## Prompt de sistema: escreva na voz da UBLE

Copie o bloco abaixo para qualquer assistente de IA que vá produzir texto da UBLE.

```markdown
# Voz da UBLE

Você escreve para a UBLE, uma empresa de recuperação de pagamentos para e-commerce. A UBLE recupera a venda depois que o pagamento foi recusado no checkout, sem que a loja troque de gateway ou faça projeto de integração.

## Passo 0: identifique o contexto
Antes de escrever, pergunte (ou deduza do pedido) para quem é o texto:
- Investidor (deck, dataroom, memo de fundraising): voz de investidor, nunca de vendas. Apresente a tese, mostre o cálculo, nomeie o risco antes do leitor. Em inglês.
- Comercial (proposta, deck, case, e-mail de venda): consultiva e persuasiva. O problema do cliente em número, o que a UBLE faz, o que ele ganha. Nenhuma promessa sem número e fonte.
- Produto e suporte (painel, relatório, mensagem ao consumidor): curta e resolutiva. O que aconteceu, o que fazer, uma ação. No fluxo de recuperação, fale em nome da loja, nunca "UBLE".
- Parceiro (Wake, VTEX, PagBank): didática e prática, com exemplo pronto para o time deles usar.
- Interno (SOP, memo, Slack): objetiva. Decisão, motivo, dono, prazo.

## O que não muda
- Clara: frases curtas, um parágrafo por ideia, termo técnico explicado na primeira vez.
- Direta: conclusão primeiro, explicação depois, uma ação por mensagem.
- Precisa: nenhum número sem fonte, nenhum adjetivo no lugar de um dado.
- Fale com "você" e use nome de pessoa, nunca "nossa equipe".

## Regras
- Português brasileiro, exceto material para investidor (inglês). Nunca misture.
- Nunca use travessão (—). Use vírgula, ponto ou dois-pontos.
- Sem emoji. Sem caixa alta em títulos.
- Formato de número em PT-BR: R$ 184.320,00 e 9,94%.
- Rotule projeções ("2026, projetado").
- Negrito só no dado ou na conclusão, uma vez por parágrafo.
- Não use: solução, inovador, disruptivo, sinergia, jornada, robusto, poderoso, "sem firula", "direto ao ponto", "é sobre isso", "mais do que X, Y", "no final do dia".
- Use: recuperação de pagamentos, venda perdida, pagamento recusado, receita recuperada, emissor, adquirente, gateway, checkout.

## Estrutura de qualquer mensagem
1. O fato, com número.
2. Por que importa, com número.
3. Um próximo passo, só um.

## Teste final
Leia em voz alta como o leitor do contexto leria. Se soar como anúncio, como manual de sistema ou como texto gerado por IA, reescreva até soar como uma pessoa que conhece o dado.
```
