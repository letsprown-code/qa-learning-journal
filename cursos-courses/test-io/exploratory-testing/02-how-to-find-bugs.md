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

## Do vídeo: como encontrar bugs de verdade

Vídeo: [5 Proven Bug Finding Techniques: Exploratory Testing Mastery, canal Test IO Community no YouTube](https://www.youtube.com/watch?v=FXb68zt4xls), cerca de 3 minutos. Resumo feito a partir da transcrição do vídeo.

### 1. Antes de começar

Revisar a configuração do teste:

- o que a função **deveria fazer**;
- a **lista de bugs já conhecidos** (known bugs), para não enviar repetido;
- o que está **fora do escopo** (por exemplo, finalizar pedidos ou usar meios de pagamento).

### 2. Caminho positivo e caminho negativo

| Tipo de teste | O que é | Exemplo do vídeo |
| --- | --- | --- |
| **Positivo** (caminho feliz) | Usar do jeito certo, com dados válidos | Criar conta com um e-mail válido. Funcionou. |
| **Negativo leve** | Errar como um usuário comum erraria | Digitar sem querer um caractere especial no e-mail (como #). O sistema aceitou sem mostrar erro. **Bug encontrado.** |

Regra: no teste negativo, tentar **erros razoáveis**, que um usuário típico cometeria. Não vale inventar situações absurdas.

Dica extra: às vezes basta começar a preencher os campos. No vídeo, o texto de exemplo do campo (placeholder) ficou por cima do e-mail digitado: um **bug visual**.

### 3. Onde os bugs gostam de se esconder

| Onde procurar | Exemplo do vídeo | Tipo e gravidade (pelo módulo 1) |
| --- | --- | --- |
| **Envio de dados** | Pedir aviso por e-mail quando o produto voltar ao estoque: a tela ficou carregando sem fim. | Funcional, gravidade alta (o vídeo chama de bug de alta gravidade) |
| **Login e senha** | Pedir para redefinir a senha e tentar entrar antes de abrir o e-mail: o sistema travou e nenhuma senha funcionava. | Funcional |
| **Navegação** | Link de termos e condições no **rodapé** da página de perguntas frequentes levava a erro 404. | Funcional baixo (link quebrado no rodapé) |

### 4. Técnicas práticas

- **Testar em navegadores diferentes:** o que funciona no Chrome pode quebrar no Firefox ou no Safari.
- **Clicar em tudo que é clicável:** no vídeo, aplicar o filtro de preço abriu uma página em branco com erro de banco de dados. Era um caminho normal de usuário e virou um **bug crítico**.
- **Prestar atenção no comportamento estranho:** ao dar play numa playlist, a página subiu sozinha.

### A mensagem principal

Não ficar só no caminho feliz. Os bugs mais graves aparecem nos caminhos inesperados, **mas sempre pensando em como um usuário típico se comporta**.

---

<a id="english"></a>

## English

**Main idea:** each test is a small customer project with a defined **scope**. I look for bugs inside that scope and report each one. I only get paid for valid bugs that are approved.

**Test flow:** invitation (based on profile, devices and performance) → read all instructions before accepting → read the scope → choose the device carefully (until Bronze level, it is the only device I can use for the whole cycle) → the test environment appears only after the test starts → start a **Test Session** to enable "Submit Bug" → report in-scope bugs → the **Team Leader** reviews, may ask questions, approves or rejects; approved bugs go to the customer for the final decision → keep checking bug status and email, even after the cycle ends → if I disagree, comment on the report and, if needed, open a **dispute**.

**Levels:** Copper (level 1) testers can join only **2 cycles at a time**; Bronze and above can join as many as they can handle.

**Video:** before testing, review what the feature should do, the known bugs list and what is out of scope. Test the positive path first, then light negative tests with mistakes a typical user would make (e.g., a special character in an email). Look where bugs hide: data submissions (endless loading), authentication (password reset), navigation (404 links in the footer). Test across browsers and click everything clickable. Go beyond the happy path, but keep typical user behavior in mind.

**Rules:** no browser translation add-ons on platform content; customer data is confidential and must not be sent to third-party tools; when in doubt, ask the Team Leader in the cycle chat.
