# Test IO · Flashcards (ações, features e bugs de IA)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Actions and Movements Flashcards · Standard Feature Descriptions Flashcards · AIIAT (LLM) Testing Flashcards |
| Situação · Status | ✅ Concluídos · 20/11/2026 (sem nota; cartões de estudo) / Completed (study cards, no score) |
| Fonte · Source | Flashcards no Typeform, a partir do painel da Test IO |

🇧🇷 Resumos com as minhas palavras, para usar o **nome certo** no título e nos passos do relatório de bug. 🇺🇸 My own summaries, to use the **right term** in bug titles and steps.

## 1. Ações e movimentos / Actions and movements
| Termo / Term | 🇧🇷 | 🇺🇸 |
|---|---|---|
| Background / Foreground | minimizar o app sem fechar / voltar para ele | minimize without closing / bring back |
| Click / Right-click | botão esquerdo (ação direta) / direito (menu de contexto) | left button / context menu |
| Copy and Paste | Ctrl+C e Ctrl+V (⌘ no Mac); no celular, toque longo | copy/paste |
| Filter / Sort | **filtrar** reduz a lista por critério; **ordenar** muda a ordem | narrow vs. reorder |
| Hover | passar o mouse sobre um elemento (tooltip, menu) | mouse over |
| Long press | toque longo, o "clique direito" do celular | touch equivalent of right-click |
| Pull to Refresh | puxar a tela para baixo para recarregar | drag down to reload |
| Pinch | gesto de pinça para dar zoom | zoom gesture |
| Rotate | girar o aparelho (retrato ↔ paisagem) | orientation change |
| Scroll / Tap | rolar / tocar para acionar | scroll / tap |
| Undo / Redo | desfazer / refazer | reverse / restore |
| Deep Link | link que abre direto uma tela específica do app | link to a specific screen |
| Breadcrumb | trilha "Início > Categoria > Produto" | position in the hierarchy |
| Redirect | ser levada automaticamente para outra página | automatic forwarding |
| Back Navigation | voltar pela seta, navegador ou gesto | go back |
| Modal Open / Close | abrir / fechar janela sobre a tela | dialog over content |
| Expand / Collapse | abrir / fechar menu, acordeão ou lista | show / hide content |
| Autofill | preencher campos sozinho com dados salvos | auto-populate fields |

## 2. Features padrão / Standard features
| Feature | 🇧🇷 O que inclui | 🇺🇸 |
|---|---|---|
| **Cart** | carrinho e **mini cart** (no cabeçalho): editar quantidade, remover, comprar | cart and mini cart |
| **Header** | topo da página | top of page |
| **Footer** | rodapé: links legais, contato, redes sociais | bottom of page |
| **Navigation** | toda a movimentação: menu principal, hambúrguer, menu fixo, barra lateral, breadcrumbs | all navigation menus |
| **Homepage** | conteúdo **entre** cabeçalho e rodapé da página inicial | content between header and footer |
| **Landing Page** | página de chegada de um link ou anúncio | page reached from a link/ad |
| **Login** | entrar e sair da conta | log in / out |
| **Sign Up** | criar conta | register |
| **My Account** | dados pessoais e configurações | personal info and settings |
| **PDP** (Product Detail Page) | página de um produto: informações, fotos, opções, sugestões | single product page |
| **PLP** (Product Listing Page) | lista de produtos de uma categoria | category list |

> ⚠️ 🇧🇷 **Header, Navigation e Footer são features separadas.** Um bug no menu do topo da Home é de **Navigation**, não de Homepage. 🇺🇸 Header, Navigation and Footer are separate features.

## 3. Bugs de IA (AIIAT / LLM) / AI bugs
| Tipo / Type | 🇧🇷 | 🇺🇸 |
|---|---|---|
| Bias | resposta com estereótipo ou injusta sobre um grupo | unfair/stereotyped answer |
| Context Window Issue | esquece ou mistura o que foi dito antes na conversa | forgets earlier context |
| Hallucination | inventa um fato falso como se fosse verdade | made-up fact |
| Citation Hallucination | inventa fontes, estudos ou links que não existem | fake sources |
| Wrong Answer | erra sem inventar (ex.: conta errada) | simply wrong |
| Ignoring Instructions | não segue o formato ou a instrução pedida | ignores format/instructions |
| Irrelevant Response | responde outra coisa | off-topic |
| Language Mixing | responde no idioma errado ou mistura idiomas | wrong/mixed language |
| Overly Generic Response | resposta genérica, sem detalhe útil | too generic |
| Leaking Hidden Instructions | revela regras internas ou do sistema (risco de segurança) | reveals system prompt |
| Prompt Injection | usuário manipula a IA para ignorar as regras | manipulated instructions |
| Privacy Issue | expõe dados pessoais sem cuidado | exposes personal data |
| Refusing Safe Request | recusa um pedido inofensivo | over-refusal |
| Toxic or Offensive Content | grosseria, insulto, crítica desrespeitosa | rude/insulting |
