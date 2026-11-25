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
| [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md) | Cronograma mestre de 53 aulas (`20/11/2026` a `10/01/2027`) com status `[ ]`/`[x]` e links de apoio. |
| [gestao/PAINEL_QUESTOES.md](gestao/PAINEL_QUESTOES.md) | Placar consolidado de acertos, aproveitamento e pontos de revisão por matéria. |
| [gestao/CONTROLE_HORAS.md](gestao/CONTROLE_HORAS.md) | Registro diário de horários e tempo líquido de estudo. |
| `materias/` | PDFs principais, mapas mentais e listas extras organizados por disciplina *(ignorado no Git)*. |
| `resumos/` | Resumos de Ramp-Up por dia real (`Dia-XX-DD.MM/<SIGLA>-<NN>-<Tema>.md`). |
| `questoes/` | Cadernos de questões em Markdown com checkboxes (`- [ ]`) por disciplina (`questoes/<disciplina>/`). |
| [.agent/skills/skill-resumo.md](.agent/skills/skill-resumo.md) | **Skill obrigatória** para gerar Resumos de Ramp-Up e conduzir prática interativa. |
| [.agent/skills/skill-questoes.md](.agent/skills/skill-questoes.md) | **Skill obrigatória** para gerar Cadernos de Questões (`A–E`) pós-leitura. |

---

## 3. 📅 Regra de Ouro: Dia Real × Dia do Cronograma

- O candidato pode estar **adiantado ou atrasado** em relação às datas planejadas no `gestao/CRONOGRAMA_ESTUDOS.md`.
- **Sempre** nomear as pastas em `resumos/` e os arquivos em `questoes/` usando o **dia real de estudo e a data de hoje** (`Dia-XX-DD.MM`), mantendo a sequência real (`Dia-01`, `Dia-03`, `Dia-04`, `Dia-05`, `Dia-06`...).
- No `gestao/CRONOGRAMA_ESTUDOS.md`, localizar a próxima aula `[ ]` solicitada e vincular o resumo apontando para `../resumos/Dia-XX-DD.MM/...`. **Nunca** marcar `[x]` antes de o candidato concluir as questões.

---

## 4. 🔄 Fluxo Padrão de Cada Sessão de Estudo

1. **Identificar a Aula:** Conferir em [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md) qual aula está em andamento (próxima `[ ]` ou a indicada pelo candidato) e verificar o próximo `Dia-XX` em `resumos/`.
2. **Gerar Resumo de Ramp-Up:** Seguir integralmente [.agent/skills/skill-resumo.md](.agent/skills/skill-resumo.md) (inspecionar o PDF real com `pdftotext`/`pdfinfo`, checar divergência Edital × PDF, tabelas Pareto 80/20, Raio-X FAPEC, questões-modelo e roteiro no PDF) e adicionar o link no `gestao/CRONOGRAMA_ESTUDOS.md` (sem marcar `[x]`). *(O Quartz gera a árvore de navegação automaticamente no deploy.)*
3. **Gerar Caderno de Questões (enquanto o candidato lê o resumo):**
   - Seguir [.agent/skills/skill-questoes.md](.agent/skills/skill-questoes.md): **10 questões no formato FAPEC (`A–E`)**, com checkboxes `- [ ]` e **gabarito seco no final (sem comentários)**, salvas em `questoes/<disciplina>/Dia-XX-DD.MM-<Tema>.md`.
   - *(Se o candidato pedir prática interativa no chat em vez de caderno, enviar 1 questão por vez sem gabarito, conforme seção 5 de `skill-resumo.md`.)*
4. **Regra Especial de Língua Portuguesa:**
   - **Sempre** que a matéria do dia for **Língua Portuguesa**, intercalar **50% de questões do assunto do dia + 50% de Compreensão e Interpretação de Textos (Aula 17)**, pois Interpretação equivale a ~40% da prova de Português.
5. **Fechamento da Sessão (após o candidato responder):**
   - Explicar os erros/dúvidas no chat (com mnemônicos para decorebas).
   - Atualizar o resumo do dia em `resumos/Dia-XX-DD.MM/` com a seção `📊 Resultado da Prática de Questões`.
   - Atualizar [gestao/PAINEL_QUESTOES.md](gestao/PAINEL_QUESTOES.md) com o novo placar e pontos de atenção.
   - Atualizar [gestao/CONTROLE_HORAS.md](gestao/CONTROLE_HORAS.md) se o candidato informar o tempo líquido.
   - Marcar `[x]` na aula e no checklist correspondente do [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md).

