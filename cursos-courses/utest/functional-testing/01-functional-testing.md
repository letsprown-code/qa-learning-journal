# uTest Academy · Functional Testing · 01: Functional Testing

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: Functional Testing](https://platform.utest.com/academy/tracks/4/courses/147/lessons/introduction-to-functional-testing) (login) |
| Referências / References | [ISTQB Glossary](https://glossary.istqb.org/) |
| Comparar com / Compare with | [Test IO: 02 How to find bugs?](../../test-io/exploratory-testing/02-how-to-find-bugs.md) |

## O que é / What it is
🇧🇷 **Teste funcional** confere se cada recurso do produto **funciona como deveria** e segue os requisitos. O testador age como um usuário, compara o **resultado real** com o **esperado** e, se forem diferentes, é **bug**. 🇺🇸 Checks that each feature **works as intended**; actual ≠ expected → **bug**.

**Metodologias no uTest / Methodologies at uTest:** **Test Case (roteirizado / scripted)** e **Exploratório / Exploratory**. O ciclo pode usar uma delas ou as duas.

## Tipos de teste funcional / Functional testing types
| Tipo / Type | 🇧🇷 Em uma frase | 🇺🇸 In one line |
|---|---|---|
| **Unit** | uma peça pequena do código (ex.: a função que valida senha) | single unit/function |
| **Component** | um módulo inteiro (ex.: o login todo) | a whole module |
| **Smoke** | logo após uma nova versão: **o essencial funciona?** (abrir, logar, carrinho, checkout) | after a build: **critical functions OK?** |
| **Sanity** | depois do smoke: **a correção ou o recurso novo funcionou?** | after smoke: **did the fix/new feature work?** |
| **Regression** | **o que já funcionava continua funcionando** depois da mudança | **existing features still work** |
| **Ad-hoc** | informal, sem roteiro; o exploratório é um exemplo | informal; exploratory is an example |
| **Integration** | várias partes juntas trocando dados certo | combined parts exchange data |
| **System** | o sistema inteiro, de ponta a ponta | end-to-end |
| **UAT** | usuários reais ou o cliente aprovam antes do lançamento | real users approve before release |
| **Interface** | comunicação entre sistemas (APIs, serviços externos) | system-to-system communication |

~~~mermaid
flowchart LR
    B[Nova versão<br/>New build] --> S[Smoke:<br/>o essencial funciona?]
    S --> SA[Sanity:<br/>a correção funcionou?]
    SA --> R[Regression:<br/>o resto continua funcionando?]
~~~

## SDLC (ciclo de vida do software / software development life cycle)
~~~mermaid
flowchart LR
    P[Planning] --> A[Analysis] --> D[Design] --> I[Implementation] --> T[Testing] --> DE[Deployment] --> M[Maintenance]
    M -.feedback.-> P
~~~
🇧🇷 A fase **Testing** é a que busca garantir que o software esteja **sem defeitos** e cumpra os requisitos. Achar bug cedo **sai mais barato** do que depois do lançamento. 🇺🇸 **Testing** phase aims for defect-free software; early bugs are **cheaper** to fix.

## Manual × automação / Manual vs automation
| | 🇧🇷 Manual | 🇺🇸 Automation |
|---|---|---|
| Força / Strength | avalia o **subjetivo**: facilidade de uso, aparência, experiência; se adapta rápido a mudanças; base do teste exploratório | fast, repeatable; great for **regression**, load and performance |
| Fraqueza / Weakness | lento, sujeito a erro humano, ruim para tarefas repetitivas, difícil simular milhares de usuários | needs scripts and maintenance |

💡 🇧🇷 O uTest entrega **teste manual em escala**: muitos testadores, em muitos aparelhos e países reais. 🇺🇸 uTest = manual testing at scale on real devices.

## Test Case (roteirizado / scripted)
- 🇧🇷 Siga os passos. Se o **resultado real = esperado → Pass**; se for **diferente → Fail** e reporte o bug, a menos que ele já esteja reportado ou na lista de *known issues*. 🇺🇸 Actual = expected → **Pass**; otherwise **Fail** + report.
- 🇧🇷 **Antes:** leia o test case inteiro, veja as pré-condições e **pergunte ao TTL** se algo não estiver claro (não chute). Prepare o ambiente e os dados, limpe o cache se precisar e deixe a ferramenta de print ou vídeo pronta. Só abra o app quando o passo mandar. 🇺🇸 Read it all, check preconditions, ask the TTL, prepare environment and capture tools.
- 🇧🇷 **Vantagens:** clareza e reprodutibilidade, cobertura completa, métricas de progresso, fácil para iniciantes, menos erro humano, funciona como documentação. 🇺🇸 Clarity, coverage, metrics, beginner-friendly.

## Exploratório / Exploratory
🇧🇷 **Aprender, desenhar e executar testes ao mesmo tempo**: cada teste nasce do que você observou no anterior. No exploratório, o pagamento é pelos **bugs e trabalhos aprovados**, não por hora. 🇺🇸 **Simultaneous learning, test design and execution**; paid per approved work, not hourly.

~~~mermaid
flowchart TD
    N[Abrir um bloco de notas<br/>Open notes] --> E[Explorar como usuário,<br/>sem caçar bug ainda<br/>Explore as a user]
    E --> V[Voltar às áreas suspeitas<br/>Target suspicious areas]
    V --> C[Cenários reais + variações incomuns<br/>Real + unusual scenarios]
    C --> F[Seguir a trilha: 1 bug leva a outros<br/>Follow the trail]
    F --> V
~~~

## Técnicas / Techniques
| Técnica / Technique | 🇧🇷 Ideia + exemplo (campo que aceita 1 a 100) | 🇺🇸 Idea |
|---|---|---|
| **Equivalence Class Partitioning** | divide as entradas em grupos que se comportam igual e testa **1 de cada**: -25 (inválido), 50 (válido), 125 (inválido) | one value per class |
| **Boundary Value Analysis** | testa as **bordas**: 0, 1, 2 e 99, 100, 101 | test the **edges** |
| **Decision Table** | tabela com **todas as combinações** de condições (ex.: plano de 1, 3 ou 12 meses × cliente novo ou antigo → desconto) | all condition combinations |
| **State Transition** | como o sistema muda de **estado** conforme a sequência de ações (ex.: PIN errado 1-2× → aviso; 3× → cartão bloqueado) | state changes by event sequence |

## Funcional × não funcional / Functional vs non-functional
| | 🇧🇷 Funcional | 🇺🇸 Non-functional |
|---|---|---|
| Pergunta / Question | **O QUE** o software faz? (o botão funciona? o login entra? a busca acerta?) | **HOW** does it perform? (speed, 1,000 users, security, ease of use) |
| Tipos / Types | unit, smoke, sanity, regression, integration, system, UAT… | performance (load, stress, spike, endurance), security, usability, reliability, scalability, compatibility |
| Técnica / Technique | normalmente **caixa-preta**, sem olhar o código | |

🇧🇷 O funcional é a **base**: não adianta medir a velocidade de algo que não funciona. 🇺🇸 Functional is the **foundation** for non-functional testing.

## Quiz comentado / Commented quiz (10/10)
1. Objetivo do teste funcional / Main goal → ✅ **Garantir que os recursos funcionem como deveriam e sigam os requisitos.**
2. Duas metodologias no uTest / Two methodologies → ✅ **Exploratório e Test Case (roteirizado)**.
3. Depois de uma versão nova, checar o essencial / Critical functions after update → ✅ **Smoke** (Sanity é a correção específica; Regression é o resto).
4. Fase do SDLC que busca software sem bugs / SDLC phase → ✅ **Testing**.
5. Força do teste manual / Manual strength → ✅ **Avaliar aspectos subjetivos, como facilidade de uso e aparência**.
6. Vantagem do Test Case / Test Case advantage → ✅ **Clareza e reprodutibilidade com passo a passo**.
7. Real diferente do esperado / Actual ≠ expected → ✅ **Marcar o passo como Failed**.
8. O que é exploratório / Exploratory → ✅ **Aprender, desenhar e executar testes ao mesmo tempo**.
9. Testar mínimo, máximo e valores logo dentro e fora dos limites / Min/max and edges → ✅ **Boundary Value Analysis**.
10. Diferença do não funcional / Non-functional difference → ✅ **Foca na qualidade e em COMO o sistema se comporta em várias condições**.
