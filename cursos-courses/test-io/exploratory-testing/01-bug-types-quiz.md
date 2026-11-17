# Test IO · Módulo 1: Quiz comentado · Module 1: Annotated quiz

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 1 de 4 · Bug Types |
| Resultado · Result | 9 de 9 acertos · 9 out of 9 correct |
| Data · Date | 16/11/2026 |
| Nota de estudo · Study note | [01-bug-types.md](01-bug-types.md) |

Para cada pergunta: o enunciado (em inglês, como no curso, e traduzido), a resposta certa, **por que ela está certa** e **por que as outras estão erradas**. As explicações são minhas, com base no conteúdo do curso.

---

## Pergunta 1 · Question 1

**Em inglês:** A content bug (a broken link (404 error)) is upgraded to a low functional bug if the link is located in: (3 correct answers)

**Em português:** Um bug de conteúdo (link quebrado, erro 404) passa a ser um bug funcional de gravidade baixa quando o link está em quais lugares? (3 respostas certas)

| Opção | Resultado |
| --- | --- |
| Breadcrumb navigation (trilha de navegação) | Certa |
| Header/footer (cabeçalho e rodapé) | Certa |
| Navigation menu (menu de navegação) | Certa |
| Product description on the product detail page (descrição do produto) | Errada |
| Image on the landing page (imagem na página inicial) | Errada |

**Por que as certas estão certas:** o curso diz que o link quebrado só vira bug funcional baixo quando está nas partes do site que servem para **navegar**: menu de navegação, cabeçalho, rodapé e trilha de navegação. Essas partes aparecem em quase todas as páginas e o usuário depende delas para se movimentar.

**Por que as outras estão erradas:** a descrição do produto e a imagem da página inicial são **conteúdo comum**. Um link quebrado ali continua sendo bug de conteúdo, sem promoção para funcional.

---

## Pergunta 2 · Question 2

**Em inglês:** Can you submit spelling mistakes as content bugs on our platform?

**Em português:** Posso enviar erros de ortografia como bugs de conteúdo na plataforma?

| Opção | Resultado |
| --- | --- |
| No (não) | Certa |
| Yes (sim) | Errada |

**Por que:** regra explícita do curso. No Test IO, erro de ortografia **não** é considerado bug de conteúdo e não pode ser enviado.

**Atenção:** isso é regra do Test IO. Outras plataformas podem aceitar erros de ortografia, então sempre leia as regras de cada teste.

---

## Pergunta 3 · Question 3

**Em inglês:** Which of the following scenarios are certainly functional bugs (as compared to usability suggestions)? (3 correct answers)

**Em português:** Quais situações são, com certeza, bugs funcionais (e não sugestões de usabilidade)? (3 respostas certas)

| Opção | Resultado |
| --- | --- |
| The customer's product works differently from what was stated in the test instructions (o produto funciona diferente do que dizem as instruções do teste) | Certa |
| An unknown error appears that does not let you continue (aparece um erro desconhecido que impede de continuar) | Certa |
| A button does not trigger any action (um botão não faz nada) | Certa |
| Your expectation of how the feature should work differs from how it actually works (a sua expectativa é diferente de como a função funciona) | Errada |

**Por que as certas estão certas:** nas três existe **prova** de que algo não funciona como deveria. As instruções do teste dizem uma coisa e o produto faz outra. O erro bloqueia o usuário. O botão não responde.

**Por que a outra está errada:** a **sua expectativa** não é prova. O curso diz que o cliente pode construir o produto do jeito que quiser. Funcionar diferente do que você esperava, ou de outros sites, não é bug. No máximo é uma sugestão de usabilidade.

---

## Pergunta 4 · Question 4

**Em inglês:** When the user clicks on the test IO logo at the top left corner of the Pricing page, they get redirected back to the landing page.

**Em português:** Quando o usuário clica no logo do test IO, no canto superior esquerdo da página de preços, ele volta para a página inicial. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Not a bug (não é bug) | Certa |
| Functional (Low) | Errada |
| Visual | Errada |
| Content | Errada |

**Por que está certa:** clicar no logo e voltar para a página inicial é o **comportamento padrão e esperado** em quase todos os sites. Nada está quebrado.

**Por que as outras estão erradas:** não há função quebrada (funcional), nada aparece errado na tela (visual) e nenhum texto, imagem ou link está faltando (conteúdo). É uma pegadinha para ver se você reconhece quando **não** é bug.

---

## Pergunta 5 · Question 5

**Em inglês:** On the landing page, when changing the language to Russian, some tabs of the main navigation menu remain in English.

