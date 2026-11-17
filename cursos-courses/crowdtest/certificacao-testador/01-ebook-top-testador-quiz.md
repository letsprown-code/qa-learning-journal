# Crowdtest · Certificação de Testador · 01: Quiz comentado · Annotated quiz

**Português (Brasil)** | [English below](#english)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Crowdtest (Base2, Belo Horizonte) |
| Curso · Course | Certificação de Testador Crowdtest · Crowdtest Tester Certification |
| Prova · Exam | Avaliação Inicial de Conhecimentos em Crowdtesting: 20 questões de única escolha, mínimo de 70% · 20 single-choice questions, 70% to pass |
| Situação · Status | Aprovada com **18 de 20 (90%)** em 17/11/2026 · Passed with 18/20 (90%) |
| Nota de estudo · Study note | [01-ebook-top-testador.md](01-ebook-top-testador.md) |

As perguntas estão reescritas com as minhas palavras; a explicação vem do e-book. · Questions are paraphrased; explanations come from the e-book.

> ⚠️ A plataforma mostra só a nota, não quais questões erramos. Errei **2**. A mais provável é a **15** (o e-book não lista formatos de arquivo). A outra não deu para identificar. · The platform only shows the score, not which answers were wrong. I missed 2; the most likely is #15.

## Questões comentadas

### 1. Por que preencher o máximo de informações no cadastro?
✅ **Para aumentar a chance de ser selecionada em projetos que pedem um perfil ou um aparelho específico.**
A maioria dos projetos é privada, e a equipe usa o cadastro para escolher quem convidar. ❌ Estatística, personalizar a tela ou recomendar cursos não aparecem no e-book.

### 2. O que fazer se o meu aparelho não está na lista?
✅ **Mandar um e-mail para o suporte (contato@crowdtest.com.br) com a marca e o modelo.**
❌ Ignorar e usar outro aparelho, esperar atualização automática ou reinstalar o app não resolvem.

### 3. Como entro num projeto público?
✅ **Direto na plataforma, em "Projetos Disponíveis", sem formulário.**
❌ Convite por e-mail é dos projetos **privados**; redes sociais só divulgam; não existe regra de "10 testes antes".

### 4. Qual destes **não** é um tipo de teste feito no Crowdtest?
✅ **Teste de performance automatizada.**
O Crowdtest usa pessoas testando à mão: casos de teste, testes exploratórios e testes de usabilidade. Performance automatizada é feita por ferramentas, sem testador humano.

### 5. Para que serve o campo "Resultado encontrado" no caso de teste?
✅ **Descrever o que aconteceu depois de seguir os passos.**
❌ O aparelho tem campo próprio ("Dispositivo"); o valor aparece no título do teste; sugestão de melhoria é um tipo de bug do exploratório.

### 6. Quando marcar "Bloqueado"?
✅ **Quando uma falha da aplicação impede fazer o teste.**
❌ Teste que terminou certo = **Passou**. Falhas visuais pequenas que não impedem o objetivo = **Passou**. Prazo vencido: o teste vai para outra pessoa, não se marca nada.

### 7. Qual "Resultado encontrado" está bem escrito?
✅ **"Após clicar em 'Enviar', o app exibiu a mensagem de sucesso conforme esperado."**
Diz o que fiz, o que apareceu e compara com o esperado. ❌ "Deu certo", "Tudo funcionando normal" e "App ok" são genéricos e levam a pedido de esclarecimento ou reprovação.

### 8. Um bug foi registrado com título, passos, resultado esperado e vídeo. Está completo?
✅ **Não: está incompleto, faltaram o tipo e a feature (funcionalidade).**
No registro de bug são obrigatórios: título, **tipo**, descrição, passos, resultado esperado, **feature**, dispositivo e evidências. ❌ "Resultado encontrado" é campo do caso de teste, não do bug; "observação adicional" é opcional.

### 9. Situação "Passou", mas o resultado encontrado diz que o app travou na tela de login. Qual é o erro?
✅ **A situação deveria ser "Falhou".**
"Passou" só vale quando o objetivo do teste foi alcançado. ❌ O vídeo é obrigatório, mas não corrige a situação errada; travamento é sempre relevante.

### 10. Erro de digitação ou palavra repetida é registrado como:
✅ **Texto.**
❌ Melhoria = sugestão; Funcional = algo não funciona; Interface = problema visual (ex.: botão fora do lugar).

### 11. Layout desalinhado é bug de qual tipo?
✅ **Interface.**
É problema visual: a tela aparece errada, mas a função continua funcionando. ❌ Funcional = a ação não dá certo; Impeditivo = trava ou impede a ação; Melhoria = sugestão.

### 12. Falha que deixa ver informação sigilosa é bug de qual tipo?
✅ **Segurança.**
É quando aparece uma informação que não deveria estar visível. Paga como o impeditivo (R$ 20, valores da v6).

### 13. O que é obrigatório em qualquer tipo de teste?
✅ **Gravar a tela do aparelho.**
O vídeo é a evidência que a equipe usa para aprovar. ❌ Não precisa logar com conta pessoal nem mandar mais de um vídeo; e nem todo teste tem bug (um caso de teste pode simplesmente passar).

### 14. E se eu não responder um pedido de esclarecimento em 24 horas?
✅ **O teste é reprovado (automaticamente).**
❌ Não é reavaliado, a dúvida não vai para o cliente e ninguém é removido da plataforma por isso.

### 15. Qual formato de evidência é aceito? (só uma alternativa)
❓ Marquei **MP4**. **Provável erro:** a resposta certa pode ser **JPG, PNG, WEBP** (prints) ou outra que o campo de upload aceite. Conferir no primeiro upload real.
O e-book não lista formatos: diz só que o vídeo é obrigatório e que dá para anexar prints ou "outro tipo de arquivo". Escolhi MP4 porque a própria prova usa "vídeo em MP4" como evidência válida nas questões 8 e 9. Lição: converter o .mov do QuickTime para .mp4 antes de anexar.

### 16. No teste exploratório, qual é o tempo mínimo de vídeo?
✅ **45 minutos.**
Está no e-book novo (dez/2025), seção "5.2 – Teste exploratório": gravar a tela do início ao fim, com **no mínimo 45 minutos**. A versão anterior do e-book não tinha essa regra. Mesma seção: média de pagamento de **R$ 60 por projeto** exploratório (os bugs são pagos individualmente).

### 17. Abri um caso de teste e não quero ou não posso fazer. E agora?
✅ **Clicar em "Cancelar" ou "Pular".**
Assim o teste fica livre para outra pessoa. ❌ Enviar em branco ou com vídeo incompleto leva à reprovação; fechar o navegador deixa o teste preso até o prazo acabar.

### 18. Qual é o único meio de pagamento do Crowdtest?
✅ **PayPal.**
Todo dia 10, só do que foi aprovado. O e-mail do PayPal vai em Perfil, Dados financeiros. ❌ Não há Pix, transferência direta nem PagSeguro.

### 19. Quando o pagamento é feito, depois da aprovação?
✅ **Todo dia 10 de cada mês.**
❌ Não é toda sexta, nem no último dia útil (essa é a regra da uTest: dias 15 e último dia do mês), nem a cada teste aprovado.

### 20. Para entrar em projetos privados, o que é preciso?
✅ **Ter o perfil compatível com o que o cliente pede.**
Os projetos privados procuram perfis específicos (cidade, idade, banco, aparelho) e chegam por formulário ou convite por e-mail. ❌ Não existe mínimo de testes públicos, inscrição presencial nem conta premium.

## Lições da prova

- O e-book da prova é a versão de **dez/2025**; ele tem regras que a versão antiga não tinha (vídeo de **45 min** no exploratório, média de **R$ 60** por projeto exploratório).
- Quando o material não traz a resposta, anotar a dúvida e conferir na prática (ex.: formatos aceitos no upload).
- Não confundir com a uTest: Crowdtest paga **dia 10, só PayPal**.

---

<a id="english"></a>

## English

**Result:** passed with **18/20 (90%)** on Nov 17, 2026. The platform shows only the score; the most likely miss is #15 (evidence formats are not listed in the e-book).

**Key answers:** a complete profile raises the chance of private-project invites · missing device → email support with brand and model · public projects: "Projetos Disponíveis", no form · not a Crowdtest test type: automated performance testing · "Resultado encontrado" = what actually happened after the steps · **Blocked** = an app failure prevents testing · good actual result: says what was done, what appeared and compares to expected · a bug report without **type** and **feature** is incomplete · app froze but status "Passed" → should be **Failed** · typo = **Text** bug · misaligned layout = **Interface** · exposed confidential data = **Security** · screen recording is mandatory in every test · no reply to a clarification in **24 h** → rejected · exploratory video: **at least 45 minutes** · can't run a test case → **Cancel/Skip** · payment: **PayPal only**, on the **10th** · private projects require a **matching profile**.
