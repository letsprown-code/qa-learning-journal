# Test IO · Reproduction Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 6 de 6 (mínimo 5) · 17/11/2026 / Completed · quiz 6 of 6 (min. 5) |
| Por que · Why | É o jeito **mais rápido de começar a ganhar** na Test IO, mas com menos oportunidades / **Fastest way to start earning**, with fewer opportunities |
| Fontes · Sources | [Bug Reproductions](https://academy.test.io/en/articles/2541944-bug-reproductions-repros) · [Reproduction Feature](https://academy.test.io/en/articles/2668017-reproduction-feature) |

## O que é / What it is
🇧🇷 Achou um bug que **outro testador já reportou**? Você não pode reportar de novo, mas pode enviar uma **reprodução**. Ela mostra ao cliente em quais ambientes o bug acontece e se ele depende do aparelho, o que ajuda a medir a gravidade. 🇺🇸 Found a bug **already reported**? Submit a **reproduction** instead; it shows which environments are affected.

| Tipo / Type | 🇧🇷 | 🇺🇸 |
|---|---|---|
| **Positiva / Positive** | seguiu os mesmos passos e **o bug aconteceu** | same steps, **bug occurs** |
| **Negativa / Negative** | seguiu os mesmos passos e **o bug não aconteceu**; o vídeo mostra que funciona no seu aparelho | **no bug**; video shows it works |
| Bug diferente / Different bug | ❌ não é reprodução: reporte um bug novo ou reproduza o bug certo | report it separately |

## Onde encontrar / Where to find it
1. 🇧🇷 **Dashboard**: pedidos de reprodução de bugs já aprovados pelo TL. 🇺🇸 **Dashboard** requests.
2. 🇧🇷 **No relatório de outro testador**: botão **Start Reproduction**. 🇺🇸 On another tester's report.
3. 🇧🇷 **Na lista "Similar bug reports"**, enquanto você escreve um bug: se o seu bug já está lá, pare e clique em reproduzir. 🇺🇸 In the similar bugs list while reporting.
4. 🇧🇷 **Na lista de bugs do ciclo**, com o filtro **"Reproductions available"**. 🇺🇸 Bugs list filter.

🇧🇷 O botão só aparece **com o teste rodando**, em **bugs funcionais de outros testadores**, **ainda não revisados pelo cliente** e com **vaga sobrando**. 🇺🇸 Only while the test runs, for others' functional bugs not yet reviewed by the customer, with seats left.

## Regras / Rules

~~~mermaid
flowchart LR
    S[Start reproduction<br/>vaga reservada por 30 min] --> R[Seguir os passos do bug original]
    R --> Q{Aconteceu?}
    Q -- Sim --> P[Positiva]
    Q -- Não --> N[Negativa]
    P & N --> V[Vídeo até 15 s + URL visível<br/>crash: + crash log]
    V --> C[Create reproduction]
~~~

- 🇧🇷 **Sessão de 30 minutos.** Se cancelar ou o tempo acabar, a vaga volta para outros testadores. 🇺🇸 **30-minute session.**
- 🇧🇷 **Uma tarefa por vez:** não dá para reproduzir enquanto um test case, uma sessão de teste ou uma confirmação está ativa. 🇺🇸 **One task at a time.**
- 🇧🇷 **Vídeo obrigatório, de até 15 segundos**, mostrando a ação que dispara o bug. Só pode passar disso em casos raros, como uma página que nunca termina de carregar, e mesmo assim sem ultrapassar o vídeo original. 🇺🇸 **Screencast ≤ 15 s.**
- 🇧🇷 **Barra de endereço visível** em sites. **Crash de app:** anexe também o **crash log**, com horários que batam com o vídeo. 🇺🇸 URL bar; crash → crash log.
- ⚠️ 🇧🇷 Reproduzir um bug **fora do escopo** (ex.: fazer pedido em ambiente real) gera **rejeição e advertência**. 🇺🇸 OOS repro → rejection + warning.
- 🇧🇷 Para apagar: aba **My Reproductions** → abrir → **Delete**. 🇺🇸 Delete via My Reproductions.

## Quiz comentado / Commented quiz (6/6)
1. Onde enviar uma reprodução (3) / Where (3) → ✅ **lista "Similar bug reports"**, **Dashboard** e **no relatório de outro testador** (❌ página Overview do teste).
2. Reprodução negativa / Negative → ✅ **Você seguiu os passos e não conseguiu reproduzir o bug no seu aparelho.**
3. Requisitos do vídeo (3) / Screencast (3) → ✅ **mostrar a ação que dispara o bug**, **até 15 s na maioria dos casos** e **seguir as regras de anexos** (❌ no mínimo 1 minuto).
4. Duração da sessão / Session → ✅ **30 minutos**.
5. Quando dá para reproduzir (2) / When (2) → ✅ **o teste ainda está rodando** e **o bug ainda não foi revisado e há vaga** (❌ já revisado pelo cliente; ❌ seu próprio bug).
6. Crash de app reproduzido "num iPhone, no Safari" é aceito? → ✅ **Rejeitado**: ambiente errado (é app, não navegador) e **falta o crash log**.
