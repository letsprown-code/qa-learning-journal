# Test IO · Dispute Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Disputes Course (oportunidade do painel · dashboard opportunity) |
| Situação · Status | ✅ Aprovado · "Dispute Certified Tester" · 10/10 perguntas, 3/5 exemplos · 20/11/2026 / Passed |
| Fontes · Sources | [Bug Rejections & Dispute Feature](https://academy.test.io/en/articles/2541994-bug-rejections-dispute-feature) · [Bug Disputes – Good VS Bad examples](https://academy.test.io/en/articles/6757953-bug-disputes-good-vs-bad-examples) |

## O que é / What it is
🇧🇷 A **contestação (dispute)** é o pedido para a equipe de disputas revisar a decisão do TL quando você acha que o bug foi rejeitado ou rebaixado sem razão.
🇺🇸 A **dispute** asks the dispute team to review a TL's decision when you believe a bug was wrongly rejected or downgraded.

## Regras / Rules
| 🇧🇷 | 🇺🇸 |
|---|---|
| Prazo de **72 horas** depois da decisão do TL | **72-hour** window |
| **Uma** contestação por bug | **One** dispute per report |
| Ao contestar, o relatório **fica travado**: nem você nem o TL podem mudar | Report gets **locked** |
| Quem decide: **gerentes de disputa** (não são TLs), decisão **final** | Dispute managers decide; **final** |
| O gerente não reabre o bug nem pede mais informações | Manager can't reopen or ask for info |
| Analisado até o dia 2 do mês seguinte | Reviewed by the 2nd of next month |
| **5+ contestações no mês com menos de 60% aceitas → bloqueio de 1 mês** | 5+ disputes with <60% accepted → 1-month block |
| Bug rejeitado não pode ser apagado (só antes da revisão do TL) | Rejected reports can't be deleted |
| Se os argumentos dos dois lados pesarem igual, a vantagem é da testadora | Ties favor the tester |

## Como escrever / How to write
✅ 🇧🇷 Antes, **respire** e leia o motivo da rejeição. Na mensagem: cumprimento, **referência ao motivo da rejeição**, onde as **instruções ou a user story** dizem o comportamento esperado (citação curta), **prova nova** se tiver (link de vídeo ou log), pedido de revisão e agradecimento. **Curta e clara.**
❌ 🇧🇷 Mensagem com raiva, só "Please review!", chamar o gerente de TL, copiar textos longos, mentir. **Se você mesma admitir que é duplicado ou fora do escopo, a contestação perde.**
🇺🇸 Calm, short, cite the rejection reason and the instructions/user story, add new evidence if needed. Never angry, never just "Please review!".

## Exemplos comentados / Commented examples
| # | Contestação / Dispute | Resultado / Result | Por quê / Why |
|---|---|---|---|
| a | "os dois botões não funcionam; por causa dos duplicados, pelo menos um deve ser aceito" | Rejeitada | Admite que é duplicado. |
| b | "não havia opção de bug de conteúdo, então mandei como funcional" | Rejeitada ⚠️ *errei* | Admite que conteúdo estava fora do escopo. |
| c | "mas não deveria voltar para o card mais próximo?" | Rejeitada | Só opinião de como "deveria" ser; o cliente decide o design. |
| d | Mensagem educada citando a **user story** e o comportamento real | Aceita ⚠️ *errei* | Comportamento diferente da user story = bug válido. |
| e | Mensagem educada citando a **instrução do teste** e o motivo da rejeição | Aceita | Mostra a diferença entre o esperado e o real. |
