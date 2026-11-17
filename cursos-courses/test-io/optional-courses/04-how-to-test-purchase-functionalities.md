# Test IO · How to Test Purchase Functionalities Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 5 de 5 (mínimo 3) · 17/11/2026 / Completed · 5 of 5 |
| Fonte · Source | [Preventing Purchases and Orders](https://academy.test.io/en/articles/5444270-preventing-purchases-and-orders) |

> 🛑 🇧🇷 **"Na dúvida se deve clicar num botão, não clique."** Pergunte ao TL no chat do teste. 🇺🇸 **"If unsure whether to click a button, don't."** Ask the TL.

## Por que não comprar em ambiente real / Why never buy on live sites
- 🇧🇷 O cliente tenta **entregar o pedido** e tem trabalho manual para cancelar. 🇺🇸 Manual cancellation work.
- 🇧🇷 Pedidos cancelados **estragam as métricas de vendas** e a taxa de conversão. 🇺🇸 Hurts sales metrics.
- 🇧🇷 Até uma **tentativa** de pedido pode gerar **taxas no meio de pagamento**, um custo sem valor nenhum para o cliente. 🇺🇸 Payment-provider fees even for attempts.

## Como evitar / How to avoid

~~~mermaid
flowchart LR
    C[Carrinho] --> E[Entrega/Dados] --> P{Tela de pagamento}
    P -- ❌ --> X1[Continue to PayPal<br/>PayPal Express<br/>Amazon Express]
    P --> F[Última etapa do checkout]
    F -- ❌ --> X2[Complete order / Finish order<br/>Complete purchase / booking]
    F -- ✅ --> L[Parar e SAIR da página]
~~~

- 🇧🇷 Na **tela de pagamento**, leia tudo com calma: qualquer botão de "continuar" depois de escolher o pagamento pode iniciar a cobrança. 🇺🇸 Read every label on the payment step.
- 🇧🇷 **Não envie o formulário com campos obrigatórios vazios**: isso pode acabar finalizando o pedido. 🇺🇸 Don't submit with empty required fields.
- 🇧🇷 Se aparecer uma tela de login do PayPal ou de outro meio de pagamento, **você já disparou uma tentativa**. 🇺🇸 A PayPal login screen means an attempt was triggered.

## Quiz comentado / Commented quiz (5/5)
1. Motivo para não comprar → ✅ **custos desnecessários para o cliente, como taxas do meio de pagamento**.
2. Na última etapa do checkout → ✅ **parar e sair da página**.
3. Na tela de pagamento → ✅ **evitar "Continue to PayPal" e "PayPal Express", que iniciam o pagamento**.
4. Na dúvida sobre um botão → ✅ **não clicar e perguntar ao TL**.
5. Como evitar enviar o pedido → ✅ **não clicar em "Complete order" ou "Finish order"** (❌ enviar com campos vazios; ❌ "Pay Later").
