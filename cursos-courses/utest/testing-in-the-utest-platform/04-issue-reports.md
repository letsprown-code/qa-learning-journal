# uTest Academy · Testing in the uTest Platform · 04: Issue Reports

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: Issue Reports](https://platform.utest.com/academy/tracks/2/courses/17/lessons/understanding-bug-report) (login) |
| Comparar com / Compare with | [Test IO: 04 Bug Reports](../../test-io/exploratory-testing/04-bug-reports.md) |

## Campos do relatório e regras / Report fields and rules

| Campo / Field | 🇧🇷 Regra | 🇺🇸 Rule |
|---|---|---|
| **Title** | siga o formato do Overview (por exemplo <code>SO - Página - Descrição</code>); diga a área e o problema; **sem MAIÚSCULAS**; navegador só se pedirem | follow the Overview format; area + issue; **no ALL CAPS**; browser only if asked |
| **Issue Type** | Functional, Visual, Content, Performance ou Crash | |
| **Frequency** | Every time, Hardly ever, Occasionally, Once | |
| **Severity** | Low, Medium, High, Critical (veja abaixo) | see below |
| **Source** | *Exploratory* (fora dos passos) ou *Structured* (achado num caso de teste) | outside steps vs found in a test case |
| **Environment** | aparelho + sistema + navegador; app nativo = **"Native (No mobile browser)"** | native app = **"Native (No mobile browser)"** |
| **Actions Performed** | passos numerados, **1 ação por passo**; o passo 1 abre a URL ou o app; **Click** no computador e **Tap** no celular; *Precondition:* antes do passo 1; ❌ "Observe/Check/See" como passo | numbered, **1 action per step**; step 1 opens URL/app; **Click** (desktop) / **Tap** (mobile) |
| **Expected / Actual** | o que deveria acontecer / o que acontece de fato | |
| **Error Message** | só se houver; **deixe vazio** se não houver (❌ "N/A", "None", "-") | only if present; **leave empty** otherwise |
| **Attachments** | até **2 prints** (.png/.jpg, tela inteira com a URL, destaque com retângulo, círculo ou seta vermelha ou amarela) + **1 vídeo** (.mp4, sem áudio, igual aos passos) + logs (.txt/.log) | max **2 screenshots** + **1 video** + logs |

## Gravidade × valor / Severity vs value

| Severity | 🇧🇷 Exemplos | 🇺🇸 Examples |
|---|---|---|
| Low | desalinhamento, erro de ortografia | misalignment, typo |
| Medium | atrapalha, mas tem alternativa (*workaround*) | has a workaround |
| High | funcionalidade principal muito afetada | core feature heavily impacted |
| **Critical** | **crash ou congelamento**, vazamento de privacidade | **crash/freeze**, privacy breach |

💰 🇧🇷 **O pagamento depende do VALOR que o cliente dá ao bug** (Somewhat, Very ou Exceptionally Valuable; Won't Fix), **não** da gravidade que você escolhe. 🇺🇸 **Pay depends on the client-assigned VALUE**, not your severity.

## Rejeição e contestação / Rejection and dispute

~~~mermaid
flowchart TD
    R[Bug rejeitado<br/>Bug rejected] --> M[Leia o MOTIVO, não só o tipo<br/>Read the REASON, not just the type]
    M --> T{Tipo / Type}
    T -- WAD --> OK[Não afeta o rating; aceite<br/>No rating impact; accept]
    T -- DUP / OOS / DNFI --> NO[Não conteste<br/>Don't dispute]
    T -- Outro motivo e você tem certeza<br/>Other and you're sure --> D[Dispute: 1 vez por bug,<br/>com novas provas e tom educado<br/>1 per bug, new evidence, polite]
    D --> A{Resultado / Outcome}
    A -- Aprovado / Approved --> Y[✅]
    A -- Rejeitado de novo / Rejected again --> N2[Rating cai: dupla rejeição<br/>Rating drops: double rejection]
~~~

- ⚠️ 🇧🇷 **DNFI** (não seguiu as instruções) tem **impacto negativo dobrado** no rating. 🇺🇸 **DNFI** has a **double** negative impact.
- 🇧🇷 Há um **limite de contestações por mês**. Nunca negocie aprovação no chat. 🇺🇸 **Monthly dispute limit**; never negotiate approval.

## Outras regras / Other rules
- 🇧🇷 Novatos (Unrated e Rated) têm **no máximo 5 bugs não aprovados por ciclo**: **qualidade antes de quantidade**. 🇺🇸 New testers: **5 unapproved bugs per cycle**.
- 🇧🇷 **+1**: só se você reproduziu, sempre com anexo (print para bug visual, vídeo para os outros). Se o bug for aprovado, ganha um pequeno bônus no rating. 🇺🇸 **+1** only if reproduced, with attachment.
- 🇧🇷 **Placeholder é proibido**: nada de campos com "1. 2. 3.", anexo "provisório" ou trocar o bug por outro depois de enviado. 🇺🇸 **No placeholders.**
- 🇧🇷 **Editar:** pode em New, Info Requested e Rejected (só para contestar); **não** pode em Pending nem Approved. 🇺🇸 **Edit:** yes in New / Info Requested / Rejected (for dispute); **no** in Pending / Approved.
- 🇧🇷 **Issue Quality Review:** uma IA revisa o relatório **uma vez**. Confira as sugestões dela, porque ela pode piorar o texto. 🇺🇸 An AI reviews the report **once**; check its suggestions.
- 🇧🇷 **Templates:** use *Save as Template* quando o título tiver prefixo fixo ou as pré-condições se repetirem. 🇺🇸 Use templates for fixed prefixes or preconditions.

### Exemplo de contestação educada / Polite dispute example
> *"Hi TTL, thank you for reviewing the report. I believe the issue is valid and in scope because [short, clear reason]. I have improved the steps and attached a new video that shows the issue. Could you please review it again? Thank you."*

## Quiz comentado / Commented quiz (10/10)
1. Título "OS - Page - Description" / Title format → ✅ **"Windows 10 - Cart - User is unable to remove any products from cart"** (❌ Chrome não é sistema operacional; ❌ falta a página; ❌ MAIÚSCULAS).
2. ERRADO sobre o título / WRONG about titles → ✅ **"sempre colocar o navegador"**.
3. Rejeição que não afeta o rating / No rating impact → ✅ **WAD**.
4. Sem mensagem de erro / No error message → ✅ **deixar o campo vazio**.
5. Viola os Termos / Violates the Terms → ✅ **placeholder**.
6. Quando usar +1 / When to +1 → ✅ **quando você reproduziu e tem certeza de que é válido**.
7. Quando contestar / When to dispute → ✅ **quando tem certeza, seguiu as instruções e traz mais provas**.
8. NÃO é boa prática / NOT good practice → ✅ **demorar para responder um Info Request**.
9. Não pode editar quando / Can't edit when → ✅ **Pending**.
10. "App trava ao abrir o carrinho" / "App crashes on cart" → ✅ **Critical**.
