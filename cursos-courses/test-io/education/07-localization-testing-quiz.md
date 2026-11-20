# Test IO · Localization Testing (quiz)

| Campo · Field | Informação · Details |
| --- | --- |
| Plataforma · Platform | Test IO |
| Curso · Course | Localization testing skill assessment (convite da Test IO Community por e-mail · community invitation) |
| Situação · Status | ✅ Enviado · nota 4,61 de 5 · 20/11/2026 / Submitted · score 4.61 of 5 |
| Fonte · Source | Leitura curta + quiz no Typeform (uma tentativa só · one attempt) |

## O que é / What it is
🇧🇷 **Localização** é traduzir e **adaptar** o produto para um país ou cultura. **Teste de localização** verifica se o resultado está certo: textos, imagens, formatos, cultura e as funções ligadas ao conteúdo. **Traduzir não é tarefa de quem testa.**
🇺🇸 **Localization** = translating and adapting a product for a market. **Localization testing** checks the result. Translating is not the tester's job.

## Escopo / Scope
- 🇧🇷 Tradução certa de textos, dicas, mensagens · 🇺🇸 translation correctness
- Materiais localizados: imagens, banners, documentos · localized assets
- Adaptação cultural, religiosa e política · cultural fit
- **Formatos:** moeda, números, data e hora, telefone · formats
- Funções ligadas a idioma e região (ex.: trocar o país da loja e o idioma não mudar) · locale-related functionality

❌ 🇧🇷 **Fora do escopo:** teste unitário, teste de usabilidade, teste de segurança. 🇺🇸 Unit, usability and security testing are out.

## Categorias de bug / Bug categories
| Categoria | 🇧🇷 | 🇺🇸 |
|---|---|---|
| Context | tradução errada para aquele contexto | wrong in context |
| Culture | inadequado para a cultura | culturally inappropriate |
| Tone | tom errado para o público | wrong tone |
| Consistency | termos diferentes para a mesma coisa | inconsistent terms |
| Format | moeda, data, hora, número | formats |
| Grammar | gramática, pontuação, erro de digitação | grammar, typos |
| Missing translation | texto não traduzido ou em outro idioma | untranslated |
| UI | texto cortado, sobreposto, fonte ilegível | layout |
| Functional | função ligada ao conteúdo ou ao idioma | content-related function |

## Exemplo: e-mail de pedido para os EUA / Example: US order email
| Problema | Certo nos EUA |
|---|---|
| "February 9**th**, 2024" | sem "th" (February 9, 2024) |
| "14:50:38 PM" | relógio de 12 horas (2:50:38 PM) |
| "Shi**p**ing" | Shipping (erro de digitação) |
| "$89**,**15" | ponto decimal ($89.15) |
| "Co**lour**" | Color (inglês americano) |
| Tamanho **39** (europeu) | numeração americana |

## Respostas / Answers
1. Foco → garantir que o produto funciona bem num lugar ou cultura específica.
2. Fora do escopo → teste unitário, de usabilidade e de segurança.
3. Loja em inglês e italiano: bugs de localização → data no formato americano na versão italiana; moeda em pesos em qualquer idioma; site que não muda para italiano. *(Não marquei a imagem de produto faltando só na versão italiana.)*
4. Página alemã de passagens → texto não traduzido (calendário em inglês), texto cortado e **semana começando no domingo** (na Alemanha começa na segunda).
5. E-mail americano → erro de digitação, numeração europeia, formato de número, data, hora e termo britânico. *(Não marquei pontuação; "contains :" com espaço antes dos dois-pontos também é erro, o que pode explicar a nota 4,61.)*
