# uTest Academy · Testing in the uTest Platform · 02: uTest Cycle Process

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: uTest Cycle Process](https://platform.utest.com/academy/tracks/2/courses/31/lessons/test-cycle-terms) (login) |

## Ciclo de vida de um ciclo de teste / Test cycle lifecycle

~~~mermaid
stateDiagram-v2
    [*] --> Convite: e-mail, Home ou Projects<br/>email, Home or Projects
    Convite --> Pending: aceitou NDA + Overview<br/>accepted NDA + Overview
    Convite --> Recusado: Decline (sem penalidade / no penalty)
    Pending --> Active: ciclo começa / cycle starts
    Active --> Locked: tempo acabou / time is up
    Locked --> Closed: revisão em até 15 dias<br/>review within 15 days
    Closed --> [*]
~~~

| Status | 🇧🇷 O que dá para fazer | 🇺🇸 What you can do |
|---|---|---|
| Pending | ler o Overview e pegar slot; **não** dá para testar nem reportar | read the Overview, claim a slot; **no** testing/reporting |
| Active | testar, reportar e editar bugs, executar casos de teste, enviar reviews | test, report/edit bugs, run test cases, submit reviews |
| Locked | **sem** envios novos; editar o que estiver em *Info Requested*; usar o chat | **no** new submissions; edit *Info Requested* items; chat |
| Closed | só visualizar | view only |

## Aceitar um convite / Accepting an invitation
1. 🇧🇷 Leia e aceite o **NDA** (precisa do endereço completo no perfil). 🇺🇸 Read and accept the **NDA** (needs your full address in the profile).
2. 🇧🇷 Leia o **Overview inteiro** antes de decidir: tenho tempo? Atendo aos requisitos? Tenho interesse? 🇺🇸 Read the **whole Overview** first: time? requirements? interest?
3. 🇧🇷 Aceite (marque os requisitos especiais) ou **recuse cedo**. Recusar **não tem penalidade**. 🇺🇸 Accept or **decline early**: declining has **no penalty**.

### Seções do Overview / Overview sections
Description · **In Scope** · **Out of Scope** · Setup Instructions · **Issue Reporting Instructions** · Test Case Instructions · Special Instructions · Attachments · Team Contact Information · Payouts · Specified Environment · Special Requirements · Bonus Instructions.
> 🇧🇷 O Overview **não** mostra a lista de testers participantes. 🇺🇸 The Overview does **not** list participating testers.

### Abas do ciclo / Cycle tabs
Overview, Slots, **Announcements** (leia e clique em *Acknowledge*), Builds, Issues (Known Issues têm marcador azul), Test Cases, Reviews, My Earnings, Tester Scorecard, Cycle Feedback.

## MFA (verificação em duas etapas) / Two-factor authentication
- 🇧🇷 **Obrigatório para os projetos.** Sem MFA os convites chegam "escondidos" e você não consegue aceitar. Ative em *Account Security > Enable MFA* com Google Authenticator, Microsoft Authenticator ou FreeOTP. **Depois de ativado, não dá para desativar.** 🇺🇸 **Required for projects**; cannot be disabled once on.
- 🇧🇷 A uTest **nunca** pede o seu código. Se alguém pedir, denuncie. 🇺🇸 uTest **never** asks for your code.

## Comunicação / Communication

| Canal / Channel | 🇧🇷 Use para | 🇺🇸 Use for |
|---|---|---|
| Chat do ciclo / Cycle chat | dúvidas do ciclo, em **inglês**, tom profissional; marque <code>@ttl</code> | cycle questions, **English**, professional; tag <code>@ttl</code> |
| Mensagem privada / PM | só assunto sensível (por exemplo, má conduta de outro tester), **com permissão do TTL** | sensitive matters only, **after the TTL agrees** |
| Messages (bug ou caso de teste) | responder ao TTL, TE ou cliente | replying to TTL/TE/customer |
| E-mail ao TE, depois ao TSM | urgência, pagamento, sem resposta no chat por mais de 24 h; **ID do ciclo no assunto** | urgent, payout, no chat reply >24 h; **cycle ID in subject** |

🚫 🇧🇷 **No chat, nunca:** perguntar sobre pagamento, pedir aprovação, discutir rejeição, ser grosseira, escrever EM MAIÚSCULAS. 🇺🇸 **Never in chat:** payouts, approval requests, rejection debates, rudeness, ALL CAPS.

## Quiz comentado / Commented quiz (10/10)
1. Ciclo de teste / Test cycle → ✅ **um teste específico do produto de uma empresa** / one specific test of a company's product.
2. Onde ficam os convites / Where are invites → ✅ **e-mail, My Activity na Home e Projects** (❌ não é "só" um deles / not "only" one).
3. O Overview NÃO tem / Overview does NOT include → ✅ **a lista de testers** / the list of testers.
4. O Overview serve para decidir / Overview helps decide → ✅ **aceitar ou recusar** / accept or decline.
5. Depois de aceitar / After accepting → ✅ **aparecem mais informações do ciclo** / more cycle info becomes available.
6. Testar é / Testing is → ✅ **avaliar um app, site ou produto em busca de problemas** / evaluating for issues.
7. 4 formas de envio / 4 submission types → ✅ **bug reports, casos de teste, reviews de app e estudos de usabilidade**.
8. 3 canais principais / 3 main channels → ✅ **chat do ciclo, mensagens (messenger) e e-mail**.
9. Depois que trava (Locked) / After lock → ✅ **editar bugs e casos de teste já enviados** / edit submitted work.
10. Como se comunicar / How to communicate → ✅ **todas: chat, Messages e e-mail (urgência)** / all.
