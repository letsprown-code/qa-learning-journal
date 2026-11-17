# uTest Academy · Data Security In Testing · 01: Personally Identifiable Information (PII)

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: PII](https://platform.utest.com/academy/tracks/3/courses/44/lessons/what-is-personally-identifiable-information) (login) |
| Referências / References | [LGPD (Lei 13.709/2018)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) · [GDPR (EUR-Lex)](https://eur-lex.europa.eu/eli/reg/2016/679/oj) · [LibreOffice](https://www.libreoffice.org/) · [Kdenlive](https://kdenlive.org/) |
| Ligado a / Related | [Screenshots](../testing-tools/01-screenshots.md) · [Screen Recordings](../testing-tools/02-screen-recordings.md) |

## O que é PII / What PII is
🇧🇷 **PII (informação pessoal identificável)** é qualquer dado que identifica **uma pessoa específica**: a sua **ou a de qualquer outra pessoa**, inclusive um endereço onde moram várias pessoas. No Brasil, o tema é tratado pela **LGPD**. 🇺🇸 Any information that can identify **any** person (yours or someone else's).

| País / Country | Lei / Law |
|---|---|
| 🇧🇷 Brasil | **LGPD**: Lei Geral de Proteção de Dados |
| 🇪🇺 União Europeia | **GDPR** |
| 🇺🇸 EUA (exemplo: Califórnia) | **CCPA** |
| 🇨🇦 Canadá | PIPEDA |
| 🇦🇺 Austrália | CDR |
| 🇿🇦 África do Sul | Electronic Communications and Transactions Act |
| 🇯🇵 Japão | Act on the Protection of Personal Information |

💡 🇧🇷 O que é PII num país pode não ser em outro. Considere a lei **do país para o qual você está testando**. 🇺🇸 Consider the privacy law **of the country you test for**.

## Por que borrar / Why redact
1. 🇧🇷 Para **proteger você e outras pessoas**. 🇺🇸 To **protect yourself and others**.
2. 🇧🇷 Para o uTest e os clientes **cumprirem as leis** de proteção de dados. 🇺🇸 So uTest and customers **comply with the law**.

## O que esconder / What to hide (exemplos / examples)
| 🇧🇷 | 🇺🇸 |
|---|---|
| Nome completo, telefone, endereço | Full name, phone, address |
| Dados bancários: IBAN, conta, cartão | Bank details: IBAN, account, card numbers |
| CNH, CPF/RG, passaporte | Driver's license, national ID (e.g. SSN), passport |
| Fotos, biometria, dados genéticos | Photos, biometrics, genetic data |
| Raça, origem étnica, opinião política, religião | Race, ethnicity, political/religious beliefs |
| Login: e-mail com nome ou sobrenome, senha | Login details incl. email with name, password |
| Endereço MAC, **IP**, ID do aparelho, cookies | MAC, **IP address**, device IDs, cookies |
| **Teclado** enquanto você digita dado pessoal | **Keyboard** while typing PII |
| Bens: ex.: chassi de veículo (VIN) | Owned property: e.g. VIN |

- ⚠️ 🇧🇷 **Só o primeiro nome não é PII** (o curso fala em nome **completo**). 🇺🇸 **First name alone** is not PII.
- 🇧🇷 **Cada cliente tem regras próprias**: às vezes pedem para esconder só parte, como os últimos dígitos, ou usar a cor do fundo. **Leia o Overview** e, na dúvida, pergunte ao **TTL ou TE**. 🇺🇸 Customer rules vary; read the Overview, ask the TTL/TE.
- 🇧🇷 Alguns projetos pedem gravação com dados reais. Nesse caso, a equipe do projeto esconde os dados antes de enviar ao cliente. 🇺🇸 Some projects want real data recorded; the TTL/TE redacts it.
- 🇧🇷 A tarja precisa ficar **apresentável**, porque o cliente vai ver. 🇺🇸 Redaction must look **presentable**.

## Como esconder / How to redact

~~~mermaid
flowchart TD
    A{Tipo de anexo<br/>Attachment type} --> I[Imagem / Image]
    A --> P[PDF]
    A --> V[Vídeo / Video]
    I --> I1[Paint ou Pré-Visualização:<br/>retângulo PRETO e SÓLIDO só sobre o dado<br/>Paint/Preview: solid black box over PII only]
    P --> P1[LibreOffice: Tools → Redact → Rectangle<br/>→ Export Redacted PDF Black/White]
    V --> V1[VSDC: DeLogo · iMovie: Picture in Picture<br/>Kdenlive · InShot: Detail blur<br/>do começo ao fim da aparição<br/>from first to last frame]
    I1 & P1 & V1 --> C[Conferir o arquivo final<br/>Final check]
~~~

| Formato / Format | 🇧🇷 Regras | 🇺🇸 Rules |
|---|---|---|
| **Imagem** | Retângulo **preto sólido** (Paint: Fill → Solid color, cores 1 e 2 pretas; Pré-Visualização: Markup → Fill Color preto → Shapes). Cubra **o texto inteiro**, **sem cobrir rótulos** ou outros campos, com uma **folga visível** entre a tarja e o resto. Campos de 1 caractere: **uma tarja por campo**. Esconda também e-mails, alertas e chats que aparecerem. | Solid black box; cover all PII; don't overlap labels; leave a visible gap; one box per single-character field |
| **PDF** | **LibreOffice** → Tools → Redact → Rectangle → **Export Redacted PDF** (Black ou White). O "Export Preview" ainda deixa ler o dado, então serve só para conferir. Depois, teste: **não pode dar para copiar e colar o texto**, e os **links precisam estar desativados** (PDF "achatado"). | Must not be copy-pasteable; links inactive (flattened) |
| **Vídeo** | Esconda o dado **do primeiro ao último quadro** em que aparece, **sem cobrir tela demais**; dica: uma tarja para o dado parado e outra para quando ele se move. **Corte o que está fora do fluxo do teste**, como cadastrar Apple Pay. Não grave a plataforma do uTest nem planilhas do teste. Borre o **teclado** do celular. | Redact the whole appearance; cut out-of-flow parts; don't show the platform/test sheets; blur keyboard |

### Print da página inteira / Full-page capture
- 🇧🇷 **Edge:** ⋯ → Web Capture → Capture full page. **Firefox:** botão direito → Take Screenshot → Save full page. **Chrome:** DevTools → <code>Ctrl/Cmd+Shift+P</code> → **Capture full size screenshot** (ou imprimir → Salvar como PDF, ou a extensão GoFullPage, se o ciclo exigir). **Safari:** Arquivo → Exportar como PDF → abrir na Pré-Visualização → Exportar PNG/JPEG. **iOS:** print → aba **Página inteira**. Depois, **esconda os dados pessoais**. 🇺🇸 Use each browser's full-page option, then redact.

## Quiz comentado / Commented quiz (10/10)
1. Definição correta de PII / Correct definition → ✅ **Qualquer informação única de uma pessoa que possa identificar qualquer pessoa** (não só a sua).
2. Considerar a lei do país em que se testa → ✅ **Verdadeiro / True**.
3. NÃO é motivo para esconder PII / NOT a reason → ✅ **"Esconder que o testador trabalha para o uTest"**.
4. É PII / Is PII → ✅ **Dados bancários** (❌ produtos comprados, usuário sem nome, CEP).
5. NÃO é PII / NOT PII → ✅ **Primeiro nome** (❌ documentos, endereço completo, IP).
6. Afirmação correta / Correct statement → ✅ **Ler o Overview para entender as regras do cliente e, na dúvida, perguntar ao TTL ou TE.**
7. "É boa prática bloquear a página inteira" → ✅ **Falso / False** (esconda só o dado pessoal).
8. INCORRETO em imagem ou PDF / INCORRECT → ✅ **"Não deve haver folga visível entre a tarja e o texto"** (deve haver folga).
9. INCORRETO em PDF / INCORRECT for PDF → ✅ **"Tudo bem se ainda der para copiar o texto e o link"**.
10. Correto em vídeo / Correct for video → ✅ **Todas**: esconder do começo ao fim sem exagerar, tirar o que está fora do fluxo do teste e esconder telas e alertas com PII.
