# Test IO · Education quiz: Bug Severity

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Education quizzes (oportunidade do painel · dashboard opportunity) |
| Situação · Status | ✅ Enviado · 10 de 14 · 20/11/2026 / Submitted · 10 of 14 |
| Fonte · Source | [How to select the correct severity of a functional bug (Academy)](https://academy.test.io/) · quiz no Typeform |

## Regra prática / Rule of thumb
| Gravidade / Severity | 🇧🇷 Quando | 🇺🇸 When |
|---|---|---|
| **Critical** | fluxo principal travado **sem saída**; app fecha (crash) em caminho principal; **erro de dinheiro** no checkout (preço ou desconto errado); **método de pagamento principal** quebrado, mesmo com outros funcionando | core flow blocked with no workaround; crash on a key path; money/pricing errors; main payment method broken |
| **High** | função **importante** quebrada, mas **existe outro caminho** | important function broken, workaround exists |
| **Low** | problema **intermitente** ou com saída **simples e óbvia** (recarregar, copiar à mão) | intermittent, or quick obvious workaround |
| **Sem gravidade** | bug **visual** ou de **conteúdo** | visual or content bugs have no severity |

> 🇧🇷 A Test IO pesa o **impacto no negócio**, não só se "dá para contornar". 🇺🇸 Test IO weighs **business impact**, not only whether a workaround exists.

## Questões comentadas / Commented questions
| # | Bug | Resposta / Answer | Por quê / Why |
|---|---|---|---|
| 1 | Botão de finalizar compra não faz nada, sem saída | **Critical** | Bloqueia a compra para todos. |
| 2 | Arrastar foto de perfil não funciona; pelo botão funciona | **Low** | Saída fácil, área secundária. |
| 3 | Preço cobre o botão "Add to Cart" no celular | **Visual** | Sem gravidade. |
| 4 | Cartão recusado; PayPal e carteiras funcionam | **Critical** ⚠️ *errei (High)* | Método de pagamento **principal** afetado. |
| 5 | "Add to Cart" não funciona em nenhum produto | **Critical** | Sem caminho para comprar. |
| 6 | Busca sempre sem resultado; dá para navegar por categorias | **High** ⚠️ *errei (Critical)* | Função importante, mas com saída viável. |
| 7 | Botão "Copiar código" não copia; dá para copiar à mão | **Low** | Impacto mínimo, saída óbvia. |
| 8 | Miniatura de um produto quebrada | **Conteúdo** | Sem gravidade. |
| 9 | Cupom "aplicado", mas o total não muda | **Critical** | Erro de preço no checkout (dinheiro). |
| 10 | App fecha ao tocar em "Login" | **Critical** | Crash em caminho principal. |
| 11 | Símbolo de moeda misturado ($/£), valores certos | **Conteúdo** ⚠️ *errei (High)* | Texto errado, não função. |
| 12 | Filtro falha em ~20% das vezes; recarregar resolve | **Low** | Intermitente com saída simples. |
| 13 | Cadastro recusa Gmail/Yahoo; login social funciona | **High** ⚠️ *errei (Critical)* | Afeta muita gente, mas tem saída. |
| 14 | "Buy Now" falha em um produto; carrinho funciona | **High** | Atalho importante, escopo limitado. |
