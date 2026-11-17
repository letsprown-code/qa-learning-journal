# Test IO · Onboarding User Story Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 6 de 6 (mínimo 4) · 17/11/2026 / Completed · quiz 6 of 6 (min. 4) |
| Por que fiz · Why | Recomendado pela comunidade Test IO: projetos de User Stories têm **pagamento garantido** e fluxo constante de tarefas / Recommended by the Test IO community: User Story projects have **guaranteed payout** and a steady flow |
| Fontes · Sources | [User Story Testing](https://academy.test.io/en/articles/4156595-user-story-testing) · [Executing a User Story](https://academy.test.io/en/articles/4156596-executing-a-user-story) · [User Story Rejections Explained](https://academy.test.io/en/articles/4156594-user-story-rejections-explained) · [More Good and Bad Examples](https://academy.test.io/en/articles/7261905-user-stories-more-good-and-bad-examples) |
| Ligado a · Related | [Exploratory Testing: 03 Bug Report Attachments](../exploratory-testing/03-bug-report-attachments.md) |

## O que é uma User Story / What a User Story is
🇧🇷 Uma frase curta que descreve **o que o usuário deve conseguir fazer**. A sua tarefa é **confirmar se funciona**. Normalmente leva **até 5 minutos** e fica em **Feature description → User Stories**. Nem todo teste tem User Stories, e só quem **passou neste curso** vê os botões para executá-las.
🇺🇸 A short statement of **what a user should be able to do**; you **confirm whether it works**. Usually **≤ 5 minutes**; found under **Feature description → User Stories**. Only testers who **passed this course** see the execution buttons.

> Exemplos / Examples: *"A user can add the product to the cart."* · *"A user can log in with valid login data."* · *"When a user applies a valid promo code, the correct discount is applied."*

## Reserva / Reservation

~~~mermaid
stateDiagram-v2
    [*] --> Disponivel: User Story no teste
    Disponivel --> Reservada: clicar Start (30 min)
    Reservada --> Enviada: Submit dentro do prazo
    Reservada --> Disponivel: tempo acabou ou Cancel
    Enviada --> Aprovada: TL aprova
    Enviada --> Rejeitada: TL rejeita
    Disponivel --> Locked: todas as execuções já feitas
~~~

| 🇧🇷 | 🇺🇸 |
|---|---|
| Ao clicar **Start**, a execução fica reservada para você por **30 minutos**, e um cronômetro mostra o tempo restante | **Start** reserves it for **30 minutes** (timer shown) |
| No máximo **3 reservas ao mesmo tempo**; com 3, as outras aparecem como **limited** | Max **3 reservations at a time** (otherwise **limited**) |
| **reserved** = outros testadores já estão fazendo; se alguém desistir ou o tempo acabar, ela volta a ficar disponível | **reserved** = others working on it; may free up again |
| **locked** = todas as execuções já foram feitas | **locked** = all executions done |
| Dá para retomar pela página do teste enquanto a reserva estiver valendo | Resume from the test overview while reserved |

## Executar / Execute
**1. "Can you confirm the User Story is working?"**
| Resposta / Answer | 🇧🇷 Quando | 🇺🇸 When |
|---|---|---|
| **Yes** | testou com cuidado e funciona como descrito | tested thoroughly, works |
| **No** | não funciona como esperado → **reporte o bug** (se estiver no escopo e não for *Known Bug*) | doesn't work → **report a bug** |
| **Not possible to test** | algo impede o teste (ex.: não há login disponível) → **explique o motivo** no comentário | blocked → **explain why** |

**2. Comentário / Comment**
- 🇧🇷 **Yes:** se o vídeo mostra tudo, escreva **"n/a"**. Comente só quando houver contexto que o vídeo não mostra. Alguns ciclos pedem comentário em todos os "Yes": siga as instruções do ciclo. 🇺🇸 **Yes:** "n/a" if the screencast shows everything.
- 🇧🇷 **No / Not possible to test:** comentário **obrigatório e detalhado**: o que fez, o que falhou e o que tentou. 🇺🇸 **Mandatory and detailed.**
- ❌ 🇧🇷 Evite frases genéricas ("works as expected", "no issues found"), repetir o que o vídeo já mostra ou copiar o texto da User Story. 🇺🇸 No generic phrases, no repeating the video or the story text.

| Situação / Case | ✅ Bom / Good | ❌ Ruim / Bad |
|---|---|---|
| Yes | n/a | "The page opened successfully." |
| No | "Clicked the 'Become a Tester' button in the header, but no redirection occurred, and the button did not respond to further clicks." | "The page didn't open." |
| Not possible | "Attempted to access the website multiple times but consistently faced a blank page even after refreshing and trying different browsers." | "Couldn't test this." |

**3. Anexo / Attachment**: 🇧🇷 **vídeo curto, de no máximo 15 segundos**, obrigatório em toda execução. Se a história tiver vários passos, pode gravar só o último. Cada vídeo serve para **uma única** execução, e valem as regras gerais de screencast: **.mp4**, barra de endereço visível, mostrar as ações. 🇺🇸 **Screencast ≤ 15 s**, mandatory, one per execution, .mp4, URL bar visible.

**4. Device/Browser:** 🇧🇷 use o aparelho pedido, e ele tem que ser o mesmo que aparece no vídeo. 🇺🇸 Use the requested device, matching the video.

**5. Tempo (opcional) e Linked bug (opcional) / Time (optional) and Linked bug (optional)**: 🇧🇷 se já existe um bug que explica a falha, **vincule** esse bug. Se não existe, **reporte o bug primeiro** ("Submit bug" abre em outra aba) e depois envie a execução. Só dá para vincular **antes** de enviar. 🇺🇸 Link an existing bug or submit one first; linking only before submitting.

**6. Submit:** 🇧🇷 depois de enviar, **não dá para editar nem apagar**. Envie só depois de testar de verdade. 🇺🇸 Can't edit/delete after submitting.

## Motivos de rejeição / Rejection reasons
| Motivo / Reason | 🇧🇷 O que significa |
|---|---|
| Actions not visualised | o vídeo não mostra o passo importante (como o resultado foi gerado) |
| Attachment can't be opened | vídeo quebrado ou fora do formato **.mp4** |
| Test instructions not followed | não seguiu as instruções do ciclo |
| **Screencast is too long** | vídeo com **mais de 15 segundos** |
| Wrong or missing screencast | vídeo errado ou **print no lugar do vídeo** |
| Low-quality comment | comentário fraco para o resultado escolhido |
| **No URL bar or date** | a barra de endereço não aparece |
| Execution not done properly | marcou No ou Not possible quando funcionava, ou não seguiu a história à risca |
| Other | ex.: aparelho errado |

⚠️ 🇧🇷 Com **muitas rejeições**, você pode ser **excluída** das User Stories. A equipe de *Compliance* também avalia todas as execuções: comentário fora do assunto pode gerar advertência ou banimento. 🇺🇸 High rejection rate → excluded; irrelevant comments → warning/ban.

## Pagamento / Payout
- 🇧🇷 O valor de cada execução aparece nos detalhes do teste. O crédito cai na conta **quando o teste é arquivado**, em até **10 dias depois do fim do teste**. Mesmo que o TL não revise, a execução é paga quando o teste é arquivado. 🇺🇸 Shown in test details; credited when the test is archived (**≤ 10 days** after end), even if not reviewed.

## Quiz comentado / Commented quiz (6/6)
1. User Story impossível de testar / Not possible to test → ✅ **Escolher "Not possible to test" e explicar em detalhe no comentário** (❌ deixar incompleta, pular ou falar com o suporte).
2. Tempo da reserva / Reservation time → ✅ **30 minutos**.
3. Comentário quando funciona / Comment when it works → ✅ **"n/a"**, se o vídeo mostra claramente (❌ "no issues found", "worked as expected").
4. Se não terminar no prazo / Reservation expires → ✅ **A User Story volta a ficar disponível para outros testadores.**
5. Anexo obrigatório / Required attachment → ✅ **Vídeo curto, de até 15 segundos** (❌ só print, ❌ vídeo com áudio).
6. Achou um bug durante a User Story / Bug found during it → ✅ **Vincular o bug que já existe ou criar um novo, se não houver.**
