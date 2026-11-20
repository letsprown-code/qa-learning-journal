# Test IO · Education quiz: In or Out of Scope?

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Education quizzes (oportunidade do painel · dashboard opportunity) |
| Situação · Status | ✅ Enviado · 14 de 15 · 20/11/2026 / Submitted · 14 of 15 |
| Fonte · Source | [Test Scope (Academy)](https://academy.test.io/) · quiz no Typeform |

## Ideia central / Key idea
🇧🇷 Antes de reportar, confira **cada parte das instruções do teste**: ambiente, tipos de bug permitidos, fora do escopo, requisitos adicionais, funcionalidades (*features*), aparelhos, anexos e **avisos do líder do teste (TL) no chat**. Se uma delas exclui o bug, ele está fora do escopo, mesmo que seja um bug de verdade.
🇺🇸 Before reporting, check **every part of the test instructions**: environment, allowed bug types, out of scope, additional requirements, features, devices, attachments and **TL announcements in the chat**. If any of them excludes the bug, it is out of scope, even if it is a real bug.

~~~mermaid
flowchart TD
    B[Achei um bug] --> E{Ambiente indicado?}
    E -- não --> X[Fora do escopo]
    E -- sim --> T{Tipo de bug permitido?<br/>e gravidade permitida?}
    T -- não --> X
    T -- sim --> F{Feature listada?<br/>e não excluída por TL/anexo/requisitos?}
    F -- não --> X
    F -- sim --> D{Aparelho e navegador pedidos?}
    D -- não --> X
    D -- sim --> R[Reportar ✅]
~~~

## Questões comentadas / Commented questions
| # | Situação / Situation | Resposta / Answer | Por quê / Why |
|---|---|---|---|
| 1 | Texto do botão "Subscribe" cortado na Home; só bugs **funcionais** permitidos | ❌ Não reportar | É bug **visual**, tipo não permitido. / Visual bug, not allowed. |
| 2 | Filtro por preço mostra produtos errados na PLP | ✅ Reportar | Funcional, PLP está nas features. / Functional, PLP in scope. |
| 3 | Pagamento falha ao fazer pedido; termos dizem "No orders allowed!" | ❌ Não reportar | Fazer pedido é proibido. Desobedecer pode trazer **consequências para a conta**. / Placing orders is forbidden; it can hurt your account. |
| 4 | Fui redirecionada para produção e achei bug na página de produto | ❌ Não reportar | Só vale o ambiente indicado (staging), **mesmo com redirecionamento automático**. / Only the given environment counts, even after an automatic redirect. |
| 5 | Subcategorias se sobrepõem ao passar o mouse no **menu do cabeçalho** da Home | ❌ Não reportar ⚠️ *errei* | Menu do cabeçalho = feature **Navigation**, não "Homepage". Navigation não estava listada. / Header menu = **Navigation** feature, not Homepage. |
| 6 | Checkout: campos de endereço desabilitados | ✅ Reportar | Checkout está no escopo; dá para testar sem fazer o pedido. / In scope as long as you don't place the order. |
| 7 | Busca por "t-shirt" não acha nada | ❌ Não reportar | Requisito adicional: "não testar a busca". / Additional requirement excludes search. |
| 8 | No app, "Termos e Condições" abre página web com outro visual | ❌ Não reportar | **Web Viewer** é fora do escopo por padrão; na dúvida, perguntar ao TL. / Web Viewer is out of scope by default. |
| 9 | Nome errado do produto no carrinho | ✅ Reportar | Sem contradição com as instruções. / No conflict with instructions. |
| 10 | "Add to Wishlist" na PLP não faz nada; só bugs **Critical** permitidos | ❌ Não reportar | É **High**, não Critical. / High severity, only Critical allowed. |
| 11 | Bug só no Chrome do iOS; iOS pede **Safari** | ❌ Não reportar | Só o navegador pedido. / Only the requested browser. |
| 12 | Filtro por preço errado; anexo diz que **só o filtro por nome** deve funcionar | ❌ Não reportar | O anexo limita o escopo. / The attachment limits scope. |
| 13 | Ícone de "entrega rápida" quebrado na página de produto; fora do escopo: imagens de produto | ✅ Reportar | Ícone ≠ imagem de produto. / An icon is not a product image. |
| 14 | Não salva alterações no perfil; TL avisou "não reportar Account" | ❌ Não reportar | Perfil = feature **Account**, retirada pelo TL. / Profile = Account, removed by TL. |
| 15 | Imagens de produto quebradas no carrinho | ❌ Não reportar | "Product images" está fora do escopo. / Out of scope. |

## Lição / Lesson
🇧🇷 **Header, Navigation e Footer são features separadas** da Homepage e da Landing Page, a não ser que as instruções digam outra coisa.
🇺🇸 **Header, Navigation and Footer are separate features** from Homepage and Landing Page unless instructed otherwise.
