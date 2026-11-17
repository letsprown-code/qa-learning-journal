# Test IO · Módulo 1: Tipos de bug · Module 1: Bug Types

**Português (Brasil)** | [English below](#english)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 1 de 4 · Bug Types |
| Situação · Status | Em andamento · In progress |
| Fonte original · Original source | [Bug Types - Summary, Test IO Academy](https://academy.test.io/en/articles/4325756-bug-types-summary) |

Estas são as minhas anotações, escritas com as minhas palavras. · These are my own notes.

## O que é um bug

Um **bug** é um problema no software: algo no site ou no aplicativo que não funciona do jeito que deveria.

O Test IO separa os bugs em quatro tipos:

| Tipo em português | Nome em inglês | Em uma frase |
| --- | --- | --- |
| Funcional | Functional bug | Uma ação não dá o resultado esperado |
| De conteúdo | Content bug | Texto, imagem, link ou dado está faltando, quebrado ou errado |
| Visual | Visual bug | A tela aparece desalinhada, cortada ou sobreposta |
| Sugestão de usabilidade | Usability suggestion | Uma ideia para deixar o produto mais fácil de usar (não é um defeito) |

## 1. Bug funcional

Acontece quando eu faço uma ação e o produto não responde como deveria. Exemplos: um botão que não envia o formulário, uma busca que não reage ao que eu digito, um app que fecha sozinho.

**Como confirmar que é bug, e não uma escolha da empresa:**

- Testar a função sozinha e junto com outras, para ver se o comportamento muda.
- Pensar no que o cliente quis fazer. Funcionar diferente de outros sites **não** é bug.
- Ter **prova**. Exemplo: para dizer que um campo deveria ser validado, mostrar que ele é validado em um caso e não em outro. Sem prova, é só opinião.
- Se a função se comporta sempre do mesmo jeito, sem problema óbvio, provavelmente é intencional.

### Gravidade (severity) de um bug funcional

| Nível | Quando usar |
| --- | --- |
| **Low** (baixa) | Pouco impacto. O uso geral continua normal, afeta poucos usuários ou itens, ou existe um jeito fácil de contornar. |
| **High** (alta) | Impacto sério, mas a função principal continua funcionando. Afeta muitos usuários, ou uma função importante quebrou (com ou sem forma de contornar). |
| **Critical** (crítica) | Impede a função principal. Trava o processo principal (por exemplo, finalizar a compra) ou pode causar perda de vendas. |

O Test IO tem uma lista com a gravidade já definida para casos comuns (Bug Assessment Sheet). Vale consultar sempre.

## 2. Bug de conteúdo

Problema no **conteúdo**: textos, rótulos, imagens, vídeos, ícones, links e dados. Exemplos:

- link ou imagem quebrada (erro 404);
- redirecionamento errado;
- texto faltando, como uma dica (tooltip) vazia;
- área de conteúdo vazia;
- 4 de 5 ícones têm dica e 1 não tem;
- tradução faltando, como botões em francês num site em inglês;
- produto que não aparece na busca, embora a busca funcione;
- dados faltando.

**Atenção:** erro de ortografia **não** conta como bug de conteúdo no Test IO e não pode ser enviado.

## 3. Bug visual

Problema na **aparência** da tela. Exemplos:

- textos ou elementos desalinhados;
- problema de layout responsivo, quando algo aparece em um celular e não em outro;
- elementos sobrepostos sem querer;
- textos ou elementos cortados.

## Quando um bug de conteúdo ou visual vira funcional

Se o problema de conteúdo ou visual **impede uma função**, ele deve ser enviado como **bug funcional**.

Caso importante: link quebrado no **menu de navegação, cabeçalho, rodapé ou trilha de navegação (breadcrumb)** é enviado como **bug funcional de gravidade baixa (Low)**, e não como bug de conteúdo.

## Problemas repetidos

Se o mesmo problema de conteúdo ou visual aparece em vários lugares, envio **um único relatório** e cito as outras páginas ou itens afetados. Um relatório para cada ocorrência é **rejeitado**.

## Resumo para revisar antes do quiz

- 4 tipos: funcional, conteúdo, visual e sugestão de usabilidade.
- Funcional precisa de prova de que não é o comportamento planejado.
- 3 gravidades para funcional: Low, High e Critical.
- Ortografia não é bug de conteúdo.
- Link quebrado em menu, cabeçalho, rodapé ou breadcrumb é funcional Low.
- Visual ou conteúdo que bloqueia uma função vira funcional.
- Problema repetido: um relatório só.

---

<a id="english"></a>

## English

### What a bug is

A **bug** is a software problem: something on a website or app that does not work as intended. Test IO uses four bug types:

| Type | In one sentence |
| --- | --- |
| Functional bug | An action does not produce the expected result |
| Content bug | Text, image, link or data is missing, broken or wrong |
| Visual bug | The screen looks misaligned, cut off or overlapping |
| Usability suggestion | An idea to make the product easier to use (not a defect) |

### Functional bugs and severity

To report a functional bug, I need evidence that the behavior is not intended (for example, a field validated in one case but not another). Working differently from other websites is not a bug.

| Severity | When to use it |
| --- | --- |
| Low | Minimal impact, few users or items affected, or an easy workaround exists |
| High | Serious impact but the main functionality still works; many users affected, or important functionality broken |
| Critical | Blocks core functionality or the main process (such as checkout), or may cause lost sales |

### Key rules

- Spelling mistakes are **not** content bugs on Test IO.
- A content or visual problem that blocks a function is reported as a **functional** bug.
- Broken links in the navigation menu, header, footer or breadcrumb are **Low functional** bugs.
- Repeated content or visual problems go in **one** report that lists the other places affected.
