# Test IO · Bug Fix & Bug Report Confirmation Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 8 de 8 (mínimo 6) · 17/11/2026 / Completed · 8 of 8 |
| Atenção · Note | 🔒 🇧🇷 Para receber essas tarefas, além do curso, é preciso ter **mais de 50 bugs enviados** e nível **Silver ou acima**. 🇺🇸 Also requires **50+ bugs** and **Silver level+** |
| Fontes · Sources | [Bug Fix Confirmation](https://academy.test.io/en/articles/3650880-bug-fix-confirmation) · [Bug Report Confirmation](https://academy.test.io/en/articles/5594889-bug-report-confirmation) |

## Diferença / Difference
| | 🇧🇷 Bug Fix Confirmation | 🇧🇷 Bug Report Confirmation |
|---|---|---|
| Quando / When | o cliente **corrigiu** um bug e quer saber se ficou resolvido | o cliente quer **confirmar se um bug novo existe**, fora do ciclo |
| Respostas / Options | **Bug is fixed** · **Bug is not fixed** · **Can't proceed** | **Bug exists** · **Bug doesn't exist** · **Can't proceed** |
| Extras | — | o cliente pode pedir **tamanho da tela**, **versão do navegador**, uma pergunta aberta ou **anexos especiais**: velocidade da internet (ex.: fast.com no começo e no fim do vídeo), console, câmera externa ou crash log |

## Como fazer / How to

~~~mermaid
flowchart LR
    D[Dashboard → Bug Confirmations] --> B[Begin<br/>reserva por 30 min]
    B --> R[Seguir os passos do bug original]
    R --> O{Resultado}
    O --> C[Comentário curto e preciso<br/>+ aparelho/navegador<br/>+ anexo]
    C --> S[Submit → vai direto ao cliente<br/>não dá para editar]
    B -.não consegue.-> X[Cancel/Reject → libera para outros]
~~~

- 🇧🇷 **Anexo:** vídeo quando há ação; print para problemas visuais. Valem as regras gerais de anexos. 🇺🇸 Screencast for actions, screenshot for UI.
- 🇧🇷 **Comentário:** é obrigatório principalmente quando o bug **continua**. Descreva com precisão e só o que importa, do ponto de vista do usuário. Se travou, diga o que impediu. 🇺🇸 Precise, relevant comment.
- 🇧🇷 **Additional requirements:** siga as instruções extras do cliente. 🇺🇸 Follow customer instructions.
- ⚠️ 🇧🇷 O resultado **vai direto para o cliente**, então escreva de forma profissional. 🇺🇸 Goes straight to the customer.

## Quiz comentado / Commented quiz (8/8)
1. Objetivo do Bug Fix Confirmation → ✅ **confirmar se um bug corrigido foi resolvido ou continua**.
2. Requisito do Bug Report Confirmation → ✅ **passar no curso + nível Silver ou acima + mais de 50 bugs**.
3. Reserva ao clicar em Begin → ✅ **30 minutos**.
4. Anexo → ✅ **vídeo quando há ação; print para problema visual**.
5. Não dá para seguir por problema técnico → ✅ **"Can't proceed" + explicação no comentário**.
6. Bug não corrigido → ✅ **"Bug is not fixed" + explicação no comentário**.
7. Onde aparece a tarefa → ✅ **no Dashboard (seção Bug Confirmations) e no menu de tarefas disponíveis**.
8. Exigência possível no Bug Report Confirmation → ✅ **anexo específico pedido pelo cliente**: velocidade da internet, console ou crash log.
