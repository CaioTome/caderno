# 🚀 Ramp-Up & Guia de Decorebas — Dia 05 (23/11/2026)
## 💻 Governança de TI: Aula 04 — Melhoria de Processo do Software Brasileiro (MPS.BR) — Guia de Implementação Nível F do MR-MPS-SW:2012

> **🎯 Foco Estratégico (TIER S — Altíssima Incidência):** O PDF principal tem **153 páginas**: **págs. 3 a 41** são teoria, **págs. 42 a 46** são resumo, **pág. 46** indica o mapa mental e **págs. 48 a 153** são questões comentadas (incluindo **2 questões literais da prova anterior FAPEC/UFMS 2022 para o seu exato cargo** nas págs. 111–113!). Modo da aula: **`🎯 Teoria Direcionada + Mapa Mental`**.

> 🚨 **ALERTA CRÍTICO DE EDITAL × PDF DO CURSO (LEIA ANTES DE TUDO!):**
> - **O Edital da Universidade Federal de Mato Grosso do Sul (UFMS)** cobra expressamente o **`Guia de Implementação Nível F do MR-MPS-SW:2012`** — e a prova anterior da **Fundação de Apoio à Pesquisa, ao Ensino e à Cultura (FAPEC) / UFMS 2022** cobrou exatamente a **versão 2012** (com `GRE`, `AQU`, `GCO`, `GQA`, `GPP`, `MED` e `AP 1.1 / AP 2.1 / AP 2.2`).
> - **O PDF de Teoria do curso (págs. 3–46) e o Mapa Mental de 2023** foram atualizados pelo professor para a **versão 2021/2023 do MR-MPS-SW** (que renomeou processos, absorveu `GQA`/`GPP` e trocou os `AP` por `CP-G`, `CP-F`, `CP-E/D/C`, `CP-B`, `CP-A`).
> - **Como este resumo blinda você:** trazemos **primeiro o núcleo cirúrgico do MR-MPS-SW:2012 (exigido no edital e na FAPEC 2022)** e, logo em seguida, o **mapa completo da versão 2021/2023 (usada no PDF e nas questões recentes da FCC/CEBRASPE/FGV)**, com tabela comparativa lado a lado para você nunca confundir as duas versões!

---

## 1. 🧭 Visão Geral, Origem e Componentes do MPS.BR (PDF págs. 3–16 e 42–43)

- **O que é o MPS.BR?** Programa **Melhoria de Processo do Software Brasileiro**, criado pela **Associação para Promoção da Excelência do Software Brasileiro (SOFTEX)** em **dezembro de 2003**.
- **Objetivo:** Oferecer um modelo de melhoria de processos de software **acessível, escalável e adaptado à realidade brasileira** (especialmente **pequenas e médias empresas — PMEs**), com menor custo de implementação/avaliação que modelos internacionais pesados.
- **Natureza:** O MPS.BR é um **modelo de referência / guia** (diz **o quê** fazer — propósito e resultados esperados), e **NÃO é uma metodologia** com passo a passo prescritivo (o **como** fazer fica a cargo da organização).
- **Relação com o CMMI (*Capability Maturity Model Integration*):** O MPS.BR **NÃO substitui** o CMMI — ele é **compatível** com o CMMI, porém dividido em **7 níveis (G a A)** em vez de 5, permitindo degraus menores e mais graduais (especialmente nos níveis iniciais G e F, que equivalem ao Nível 2 do CMMI).

### A) Os 5 Componentes do Programa MPS.BR (Decoreba Clássica!)

| Sigla | Nome Completo | O que define / Foco |
| :--- | :--- | :--- |
| **MR-MPS-SW** | **Modelo de Referência MPS para Software** | Processos e níveis de maturidade/capacidade para **desenvolvimento, manutenção e evolução de software**. *(É o foco da sua prova!)* |
| **MR-MPS-SV** | **Modelo de Referência MPS para Serviços** | Gestão de **serviços de TI** (alinhado à **ISO/IEC 20000**). |
| **MR-MPS-RH** | **Modelo de Referência MPS para Gestão de Recursos Humanos** | Gestão de pessoas / RH (recrutamento, capacitação, desempenho). |
| **MA-MPS** | **Método de Avaliação MPS** | Metodologia para **avaliar a conformidade** dos processos e emitir certificação por nível de maturidade. |
| **MN-MPS** | **Modelo de Negócio MPS** | Estrutura operacional e comercial: regras de **credenciamento** de **Instituições Implementadoras (II)** e **Instituições Avaliadoras (IA)** e governança do programa. |

