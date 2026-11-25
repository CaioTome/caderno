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
| [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md) | Cronograma mestre planejado de 53 aulas (`20/11/2026` a `10/01/2027`) com status `[ ]`/`[x]` e links de apoio. |
| [gestao/DIARIO_ESTUDOS.md](gestao/DIARIO_ESTUDOS.md) | Diário real dia a dia comparando **Planejado × Realizado** para identificar problemas, lacunas e oportunidades. |
| [gestao/PAINEL_QUESTOES.md](gestao/PAINEL_QUESTOES.md) | Placar consolidado de acertos, aproveitamento e pontos de revisão por matéria. |
| [gestao/CONTROLE_HORAS.md](gestao/CONTROLE_HORAS.md) | Registro diário de horários e tempo líquido de estudo. |
| `materias/` | PDFs principais, mapas mentais e listas extras organizados por disciplina *(ignorado no Git)*. |
| `resumos/` | Resumos de Ramp-Up organizados **por disciplina** (`resumos/<disciplina>/<SIGLA>-<NN>-<Tema>.md`). |
| `questoes/` | Cadernos de questões em Markdown com checkboxes (`- [ ]`) **por disciplina** (`questoes/<disciplina>/Dia-XX-DD.MM-<Tema>.md`). |
| `site/` | Projeto Quartz v5 (`5.2.2`) para publicação automática no GitHub Pages. |
| [.agent/skills/skill-resumo.md](.agent/skills/skill-resumo.md) | **Skill obrigatória** para gerar Resumos de Ramp-Up e conduzir prática interativa. |
| [.agent/skills/skill-questoes.md](.agent/skills/skill-questoes.md) | **Skill obrigatória** para gerar Cadernos de Questões (`A–E`) pós-leitura. |

### Pastas padronizadas por disciplina (`resumos/` e `questoes/`):
- `lingua-portuguesa/` (`LP-XX`)
- `governanca-ti/` (`GTI-XX`)
- `engenharia-software/` (`ES-XX`)
- `legislacao-ti/` (`LTI-XX`)
- `legislacao/` (`DC-XX`, `L8112-XX`, `L9784-XX`)
- `raciocinio-logico/` (`RLM-XX`)
- `lingua-inglesa/` (`ING-XX`)

---

## 3. 📅 Regra de Ouro: Dia Real × Dia do Cronograma

- O candidato pode estar **adiantado ou atrasado** em relação às datas planejadas no `gestao/CRONOGRAMA_ESTUDOS.md`.
- **Resumos** são salvos **por disciplina** (`resumos/<disciplina>/<SIGLA>-<NN>-<Tema>.md`), registrando no cabeçalho a data real e o dia correspondente do cronograma.
- **Cadernos de Questões** mantêm a referência cronológica no nome (`questoes/<disciplina>/Dia-XX-DD.MM-<Tema>.md`), usando sempre o **dia real de estudo e a data de hoje** (`Dia-01`, `Dia-03`, `Dia-04`, `Dia-05`, `Dia-06`...).
- **Diário de Estudos (`gestao/DIARIO_ESTUDOS.md`):** registrar tudo o que foi feito no dia real e atualizar o comparativo com o cronograma, destacando problemas (baixo aproveitamento, atrasos, aulas sem placar) e oportunidades (adiantamentos, janelas livres para revisão).
- No `gestao/CRONOGRAMA_ESTUDOS.md`, localizar a aula solicitada e vincular o resumo apontando para `../resumos/<disciplina>/...`. **Nunca** marcar `[x]` antes de o candidato concluir as questões.

---

## 4. 🔄 Fluxo Padrão de Cada Sessão de Estudo

1. **Identificar a Aula & Dia Real:** Conferir em [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md) a aula solicitada/pendente e verificar em [gestao/DIARIO_ESTUDOS.md](gestao/DIARIO_ESTUDOS.md) e [gestao/CONTROLE_HORAS.md](gestao/CONTROLE_HORAS.md) qual é o `Dia-XX` real de hoje.
2. **Gerar Resumo de Ramp-Up:** Seguir integralmente [.agent/skills/skill-resumo.md](.agent/skills/skill-resumo.md) (inspecionar o PDF real com `pdftotext`/`pdfinfo`, checar divergência Edital × PDF, tabelas Pareto 80/20, Raio-X FAPEC, questões-modelo e roteiro no PDF), salvar em `resumos/<disciplina>/<SIGLA>-<NN>-<Tema>.md` e adicionar o link no `gestao/CRONOGRAMA_ESTUDOS.md` (sem marcar `[x]`). *(O Quartz gera a árvore de navegação automaticamente no deploy.)*
3. **Gerar Caderno de Questões (enquanto o candidato lê o resumo):**
   - Seguir [.agent/skills/skill-questoes.md](.agent/skills/skill-questoes.md): **10 questões no formato FAPEC (`A–E`)**, com checkboxes `- [ ]` e **gabarito seco no final (sem comentários)**, salvas em `questoes/<disciplina>/Dia-XX-DD.MM-<Tema>.md`.
   - *(Se o candidato pedir prática interativa no chat em vez de caderno, enviar 1 questão por vez sem gabarito, conforme seção 5 de `skill-resumo.md`.)*
4. **Regra Especial de Língua Portuguesa:**
   - **Sempre** que a matéria do dia for **Língua Portuguesa**, intercalar **50% de questões do assunto do dia + 50% de Compreensão e Interpretação de Textos (Aula 17)**, pois Interpretação equivale a ~40% da prova de Português.
5. **Fechamento da Sessão (após o candidato responder):**
   - Explicar os erros/dúvidas no chat (com mnemônicos para decorebas).
   - Atualizar o resumo da aula em `resumos/<disciplina>/` com a seção `📊 Resultado da Prática de Questões` e os pontos para próximas revisões.
   - Atualizar [gestao/PAINEL_QUESTOES.md](gestao/PAINEL_QUESTOES.md) com o novo placar e pontos de atenção.
   - Atualizar [gestao/DIARIO_ESTUDOS.md](gestao/DIARIO_ESTUDOS.md) anotando o que foi concluído no dia real, placar e eventuais problemas/oportunidades frente ao cronograma.
   - Atualizar [gestao/CONTROLE_HORAS.md](gestao/CONTROLE_HORAS.md) com conteúdo e tempo líquido (quando informado).
   - Marcar `[x]` na aula e no checklist correspondente do [gestao/CRONOGRAMA_ESTUDOS.md](gestao/CRONOGRAMA_ESTUDOS.md).
