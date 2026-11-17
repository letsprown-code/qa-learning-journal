# uTest Academy · Testing Tools · 02: Screen Recordings

| Campo / Field | Valor / Value |
|---|---|
| Plataforma / Platform | uTest (Applause) |
| Situação / Status | ✅ Concluído · quiz 5 de 5 / Completed · quiz 5 of 5 |
| Fonte / Source | [uTest Academy: Screen Recordings](https://platform.utest.com/academy/tracks/6/courses/38/lessons/basics-screen-recording) (login) |
| Referências / References | [HandBrake](https://handbrake.fr/) · [Apple: gravar a tela do Mac / record the Mac screen](https://support.apple.com/guide/mac-help/mh26782/mac) |

⚠️ 🇧🇷 **Nunca salve nem envie vídeos e anexos para a nuvem** (ex.: o botão "upload" do ScreenPal). Isso viola os Termos de Uso do uTest. Salve só no computador e anexe direto no relatório. 🇺🇸 **Never save or upload recordings to the cloud**; it violates the uTest Terms of Use. Save locally and attach to the report.

## Regras do vídeo / Recording rules

| 🇧🇷 Regra | 🇺🇸 Rule |
|---|---|
| **Sem som**: microfone desligado, a não ser que o ciclo peça narração | **No noise**: mic off unless the cycle asks |
| **Tela inteira**, com a barra de endereço quando for site | **Entire screen**, incl. URL bar |
| O vídeo **segue os passos do "Actions Performed"** e começa no site ou ao abrir o app | **Matches the Actions Performed**, starting from the site/app |
| Só **.mp4** | **.mp4 only** |
| **Curto**: tente ficar abaixo de 1 minuto; passe disso só se precisar | **Short**: aim for under 1 minute; longer only if needed |
| **1 vídeo por relatório** | **One recording per report** |
| **Comprima** arquivos grandes (HandBrake) | **Compress** large files |
| Câmera externa ou segundo celular só se o ciclo pedir ou se não der para gravar por software | External camera only if asked or software recording isn't possible |
| Confira se o vídeo **toca dentro da plataforma** | Check the video **plays on the platform** |
| Borre dados pessoais (PII) | Blur PII |

## Como gravar / How to record

| Sistema / OS | 🇧🇷 Como | 🇺🇸 How |
|---|---|---|
| **macOS** | QuickTime Player → Arquivo → **Nova Gravação de Tela** → **Gravar Tela Inteira** → Opções: Microfone **Nenhum**, **Mostrar cliques do mouse**, salvar na Mesa. Depois troque **.mov → .mp4** e comprima. | QuickTime → File → **New Screen Recording** → **Record Entire Screen**; mic **None**, **Show Mouse Clicks**; rename **.mov → .mp4** and compress |
| **Windows** | **ScreenPal** ou **BandiCam** (MP4, sem áudio, tela cheia, cursor visível) ou **Xbox Game Bar** (<code>Win + G</code>; vídeo maior, sem pausa, só grava a janela ativa) | ScreenPal / BandiCam / Xbox Game Bar |
| **Linux** | **Kazam** (<code>sudo apt install kazam -y</code>), sem som, cursor e tela cheia | Kazam, no sound, cursor on, fullscreen |
| **Android** | Gravador nativo (Android 11+) ou **AZ Screen Recorder** sem áudio. Dica: ative **Mostrar toques** nas Opções do desenvolvedor (toque 7× no Número da versão). | Built-in recorder or AZ; enable **Show taps** in Developer Options |
| **iOS** | Central de Controle → **Gravação de Tela** (segure → microfone desligado). Para mostrar toques: AssistiveTouch com gesto personalizado. Alternativa: **AirServer** (espelhar no computador). | Control Center → **Screen Recording**, mic off; AssistiveTouch for touches; or AirServer |

## HandBrake: para que serve / what it's for

~~~mermaid
flowchart TD
    V[Vídeo gravado<br/>Recorded video] --> H[Abrir no HandBrake<br/>Open in HandBrake]
    H --> F[Formato .mp4<br/>Output .mp4]
    H --> C[Comprimir: Very Fast 720p30 ou 1080p30<br/>Compress]
    H --> A[Áudio: None<br/>Remove audio]
    H --> O[Dimensions: girar se precisar<br/>Rotate if needed]
    H --> N[Anamorphic: None/Off<br/>Fix squeezed video]
    F & C & A & O & N --> S[Start Encode → assistir o resultado<br/>Encode → watch the output]
~~~

- 🇧🇷 Vídeo com **menos de 5 MB** normalmente não precisa comprimir. 🇺🇸 Under **5 MB** usually needs no compression.
- 🇧🇷 Crie um **preset personalizado** (sem áudio, anamorphic desligado) para não configurar tudo de novo a cada vídeo. 🇺🇸 Save a **custom preset** to reuse the settings.

## Quiz comentado / Commented quiz (5/5)
1. Qual NÃO é verdade? / Which is NOT true? → ✅ **"Grave o barulho de fundo"** (o certo é sem som / should be silent).
2. Formato do vídeo / Video format → ✅ **mp4** (❌ mov, m4v, mp3).
3. Quando usar aparelho externo para gravar / When to use an external device → ✅ **Todas as opções**: quando o ciclo pede, quando não dá por software e quando o gravador não captura o app por segurança.
4. Software para comprimir / Compression software → ✅ **HandBrake**.
5. Vídeo com mais de 1 minuto? / Longer than a minute? → ✅ **Tente ficar abaixo de 1 minuto; passe só se for necessário.**
