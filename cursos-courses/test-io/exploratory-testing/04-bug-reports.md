# Test IO · Módulo 4: Relatórios de bug · Module 4: Bug Reports

**Português (Brasil)** | [English below](#english)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 4 de 4 · Bug Reports |
| Situação · Status | ✅ Concluído: 2 tarefas aprovadas e curso Exploratory Testing 4 de 4 (conferido em 17/11/2026) · Completed: 2 tasks approved, Exploratory Testing course 4 of 4 |
| Fonte original · Original source | [Bug Report Requirements, Test IO Academy](https://academy.test.io/en/articles/2541949-bug-report-requirements) |

Estas são as minhas anotações, escritas com as minhas palavras. · These are my own notes.

## Os campos do relatório de bug

| Campo | Regra | Dica prática |
| --- | --- | --- |
| **Feature** | Escolher primeiro a função do escopo onde o bug está | Se ela não aparece na lista, ler e marcar como lidas as descrições das funções do teste |
| **Severity** (só funcional) | Low, High ou Critical, conforme o impacto | Ver as definições do módulo 1. Se a função não fecha, trava ou cobre partes importantes da tela, provavelmente não é Low |
| **Title** | Resume o bug: **o quê**, **onde** e **quando ou em que condição** | Descrever o que acontece, nunca "não funciona". Incluir a condição se o bug só acontece nela |
| **URL** | Endereço da página onde o bug acontece | Copiar da barra de endereço. Link quebrado: a URL é a da página com o link, não a da página de erro |
| **Steps** | Um passo por ação, do início até a ação que causa o bug | O 1º passo abre o site ou o app. Passos gerais ("any product"), a não ser que o bug dependa de algo específico. O mínimo de passos possível |
| **Actual result** | O que aconteceu, com detalhes e exemplos | Não pode ser igual ao título nem só o contrário do esperado |
| **Expected result** | Como deveria ser se não houvesse bug | **Impessoal**: descrever o estado da tela. **Não usar "the user should"** nem dar instruções |
| **Attachment** | Print ou gravação que prova o bug | Regras do módulo 3 |
| **Used environment** | O aparelho e o navegador usados | Só um, o mesmo do convite. Bug em outros aparelhos vai no resultado atual |

**Outras regras:** não enviar relatório incompleto para completar depois. Usar dados realistas, nada como "asdfgh". Dá para editar depois de enviar (menos o tipo de bug) e apagar se o líder do time ainda não revisou.

## Tarefa 1: relatório de bug funcional (comentado)

**O que o vídeo mostrava:** numa loja, o resumo de avaliações abre normal na página de busca. Na página do produto, ao clicar na seta de "677 Reviews", ele abre no canto de cima, por cima do cabeçalho, cortado e sem o botão de fechar. Clicar na seta de novo não fecha.

| Campo | O que enviei |
| --- | --- |
| Severity | High |
| Title | Product details page - "Summary of Reviews" pop-up opens cut off at the top of the page and cannot be closed after clicking the reviews arrow |
| URL | https://www.dummy.com/product_details_page |
| Steps | 1. Open https://www.dummy.com/ · 2. Click on the search bar in the top-right corner, type "robot" and press Enter · 3. Click on the "Dyson 360 Vis Nav" product · 4. On the product details page, click on the arrow next to "677 Reviews" · 5. Click on the arrow next to "677 Reviews" again |
| Actual result | Explica onde o pop-up abre, o que fica cortado (título, X, texto), que ele não fecha e que **na página de busca funciona** (é a prova de que é bug) |
| Expected result | After the arrow next to "677 Reviews" is clicked again, the "Summary of Reviews" pop-up is closed. While open, the pop-up is displayed directly below the "677 Reviews" link and is fully visible, including its title, the complete review summary and the close (X) button, as on the search results page. |

**O que a IA corrigiu na 1ª tentativa:**

1. **Gravidade:** eu tinha colocado Low. A IA apontou que um pop-up que **não fecha** e **cobre o cabeçalho e a busca** é mais do que um problema pequeno. Mudei para **High**.
2. **Resultado esperado:** eu tinha escrito "the user should be able to close it...". A IA não aceita **"the user should"** nem instruções. Reescrevi descrevendo **o estado da tela**.

A IA aprovou na 2ª tentativa.

## Tarefa 2: relatório de bug visual (comentado)

**O que o print e o vídeo mostravam:** na página de um produto, ao clicar na lupa do cabeçalho, o campo de busca abre com a parte de cima escondida atrás do cabeçalho. O texto "Search" e a palavra digitada aparecem cortados em cima.

| Campo | O que enviei |
| --- | --- |
| Bug type | Visual (texto cortado; a busca funciona, só aparece mal) |
| Title | Product details page - Search field text is cut off at the top after opening the search from the header |
| URL | https://www.dummy.com/product_details_page |
| Steps | 1. Open https://www.dummy.com/ · 2. Click on "SLEEP" in the navigation menu · 3. Click on any product · 4. On the product details page, click on the search (magnifying glass) icon in the top-left corner of the header · 5. Type any search term in the search field (e.g., "massage") |
| Actual result | Explica que o campo abre logo abaixo do menu, que a parte de cima fica escondida e que só a metade de baixo das letras aparece |
| Expected result | The search field is displayed fully below the navigation menu, and both the placeholder "Search" and the entered search term (e.g., "massage") are completely visible. |

A IA aprovou na 1ª tentativa, porque já apliquei o que aprendi na tarefa 1.

## O que levar deste módulo

- **Título:** o quê + onde + quando. Nunca "não funciona".
- **Passos:** começam abrindo o site, terminam na ação que causa o bug, e são gerais.
- **Resultado atual:** detalhado, com a prova de que é bug (por exemplo, "em outra página funciona").
- **Resultado esperado:** impessoal, descrevendo a tela. Sem "the user should".
- **Gravidade:** pensar no impacto real. Função que não fecha ou bloqueia partes importantes não é Low.

---

<a id="english"></a>

## English

Bug report fields: Feature first; Severity (functional only); Title with what, where and when, describing the actual behavior (never "doesn't work"); URL of the page where the bug occurs; one action per step, starting by opening the site or app and ending with the action that triggers the bug, as general as possible; detailed Actual result, different from the title and not just the opposite of the expected result; impersonal Expected result describing the correct UI state (no "the user should", no instructions); attachment; one used environment.

Practical tasks: a functional bug (reviews summary pop-up cut off and impossible to close on the product details page; severity changed from Low to High and expected result rewritten impersonally after AI feedback, approved on the 2nd attempt) and a visual bug (search field text cut off under the header on the product details page; approved on the 1st attempt).
