# Test IO · Streaming Testing Course

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Situação · Status | ✅ Concluído · quiz 12 de 12 (mínimo 8) · 17/11/2026 / Completed · 12 of 12 |
| Por que · Why | **Obrigatório para receber convites de testes de streaming**. Tenho Smart TV Samsung e Fire TV Stick / **Required for streaming invites** |
| Fontes · Sources | [Best Practices and Bug Examples](https://academy.test.io/en/articles/9070542-best-practices-and-relevant-bug-examples-in-streaming-testing) · [Commonly used terms](https://academy.test.io/en/articles/9094513-the-most-commonly-used-terms-in-streaming-testing) · [Vídeo/Video](https://www.youtube.com/watch?v=tw2dSE5ojnk) |

## Boas práticas / Best practices
| 🇧🇷 | 🇺🇸 |
|---|---|
| Teste num **lugar silencioso**: muitos bugs são de **áudio**, e nesse caso grave o vídeo **com som** | Quiet place; record sound for audio bugs |
| Use o **trick play**: pausar, retomar, legendas, avançar, voltar, arrastar a barra (*scrub*) | Use **trick play** |
| **Aja como um usuário comum.** Apertar botões muito rápido gera bugs de "edge case", que são **rejeitados** | Mimic real users; no button mashing |
| Tenha uma **VPN confiável**: o conteúdo muitas vezes é bloqueado por país (*geo-blocking*) | Reliable **VPN** |
| **Cadastre todos os seus aparelhos de streaming** no perfil, com **modelo e sistema exatos** | Add all streaming devices, exact model/OS |
| Ao terminar, **apague o app e as credenciais de teste**. Usar a conta premium fora do teste dá **banimento** | Remove app & credentials after testing |
| Respeite o **escopo**. Bugs de **conteúdo** (catálogo) às vezes não são aceitos, porque o cliente não controla o catálogo | Respect scope; content bugs may be disabled |

✅ 🇧🇷 **Bugs que interessam:** legenda fora de sincronia ou que não funciona, erro ao dar play, **crash numa ação normal** (pausar, voltar, avançar), vídeo que não entra em "Salvos" ou "Continuar assistindo", anúncio que não toca. 🇺🇸 Relevant bug examples.

## Glossário / Glossary
| Termo / Term | 🇧🇷 Significado |
|---|---|
| Buffering | carregar parte do vídeo antes para tocar sem travar |
| Subtitles × Captions (CC) | legenda só com as falas × legenda com **todo o áudio**: falas, efeitos e quem fala (acessibilidade) |
| Live TV · EPG | TV ao vivo · guia de programação na tela |
| Hero Lane | faixa de destaque no topo da tela inicial |
| MDP · SDP | página de detalhes do filme · da série |
| VOD · SVOD · AVOD · FAST | vídeo sob demanda · por assinatura · grátis com anúncio · canais lineares grátis com anúncio |
| OTT | conteúdo pela internet, sem precisar de TV a cabo |
| PiP | vídeo numa janelinha por cima de outras telas |
| **Scrub** | **arrastar a barra** para ir a um ponto do vídeo |
| Skip | pular, por exemplo, +30 s ou −30 s |
| Geo-blocking | bloqueio de conteúdo por país |
| Chromecast · AirPlay | transmitir do celular ou computador para a TV |
| **Focus** | o elemento **selecionado ou ativo** na tela (navegação pelo controle) |
| **CTA** | botão que **chama para uma ação** (assinar, comprar) |
| Upselling · Regwall | oferecer um plano melhor · exigir cadastro para ver o conteúdo |

## Quiz comentado / Commented quiz (12/12)
1. Lugar silencioso → ✅ **para perceber bugs de som**.
2. Trick play → ✅ **imita as ações normais do usuário com o vídeo e ajuda a achar bugs**.
3. VPN → ✅ **acessar conteúdo bloqueado por país**.
4. CTA → ✅ **incentivar o usuário a fazer uma ação**.
5. Apagar app e credenciais → ✅ **evitar o uso indevido do conteúdo premium do teste**.
6. Como achar bugs → ✅ **agir como um usuário comum** (❌ apertar botões muito rápido; ❌ edge cases).
7. Tipo de teste → ✅ **funcional**.
8. Como ser convidada → ✅ **cadastrar o aparelho real no perfil e passar no curso**.
9. Ao cadastrar um aparelho → ✅ **escolher a versão exata do aparelho e do sistema**.
10. Scrubbing → ✅ **ir a um ponto específico do vídeo**.
11. Focus → ✅ **o elemento selecionado ou ativo na tela**.
12. Legendas e captions → ✅ **texto mostrado na tela durante o vídeo**.
