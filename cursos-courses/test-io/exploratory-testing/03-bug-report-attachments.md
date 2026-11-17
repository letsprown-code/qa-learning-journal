# Test IO · Módulo 3: Anexos do relatório de bug · Module 3: Bug Report Attachments

**Português (Brasil)** | [English below](#english)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Exploratory Testing Course |
| Módulo · Module | 3 de 4 · Bug Report Attachments |
| Situação · Status | Quiz: 6 de 6. Tarefa prática: enviada, em análise · Quiz: 6/6. Practical task: submitted, under review |
| Quiz comentado · Annotated quiz | [03-bug-report-attachments-quiz.md](03-bug-report-attachments-quiz.md) |
| Fontes originais · Original sources | [Bug Report Attachments](https://academy.test.io/en/articles/2541954-bug-report-attachments), [Screencasts](https://academy.test.io/en/articles/2541905-screencasts) e [Screenshots](https://academy.test.io/en/articles/2541936-screenshots), Test IO Academy |

Estas são as minhas anotações, escritas com as minhas palavras. · These are my own notes.

## Para que serve o anexo

Todo bug precisa de **pelo menos um anexo**. O anexo é a **prova** de que o bug acontece no meu aparelho, sistema e navegador. Ele **não substitui** o texto do relatório: mostra o que o texto descreve.

## Print ou gravação de tela?

| Use | Quando | Exemplos de tipo de bug |
| --- | --- | --- |
| **Gravação de tela** (screencast) | Quando é preciso **fazer uma ação** para o bug aparecer, ou mostrar um processo | Bugs **funcionais** sempre pedem gravação |
| **Print** (screenshot) | Quando o problema é **parado**, aparece na tela sem precisar de ação | Bugs **visuais** e **de conteúdo** |

## Regras gerais de todo anexo

- Criar um **anexo novo** para cada relatório ou reprodução. **Proibido reaproveitar** anexo de outro relatório.
- Mostrar **toda a informação** que prova o bug.
- Estar no **idioma do teste** (quase sempre inglês). Se preciso, mudar o idioma do aparelho ou do navegador antes de gravar.
- Um aparelho ou navegador por relatório. Se o bug acontece em outros, escrever isso no resultado atual.
- **Não mostrar** nada de outros clientes do Test IO (e-mails de convite, nomes de abas) nem dados pessoais ou conteúdo pouco profissional.
- Em teste de **site**, a **barra de endereço (URL) precisa aparecer**.
- Resolução boa o bastante para ler textos e elementos.
- Gravar **a tela inteira**.
- Se o app **fechar sozinho** (crash): o **registro de erro (crash log) é obrigatório**, e o vídeo e o registro precisam ser do **mesmo crash**, com horários que batem.

## Regras do print

- Formato **JPG ou PNG**.
- **Destacar o bug** no print (por exemplo, com um retângulo).
- No Mac: **cmd + shift + 3** para a tela inteira, **cmd + shift + 4** para um pedaço.

## Regras da gravação de tela

| Regra | Detalhe |
| --- | --- |
| Formato | **MP4** (no Mac, a gravação sai em .mov e precisa virar .mp4) |
| Tamanho máximo | 25 MB |
| Duração | **O mais curto possível, mas sem cortar o necessário.** Até **60 segundos** em relatório de bug; até **15 segundos** em reprodução e user story |
| Gravação | **De uma vez só**: sem pausar e sem cortar o meio. Só pode cortar o começo ou o fim |
| Velocidade | **Proibido acelerar** o vídeo |
| Som | **Sem barulho** (conversa, TV, música, animais). Melhor desligar o microfone antes |
| Edição | Só para **borrar dados sensíveis** (senhas, dados de pagamento) |

**Como gravar o mínimo necessário:** deixar tudo pronto antes de começar (formulário preenchido, página aberta). Gravar só o último passo de navegação, a ação que causa o bug e o bug acontecendo.

**Depois de enviar:** sempre assistir ao próprio vídeo, porque o arquivo pode corromper na conversão ou no envio.

## Na prática: como gravei a tela no Mac (aprendizados da tarefa prática)

| Problema que aconteceu | Solução |
| --- | --- |
| O atalho cmd + shift + 5 ficava no modo de foto | Usar o **QuickTime Player**: Arquivo, Nova Gravação de Tela. Na barrinha, escolher **Gravar a Tela Inteira** (retângulo cheio com bolinha) |
| Com dois monitores, o Mac pergunta Tela 1 ou Tela 2 | Passar o mouse em cada opção: o monitor que **acende** é o que será gravado. Escolher o monitor onde está o navegador |
| O vídeo saiu todo preto, só com o ponteiro | Faltava permissão: Ajustes do Sistema, Privacidade e Segurança, **Gravação de Tela e Áudio do Sistema**, adicionar o QuickTime com o botão **+** e reabrir o app |
| A sugestão da barra de endereço mostrou o meu histórico | Cortar o começo do vídeo (permitido) ou usar uma janela anônima sem histórico. Dados pessoais não podem aparecer |
| Vídeo com mais de 60 segundos | Deixar tudo pronto antes de gravar, rolar sem pausas e parar assim que o resultado aparecer |
| Arquivo .mov grande | Converter para **.mp4 (H.264)**, o que também reduz o tamanho |

---

<a id="english"></a>

## English

Every bug needs at least one attachment as proof; it does not replace the written report. **Screencast** when an action triggers the bug (functional bugs always); **screenshot** for static content or visual issues.

General rules: new attachments for every report, never reused; enough information to prove the bug; in the test cycle language; one device per report; no other customers' or personal data; URL visible for websites; readable resolution; record the whole screen; crash log mandatory for crashes, matching the video.

Screenshots: JPG or PNG, bug highlighted. Screencasts: MP4, max 25 MB, as short as possible (max 60 s for bug reports, 15 s for reproductions and user stories), recorded in one go, no speed-up, no noise, editing only to blur sensitive data. Always watch your own video after uploading.

**Lessons from the practical task (macOS):** record with QuickTime (File, New Screen Recording, Record Entire Screen); grant Screen Recording permission in System Settings or the video comes out black; with two monitors, pick the one that lights up; keep browser history suggestions out of the video; convert .mov to .mp4.
