# uTest Academy · Testing in the uTest Platform · 07: Academy Tips and Tricks

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído (sem quiz) / Completed (no quiz) |
| Fonte / Source | [uTest Academy: Academy Tips and Tricks](https://platform.utest.com/academy/tracks/2/courses/46/lessons/Terms-and-Acronyms) (login) |

## 1. Ler é a habilidade nº 1 / Reading is skill #1
- 🇧🇷 Leia o Overview **mais de uma vez**; nunca leia na diagonal. Releia **antes de cada ação**: instruções de slot antes de pegar, Setup antes de testar, In Scope, Out of Scope e Known Issues antes de reportar, Issue Reporting Instructions antes de escrever, avisos (Announcements) assim que chegarem. 🇺🇸 Read the Overview **more than once**; re-read the relevant section **before each action**.
- 🇧🇷 Responda os SRS com honestidade e só se candidate a projetos para os quais você atende aos requisitos. 🇺🇸 Answer SRS honestly; only apply when you qualify.

## 2. Quem é quem / Who's who

~~~mermaid
flowchart LR
    T[Tester] -->|chat do ciclo<br/>cycle chat| TTL[Test Team Lead<br/>revisa bugs e casos<br/>reviews work]
    TTL -->|escala / escalates| TE[Test Engineer<br/>monta o ciclo<br/>builds the cycle]
    TE -->|escala / escalates| TSM[Testing Services Manager<br/>cliente e pagamentos<br/>client & payouts]
    TSM -.->|sem resposta<br/>no reply| SUP[Tester Support]
~~~

🇧🇷 Ordem de escalada: **TTL (chat) → TE (e-mail) → TSM (e-mail) → Tester Support.** O TSM só para pagamento, emergência ou falta de resposta do TE. 🇺🇸 Escalation order as above; TSM only for payouts, emergencies or no TE reply.

## 3. Reputação / Reputation
🇧🇷 **Atenção aos detalhes + confiabilidade + trabalho de qualidade** = mais convites. 🇺🇸 **Detail + reliability + quality** = more invites.

## 4. Erros mais comuns nos ciclos da Academy / Most common Academy mistakes

| ❌ Erro / Mistake | ✅ Como evitar / How to avoid |
|---|---|
| área errada no título / wrong area in title | confira a aba do navegador ou o breadcrumb / check the browser tab or breadcrumb |
| título vago / vague title | clareza antes de brevidade: cite o nome do link ou item / clarity over brevity |
| tipo errado / wrong type | afetou o funcionamento → Functional / affects function → Functional |
| várias ações num passo / several actions per step | 1 ação por passo; detalhes entre parênteses / 1 action; details in parentheses |
| URL inválida / invalid URL | copie a URL do Overview, sem símbolos em volta / copy it from the Overview |
| sem pré-condição / no precondition | *Precondition: The user has logged in.* |
| "not working properly" | descreva o que acontece / describe what happens |
| anexo faltando ou no formato errado / missing or wrong-format attachment | .png/.jpg · .mp4 · logs em .txt |
| vídeo fora dos passos / video off-steps | comece na Home, siga os passos e não mostre a plataforma da uTest / start at Home, follow steps |

⚠️ 🇧🇷 Na **Academy Challenge**, relatório com erro = rejeição. Bugs com a **mesma causa** contam como duplicados. 🇺🇸 In the **Academy Challenge**, report mistakes = rejection; same root cause = duplicate.

## 5. Controle emocional / Handling frustration
🇧🇷 Pare → respire ou faça uma pausa → releia as instruções → entenda a decisão → só então **Dispute** (bug) ou **e-mail ao TE** (outros casos), sempre educada e com o ID do ciclo no assunto. Nunca discuta no chat nem procure apoio na comunidade contra uma decisão.
🇺🇸 Pause → breathe → re-read → understand → then **Dispute** or **email the TE**, politely, cycle ID in the subject.

## 6. Escrita eficaz / Effective writing

| ❌ Evite / Avoid | ✅ Prefira / Prefer |
|---|---|
| "Can't register an account" | "An error page opens after tapping the Sign Up button" |
| "Search is not working" | "The homepage reloads after clicking a search suggestion" |
| "What do you expect me to test this way?" | "The test app can't be opened on two devices. Could you please check the build?" |

🇧🇷 Seja **concisa e clara**, organize em sequência lógica, use **tom profissional** e **revise** antes de enviar. 🇺🇸 Be **concise and clear**, structured, professional; **proofread**.

## 7. ⚠️ IA e a uTest / AI and uTest
- 🇧🇷 Reviews, pesquisas, estudos de usabilidade e respostas abertas **escritos por IA** = perda de credibilidade, menos convites e **risco de encerramento da conta** (Diretrizes de IA da uTest). O cliente paga pela **sua** experiência humana.
- 🇺🇸 **AI-written** reviews, surveys, usability studies or open answers = lost credibility, fewer invites and **account termination risk**. Clients pay for **your** human experience.
- 🇧🇷 **Como eu uso IA neste repositório:** para **estudar** os cursos e organizar notas. Nos testes reais, opinião e review são 100% minhas, e dados de clientes nunca vão para ferramentas de terceiros. 🇺🇸 **How I use AI here:** for **studying** and organizing notes only.
