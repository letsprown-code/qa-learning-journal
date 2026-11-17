# Test IO · Módulo 3: Quiz comentado · Module 3: Annotated quiz

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 3 de 4 · Bug Report Attachments (Attachment Quiz) |
| Resultado · Result | 6 de 6 acertos · 6 out of 6 correct |
| Data · Date | 16/11/2026 |
| Nota de estudo · Study note | [03-bug-report-attachments.md](03-bug-report-attachments.md) |

As explicações são minhas, com base no conteúdo do curso.

---

## Pergunta 1 · Question 1

**Em inglês:** Which of the following are general attachment requirements on the platform? (3 correct answers)

**Em português:** Quais destas são regras gerais de anexos na plataforma? (3 respostas certas)

| Opção | Resultado |
| --- | --- |
| Attachments must show enough information to prove the bug (o anexo precisa mostrar informação suficiente para provar o bug) | Certa |
| A new attachment must be created for each bug report or reproduction (é preciso criar um anexo novo para cada relatório ou reprodução) | Certa |
| Attachments must be in the language required by the Test Cycle (o anexo precisa estar no idioma do teste) | Certa |
| When testing a website, showing the URL field is optional (em site, mostrar a barra de endereço é opcional) | Errada |
| You can reuse attachments from another bug report if the bug is the same (pode reaproveitar anexo de outro relatório se o bug for igual) | Errada |

**Por que as certas estão certas:** as três estão na lista de regras gerais do artigo de anexos.

**Por que as outras estão erradas:** em site, a barra de endereço é **obrigatória**, não opcional. E reaproveitar anexo é **proibido**, mesmo que o bug seja o mesmo.

---

## Pergunta 2 · Question 2

**Em inglês:** When is a screencast usually required?

**Em português:** Quando normalmente é preciso gravar a tela?

| Opção | Resultado |
| --- | --- |
| When an action is needed to trigger the bug or a process needs to be shown (quando é preciso uma ação para o bug aparecer ou mostrar um processo) | Certa |
| When the bug can be shown with a static image only (quando dá para mostrar com uma imagem parada) | Errada |
| Only when a Team Leader requests it (só quando o líder do time pede) | Errada |
| Only for mobile app testing (só em teste de aplicativo) | Errada |

**Por que está certa:** é a regra do curso. O print é uma foto e não mostra a causa; a gravação mostra a ação e o resultado.

**Por que as outras estão erradas:** imagem parada é caso de **print**. A gravação não depende de pedido do líder: é a regra padrão para bugs com ação. E vale para site e app, não só para app.

---

## Pergunta 3 · Question 3

**Em inglês:** What file format must a screencast use?

**Em português:** Qual formato a gravação de tela precisa ter?

| Opção | Resultado |
| --- | --- |
| MP4 | Certa |
| MOV | Errada |
| AVI | Errada |
| GIF | Errada |

**Por que:** a regra é **MP4**. Atenção: o Mac e o iPhone gravam em **MOV**, então é preciso converter antes de enviar.

---

## Pergunta 4 · Question 4

**Em inglês:** Which statement about screencast length is correct?

**Em português:** O que está certo sobre a duração da gravação?

| Opção | Resultado |
| --- | --- |
| As short as possible and as long as necessary, but not longer than 60 seconds for Bug Reports (o mais curto possível e o tempo necessário, até 60 segundos em relatório de bug) | Certa |
| Always at least 60 seconds long (sempre no mínimo 60 segundos) | Errada |
| Exactly 15 seconds long (exatamente 15 segundos) | Errada |
| Shorter than 10 seconds (menos de 10 segundos) | Errada |
| Reproduction screencasts can be any length if the bug is visible (reprodução pode ter qualquer duração) | Errada |

**Por que está certa:** é a frase do curso. 60 segundos é o **máximo** para relatório de bug.

**Por que as outras estão erradas:** 60 segundos é limite máximo, não mínimo. 15 segundos é o **máximo** para reprodução e user story, não uma duração exata. Não existe regra de 10 segundos. E reprodução **tem** limite: 15 segundos.

---

## Pergunta 5 · Question 5

**Em inglês:** Which of the following are required when reporting an app crash? (2 correct answers)

**Em português:** O que é obrigatório ao relatar um app que fecha sozinho? (2 respostas certas)

| Opção | Resultado |
| --- | --- |
| A crash log file must be attached (o registro de erro precisa ser anexado) | Certa |
| The screencast and crash log must show the same crash and matching timings (o vídeo e o registro precisam ser do mesmo crash, com horários que batem) | Certa |
| A screenshot is required instead of a screencast (print no lugar da gravação) | Errada |
| The crash log can come from a different crash if the error is similar (o registro pode ser de outro crash parecido) | Errada |

**Por que as certas estão certas:** o curso diz que o crash log é obrigatório e que vídeo e registro precisam corresponder.

**Por que as outras estão erradas:** crash é bug funcional, então precisa de **gravação**, não de print. E o registro precisa ser **do mesmo crash** do vídeo.

---

## Pergunta 6 · Question 6

**Em inglês:** Which of the following are screenshot-specific rules? (2 correct answers)

**Em português:** Quais são regras específicas do print? (2 respostas certas)

| Opção | Resultado |
| --- | --- |
| The screenshot must be in JPG or PNG format (formato JPG ou PNG) | Certa |
| The bug should be highlighted on the screenshot (destacar o bug no print) | Certa |
| The screenshot does not need to clearly show the bug (não precisa mostrar o bug com clareza) | Errada |
| The screenshot must be in MP4 format (formato MP4) | Errada |
| The screenshot must include all steps that triggered the bug (mostrar todos os passos) | Errada |
| The screenshot can be reused from another bug report (pode reaproveitar) | Errada |
| The screenshot must include a console log (incluir o console) | Errada |

**Por que as certas estão certas:** são as duas regras da seção de print no artigo.

**Por que as outras estão erradas:** o anexo sempre precisa provar o bug com clareza. MP4 é formato de vídeo. Um print não mostra passos, por isso bugs com ação pedem gravação. Reaproveitar é proibido. E console log não é regra do print.

---

## O que levar deste quiz

- Ação para o bug aparecer: **gravação em MP4**. Problema parado: **print em JPG ou PNG, com o bug destacado**.
- Sempre um **anexo novo**, no **idioma do teste**, com a **barra de endereço** visível em sites.
- Duração: até **60 s** em relatório de bug, até **15 s** em reprodução.
- Crash: **crash log obrigatório**, do mesmo crash do vídeo.
