# Test IO · Cybersecurity Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 10 de 10 (mínimo 6) · 17/11/2026 / Completed · 10 of 10 |
| Por que · Why | **Obrigatório para chegar ao nível Bronze ou acima** / **Required for Bronze level and above** |
| Fontes · Sources | [Social Engineering Techniques](https://academy.test.io/en/articles/9756414-social-engineering-techniques) · [What Is Phishing?](https://academy.test.io/en/articles/9716954-what-is-phishing) · [Data Privacy](https://academy.test.io/en/articles/9756578-data-privacy) · [How to keep your device safe](https://academy.test.io/en/articles/8989557-how-to-keep-your-device-safe-for-testing) · [DOs and DON'Ts](https://academy.test.io/en/articles/9716907-dos-and-don-ts-in-protecting-your-testing-devices) |

## Conceitos / Concepts
| Termo / Term | 🇧🇷 | 🇺🇸 |
|---|---|---|
| **Vulnerabilidade** | **ponto fraco** de um sistema ou rede que pode ser explorado | weakness that can be exploited |
| **Ameaça / Threat** | qualquer coisa capaz de causar dano: pessoas, acidentes, falhas de equipamento, desastres | anything capable of harm |
| **Engenharia social** | invasão **não técnica**, baseada em **enganar pessoas** e abusar da confiança | **non-technical** intrusion via human interaction |
| **Ameaça externa** | vem de fora: phishing, malware, ransomware, **SQL injection**, DDoS | from outside |
| **Ameaça interna** | vem de dentro: erro de alguém da equipe, uso indevido, bug em script de teste com dados reais | from inside |

🇧🇷 **Técnicas de engenharia social:** pedido direto, vasculhar o lixo (*dumpster diving*), mexer na correspondência, **phishing**, **se passar por outra pessoa** (suporte, chefe, fornecedor) e pesquisar o site da empresa. 🇺🇸 Direct request, dumpster diving, mailbox raiding, phishing, impersonation, surfing company sites.

🇧🇷 **Ferramentas de ataque:** varredura de vulnerabilidades, quebra de senha, *network spoofing* (tela de login falsa), vírus, worms, *logic bombs*, ransomware e DoS. 🇺🇸 Attacker tool kit.

> 🛡️ 🇧🇷 **O elo mais fraco é o fator humano. Você é a primeira linha de defesa.** 🇺🇸 **The human is the weakest link; you're the first line of defense.**

## Phishing: 7 sinais / 7 signs

~~~mermaid
flowchart TD
    E[E-mail ou mensagem suspeita] --> S{Sinais?}
    S --> A1[Remetente ou domínio estranho]
    S --> A2[Urgência: 'Urgente!', 'Ação necessária!']
    S --> A3[Saudação genérica: 'Prezado cliente']
    S --> A4[Erros de português/inglês]
    S --> A5[Pedido incomum: dinheiro, dados]
    S --> A6[Link suspeito: passe o mouse antes]
    S --> A7[Anexo inesperado, .exe]
    A1 & A2 & A3 & A4 & A5 & A6 & A7 --> R[Não clique, não responda, não encaminhe<br/>→ Reportar como phishing e depois apagar]
~~~

❌ 🇧🇷 **Não:** clicar em links, abrir anexos ou macros, **responder**, **encaminhar**, digitar senha depois de clicar num link nem passar documentos. ✅ **Sim:** usar o botão **Report Phish**/spam e depois apagar. 🇺🇸 Don't click/reply/forward; report, then delete.

## Privacidade de dados / Data privacy
| Nível / Level | 🇧🇷 Exemplos | 🇺🇸 |
|---|---|---|
| **Confidencial** | nome, e-mail, endereço, localização, data de nascimento, estado civil, foto | confidential PII |
| **Estritamente confidencial** | raça, opinião política, religião, sindicato, **biometria**, genética, orientação sexual, **saúde**, processos, **dados financeiros**, **credenciais**, documento de identidade | strictly confidential (sensitive) |

🇧🇷 Também é estritamente confidencial: dados de saúde (PHI), dados de cartão (PCI) e propriedade intelectual do cliente. **Usar ou compartilhar dados do cliente é proibido.** 🇺🇸 PHI, PCI and customer IP are strictly confidential.

## Proteja o aparelho / Protect your device
| ✅ Faça / Do | ❌ Não faça / Don't |
|---|---|
| Navegador e sistema **sempre atualizados**; antivírus atualizado | Salvar senhas no navegador |
| Senhas fortes e únicas + **2FA** | Usar a mesma senha em tudo |
| Wi-Fi com **WPA3**; **evitar Wi-Fi público** para coisas sensíveis (ou usar VPN) | Deixar o aparelho sozinho em público |
| **Criptografia** no aparelho; **bloqueio de tela** ou biometria | Usar software desatualizado |
| **Bloquear o computador** ao sair; backup regular | Abrir e-mails ou anexos suspeitos |
| Perdeu o aparelho? Avise o suporte da Test IO e troque a senha | Deixar outras pessoas usarem o seu computador |

⛔ 🇧🇷 **Proibido:** P2P/torrent sem autorização, pirataria, pornografia, *keygens* e *cracks*, anonimizadores, criptografia fora do padrão, **mineração de cripto**, ferramentas de hacking. 🇺🇸 Prohibited software list.

🦠 🇧🇷 **Suspeita de vírus?** Feche tudo, **desligue o computador** e procure assistência técnica ou faça uma varredura com um antivírus confiável. 🇺🇸 Shut down; get professional help or scan.

## Quiz comentado / Commented quiz (10/10)
1. Objetivo do phishing → ✅ **enganar a pessoa para ela entregar dados pessoais e financeiros**.
2. O que evitar com e-mail suspeito → ✅ **responder pedindo esclarecimento**.
3. Protege as contas → ✅ **evitar Wi-Fi público para atividades sensíveis**.
4. Segurança física → ✅ **bloqueio de tela com senha ou biometria**.
5. Atividade proibida → ✅ **usar P2P sem autorização**.
6. Computador infectado → ✅ **fechar tudo, desligar e procurar um profissional ou usar um antivírus confiável**.
7. Ameaça externa → ✅ **SQL injection** (❌ erro de alguém da equipe e bug em script são ameaças internas).
8. Estritamente confidencial → ✅ **biometria** (❌ nome e estado civil são só confidenciais).
9. Engenharia social → ✅ **invasão não técnica que depende de interação humana**.
10. Vulnerabilidade → ✅ **ponto fraco que deixa o sistema exposto**.
