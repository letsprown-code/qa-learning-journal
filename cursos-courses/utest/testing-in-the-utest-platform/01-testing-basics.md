# uTest Academy · Testing in the uTest Platform · 01: Testing Basics

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Trilha / Track | Testing in the uTest Platform (2 de 7 trilhas · course 1 of 7) |
| Situação / Status | ✅ Concluído · quiz 5 de 5 / Completed · quiz 5 of 5 |
| Fonte / Source | [uTest Academy: Testing Basics](https://platform.utest.com/academy/tracks/2/courses/34/lessons/testing-types) (precisa de login / login required) |
| Prática / Practice | [AcademyBugs.com](https://academybugs.com/find-bugs/), site de treino oficial / official practice site |

## Resumo / Summary

| 🇧🇷 Português | 🇺🇸 English |
|---|---|
| **Testar** = avaliar um produto para achar falhas, erros, melhorias ou requisitos faltando. | **Testing** = evaluating a product to find gaps, errors, improvements or missing requirements. |
| Por que testar: qualidade, satisfação do cliente, segurança e **custo menor** (bug achado cedo sai mais barato). | Why: quality, customer satisfaction, security and **lower cost** (early bugs are cheaper). |
| Tipo mais comum na uTest: **Functional**. Outros: Exploratory, Regression, Smoke, Usability, Localization, Security, Payment, Accessibility, API, Voice, **Bug Hunt** (só o bug pedido; fora disso = OOS/DNFI) e On-site. | Most common at uTest: **Functional**. Others listed; in **Bug Hunt** cycles report only what's asked (anything else = OOS/DNFI). |

### Os 5 tipos de bug / The 5 bug types

| Tipo / Type | 🇧🇷 Exemplo | 🇺🇸 Example |
|---|---|---|
| Functional | botão não responde, link quebrado, busca errada | button doesn't respond, broken link, wrong search results |
| Visual | elemento desalinhado, imagem faltando | misaligned element, missing image |
| Content | erro de ortografia, tradução errada | spelling or translation error |
| Performance | lentidão; congelar **mais de 10 s** | slowness; freezing **over 10 s** |
| Crash | app ou página fecha ou trava de vez | app or page closes or hangs for good |

### Quando um "bug" NÃO é bug / When an "issue" is NOT an issue

~~~mermaid
flowchart TD
    A[Achei algo estranho<br/>Found something odd] --> B{Está funcionando<br/>como foi projetado?<br/>Working as designed?}
    B -- Sim / Yes --> W[WAD: não reporte<br/>ou é só feedback<br/>Don't report, it's feedback]
    B -- Não / No --> C{Está no escopo?<br/>In scope?}
    C -- Não / No --> O[OOS: não reporte<br/>Don't report]
    C -- Sim / Yes --> D{Já foi reportado<br/>ou é Known Issue?<br/>Already reported / KI?}
    D -- Sim / Yes --> P[Faça +1 com anexo<br/>Do a +1 with attachment]
    D -- Não / No --> E{Reproduz de novo?<br/>Reproducible?}
    E -- Não / No --> F[Limpe cache, reinicie e tente de novo<br/>Clear cache, restart, retry]
    E -- Sim / Yes --> R[Reporte seguindo as instruções<br/>Report following the instructions]
~~~

- 🇧🇷 **Gosto pessoal não é bug.** Quanto mais perto de "não funciona como projetado", mais chance de aprovação. Quanto mais perto de "eu preferiria assim", mais é feedback. 🇺🇸 **Personal preference isn't a bug.**
- 🇧🇷 **Teste como usuário real**, não como "caçador de bugs": digitar centenas de caracteres num campo raramente é aprovado. 🇺🇸 **Test like a real user**: extreme negative tests are rarely approved.
- 🇧🇷 **Prepare o ambiente:** desligue extensões (ad-block), limpe cookies e cache, desligue VPN, feche abas desnecessárias. 🇺🇸 **Prepare your system:** disable extensions, clear cache, no VPN.

### Caso de teste / Test case
- 🇧🇷 Siga os passos **na ordem**, cumpra as pré-condições, marque **Pass** ou **Fail** e escreva observações. Todo passo com **Fail precisa ter um bug ligado** (novo ou +1). 🇺🇸 Follow steps **in order**, meet preconditions, mark Pass/Fail; **every failed step needs a linked bug**.
- 🇧🇷 Nome de arquivo sugerido: <code>Cliente_TesteX_macOS_Safari</code>. 🇺🇸 Suggested file name: <code>Client_TestX_macOS_Safari</code>.

### Instalar apps de teste / Installing test apps
- **Android:** pela Play Store, por **APK** (permitir "fontes desconhecidas") ou por QR code. **Confira a versão** em Configurações > Apps. / Play Store, **APK** (allow unknown sources) or QR code. **Check the version.**
- **iOS:** pela App Store, **TestFlight** ou IPA (confiar no perfil em Ajustes > Geral > VPN e Gerenciamento de Dispositivos). / App Store, **TestFlight** or IPA (trust the profile).

### Nomes dos elementos da página / Page element names
Hero, Banner, Carousel, Hamburger menu, Breadcrumb, Pop-up, Toggle, Checkbox, Radio button, Drop-down, Tabs, Footer · Páginas / Pages: Homepage, **PLP** (lista de produtos / product list), **PDP** (detalhe do produto / product detail), Cart, About us.

## Quiz comentado / Commented quiz (5/5)

1. **App lento com internet boa / Slow app on good internet** → ✅ **Performance.** ❌ Functional = não funciona; Visual = layout; Content = texto. / Functional = broken; Visual = layout; Content = text.
2. **Pode reportar bug já reportado? / Report an already-reported bug?** → ✅ **Falso / False.** Seria rejeitado como DUP; faça **+1** (isso ainda ajuda o rating). / Rejected as DUP; do a **+1** (it helps your rating).
3. **Primeiro passo para testar / First step of testing** → ✅ **Ler e entender o Overview.** / Read and understand the Overview.
4. **O que NÃO é boa prática / NOT good practice** → ✅ **Reportar bug placeholder** (proibido). / Placeholder bugs (forbidden).
5. **Testar NÃO ajuda em... / Testing does NOT help with...** → ✅ **Nenhuma das anteriores**: testar ajuda em todas. / **None of the above**: it helps with all.