### B) Bases Técnicas (Normas de Referência) e Governança

- **Normas que fundamentam o MPS.BR:**
  - **ISO/IEC 12207:** Processos de **ciclo de vida de software** (da concepção à retirada).
  - **ISO/IEC 15504 (SPICE)** *(evoluída para a família **ISO/IEC 330xx** nas versões 2021+)*: **Avaliação de processos** (maturidade e capacidade).
  - **CMMI (*Capability Maturity Model Integration*):** Compatibilidade internacional de maturidade.
  - **ISO/IEC 20000:** Gestão de serviços de TI (base do **MR-MPS-SV**).
  - **ISO 9001:** Sistema de gestão da qualidade.
  - **PNQ** (*Prêmio Nacional da Qualidade*) e **MoProSoft** (modelo mexicano equivalente para PMEs).
- **Instâncias de Governança (MN-MPS — PDF págs. 11–12):**
  - **SOFTEX:** Coordenação geral do programa.
  - **Equipe Técnica do Modelo (ETM):** Mantém e evolui os guias técnicos.
  - **Fórum de Credenciamento e Controle (FCC):** Credencia e acompanha qualidade das instituições.
  - **Comissão de Ética do Programa (CEP):** Zela pela integridade e ética do programa.
  - **Instituições Implementadoras (II)** × **Instituições Avaliadoras (IA):** Papéis separados para evitar conflito de interesses (quem implementa não avalia o mesmo projeto).

---

## 2. 📊 Os 7 Níveis de Maturidade do MR-MPS-SW (G ➔ A) — Decoreba Obrigatória!

> ⚠️ **Cuidado com a direção da escala:** Vai de **G (menos maduro / mais básico)** até **A (mais maduro / em otimização)**. **NÃO** é de 1 a 5 (como o CMMI) nem de A a E! Os níveis são **acumulativos**: alcançar o Nível F exige cumprir **todos os processos do Nível G + os do Nível F**.

| Nível | Nome Oficial (MR-MPS-SW:2012) | Nome no Guia 2021/2023 | Equivalência aproximada CMMI |
| :---: | :--- | :--- | :---: |
| **G** | **Parcialmente Gerenciado** | Parcialmente Gerenciado | Nível 2 (parcial) |
| **F** | **Gerenciado** *(Foco do Edital UFMS!)* | Gerenciado | Nível 2 (completo) |
| **E** | **Parcialmente Definido** | Parcialmente Definido | Nível 3 (parcial) |
| **D** | **Largamente Definido** | Definido | Nível 3 (parcial) |
| **C** | **Definido** | Totalmente Definido | Nível 3 (completo) |
| **B** | **Gerenciado Quantitativamente** | Gerenciado Quantitativamente | Nível 4 |
| **A** | **Em Otimização** | Em Otimização | Nível 5 |

> 💡 **Atenção à sutil diferença de nomes entre 2012 e 2021 nos níveis D e C:**
> - **Em 2012 (Edital UFMS e questões FAPEC/CONSULPLAN/FADESP no PDF):** `D = Largamente Definido` e `C = Definido`.
> - **Em 2021/2023 (Mapa Mental 2023):** `D = Definido` e `C = Totalmente Definido`.
> - **G, F, E, B e A têm EXATAMENTE o mesmo nome nas duas versões!** (F = **Gerenciado** — cobrado literalmente na Q21 da FAPEC/UFMS 2022!).

---

## 3. 🎯 NÚCLEO DO EDITAL UFMS: Guia de Implementação Nível F do MR-MPS-SW:2012

> ⚠️ **Nota de transparência:** O detalhamento completo do **MR-MPS-SW:2012 (Nível F)** abaixo complementa o PDF de teoria (que focou na versão 2021/2023) com base no guia oficial exigido no edital UFMS e nas questões da FAPEC/UFMS 2022 presentes no próprio PDF (págs. 111–113).

