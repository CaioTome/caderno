# 🤖 AGENTS.md — Fluxo de Estudos & Convenções do Repositório

> **Leia este arquivo no início de qualquer sessão** para entender o contexto completo da preparação, a estrutura das pastas e o protocolo padrão de estudo sem que o candidato precise reexplicar.

---

## 1. 🎯 Contexto do Concurso & Perfil do Candidato

- **Concurso:** **UFMS** — *Analista de Tecnologia da Informação / Gestão de Projetos de Software* (Prova em `17/01/2027`).
- **Banca Examinadora:** **FAPEC** + Comissão Docente **FACOM/UFMS**.
  - **Formato:** Objetiva de **5 alternativas (`A, B, C, D, E`)**, foco em **literalidade normativa**, listas/taxonomias clássicas, itens `I, II, III, IV` e pedidos de **`INCORRETA` / `EXCETO`**.
- **Perfil do Candidato:** **Graduado em Engenharia de Software**.
  - Aplicar **Estudo Reverso (Fast-Track)** em temas de Computação/Lógica Booleana que já domina na prática.
  - Aplicar **Teoria Direcionada / Decoreba de Banca** em normas, legislações, processos (MPS.BR, PMBOK, IN 94/2022) e gramática.

---

## 2. 📂 Estrutura do Repositório

| Caminho | Função |
| :--- | :--- |
| [CRONOGRAMA_ESTUDOS.md](CRONOGRAMA_ESTUDOS.md) | Cronograma mestre de 53 aulas (`20/11/2026` a `10/01/2027`) com status `[ ]`/`[x]` e links de apoio. |
| `materias/` | PDFs principais, mapas mentais e listas extras organizados por disciplina. |
| `resumos/` | Resumos de Ramp-Up por dia real de estudo + skills e painel consolidado. |
| [resumos/00.skill-resumo.md](resumos/00.skill-resumo.md) | **Skill obrigatória** para gerar Resumos de Ramp-Up e conduzir prática interativa. |
| [resumos/01.painel-questoes.md](resumos/01.painel-questoes.md) | Placar consolidado de acertos, aproveitamento e pontos de revisão por matéria. |
| `questoes/` | Cadernos de questões em Markdown com checkboxes (`- [ ]`) organizados por disciplina. |
| [questoes/00.skill-questoes.md](questoes/00.skill-questoes.md) | **Skill obrigatória** para gerar Cadernos de Questões (`A–E`) pós-leitura. |

---

## 3. 📅 Regra de Ouro: Dia Real × Dia do Cronograma

- O candidato pode estar **adiantado ou atrasado** em relação às datas planejadas no `CRONOGRAMA_ESTUDOS.md`.
- **Sempre** nomear as pastas em `resumos/` e os arquivos em `questoes/` usando o **dia real de estudo e a data de hoje** (`Dia X - DD.MM - DiaSemana`), mantendo a sequência real (`Dia 1`, `Dia 3`, `Dia 4`, `Dia 5`, `Dia 6`...).
- No `CRONOGRAMA_ESTUDOS.md`, localizar a próxima aula `[ ]` solicitada e vincular o resumo apontando para a pasta real em `resumos/`. **Nunca** marcar `[x]` antes de o candidato concluir as questões.

---

## 4. 🔄 Fluxo Padrão de Cada Sessão de Estudo

1. **Identificar a Aula:** Conferir em `CRONOGRAMA_ESTUDOS.md` qual aula está em andamento (próxima `[ ]` ou a indicada pelo candidato) e verificar o próximo `Dia X` em `resumos/`.
2. **Gerar Resumo de Ramp-Up:** Seguir integralmente [resumos/00.skill-resumo.md](resumos/00.skill-resumo.md) (inspecionar o PDF real com `pdftotext`/`pdfinfo`, checar divergência Edital × PDF, tabelas Pareto 80/20, Raio-X FAPEC, questões-modelo e roteiro no PDF), adicionar o link no `CRONOGRAMA_ESTUDOS.md` (sem marcar `[x]`) e atualizar o [_sidebar.md](_sidebar.md) do Docsify.
3. **Gerar Caderno de Questões (enquanto o candidato lê o resumo):**
   - Seguir [questoes/00.skill-questoes.md](questoes/00.skill-questoes.md): **10 questões no formato FAPEC (`A–E`)**, com checkboxes `- [ ]` e **gabarito seco no final (sem comentários)**, salvas em `questoes/<Disciplina>/Dia XX - DD.MM - <Tema>.md`, e atualizar o [_sidebar.md](_sidebar.md).
   - *(Se o candidato pedir prática interativa no chat em vez de caderno, enviar 1 questão por vez sem gabarito, conforme seção 5 de `00.skill-resumo.md`.)*
4. **Regra Especial de Língua Portuguesa:**
   - **Sempre** que a matéria do dia for **Língua Portuguesa**, intercalar **50% de questões do assunto do dia + 50% de Compreensão e Interpretação de Textos (Aula 17)**, pois Interpretação equivale a ~40% da prova de Português.
5. **Fechamento da Sessão (após o candidato responder):**
   - Explicar os erros/dúvidas no chat (com mnemônicos para decorebas).
   - Atualizar o resumo do dia em `resumos/Dia X.../` com a seção `📊 Resultado da Prática de Questões`.
   - Atualizar [resumos/01.painel-questoes.md](resumos/01.painel-questoes.md) com o novo placar e pontos de atenção.
   - Marcar `[x]` na aula e no checklist correspondente do [CRONOGRAMA_ESTUDOS.md](CRONOGRAMA_ESTUDOS.md).

