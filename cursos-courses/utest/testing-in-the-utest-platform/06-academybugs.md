# uTest Academy · Testing in the uTest Platform · 06: AcademyBugs.com

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) + [AcademyBugs.com](https://academybugs.com/find-bugs/) |
| Situação / Status | ✅ Concluído · quiz 9 de 9 (2ª tentativa) · **20 de 25 bugs encontrados** / Completed · quiz 9/9 (2nd attempt) · **20 of 25 bugs found** |
| Fonte / Source | [uTest Academy: AcademyBugs.com](https://platform.utest.com/academy/tracks/2/courses/35/lessons/how-to-use-website) (login) |

## O que é / What it is
🇧🇷 Site de loja **de treino**, com **25 bugs plantados**. Cada bug encontrado abre um mini-teste ("que tipo de bug é?" e "qual o resultado esperado?") e, depois, o relatório completo com GIF. O site tem 4 seções: Examples of Bugs, Types of Bugs, **Find Bugs** (a loja) e Report Bugs (praticar relatórios).
🇺🇸 A **practice** shop with **25 planted bugs**. Each find opens a mini-check (type + expected result), then the full report with a GIF.

## Os 20 bugs que encontrei / The 20 bugs I found
> 🇧🇷 Os GIFs são os **oficiais do AcademyBugs**; clique para ver. Os 5 que faltaram exigiam criar conta, fazer login ou enviar e-mail.
> 🇺🇸 GIF links are the **official AcademyBugs** ones. The 5 missing bugs required creating an account, logging in or sending email.

| # | Tipo / Type | Gravidade / Severity | 🇧🇷 O bug | 🇺🇸 The bug | GIF |
|---|---|---|---|---|---|
| 1 | Functional | High | quantidade no carrinho não passa de 2 | cart quantity can't go above 2 | [ver / view](https://academybugs.com/wp-content/uploads/2020/10/1.gif) |
| 2 | Functional | Critical | total geral US$ 100 maior que a soma | grand total is $100 more than the sum | [ver](https://academybugs.com/wp-content/uploads/2020/10/F2.gif) |
| 3 | Functional | Medium | link do fabricante abre página 404 | manufacturer link opens a 404 | [ver](https://academybugs.com/wp-content/uploads/2020/11/Fn3.gif) |
| 4 | Functional | Medium | filtro de preço não filtra | price filter doesn't filter | [ver](https://academybugs.com/wp-content/uploads/2020/10/4.gif) |
| 5 | Functional | Medium | botão de compartilhar no Twitter quebrado | Twitter share button broken | [ver](https://academybugs.com/wp-content/uploads/2020/10/5.gif) |
| 6 | Visual | Medium | imagem da calça não preenche o quadro | jeans image doesn't fill its box | [ver](https://academybugs.com/wp-content/uploads/2020/10/Find-6.gif) |
| 8 | Visual | Low | espaço vazio sob as imagens (All Items) | empty space under images | [ver](https://academybugs.com/wp-content/uploads/2020/10/F8.gif) |
| 9 | Visual | Low | botão Sign In sobrepõe o rodapé | Sign In button overlaps the footer | [ver](https://academybugs.com/wp-content/uploads/2020/10/F9.gif) |
| 10 | Visual | Low | rótulo "Password" desalinhado | "Password" label misaligned | [ver](https://academybugs.com/wp-content/uploads/2020/10/F10.gif) |
| 11 | Content | Low | texto em russo em "New User" | Russian text under "New User" | [ver](https://academybugs.com/wp-content/uploads/2020/10/F11.gif) |
| 12 | Content | Low | símbolos estranhos no mini carrinho ("xz3@#") | garbage symbols in the mini cart | [ver](https://academybugs.com/wp-content/uploads/2020/10/F12.gif) |
| 13 | Content | Medium | descrição do produto em latim | product description not in English | [ver](https://academybugs.com/wp-content/uploads/2020/10/Find-13.gif) |
| 14 | Content | Low | cores "Yelow" e "Orang" | "Yelow" and "Orang" misspelled | [ver](https://academybugs.com/wp-content/uploads/2020/10/14.gif) |
| 15 | Content | Low | "RETURN TO STOR E" (espaço errado) | wrong spacing in "Return to Store" | [ver](https://academybugs.com/wp-content/uploads/2020/10/F15.gif) |
| 19 | Performance | High | produto do Hot Item carrega para sempre | Hot Item product loads forever | [ver](https://academybugs.com/wp-content/uploads/2020/10/19.gif) |
| 20 | Performance | Low | página do MySpace carrega para sempre | MySpace share page loads forever | [ver](https://academybugs.com/wp-content/uploads/2020/10/20.gif) |
| 21 | Crash | High | página trava ao trocar a moeda | page freezes when changing currency | [ver](https://academybugs.com/wp-content/uploads/2020/10/21.gif) |
| 22 | Crash | High | trava ao clicar em 10/25/50 resultados | freezes on results-per-page buttons | [ver](https://academybugs.com/wp-content/uploads/2020/10/22.gif) |
| 23 | Crash | High | trava ao clicar em "Post Comment" | freezes on "Post Comment" | [ver](https://academybugs.com/wp-content/uploads/2020/10/23.gif) |
| 25 | Crash | High | trava ao aumentar a quantidade com cor rosa ou verde | freezes when increasing quantity with pink/green | [ver](https://academybugs.com/wp-content/uploads/2020/10/25.gif) |

### Distribuição / Breakdown
~~~mermaid
pie title Bugs encontrados por tipo / Bugs found by type
    "Functional" : 5
    "Visual" : 4
    "Content" : 5
    "Performance" : 2
    "Crash" : 4
~~~

## Lição de QA / QA lesson
🇧🇷 Na 1ª tentativa errei a pergunta 8 ("adicione 3 unidades pela página do produto"). Achei que o bug do "trava em 2" valia ali, mas, **ao reproduzir, as 3 unidades entraram certinho**: o bug só acontece **no carrinho**, ao atualizar. **Reproduza exatamente os passos antes de concluir.**
🇺🇸 I missed Q8 on the first try by assuming. **Reproducing showed it worked**: the bug only happens **in the cart**. **Reproduce the exact steps before concluding.**

## Quiz comentado / Commented quiz (9/9)
1. Objetivo do site / Purpose → ✅ **ensinar a achar bugs com exemplos práticos** / teach bug finding with practical examples.
2. App fecha sozinho ao clicar num ícone / App quits on icon click → ✅ **Crash**.
3. Fim do menu lateral na página de produto / Bottom of side menu → ✅ **Visual** (Sign In sobre o rodapé / overlaps footer).
4. Trocar a moeda causa crash? / Currency change crash? → ✅ **Sim / Yes** (bug 21).
5. Total calculado errado / Wrong total → ✅ **Functional**.
6. Carrinho de 1 para 4 → Update / Cart 1→4 → Update → ✅ **fica em 2 / becomes 2** (bug 1).
7. Passo que leva a bug de Performance / Step leading to a Performance bug → ✅ **abrir o produto do Hot Item** (❌ moeda = Crash).
8. Adicionar 3 unidades pela página do produto / Add 3 units from product page → ✅ **nenhuma das opções** (funciona) — ⚠️ errei na 1ª tentativa / missed on 1st try.
9. Achou 20 bugs? / Found 20? → ✅ **Sim**, de verdade: 20 / 25.