No **MR-MPS-SW:2012**, uma organização no **Nível F (Gerenciado)** deve implementar **7 processos ao todo** (**2 do Nível G + 5 adicionados no Nível F**) e satisfazer **3 Atributos de Processo (`AP 1.1`, `AP 2.1`, `AP 2.2`)** em todos eles!

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    NÍVEL F — GERENCIADO (MR-MPS-SW:2012)                │
├─────────────────────────────────────────────────────────────────────────┤
│  PROCESSOS DO NÍVEL G (Herança obrigatória — 2 processos):              │
│   1. GPR — Gerência de Projetos                                         │
│   2. GRE — Gerência de Requisitos                                       │
├─────────────────────────────────────────────────────────────────────────┤
│  PROCESSOS ADICIONADOS NO NÍVEL F (5 processos — DECORE!):              │
│   3. AQU — Aquisição                                                    │
│   4. GCO — Gerência de Configuração                                     │
│   5. GQA — Garantia da Qualidade                                        │
│   6. GPP — Gerência de Portfólio de Projetos                            │
│   7. MED — Medição                                                      │
├─────────────────────────────────────────────────────────────────────────┤
│  CAPACIDADE EXIGIDA NO NÍVEL F (3 Atributos de Processo):               │
│   • AP 1.1 — O processo é executado                                     │
│   • AP 2.1 — O processo é gerenciado                                    │
│   • AP 2.2 — Os produtos de trabalho do processo são gerenciados        │
└─────────────────────────────────────────────────────────────────────────┘
```

### A) Os 7 Processos do Nível F (MR-MPS-SW:2012) — Propósito Literal (Despenca na FAPEC!)

| Nível | Sigla | Processo | Propósito Oficial (Palavras-Chave de Prova) | Pegadinha Clássica FAPEC |
| :---: | :---: | :--- | :--- | :--- |
| **G** | **GPR** | **Gerência de Projetos** | Estabelecer e manter atualizados **planos** que definam as **atividades, recursos e responsabilidades** do projeto, bem como prover informações sobre o **andamento** do projeto para correções quando houver desvios significativos. | Dizer que GPR só atua no planejamento inicial (errado: inclui **monitoramento e ações corretivas**). |
| **G** | **GRE** | **Gerência de Requisitos** | Gerenciar os **requisitos do produto e dos componentes** do produto do projeto e identificar **inconsistências** entre os requisitos, os planos do projeto e os produtos de trabalho do projeto. | Confundir **GRE** (Nível G — *gerenciar* mudanças/rastreabilidade/inconsistências) com **DRE** — Desenvolvimento de Requisitos (Nível D — *elicitar/desenvolver* requisitos). |
| **F** | **AQU** | **Aquisição** | Gerenciar a **aquisição de produtos** que satisfaçam às necessidades expressas pelo adquirente — inclui **seleção de fornecedores**, acordo/contrato, monitoramento do fornecedor e aceitação do produto. | *(FAPEC 2022!)* Dizer que AQU **não** se aplica à **seleção de fornecedores** (ERRADO — selecionar fornecedores é parte essencial de AQU!). **Único processo que pode ser excluído** da avaliação se a empresa não adquire nada. |
| **F** | **GCO** | **Gerência de Configuração** | Estabelecer e manter a **integridade** de todos os **produtos de trabalho** de um processo ou projeto e disponibilizá-los a todos os envolvidos. Inclui controle de versões, **baselines** e **auditorias de configuração** (obrigatórias!). | *(FAPEC 2022!)* Dizer que GCO é restrita ao código ou apenas a uma etapa do ciclo de vida (ERRADO — aplica-se a **todo o ciclo de vida** e a **todos os produtos de trabalho**, incluindo documentos e planos). |
| **F** | **GQA** | **Garantia da Qualidade** | Assegurar que os **produtos de trabalho** e a **execução dos processos** estejam em **conformidade com os planos, procedimentos e padrões estabelecidos** (avaliação objetiva e tratamento de não conformidades). | *(FAPEC 2022!)* Dizer que GQA **assegura que os produtos não apresentarão defeitos** (ERRADO! GQA garante **conformidade com processos e padrões**, não ausência absoluta de bugs!). |
| **F** | **GPP** | **Gerência de Portfólio de Projetos** | Iniciar e manter **projetos necessários, suficientes e sustentáveis**, de forma a atender aos **objetivos estratégicos** da organização. | *(FAPEC 2022!)* Cobrou literalmente essa frase! *(Obs.: na prova de 2022 apareceu com erro de digitação da banca como "Portifólio de Trabalho (GPT)", mas o gabarito foi ela pela definição literal de GPP!).* |
| **F** | **MED** | **Medição** | **Coletar, armazenar, analisar e relatar** os dados relativos aos produtos desenvolvidos e aos processos implementados na organização e em seus projetos, de forma a **apoiar os objetivos organizacionais**. | *(FAPEC 2022!)* Dizer que MED serve para "mensurar quantitativamente o sucesso de um produto com base histórica comparativa" (ERRADO — o propósito é **coletar, armazenar, analisar e relatar dados objetivos** para apoiar decisões/objetivos). |

> 🧠 **Mnemônico para os 5 processos adicionados no Nível F (2012):** **"AQUi GCO GQA GPP MEDe"** ➔ **AQU**isição, **GCO** (Configuração), **GQA** (Qualidade), **GPP** (Portfólio), **MED**ição. *(E nunca esqueça que o Nível F herda **GPR** e **GRE** do Nível G = 7 processos no total!)*

### B) Atributos de Processo (AP) no MR-MPS-SW:2012 (PDF págs. 93 e questões)

| Atributo de Processo (AP) | Significado Oficial | Exigido a partir do Nível |
| :---: | :--- | :---: |
| **AP 1.1** | **O processo é executado** (atinge seu propósito) | **G** *(e todos acima)* |
| **AP 2.1** | **O processo é gerenciado** (planejado, monitorado e ajustado) | **G** *(e todos acima)* |
| **AP 2.2** | **Os produtos de trabalho do processo são gerenciados** | **F** *(e todos acima)* |
| **AP 3.1** | **O processo é definido** (processo padrão mantido) | **E** *(E, D, C, B, A)* |
| **AP 3.2** | **O processo está implementado** (desdobrado a partir do padrão) | **E** *(E, D, C, B, A)* |
| **AP 4.1** | **O processo é objeto de análise quantitativa** | **B** *(B e A)* |
| **AP 4.2** | **O processo é controlado quantitativamente** | **B** *(B e A)* |
| **AP 5.1** | **O processo é objeto de melhorias incrementais e inovações** | **A** |
| **AP 5.2** | **O processo é otimizado continuamente** | **A** |

> 🚨 **Pegadinha mortal sobre Nível G vs Nível F (2012):**
> - **Nível G** exige **`AP 1.1` e `AP 2.1`** (2 atributos).
> - **Nível F** acrescenta o **`AP 2.2`** (passa a exigir **`AP 1.1`, `AP 2.1` e `AP 2.2`** = 3 atributos).

---

## 4. 🔄 Evolução MR-MPS-SW:2012 × MR-MPS-SW:2021/2023 (Teoria do PDF págs. 17–46)

Para acertar **tanto** a prova da FAPEC (edital 2012) **quanto** as questões recentes do PDF (2021–2025, FCC/CEBRASPE/FGV), domine o que mudou na reestruturação de 2021/2023:

| Aspecto | MR-MPS-SW:2012 *(Edital UFMS)* | MR-MPS-SW:2021 / 2023 *(PDF Teoria & Mapa Mental)* |
| :--- | :--- | :--- |
| **Divisão dos Processos** | Lista única por nível de maturidade (19 processos no total) | **2 Conjuntos:** **Processos de Projeto** (5) e **Processos Organizacionais** (7) = **12 processos** que evoluem ao longo dos níveis |
| **Capacidade do Processo** | **9 Atributos de Processo** (`AP 1.1` a `AP 5.2`) | **5 Níveis de Capacidade simplificados:** `CP-G`, `CP-F`, `CP-E/D/C`, `CP-B`, `CP-A` |
| **Requisitos** | **GRE** (Nível G) + **DRE** (Nível D) | Unificados em **REQ — Engenharia de Requisitos** (inicia no G, evolui no D) |
| **Qualidade (GQA)** | Processo separado no Nível F (**GQA**) | Absorvida na capacidade **`CP-F`** e em **GPC (Gerência de Processos)** |
| **Portfólio (GPP)** | Processo separado no Nível F (**GPP**) | Absorvida em **ORG / OSW — Gerência Organizacional de Software** |
| **Riscos (GRI)** | Processo separado no Nível C (**GRI**) | Absorvida em **GPR** (no projeto) e **ORG/OSW** (na organização) — *não existe processo separado de Riscos em 2021!* |
| **Verificação & Validação** | Separados no Nível D (**VER** e **VAL**) | Unificados em **VV — Verificação e Validação** (Nível D) |
| **Exclusão de Processos** | Exclusão completa apenas de **AQU** (se não executado) | Exclusão completa apenas de **AQU** + exclusão parcial permitida apenas de **ORG 8, ORG 9 e ORG 10** (justificada no Plano de Avaliação, aceite do Avaliador Líder) |

### Os 2 Conjuntos de Processos no MR-MPS-SW:2021/2023 (Cai MUITO na FCC e CEBRASPE — PDF págs. 23–41)

- **Processos de Projeto (5 processos — foco no produto/projeto):**
  1. **GPR** — Gerência de Projetos *(inicia no G; evolui em D, B, A)*
  2. **REQ** — Engenharia de Requisitos *(inicia no G; evolui no D)*
  3. **PCP** — Projeto e Construção do Produto *(Nível D)*
  4. **ITP** — Integração do Produto *(Nível D)*
  5. **VV** — Verificação e Validação *(Nível D)*
- **Processos Organizacionais (7 processos — foco em recursos e apoio organizacional):**
  1. **GCO** — Gerência de Configuração *(inicia no F; auditorias de configuração obrigatórias — GCO5)*
  2. **AQU** — Aquisição *(inicia no F; evolui em C, B — **único que pode ser excluído completamente**)*
  3. **MED** — Medição *(inicia no F; evolui em C, B, A)*
  4. **GPC** — Gerência de Processos *(inicia no F; evolui em E, B)*
  5. **ORG / OSW** — Gerência Organizacional (de Software) *(inicia no F; evolui em E, C, B — **único com exclusão parcial: ORG 8, 9 e 10**)*
  6. **GRH / Capacitação** — Gerência de Recursos Humanos / Capacitação *(inicia no G/E conforme tabela do PDF)*
  7. **GDE** — Gerência de Decisões *(inicia no C)*

### Os 5 Níveis de Capacidade no MR-MPS-SW:2021/2023 (PDF págs. 21–22 e 44–45)

| Capacidade | Resumo Literal | Palavras-Chave |
| :---: | :--- | :--- |
| **CP-G** | A **execução do processo é gerenciada** | Produz resultados definidos; execução planejada e monitorada; pessoas preparadas. |
| **CP-F** | A **execução do processo e os produtos de trabalho são gerenciados** | Produtos avaliados objetivamente contra padrões; resultados registrados/comunicados; **não conformidades resolvidas**. |
| **CP-E/D/C** | O **processo é definido** | Processo padrão e diretrizes de adaptação usados; oportunidades de melhoria identificadas. |
| **CP-B** | O **processo é previsível** | Técnicas **estatísticas e quantitativas** para prever alcance de objetivos de qualidade/desempenho. |
| **CP-A** | O **processo é melhorado continuamente** | Propostas de melhoria selecionadas e implementadas com base em análise estatística/quantitativa. |

---

## 5. 📏 Avaliação MPS (MA-MPS): Etapas e Escala Oficial `F, L, P, N` (PDF págs. 10–11)

### A) As 4 Etapas do Processo de Avaliação (MA-MPS)
1. **Preparar a realização da avaliação** (viabilizar, planejar escopo/critérios/recursos e preparar evidências).
2. **Realizar a avaliação inicial** (visão de partida e completar preparação).
3. **Realizar a avaliação final** (conclusiva sobre evidências + avaliar a própria execução da avaliação + relatar resultados).
4. **Documentar os resultados da avaliação** (registro formal para auditoria e melhoria contínua).

### B) Escala de Atendimento dos Atributos/Resultados — Decore os Percentuais!

| Sigla | Grau de Atendimento | Faixa Percentual |
| :---: | :--- | :---: |
| **F** | **Totalmente Satisfeito** (*Fully achieved*) | **86% a 100%** |
| **L** | **Largamente Satisfeito** (*Largely achieved*) | **51% a 85%** |
| **P** | **Parcialmente Satisfeito** (*Partially achieved*) | **16% a 50%** |
| **N** | **Não Satisfeito** (*Not achieved*) | **0% a 15%** |

> 💡 **Dica de Prova:** Para obter a certificação em um nível de maturidade, os resultados esperados e atributos exigidos devem ser classificados como **L (Largamente)** ou **F (Totalmente)** satisfeitos (não pode haver **P** ou **N** nos requisitos obrigatórios do nível).

---

## 6. 🔍 Raio-X FAPEC (UFMS) + Questões Reais da Prova Anterior Comentadas

> **🎯 Como a FAPEC/FACOM cobra MPS.BR:**
> 1. **Literalidade de nomes de níveis** (troca o nome do Nível F "Gerenciado" por "Definido", "Parcialmente Gerenciado" etc.).
> 2. **Propósito literal dos 5 processos do Nível F (`AQU, GCO, GQA, GPP, MED`)** — criando pegadinhas restritivas ("AQU *não* inclui seleção de fornecedores", "GCO é *restrita* a uma etapa", "GQA garante *zero defeitos*").
> 3. **Confusão entre Propósito × Resultado Esperado** (*Propósito* = objetivo de alto nível; *Resultado Esperado* = resultado observável quando o propósito é alcançado).
> 4. **Exclusão de processos:** Dizer que qualquer processo pode ser excluído (ERRADO: exclusão completa só de **AQU**!).

### 🧪 Questões Literais da Sua Banca no PDF (FAPEC — 2022 — Analista de TI / UFMS / Gestão de Projetos de Software)

1. **Questão 20 — Processos do Nível F *(PDF págs. 111–112)* — Gabarito: Letra C**
   - **Cobrou:** Os 5 processos adicionados no Nível F (`AQU`, `GQA`, `GCO`, `GPP`, `MED`).
   - **Por que C está certa:** **GPP** deve *iniciar e manter projetos necessários, suficientes e sustentáveis para atender aos objetivos estratégicos da organização*.
   - **Erros das outras (pegadinhas clássicas da FAPEC):**
     - `(a)` AQU **inclui sim** seleção de fornecedores.
     - `(b)` GCO **não** se restringe a uma etapa do ciclo de vida (abrange todo o ciclo de vida e todos os produtos de trabalho).
     - `(d)` GQA **não** garante ausência de defeitos (garante conformidade com planos e padrões).
     - `(e)` MED visa coletar, armazenar, analisar e relatar dados para apoiar objetivos organizacionais (não "medir sucesso com base histórica comparativa").

2. **Questão 21 — Nome do Nível F *(PDF págs. 112–113)* — Gabarito: Letra D**
   - **Cobrou:** Sobre o Nível F no MR-MPS-SW, é correto afirmar que: **o Nível F é Gerenciado**.
   - **Pegadinhas:** `(a)` Definido = C; `(b)` Parcialmente Gerenciado = G; `(c)` Quantitativamente Gerenciado = B; `(e)` Parcialmente Definido = E.

---

## ⚠️ Questões Problemáticas da FAPEC (Atenção ao Gabarito/Enunciado)

> Registro de questões da **FAPEC** com enunciado ou gabarito que merecem cautela. *(Por enquanto só a FAPEC; outras bancas não são registradas.)*

| Questão | Problema Identificado | Como lidar na prova |
| :--- | :--- | :--- |
| **FAPEC 2022 — Q20 (PDF págs. 111–112), Nível F** | A alternativa correta (`c`) traz **erro de digitação da própria banca**: "Gerência de **Portifólio de Trabalho (GPT)**" no lugar de **Gerência de Portfólio de Projetos (GPP)**. O gabarito (`C`) só se sustenta pela **definição literal** de GPP ("iniciar e manter projetos necessários, suficientes e sustentáveis…"). | Escolher pela **definição** e não pela sigla/nome, que pode vir truncado ou errado. Eliminar primeiro as alternativas com erro conceitual claro (`a, b, d, e`). |
| **FAPEC 2022 — Q21 (PDF págs. 112–113), Nome do Nível F** | O enunciado das alternativas está **mal redigido** ("o Nível MR-MPS-SW é gerenciado"), mas o gabarito (`D`) é inequívoco: F = **Gerenciado**. | Ignorar a redação truncada e associar apenas o **nome do nível**. |

---

## 📊 Resultado da Prática de Questões (23/11/2026)

> **Pontuação: 7/10 (70%)**

| # | Banca / Ano | Subtópico | Sua resposta | Gabarito | Resultado |
| :-: | :--- | :--- | :-: | :-: | :-: |
| 1 | CEPS UFPA 2022 | Níveis de maturidade e processos do F (2012) | B | B | ✅ |
| 2 | IADES 2023 | Papéis na avaliação (Observador) | B | B | ✅ |
| 3 | FCC 2025 | Processos de projeto × organizacionais (2021/23) | B | B | ✅ |
| 4 | FCC 2023 | Características do `CP-F` | B | D | ❌ |
| 5 | IADES 2023 | `AP 3.1` = processo definido | C | C | ✅ |
| 6 | FCC 2024 | Exclusão de processos, capacidade, acumulação | D | D | ✅ |
| 7 | ACAFE 2024 | O que o MPS.BR **não** exige (ISO 9001) | A | B | ❌ |
| 8 | IADES 2024 | Capacidade por nível | E | D | ❌ *(questão questionável)* |
| 9 | CEBRASPE 2025 | Evolução do `GPR` a partir do D | Certo | Certo | ✅ |
| 10 | IADES 2023 | Resultado do `AP 3.2` | D | D | ✅ |

### 🔁 Pontos Sugeridos para Revisar

1. **Capacidade do processo por nível (erro da Q4):** treinar o raciocínio *"o enunciado já diz o que falta"*. `CP-F` = execução **+ produtos de trabalho** gerenciados (`AP 2.2` em 2012). Refazer a tabela `CP-G / CP-F / CP-E-D-C / CP-B / CP-A`.
2. **Bases técnicas × requisitos (erro da Q7):** lembrar que ISO 9001, CMMI, `ISO/IEC 12207`, `20000` e `330xx` são **referências** do modelo. O MPS.BR é *compatível*, mas **não exige** SGQ da ISO 9001 nem CMMI.
3. **Níveis G, F, E, D, C, B e A além do F:** o resumo detalha só até o F. Revisar o **mapa de evolução** dos processos (`GPR` evolui em D, B, A; `REQ` no D; `MED` em C, B, A; `AQU` em C, B; `GPC` em E, B; `ORG` em E, C, B).
4. **Atributos de Processo (2012):** `AP 1.1` e `AP 2.1` no **G**; `AP 2.2` acrescenta no **F**; `AP 3.1` e `3.2` no **E/D/C**; `AP 4.x` no **B**; `AP 5.x` no **A**. Lembrar que **`AP 3.1` = definido** e **`AP 3.2` = implementado**.
5. **Dois nomes para o nível D e o nível C** (2012 × 2021): D = *Largamente Definido* → *Definido*; C = *Definido* → *Totalmente Definido*.
6. **Q8 (IADES 2024):** questão ambígua, em que `d` e `e` eram defensáveis. Na prova, em casos assim, escolher a alternativa que a banca costuma marcar. Não foi registrada na tabela de problemáticas porque é do IADES e não da FAPEC.

---

### 🧱 Complemento Pedido: O que Muda nos Níveis **E, D e C** (Virada Organizacional & Engenharia)

Enquanto **G e F** olham para **projetos individuais**, **E, D e C** padronizam a **organização inteira**:

| Nível | Nome (2012 / Edital) | Nome (2021/2023) | Ideia Central | Processos-chave que entram (MR-MPS-SW:2012) |
| :---: | :--- | :--- | :--- | :--- |
| **E** | **Parcialmente Definido** | Parcialmente Definido | Nasce o **processo padrão da empresa** (com adaptação para cada projeto) e capacitação | `DFP` (Definição do Processo Org.), `AMP` (Avaliação e Melhoria), `GRH` (Recursos Humanos), `GRU` (Gerência de Reutilização) |
| **D** | **Largamente Definido** | Definido | Entra a **engenharia técnica completa do produto** no padrão organizacional | `DRE` (Desenv. de Requisitos), `PCP` (Projeto e Construção), `ITP` (Integração do Produto), `VER` (Verificação: *construir certo*), `VAL` (Validação: *produto certo*) |
| **C** | **Definido** | Totalmente Definido | Fecha a definição total com **gestão proativa de riscos, decisões e reúso** | `GRC` (Gerência de Riscos), `GDE` (Gerência de Decisões), `DRU` (Desenv. para Reutilização) |

---

## 📊 Resultado da Prática de Questões — Sessão 2 (24/11/2026)

> **Pontuação: 4 / 5 (80%)** *(bateria alternada com PMBOK 6; questão ACAFE 2024 descartada por já ter sido feita na Sessão 1)*.

| # | Banca / Ano | Subtópico | Sua resposta | Gabarito | Resultado |
| :-: | :--- | :--- | :---: | :---: | :---: |
| **Q2** | FCC / TRT-1ª 2025 | Propósito de `GPR` (Nível G) | `E` | `E` | ✅ |
| **Q4** | FADESP / UNIFESSPA 2025 | Escala dos 7 níveis (`C` = Definido) | `A` | `A` | ✅ |
| **Q6** | FCC / TRT-2ª 2025 | Capacidade `G → F` (`AP 2.2` / `GQA`) | `D` | `B` | ❌ |
| **Q8** | FGV / MPE-RJ 2025 | Processos organizacionais × projetos | `E` | `E` | ✅ |
| **Q10** | CONSULPLAN / MPE-PA 2022 | Nível D — Verificação (`VER`) × Validação (`VAL`) | `B` | `B` | ✅ |

### 🔁 Pontos de Revisão (Sessão 2)
1. **Diferença prática `G → F` (erro da Q6):** no **Nível G**, os processos já são **executados, planejados, monitorados e com pessoas preparadas** (`AP 1.1` + `AP 2.1`). O salto para o **Nível F** acontece quando entram **auditoria/verificação objetiva** de aderência a padrões, **avaliação de produtos de trabalho** e **resolução de não conformidades** (`AP 2.2` + `GQA`).
2. **Evolução sólida:** subiu de **70% (7/10)** para **80% (4/5)**, acertando inclusive separação de processos organizacionais vs. projeto (FGV 2025) e `VER × VAL` (Nível D).

---

## 7. 🎯 Roteiro Prático no PDF (Modo `🎯 Teoria Direcionada + Mapa Mental`)

1. **Releia as tabelas das Seções 2, 3 e 5 deste resumo** (10 min) para fixar os 7 níveis, os 7 processos do Nível F (2012), os APs (`1.1, 2.1, 2.2`) e a escala `F, L, P, N`.
2. **Abra o PDF Principal** [4 MPS.BR — Guia de Implementação nível F do MR-MPS-SW:2012.pdf](file:///home/caio/Documentos/%28E%29%202026_2_%20P%C3%93S%20-%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Governan%C3%A7a%20de%20TI%20para%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o_Gest%C3%A3o%20de%20Projetos%20de%20Software%29/4%20MPS.BR%20%E2%80%94%20Melhoria%20de%20Processo%20do%20Software%20Brasileiro_%20Guia%20de%20Implementa%C3%A7%C3%A3o%20n%C3%ADvel%20F%20do%20MR-MPS-SW_2012..pdf) e o [🧠 Mapa Mental 2023](file:///home/caio/Documentos/%28E%29%202026_2_%20P%C3%93S%20-%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Governan%C3%A7a%20de%20TI%20para%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o_Gest%C3%A3o%20de%20Projetos%20de%20Software%29/MPS.BR%20%E2%80%94%20Melhoria%20de%20Processo%20do%20Software%20Brasileiro_%20Guia%20de%20Implementa%C3%A7%C3%A3o%20n%C3%ADvel%20F%20do%20MR-MPS-SW_2012./4.1%20MPS.BR%20-%20Teoria%20-%20Mapa%20mental%20-%20MPS.BR%202023%20-%20vers%C3%A3o%2018-08-2026.pdf) — passe os olhos no **Resumo das págs. 42–46** (5 min) e **pule a leitura linear das págs. 3–41**.
3. **Ordem de Ataque nas Questões Comentadas (Meta: 30 a 40 questões hoje):**
   - **Prioridade 1 — Multibancas (pág. 100 a 132):** Onde estão as questões da **FAPEC/UFMS 2022** (págs. 111–113) e diversas bancas `A–E` cobrando 2012, 2016 e 2021!
   - **Prioridade 2 — FCC (pág. 67 a 81) e IADES (pág. 90 a 94):** Múltipla escolha `A–E` muito parecida com a FAPEC (literalidade de processos, APs e níveis).
   - **Prioridade 3 — CEBRASPE (pág. 48 a 59):** Modo *Flashcard de Velocidade* (Certo/Errado) para caçar palavras trocadas em 10 segundos.
4. **Ao terminar:** Me envie os seus acertos e as questões que errou para montarmos o **Caderno de Erros** e marcarmos o `[x]` do **Dia 05** no [CRONOGRAMA_ESTUDOS.md](../../gestao/CRONOGRAMA_ESTUDOS.md)!

