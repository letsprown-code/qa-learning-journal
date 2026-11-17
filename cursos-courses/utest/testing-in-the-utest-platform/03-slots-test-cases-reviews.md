# uTest Academy · Testing in the uTest Platform · 03: Slots, Test Cases and Reviews

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 10 de 10 / Completed · quiz 10 of 10 |
| Fonte / Source | [uTest Academy: Slots, Test Cases and Reviews](https://platform.utest.com/academy/tracks/2/courses/33/lessons/what-is-a-slot) (login) |
| Ferramenta citada / Tool mentioned | [TestRail](https://www.testrail.com/), gestão de casos de teste / test case management |

## Slot × caso de teste / Slot vs test case

| | 🇧🇷 Português | 🇺🇸 English |
|---|---|---|
| **Slot** | vaga reservada com requisitos (país, idioma, aparelho, sistema, meio de pagamento) | reserved spot with requirements (country, language, device, OS, payment) |
| **Caso de teste / Test case** | os passos a seguir | the steps to follow |
| **Slot de caso de teste / Test Case slot** | traz 1 ou mais casos de teste, com **pagamento fixo** | 1+ test cases, **fixed payout** |
| **Slot exploratório / Exploratory slot** | sem caso de teste ("0 Exploratory"); paga **por bug aprovado** ("Per Bug") | no test case; paid **per approved bug** |
| **Usability** | estudos de usabilidade | usability studies |

⚠️ 🇧🇷 Se o slot tem vários casos de teste e você **não envia um deles**, **nenhum é aprovado**. Só pegue se der para terminar no prazo. 🇺🇸 Miss one test case in a multi-case slot and **none get approved**.

## Executar um caso de teste / Executing a test case

~~~mermaid
flowchart TD
    S[Abrir o caso de teste<br/>Open test case] --> P[Cumprir as pré-condições<br/>Meet preconditions]
    P --> X[Executar o passo no ambiente do slot<br/>Run step in the slot's environment]
    X --> Q{Resultado = esperado?<br/>Actual = expected?}
    Q -- Sim / Yes --> PASS[Pass e anexos pedidos<br/>Pass + required attachments]
    Q -- Sem resultado esperado<br/>No expected result --> DONE[Done]
    Q -- Não / No --> K{Bug já reportado?<br/>Already reported?}
    K -- Sim / Yes --> F1[Fail + ID do bug + confirmar +1<br/>Fail + bug ID + +1 confirm]
    K -- Não / No --> F2[Fail → Fail & Report Issue]
    PASS --> N{Último passo?<br/>Last step?}
    DONE --> N
    F1 --> N
    F2 --> N
    N -- Não / No --> X
    N -- Sim / Yes --> SUB[Submit Results + tempo gasto → Finished<br/>Submit Results + time spent]
~~~

### Resultado × status / Result vs status
- 🇧🇷 **Resultado** (andamento): New → Started → Passed / Failed / Completed (só "Done") / Unclaimed / Closed By TestCycle. **"Failed" não quer dizer reprovado**: só indica que algum passo falhou. 🇺🇸 **Result** (progress). "Failed" ≠ rejected.
- 🇧🇷 **Status** (decisão): Pending → **Info Requested** (corrija → *Undo Submission* → corrija → *Submit Results* → *Confirm all requested info is added*) → Approved (paga) / Rejected (não paga). 🇺🇸 **Status** (decision); Approved = paid.

### Boas práticas / Best practices
- 🇧🇷 Só pegue um slot se tiver o ambiente certo e tempo para começar **já**. **Nunca** cadastre aparelho falso para pegar slot. 🇺🇸 Claim only with the right environment and time to start **now**; never fake devices.
- 🇧🇷 Não vai dar tempo? **Solte o slot na hora** e avise o TTL. Segurar e soltar no fim derruba o rating. 🇺🇸 Can't finish? **Unclaim immediately** and tell the TTL.
- 🇧🇷 Anexe só o que o passo pede (aparece "Minimum 1"). Comprima vídeos (Handbrake), borre dados pessoais e dê nomes claros aos arquivos. 🇺🇸 Attach only what's required; compress videos; blur PII; clear file names.
- 🇧🇷 **Waitlist:** só entra quem não tem slot de caso de teste. Entrar na fila **não** conta como entrar no ciclo. 🇺🇸 **Waitlist:** only testers without a test case slot; joining it ≠ joining the cycle.
- 🇧🇷 **BFV** (verificar correção): use o **mesmo ambiente**; prazo de **2 horas**; se falhar, o comentário é obrigatório. 🇺🇸 **BFV:** same environment, **2-hour** limit, comment required on fail.
- 🇧🇷 **TestRail:** a conta é do cliente. Saia ao terminar, não mude senha nem configurações e execute só os seus casos. 🇺🇸 **TestRail:** the client's account; log out, change nothing, run only yours.

### Tester Review
- 🇧🇷 Escreva depois de testar tudo: frases completas, honestas, com estrelas coerentes com o texto. ⚠️ **Não use IA para escrever reviews** (Diretrizes de IA da uTest). 🇺🇸 Write after full testing; honest, full sentences; stars match the text. ⚠️ **No AI-written reviews.**

## Quiz comentado / Commented quiz (10/10)
1. Caso de teste / Test case → ✅ **conjunto de passos obrigatórios para testar um app** (❌ "um teste específico" = ciclo; "resumo de falhas" = bug report).
2. Bug novo num passo / New bug in a step → ✅ **Fail → "Fail & Report Issue"** (o bug fica ligado ao passo / linked to the step).
3. Bug já reportado / Already reported → ✅ **Fail + ID do bug existente + confirmar com +1**.
4. FALSO sobre slots / FALSE about slots → ✅ **"Slots exploratórios têm caso de teste"**.
5. Quando anexar / When to attach → ✅ **quando o passo pede e mostra um mínimo de anexos**.
6. Depois de pegar / After claiming → ✅ **começar logo e terminar no prazo**.
7. Terminou / Finished → ✅ **Submit Results**.
8. Sem tempo / No time → ✅ **soltar o slot na hora e avisar o TTL**.
9. Quem entra na waitlist / Waitlist eligibility → ✅ **quem tem slot exploratório, ou quem não tem slot de caso de teste e atende aos critérios**.
10. Quando entrou oficialmente / Officially joined → ✅ **ao pegar um slot (exploratório ou de caso de teste)**; ❌ só a fila não conta.
