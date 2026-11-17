# Test IO · Módulo 2: Como encontrar bugs · Module 2: How to find bugs?

**Português (Brasil)** | [English below](#english)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 2 de 4 · How to find bugs? |
| Situação · Status | Em andamento · In progress |
| Material · Materials | Vídeo do curso (cerca de 3 minutos) e o artigo [Test Process, Test IO Academy](https://academy.test.io/en/articles/2541890-test-process) |
| Avaliação · Assessment | Não tem quiz · No quiz |

Estas são as minhas anotações, escritas com as minhas palavras. · These are my own notes.

## A ideia principal

No Test IO, cada **teste** é um pequeno projeto de um cliente. O teste tem um **escopo**: as partes do produto que devem ser testadas. Eu procuro bugs dentro desse escopo e envio um relatório para cada bug. **Só recebo se o bug for válido e aprovado.**

## O caminho de um teste, do convite ao pagamento

| Etapa | O que acontece | O que eu faço |
| --- | --- | --- |
| 1. Convite | O sistema compara o meu perfil, os meus dispositivos e o meu desempenho com o que o cliente pediu. Se eu combinar, recebo um convite por e-mail e no painel ("Interesting tests for you"). | Manter **todos os dispositivos** cadastrados no perfil, porque isso aumenta os convites. |
| 2. Aceitar ou recusar | A decisão é minha. | **Ler todas as instruções antes de aceitar.** Para aceitar: marcar a caixa em "Join this Test" e clicar em "Accept and take seat". |
| 3. Ler o escopo | O teste traz instruções e a descrição das funções que o cliente quer testar. | Ler tudo com calma. Dá para ler antes de o teste começar e já estar pronta quando ele abrir. |
| 4. Escolher o dispositivo | Posso escolher o aparelho, se ainda houver vaga para ele. | Escolher com cuidado: **até chegar ao nível Bronze, só posso enviar bugs com esse aparelho durante todo o teste.** |
| 5. Abrir o ambiente | O ambiente de teste (site ou app) só aparece **depois que o teste começa**. Se for app, eu instalo no aparelho. | Iniciar uma **sessão de teste (Test Session)**. Sem sessão, o botão "Submit Bug" não funciona. |
| 6. Caçar e enviar bugs | Cada bug é enviado ligado a uma das funções do escopo. | Enviar só bugs **dentro do escopo**. |
| 7. Revisão | O **líder do time (Team Leader, TL)** confere os relatórios. Ele pode pedir mais informações, aprovar ou rejeitar. Os aprovados vão para o cliente, que dá a decisão final. | **Acompanhar o status dos meus bugs e os e-mails**, inclusive depois que o teste acaba, porque o líder ou o cliente podem pedir algo. |
| 8. Discordar | Se eu não concordar com a decisão do líder... | ...comento no relatório pedindo explicação. Se a resposta não resolver ou demorar demais, posso abrir uma **disputa (dispute)**. |

## Níveis de testador e limite de testes

| Nível | Quantos testes ao mesmo tempo |
| --- | --- |
| Nível 1: Copper (cobre), onde todo mundo começa | Até **2 testes** ao mesmo tempo. Para entrar num terceiro, preciso sair de um. |
| Nível 2: Bronze ou acima | Quantos quiser, desde que eu tenha tempo para todos. |

Para sair de um teste: os 3 pontinhos ao lado do teste no menu lateral, opção "Quit test cycle and free seat", ou o botão "Quit test and free seat" no rodapé da página do teste.

## Regras importantes

- **Proibido usar tradutor do navegador** (extensões que traduzem a página) no conteúdo da plataforma.
- Os dados do cliente são **confidenciais**: não podem ser colados em ferramentas de terceiros, nem para traduzir.
- Na dúvida, falar com o **líder do time** pelo chat do teste. Ele é a melhor fonte de informação.
- Também existe a comunidade do Test IO no Discord.

> **Para mim, na prática:** como eu uso o Claude para me ajudar com o inglês, **não posso colar textos dos testes** (instruções do cliente, telas, dados) para traduzir. Posso usar ajuda para escrever os **meus** relatórios a partir das minhas próprias anotações, sem dados do cliente. Na dúvida, perguntar ao líder do time.

## Do vídeo: 5 técnicas para encontrar bugs

Vídeo: [5 Proven Bug Finding Techniques: Exploratory Testing Mastery, canal Test IO Community no YouTube](https://www.youtube.com/watch?v=FXb68zt4xls).

| Técnica | O que fazer na prática |
| --- | --- |
| 1. Preparar o teste | Antes de explorar, deixar o ambiente pronto: ler o escopo, abrir o site ou instalar o app, iniciar a sessão de teste. |
| 2. Testar o caminho certo e o caminho errado | **Teste positivo:** usar do jeito esperado, com dados válidos. **Teste negativo:** usar dados inválidos e casos extremos para ver se o sistema se defende. |
| 3. Provocar os campos de entrada | Exemplo do vídeo: campo de e-mail. Testar caracteres especiais, formatos errados e campos vazios para ver se a validação funciona. |
| 4. Ir onde os bugs graves se escondem | Login, recuperação de senha e funções que dependem de dados costumam concentrar bugs de gravidade alta. |
| 5. Conferir a navegação e comparar navegadores | Procurar links quebrados (erro 404), principalmente no rodapé e nos menus. Repetir o mesmo passo em navegadores diferentes, como Chrome e Firefox, e comparar. |

O vídeo termina com um roteiro que se repete: preparar, explorar, encontrar e relatar.

Outros exemplos de bug citados: texto do formulário se sobrepondo ao texto de exemplo do campo (visual), tela carregando sem fim (funcional) e app fechando ao aplicar um filtro de preço (funcional).

*Observação: este resumo foi feito a partir da descrição e dos capítulos do vídeo. Depois de assistir, acrescento o que eu achar importante.*

---

<a id="english"></a>

## English

**Main idea:** each test is a small customer project with a defined **scope**. I look for bugs inside that scope and report each one. I only get paid for valid bugs that are approved.

**Test flow:** invitation (based on profile, devices and performance) → read all instructions before accepting → read the scope → choose the device carefully (until Bronze level, it is the only device I can use for the whole cycle) → the test environment appears only after the test starts → start a **Test Session** to enable "Submit Bug" → report in-scope bugs → the **Team Leader** reviews, may ask questions, approves or rejects; approved bugs go to the customer for the final decision → keep checking bug status and email, even after the cycle ends → if I disagree, comment on the report and, if needed, open a **dispute**.

**Levels:** Copper (level 1) testers can join only **2 cycles at a time**; Bronze and above can join as many as they can handle.

**Video (5 techniques):** prepare the test setup; test positive and negative paths; probe input fields (e.g., email validation with special characters); focus on high-risk areas such as login and password reset; check navigation for dead links and compare browsers.

**Rules:** no browser translation add-ons on platform content; customer data is confidential and must not be sent to third-party tools; when in doubt, ask the Team Leader in the cycle chat.
