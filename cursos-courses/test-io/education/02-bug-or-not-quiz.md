# Test IO · Education quiz: Bug or Not?

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Education quizzes (oportunidade do painel · dashboard opportunity) |
| Situação · Status | ✅ Enviado · 14 de 15 · 20/11/2026 / Submitted · 14 of 15 |
| Fonte · Source | [Common mistakes in testing (Academy)](https://academy.test.io/) · quiz no Typeform |

## Ideia central / Key idea
🇧🇷 Nem todo problema é bug. **Problemas de preparação** (setup) vão para o **TL no chat**; problemas causados por **extensões ou ferramentas da testadora** não contam; e **comportamentos de segurança** esperados não são bug.
🇺🇸 Not every problem is a bug. **Setup issues** go to the **TL via chat**; issues caused by **the tester's own extensions or tools** don't count; and expected **security behaviors** are not bugs.

| Categoria / Category | Exemplos / Examples | O que fazer / What to do |
|---|---|---|
| **Setup** | build não baixa ou não instala; URL do ambiente dá 404 ou 403; credenciais do cliente não funcionam; ambiente fora do ar por um tempo | Avisar o TL no chat / Tell the TL |
| **Ferramenta da testadora** | AdBlock, antivírus, extensões, **Google Tradutor** | Não reportar; desligar antes de gravar / Not a bug; disable before recording |
| **Comportamento esperado** | mensagem genérica para e-mail já cadastrado (privacidade); bloqueio de e-mail descartável; área clicável maior no checkbox | Não reportar / Not a bug |
| **Sugestão de usabilidade** | falta mensagem de confirmação que não está na especificação | Não é bug / Usability suggestion |
| **Bug de verdade** | campo inacessível por causa do teclado; mensagem de erro que não corresponde à ação; "produto adicionado" ao adicionar zero | Reportar ✅ / Report |

## Questões comentadas / Commented questions
| # | Situação / Situation | Resposta / Answer | Por quê / Why |
|---|---|---|---|
| 1 | Erro de ortografia no site | ❌ ⚠️ *errei* | Na Test IO, ortografia **não** é bug de conteúdo, a não ser que as instruções peçam. / Spelling mistakes are not content bugs unless stated. |
| 2 | Build beta não baixa ou não instala | ❌ | Setup → TL. |
| 3 | Teclado do Android deixa o campo **totalmente inacessível** | ✅ | Bug válido. Só cobrir o campo (dá para rolar) **não** é bug. / Valid; merely covering it is not. |
| 4 | Sem mensagem de confirmação ao remover do carrinho (nada na especificação) | ❌ | Sugestão de usabilidade. / Usability suggestion. |
| 5 | E-mail já cadastrado → "Invalid user email" genérico | ❌ | Intencional, por privacidade e segurança. / Intentional for privacy. |
| 6 | Ambiente fora do ar por um tempo | ❌ | Temporário; o cliente pode estar atualizando. / Temporary. |
| 7 | Filtro para de funcionar com AdBlock ligado | ❌ | Extensões não contam. / Extensions don't count. |
| 8 | Redefinir senha igual à anterior → "Sua conta está bloqueada!" (não está) | ✅ | Mensagem não corresponde à ação: bug funcional. / Message doesn't match input. |
| 9 | Clicar perto do checkbox marca o checkbox | ❌ | Padrão de UX (área clicável ampliada). / Standard UX pattern. |
| 10 | Bug só aparece com o Google Tradutor ligado | ❌ | O tradutor altera o conteúdo. / Translator changes content. |
| 11 | URL do ambiente dá 404 | ❌ | Setup → TL. |
| 12 | Não aceita e-mail descartável (@yopmail etc.) | ❌ | Esperado; testar com Gmail/Yahoo antes. / Expected; try Gmail first. |
| 13 | Adicionar **zero** produtos mostra "adicionado com sucesso" | ✅ | Comportamento ilógico: bug. / Illogical: bug. |
| 14 | 403 ao abrir o link do ambiente | ❌ | Provavelmente o cliente bloqueou o seu país; perguntar ao TL. / Likely geo-blocked. |
| 15 | Credenciais do cliente não funcionam | ❌ | Setup do cliente → TL. |
