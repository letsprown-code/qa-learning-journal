# uTest Academy · Academy Certification Program · 01: Introduction to Testing

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Curso e quiz 10 de 10 · ciclo de prática: test case e bug enviados em 17/11/2026, **aguardando aprovação** / Course & quiz 10 of 10 · practice cycle: test case and bug submitted, **pending approval** |
| Fonte / Source | [uTest Academy: Introduction to Testing](https://platform.utest.com/academy/tracks/16/courses/22/lessons/practice-test-cycles) (login) |
| Antes / Before | [Testing in the uTest Platform](../testing-in-the-utest-platform/) · [Testing Tools](../testing-tools/) |

> 🔒 🇧🇷 Por causa do **NDA**, esta nota não traz nada do site testado nem do bug reportado no ciclo. Só o que o curso ensina. 🇺🇸 Due to the **NDA**, this note contains nothing about the tested site or the bug; only the course content.

## O programa / The program
🇧🇷 São **5 ciclos de prática** em sequência, mais um ciclo "All Stars" só por convite. O programa não dá certificado formal: você recebe um e-mail a cada nível e um de formatura no final. Trabalho aprovado nesses ciclos **aumenta o tester rating**, e rating maior traz mais convites pagos. 🇺🇸 **5 sequential practice cycles** (+ invite-only All Stars). Approved work **raises your tester rating**.

~~~mermaid
flowchart LR
    A[Introduction to Testing] --> B[Computer Testing] --> C[Mobile Device Testing] --> D[Charles Proxy Testing] --> E[Academy Challenge] -.convite / invite.-> F[Academy All Stars]
~~~

## Regras de inscrição / Sign-up rules
| 🇧🇷 | 🇺🇸 |
|---|---|
| Terminar os cursos anteriores e **passar no quiz**; aí o botão azul **Sign Up** é liberado | Finish previous courses and **pass the quiz** to unlock **Sign Up** |
| Só entra no próximo ciclo depois de **passar no anterior** | Next cycle only after **passing the previous one** |
| Não dá para refazer um ciclo em que já passou | Can't redo a passed cycle |
| Inscrição de **segunda a quarta** → ciclo atual; de **quinta a domingo** → ciclo pendente, que abre na segunda seguinte | **Mon–Wed** → current cycle; **Thu–Sun** → pending, opens next Monday |

## Ciclo "Introduction to Testing"
**O que se pratica / What you practice:** aceitar o convite, ler o Overview, usar o chat do ciclo, reservar slot, executar test case, tirar e destacar prints e enviar um issue report. 🇺🇸 Accept invite, read Overview, cycle chat, claim slot, run a test case, screenshots, submit an issue.

| 🇧🇷 Regras do ciclo | 🇺🇸 Cycle rules |
|---|---|
| Pode usar computador **ou** celular | Computer **or** mobile |
| **Só 1 bug** por testador | **Only 1 bug** |
| Bugs dos outros ficam **ocultos**, então não existe duplicado | Others' bugs **hidden** (no duplicates) |
| Erros no relatório voltam como **Info Requested**; se não corrigir, o bug é rejeitado | Mistakes come back as **Info Requested**; unfixed = rejected |
| Bug inválido: pedem para **descartar** (Actions → **Discard**) e você pode mandar outro | Invalid: **Discard** and report another |
| **Print destacado é obrigatório**, mesmo que você mande vídeo | **Highlighted screenshot mandatory**, even with a video |

**Para passar / To pass:** ✅ **1 bug aprovado + 1 test case aprovado**. 🇧🇷 A nota "Pass" sai de **12 a 24 h** depois das duas aprovações, mesmo com o ciclo ainda aberto. Quem não passar é avaliado quando o ciclo fechar e pode se inscrever de novo. 🇺🇸 Pass grade within **12–24 h** of both approvals.

## Fluxo que eu segui / The flow I followed

~~~mermaid
flowchart TD
    I[Convite / Invitation] --> O[Ler o Overview<br/>Read the Overview]
    O --> S[Reservar slot<br/>Claim slot]
    S --> T[Test case: 7 passos<br/>Termos e IA, perfil, local e idioma,<br/>print do Tester ID, print do Sobre este Mac,<br/>como escrever bugs, reportar 1 bug]
    T --> R[Report Issue:<br/>título no formato do Overview,<br/>passos começando pela URL,<br/>expected/actual, 1 print destacado]
    R --> D[Done em todos os passos →<br/>Submit Results → tempo gasto → Finished]
    D --> W[Aguardar aprovação;<br/>responder Info Request em até 48 h<br/>Wait; answer within 48 h]
~~~

## O que eu aprendi na prática / What I learned hands-on
- 🇧🇷 **Título** no formato do Overview: <code>Sistema - Área - Descrição</code>. Área é a **página onde o bug aparece** (Homepage, Search Results Page, PLP, PDP, Cart), não a página de destino. 🇺🇸 Area = the **page where the bug occurs**.
  - ✅ <code>Windows 10 - Homepage - Store Locator link directs to a not found error page</code>
  - ❌ <code>Windows 10 - Store Locator - Store Locator link directs to an error page</code>
- 🇧🇷 O passo 1 de "Actions Performed" é sempre <code>1. Open https://www.site.com</code>. 🇺🇸 Step 1 always opens the URL.
- 🇧🇷 **Escopo:** sugestões de usabilidade e UX, acessibilidade, segurança e erros que só aparecem no console costumam ficar **fora**. Prefira algo **objetivamente errado** que dê para provar com 1 print. 🇺🇸 Prefer an **objectively wrong** behavior provable with 1 screenshot.
- 🇧🇷 **Type:** se o erro aparece **depois de uma ação** (clique, seleção, quantidade), é **Functional**; texto, preço ou imagem errados parados é **Content**; layout quebrado é **Visual**. 🇺🇸 Error after an action → **Functional**.
- 🇧🇷 **Regra de IA do uTest** ([AI Guidelines](https://www.utest.com/ai-guidelines)): pode pedir ideias **genéricas** a uma IA, mas **não** pode colocar dados pessoais nem pedir que ela analise o produto ou as informações de um cliente. O teste e o relatório são feitos por você. 🇺🇸 Generic ideas OK; **no** PII and **no** customer-specific analysis by AI.
- 🇧🇷 Responda os **Info Requests** e clique em **Confirm all info is added** para o status voltar a **New**. 🇺🇸 After editing, click **Confirm all info is added**.

## Quiz comentado / Commented quiz (10/10)
1. Recebeu um convite. E agora? / Got an invitation → ✅ **Ler o Overview e decidir se aceita ou recusa**.
2. Por que ler o Overview / Why read it → ✅ **Todas as opções** (escopo, regras, formato, ambiente).
3. Canal para dúvidas básicas do projeto / Channel for basic questions → ✅ **Chat do uTest (chat do ciclo)**.
4. Afirmação correta sobre prints / Screenshots → ✅ **Todas as anteriores**.
5. Editar bug / Editing a bug → ✅ **Depois de editar, clicar em "Confirm All Info is Added"**.
6. NÃO é correto nos passos / NOT correct in steps → ✅ **Escrever o resultado esperado ou o atual dentro dos passos numerados**.
7. Testando uTest.com, passo 1 / Step 1 → ✅ <code>Open https://www.uTest.com</code>.
8. Apagar um bug / Deleting a bug → ✅ **Actions → Discard**.
9. Quantos bugs nesse ciclo / How many bugs → ✅ **No máximo 1**.
10. Quando entrar no "Computer Testing" / When to sign up for Computer Testing → ✅ **Só depois de passar no Introduction to Testing (1 bug e 1 test case aprovados)**.
