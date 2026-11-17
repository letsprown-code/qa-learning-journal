# uTest Academy · Testing Tools · 01: Screenshots

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 5 de 5 / Completed · quiz 5 of 5 |
| Fonte / Source | [uTest Academy: Screenshots](https://platform.utest.com/academy/tracks/6/courses/37/lessons/basics-screenshots) (login) |
| Referências / References | [Apple: tirar print no Mac / take a screenshot on Mac](https://support.apple.com/guide/mac-help/mh26782/mac) · [ShareX](https://getsharex.com/) · [Flameshot](https://flameshot.org/) |

## Regras do print / Screenshot rules

| 🇧🇷 Regra | 🇺🇸 Rule |
|---|---|
| **Destaque o bug** com retângulo, círculo ou seta, em **vermelho ou amarelo** | **Highlight** with a red or yellow rectangle, circle or arrow |
| Salve em **.jpg ou .png** | Save as **.jpg or .png** |
| ❌ **Não desenhe à mão livre**; use uma forma pronta | ❌ **No freehand drawing**; use a proper shape |
| Capture a **tela inteira**, com a **barra de endereço** quando for site | Capture the **whole screen**, incl. the **URL bar** for websites |
| Feche as abas que não têm a ver com o teste | Close unrelated browser tabs |
| Print sempre **na vertical correta** (de pé) | Always **upright** orientation |
| **No máximo 2 prints** por relatório de bug | **Max 2 screenshots** per bug report |
| Borre dados pessoais (nome, e-mail, telefone, foto) | Blur personal data (PII) |

~~~mermaid
flowchart LR
    A[Achou o bug<br/>Found the bug] --> B[Print da tela inteira<br/>Full-screen capture]
    B --> C[Retângulo vermelho no bug<br/>Red rectangle on the bug]
    C --> D[Borrar dados pessoais<br/>Blur PII]
    D --> E[Salvar .png ou .jpg<br/>Save .png/.jpg]
    E --> F[Anexar ao relatório<br/>Attach to report]
~~~

## Como tirar o print / How to capture

| Sistema / OS | 🇧🇷 Como | 🇺🇸 How |
|---|---|---|
| **macOS** | <code>Shift + Command + 3</code> (tela inteira). Clique na miniatura no canto → retângulo ou círculo → **Done**. Vai para a Mesa. | <code>Shift + Command + 3</code>; click the thumbnail → shape → **Done**. Saved to Desktop. |
| **Windows** | <code>Win + PrintScreen</code> (salva em Imagens > Capturas) ou <code>Win + Shift + S</code> (Ferramenta de Captura) → colar no **Paint** → forma → salvar. Alternativa: **ShareX** (desmarque o envio para a nuvem). | <code>Win + PrintScreen</code> or <code>Win + Shift + S</code> → paste in **Paint** → shape → save. Or **ShareX** (turn off cloud upload). |
| **Linux** | **Flameshot** (<code>sudo apt-get install flameshot</code>) → selecionar tela inteira → forma → Save | **Flameshot** → full screen → shape → Save |
| **Android** | **Power + Volume −** juntos. Marcar com um app (ex.: iMarkup) ou no computador (Paint / Pré-Visualização). | **Power + Volume Down**; mark up with an app or on a computer |
| **iOS** | iPhone novo: **Power + Volume +**; antigo: **Home + Power**. Fotos → Editar → **Markup** → + → forma, **No Fill**, contorno vermelho ou amarelo. | New: **Power + Volume Up**; old: **Home + Power**. Photos → Edit → **Markup** → shape, **No Fill**, red/yellow stroke |

💡 🇧🇷 No Mac, <code>Shift + Command + 4</code> captura só uma área. Para o uTest, o padrão é a **tela inteira** (<code>Shift + Command + 3</code>). 🇺🇸 On Mac, <code>Shift + Command + 4</code> captures an area; uTest expects the **whole screen** (<code>Shift + Command + 3</code>).

## Quiz comentado / Commented quiz (5/5)
1. Qual afirmação NÃO é verdadeira? / Which is NOT true? → ✅ **"Sempre use a ferramenta de desenho à mão livre"** (é o contrário: use formas prontas / the opposite: use proper shapes).
2. Máximo de prints por relatório / Max screenshots per report → ✅ **2**.
3. Afirmação correta sobre prints / Correct statement → ✅ **"Todas as anteriores" / All of the above** (destacar, .jpg/.png, tela inteira).
4. Teclas no macOS / macOS keys → ✅ **Shift, Command e 3**.
5. Forma para destacar / Shape to highlight → ✅ **Retângulo / Rectangle**.
