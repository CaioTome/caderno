# 📝 Skill: Gerador de Caderno de Questões (Estilo FAPEC / Checkboxes)

> **Propósito:** Padronizar a criação de **Cadernos de Questões em Markdown** na pasta `questoes/` para prática pós-leitura do resumo, no estilo objetivo da banca **FAPEC / FACOM-UFMS** (`A–E`).

---

## 1. 📁 Organização de Pastas e Nomenclatura

- **Subpastas por disciplina** dentro de `questoes/` (sem acentos, em minúsculas):
  - `lingua-portuguesa/`
  - `governanca-ti/`
  - `engenharia-software/`
  - `legislacao-ti/`
  - `legislacao/` *(Constitucional, 8.112, 9.784)*
  - `raciocinio-logico/`
  - `lingua-inglesa/`
- **Nome do arquivo:** `Dia-<XX>-<DD.MM>-<Tema-Curto>.md` usando o **dia real de estudo** e a data de hoje (mesma referência cronológica registrada em `gestao/DIARIO_ESTUDOS.md`).
  - *Exemplo:* `questoes/lingua-portuguesa/Dia-06-25.11-Coesao-Coerencia-Interpretacao.md`

---

## 2. 🎯 Regras de Seleção das Questões

1. **Fonte real:** Extrair questões reais dos PDFs da aula em `materias/` (nunca inventar questões nem alterar gabaritos).
2. **Formato FAPEC (`A–E`):** Priorizar questões de **5 alternativas (`A, B, C, D, E`)** — da própria **FAPEC**, **FCC**, **FGV**, **Instituto AOCP**, **VUNESP (5 alt.)** ou **Multibancas (`A–E`)**. Evitar questões de 4 alternativas (`A–D`) ou `Certo/Errado`, salvo quando não houver `A–E` suficiente no PDF.
3. **Volume padrão:** **10 questões** por caderno (ou o total pedido pelo usuário).
4. **Regra Obrigatória de Língua Portuguesa (Intercalação 50/50):**
   - Sempre que a aula for de **Língua Portuguesa**, gerar **5 questões do tema do dia + 5 questões de Compreensão e Interpretação de Textos (Aula 17)**, **intercaladas** (ímpares = tema do dia; pares = Interpretação), pois Interpretação representa ~40% da prova de Português.
5. **Anti-Repetição & Qualidade:**
   - **Não repetir** questões que já constam como *Questões-Modelo Resolvidas* no resumo da aula (`resumos/<disciplina>/`) nem repetir subtópicos/pegadinhas idênticas.
   - **Descartar** questões com gabarito duvidoso, ambíguo ou contestado pelo próprio comentário do PDF (se for da FAPEC, registrar na seção de *Questões Problemáticas* do resumo).
   - **Equilíbrio:** alternar questões conceituais/interpretativas e questões de decoreba literal.

---

## 3. 🧩 Estrutura Padrão do Caderno

Todo caderno deve seguir exatamente esta estrutura:

1. **Cabeçalho:**
   - Título `# 📝 Caderno de Questões ... — <Disciplina> (Estilo FAPEC A–E)`
   - Bloco `>` com **Sessão** (`Dia XX (DD/MM/AAAA)`), **Disciplina**, **Conteúdos** e **Instruções** (*"Marque sua resposta com `[x]` nos checkboxes abaixo e confira o Gabarito apenas ao final."*).
2. **Questões numeradas (`01` a `10`):**
   - Subtítulo: `## Questão XX — <Subtópico> *(<Banca / Órgão — Ano>)*`
   - Texto de apoio completo (ou excerto necessário para resolver sem depender de página externa) em `blockquote` (`>`), seguido do enunciado.
   - 5 alternativas com checkboxes Markdown:
     ```markdown
     - [ ] **A)** ...
     - [ ] **B)** ...
     - [ ] **C)** ...
     - [ ] **D)** ...
     - [ ] **E)** ...
     ```
3. **Gabarito Seco ao Final (SEM comentários):**
   - Seção `## 📋 Gabarito` no final do arquivo com uma tabela simples contendo apenas **Questão**, **Assunto** e **Gabarito** (letra). **Não incluir justificativas nem comentários no arquivo** para manter o caderno limpo para revisão futura.

---

## 4. 🔄 Pós-Prática (Quando o Candidato Terminar)

Quando o usuário informar os acertos/erros ou pedir revisão:
1. **Registrar histórico no próprio `.md` do caderno de questões:**
   - Marcar `[x]` na alternativa que o candidato escolheu em **cada questão** (com `✅` se acertou, ou `❌ *(Sua resposta; Gabarito: X)*` se errou; se deixou em branco/teve dúvida, registrar em nota logo abaixo das alternativas).
   - Atualizar o cabeçalho com `**Resultado Registrado:** X/10 (XX,X%) — corrigido em DD/MM/AAAA`.
   - Atualizar a tabela `## 📋 Gabarito & Histórico` adicionando as colunas `Sua Resposta` e `Resultado` (`✅`/`❌`), mantendo o gabarito limpo e rastreável para futuras revisões.
2. Comentar no chat os acertos e os erros/dúvidas de forma imparcial (elogiando o raciocínio certo, pontuando exatamente onde houve falha e como corrigir, com mnemônico/regra se for decoreba).
3. Atualizar o resumo da aula em `resumos/<disciplina>/` com a seção `📊 Resultado da Prática de Questões` e sugestões para próximas revisões.
4. Atualizar `gestao/PAINEL_QUESTOES.md` com o placar consolidado e pontos de atenção.
5. Atualizar `gestao/DIARIO_ESTUDOS.md` (comparativo Planejado × Realizado, problemas e oportunidades) e `gestao/CONTROLE_HORAS.md` (se o candidato informar horas líquidas).
6. Marcar `[x]` no `gestao/CRONOGRAMA_ESTUDOS.md` quando a aula for concluída.