**Em português:** Na página inicial, ao mudar o idioma para russo, algumas abas do menu de navegação continuam em inglês. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Content (conteúdo) | Certa |
| Functional (Low) | Errada |
| Visual | Errada |
| Not a bug | Errada |

**Por que está certa:** **tradução faltando** está na lista de bugs de conteúdo do curso.

**Por que as outras estão erradas:**
- **Functional (Low):** é a pegadinha da pergunta. O problema está no menu de navegação, mas a regra do menu vale para **link quebrado**. Aqui o menu continua funcionando, só o texto não foi traduzido.
- **Visual:** nada está desalinhado, cortado ou sobreposto.
- **Not a bug:** se o site muda para russo, todos os textos deveriam mudar. Então é bug.

---

## Pergunta 6 · Question 6

**Em inglês:** On the Home & Living product page, when the custom price filter (from $10 to $12) is applied, some products outside of the given price range are still displayed.

**Em português:** Na página de produtos Casa e Decoração, ao aplicar o filtro de preço de US$ 10 a US$ 12, aparecem produtos fora dessa faixa. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Functional (High) | Certa |
| Visual | Errada |
| Content | Errada |
| Not a bug | Errada |

**Por que está certa:** o filtro é uma **função** e ele não faz o que promete. A gravidade é **alta (High)** porque a função é importante para a compra e afeta muitos produtos, mas o site continua funcionando: dá para comprar sem usar o filtro. Não chega a ser crítico.

**Por que as outras estão erradas:** não é visual, porque a tela está correta. Não é conteúdo, porque os produtos existem e aparecem; o erro está na lógica do filtro. E é bug, sim, porque o resultado contradiz a faixa de preço escolhida.

---

## Pergunta 7 · Question 7

**Em inglês:** The label "Can not reproduce" for the right button is cropped out and not fully visible.

**Em português:** O texto "Can not reproduce" do botão da direita aparece cortado e não dá para ler inteiro. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Visual | Certa |
| Functional (Low) | Errada |
| Content | Errada |
| Not a bug | Errada |

**Por que está certa:** **texto cortado** está na lista de bugs visuais do curso. O problema é de aparência.

**Por que as outras estão erradas:** o botão continua funcionando, então não é funcional. O texto existe e está correto, só aparece cortado, então não é conteúdo. E é bug, porque o usuário não consegue ler o botão inteiro.

---

## Pergunta 8 · Question 8

**Em inglês:** Users are unable to sign in with their Apple account. Tapping on "Continue with apple" on the sign-in page leads to a 403 error message.

**Em português:** Os usuários não conseguem entrar com a conta Apple. Ao tocar em "Continuar com Apple", aparece um erro 403. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Functional (High) | Certa |
| Content | Errada |
| Visual | Errada |
| Not a bug | Errada |

**Por que está certa:** o login com Apple é uma **função importante que quebrou**. A gravidade é **alta (High)**, e não crítica, porque existe **outro jeito de entrar** (por exemplo, com e-mail e senha). O curso diz que função importante quebrada **com alternativa** é High.

**Por que as outras estão erradas:** o erro 403 aqui não é um link quebrado no conteúdo, é a função de login que falha. Não há problema de aparência. E impedir o login é claramente bug.

---

## Pergunta 9 · Question 9

**Em inglês:** The app crashes when the user swipes to accept the test invitation.

**Em português:** O aplicativo fecha sozinho quando o usuário arrasta para aceitar o convite de teste. Que tipo de bug é esse?

| Opção | Resultado |
| --- | --- |
| Functional (Critical) | Certa |
| Content | Errada |
| Visual | Errada |
| Not a bug | Errada |

**Por que está certa:** o app **fecha** (crash) e impede a **ação principal** do aplicativo, que é aceitar o convite de teste. Não existe alternativa. O curso define isso como **bloqueador (showstopper)**, e bloqueador é **crítico**.

**Por que as outras estão erradas:** não é texto ou imagem (conteúdo), nem aparência (visual). E app fechando sozinho sempre é bug.

---

## O que levar deste quiz

- **Não é bug** quando o produto faz o comportamento padrão ou quando só contraria a sua expectativa.
- **Conteúdo:** algo faltando ou quebrado no texto, imagem, link, tradução ou dados.
- **Visual:** aparência errada (cortado, desalinhado, sobreposto).
- **Funcional:** uma ação não funciona. A gravidade depende do impacto:
  - **Low:** pouco impacto ou link quebrado em menu, cabeçalho, rodapé ou breadcrumb;
  - **High:** função importante quebrada, mas existe outro caminho;
  - **Critical:** trava a ação principal, sem alternativa (por exemplo, o app fecha).
- Cuidado com a pegadinha: a regra do menu de navegação vale para **link quebrado**, não para qualquer problema que aconteça no menu.
