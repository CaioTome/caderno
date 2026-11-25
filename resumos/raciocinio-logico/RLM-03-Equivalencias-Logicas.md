# 🚀 Ramp-Up & Guia de Decorebas — Dia 06 (25/11/2026)
## 📐 Raciocínio Lógico-Matemático (RLM) — Aula 03: Equivalências Lógicas (*Mapa Mental + Bateria Pesada de Questões*)

> 🎯 **Foco Estratégico:** **TIER S** (tema nº 1 de RLM em provas) • PDF de **173 págs** • Modo `🎯 Mapa Mental + Bateria Pesada de Questões`.
> **Divisão real do PDF (extraída do sumário):**
> | Seção | Páginas | Tipo |
> | :--- | :---: | :--- |
> | 3.1 Equivalências e Negações Lógicas | 3–47 | Teoria (resumo na pág. 4) |
> | 3.2 Questões Comentadas — Multibancas | 48–79 | Questões |
> | 3.3 Álgebra de Proposições | 80–109 | Teoria (resumo na pág. 81) |
> | 3.4 Questões Comentadas — Multibancas | 110–124 | Questões |
> | 3.5 Outras Equivalências e Negações | 125–153 | Teoria (resumo na pág. 126) |
> | 3.6 Questões Comentadas — Multibancas | 154–167 | Questões |
> | 3.7 Questões Extras — Multibancas | 168–173 | Questões |
>
> ℹ️ **Auditoria Edital × PDF:** não há divergência de versão (lógica é atemporal). **Nenhuma questão FAPEC/UFMS foi encontrada no PDF** (bancas: CEBRASPE, FGV, VUNESP, Quadrix, Instituto Verbena, Consulplan, Fundatec, FEPESE etc.). As questões-modelo abaixo são de bancas de perfil literal/objetivo (`A–E`), parecido com a FAPEC.

> 💡 **Como Engenheiro de Software:** quase tudo aqui se resolve **sem decorar**: monte a tabela-verdade (ou pense em código) para confirmar qualquer equivalência. Mas na prova o tempo é curto, então **decore as 5 regras de ouro da Seção 1** — elas resolvem ~90% das questões.

---

## 1. ⭐ As 5 Regras de Ouro (Págs. 4 e mapa mental) — Decore Estas!

**Conceito:** duas proposições são **equivalentes (≡)** quando têm **a mesma tabela-verdade** (mesmos valores V/F para todas as combinações).

| # | Regra | Fórmula | Em português | Em código |
| :-: | :--- | :--- | :--- | :--- |
| 1 | **Contrapositiva** | `p→q ≡ ~q→~p` | Inverte **e** nega os dois lados | `!q → !p` |
| 2 | **Condicional → OU** | `p→q ≡ ~p ∨ q` | **"NEGA a 1ª OU mantém a 2ª"** | `!p \|\| q` |
| 3 | **OU → Condicional** | `p ∨ q ≡ ~p→q` | Nega a 1ª, vira "se…então" *(também `~q→p`)* | `!p → q` |
| 4 | **De Morgan** | `~(p∧q) ≡ ~p ∨ ~q` / `~(p∨q) ≡ ~p ∧ ~q` | Nega tudo e **troca E↔OU** | `!(a&&b) == !a\|\|!b` |
| 5 | **Negação da Condicional** | `~(p→q) ≡ p ∧ ~q` | **"MANÉ":** **Ma**ntém a 1ª **E** **Ne**ga a 2ª | `p && !q` |

- **Dupla negação:** `~(~p) ≡ p`.
- **Visão algébrica (reduz o que decorar):**
  - **2 e 3 são a mesma regra** nos dois sentidos (`p→q ≡ ~p∨q`; trocando `p` por `~p`, vira `~p→q ≡ p∨q`).
  - **5 sai da 2 + De Morgan:** `~(p→q) ≡ ~(~p∨q) ≡ p ∧ ~q` (o *MANÉ* é só atalho de velocidade).
  - **Leitura intuitiva de `p→q`:** **"`p` depende de `q`"** (se `p` acontece, `q` precisa acontecer; por isso `q` é condição *necessária* para `p`, e se `q` falhar, `p` também falha: `~q→~p`).
  - **Exemplo intuitivo de `p∨q ≡ ~p→q`:** *"Paga a conta (`p`) **ou** a luz será cortada (`q`)"* ≡ *"Se **não** pagar a conta (`~p`), a luz será cortada (`q`)"*.
  - **⚡ Técnica da Única Linha Falsa (para questões confusas):** `p→q` só é falsa em `V→F` (`p ∧ ~q`), e `p∨q` só é falsa em `F∨F` (`~p ∧ ~q`). No exemplo acima, a **única situação falsa** é *"não pagou a conta e a luz não foi cortada"*. Duas proposições equivalentes têm exatamente a mesma única linha falsa — basta testar isso nas alternativas!
- 🚫 **ARMADILHA #1 (cai SEMPRE):** `p→q` **NÃO** é equivalente à **recíproca** `q→p` nem à **inversa** `~p→~q`. Só a **contrapositiva** vale.
  - Mnemônico: *Recíproca* = só **inverte**; *Inversa* = só **nega**; *Contrapositiva* = **inverte + nega** ✅.
- 🚫 **ARMADILHA #2:** a negação de uma condicional **NÃO é outra condicional** (é uma conjunção `p ∧ ~q`).
- 🚫 **ARMADILHA #3 (negar proposição simples):** **não use antônimo!** Negar "O time venceu" = "O time **não** venceu" (nunca "perdeu"). Negar "bem-informado" ≠ "mal-informado" (o PDF cobra isso, pág. 161).

### Negação com quantidade de partes (De Morgan em 3 termos)
`~(p ∧ q ∧ r) ≡ ~p ∨ ~q ∨ ~r` e `~(p ∨ q ∨ r) ≡ ~p ∧ ~q ∧ ~r`.

---

## 2. 🧮 Álgebra de Proposições (Págs. 81–82)

| Propriedade | Regra | Atenção |
| :--- | :--- | :--- |
| **Comutativa** | `p∧q ≡ q∧p` • `p∨q ≡ q∨p` • `p⊻q ≡ q⊻p` • `p↔q ≡ q↔p` | ⚠️ **Todos, EXCETO o condicional** (`p→q ≢ q→p`) |
| **Associativa** | `(p∧q)∧r ≡ p∧(q∧r)` • `(p∨q)∨r ≡ p∨(q∨r)` | Só vale para `∧` e `∨` |
| **Distributiva** | `p∧(q∨r) ≡ (p∧q)∨(p∧r)` • `p∨(q∧r) ≡ (p∨q)∧(p∨r)` | Igual à álgebra booleana |
| **Identidade** (`t` = tautologia, `c` = contradição) | `p∧t ≡ p` • `p∧c ≡ c` • `p∨t ≡ t` • `p∨c ≡ p` | |
| **Absorção** | `p∨(p∧q) ≡ p` • `p∧(p∨q) ≡ p` | |
| **Idempotência** | `p∧p ≡ p` • `p∨p ≡ p` | |

- **Bicondicional em tautologia/contradição:** `X↔Y` é **tautologia** se X e Y são **equivalentes**; é **contradição** se uma é a **negação** da outra.
- O próprio PDF diz: *"o mais importante é conhecer comutativa, associativa e distributiva; as demais raramente caem e as difíceis se resolvem por tabela-verdade."*

---

## 3. 🔬 Outras Equivalências e Negações (Págs. 126–127 — "baixa incidência, mas podem aparecer")

| Tema | Fórmulas |
| :--- | :--- |
| **Negação do E → forma condicional** | `~(p∧q) ≡ p→~q` • `~(p∧q) ≡ q→~p` |
| **Conjunção de condicionais — consequente comum** | `(p→r)∧(q→r) ≡ (p∨q)→r` *(antecedentes viram **OU**)* |
| **Conjunção de condicionais — antecedente comum** | `(p→q)∧(p→r) ≡ p→(q∧r)` *(consequentes viram **E**)* |
| **OU exclusivo (`⊻`, "ou…ou")** | `p⊻q ≡ ~p⊻~q` • `p⊻q ≡ ~p↔q` • `p⊻q ≡ p↔~q` |
| **Negação do OU exclusivo** | `~(p⊻q) ≡ p↔q` ⭐ • `~(p⊻q) ≡ ~p⊻q` • `~(p⊻q) ≡ p⊻~q` *(nega **só uma** parcela)* |
| **Bicondicional (`↔`)** | `p↔q ≡ (p→q)∧(q→p)` • `p↔q ≡ ~p↔~q` • `p↔q ≡ ~p⊻q` • `p↔q ≡ p⊻~q` |
| **Negação da bicondicional** | `~(p↔q) ≡ p⊻q` ⭐ • `~(p↔q) ≡ ~p↔q` • `~(p↔q) ≡ p↔~q` • `~(p↔q) ≡ (p∧~q)∨(q∧~p)` |

> 🧠 **Truque de ouro (em código):** `⊻` (**XOR** = `p != q`, *diferentes*) e `↔` (**XNOR / Bicondicional** = `p == q`, *iguais*) são **opostos exatos** — negar um dá o outro (`!(p != q)` é `p == q`).

---

## 4. 🎭 Tradutor Linguístico (Reaproveita a Aula 01 + Sinônimos do Condicional)

| Expressão em Português | Fórmula | Atenção / Equivalência ou Negação |
| :--- | :---: | :--- |
| *"Se `p`, então `q`"* / *"Quando `p`, `q`"* | `p → q` | Forma padrão do condicional |
| *"`p` **é condição suficiente** para `q`"* | `p → q` | **S**uficiente fica na **1ª** posição (`p`) |
| *"`q` **é condição necessária** para `p`"* | `p → q` | ⚠️ **Inverte a ordem:** `p` **depende** de `q` (o necessário vai depois da seta) |
| *"`p` **somente se** `q`"* | `p → q` | ⚠️ `p` depende de `q` — não confundir com *"se e somente se"* (`p ↔ q`) |
| *"Ou `p` ou `q`, **mas não ambos**"* | `p ⊻ q` | Negação = *"p se e somente se q"* (`p ↔ q`) |
| *"Nem `p` nem `q`"* | `~p ∧ ~q` | Equivalente a `~(p ∨ q)` (De Morgan) |
| *"Não é verdade que `p` e `q`"* | `~(p ∧ q)` | Equivalente a `~p ∨ ~q` (De Morgan) |

> 📌 **Quantificadores (*"Todo / Algum / Nenhum"*):** não pertencem a esta aula — serão tratados na **Aula 04 (Diagramas Lógicos)**, no dia 13.

---

## 5. 🚨 Raio-X FAPEC / Pegadinhas Clássicas do Tema

1. **Recíproca/Inversa disfarçada de contrapositiva** (alternativa só nega ou só inverte).
2. **Negação da condicional escrita como outra condicional** (`~(p→q)` ≠ `p→~q`).
3. **De Morgan sem trocar o conectivo** (negou as duas partes mas manteve o "e"/"ou").
4. **Antônimo no lugar da negação** (*"bom"* ≠ não-*"mau"*; *"par"* → *"não é par"* — no domínio dos inteiros, *ímpar* funciona, mas a banca aceita antônimo só se o enunciado garantir).
5. **Comutatividade aplicada ao "se…então"** (`p→q ≢ q→p`).
6. **Equivalência escondida em "ou":** `p ∨ q ≡ ~p→q` — alternativas com "Se… então" no lugar de "ou".

---

## 6. ✅ Questões-Modelo do PDF (Resolvidas)

### Q1 — (Instituto Verbena UFG / Pref. Gameleira de Goiás 2026) • *Negação de condicional com OU*
> *"Se hoje **não** chover, então eu vou à praia **ou** vou correr na orla."*
- **Gabarito: A** → *"Hoje não chove **e** eu não vou à praia **e** não vou correr na orla."*
- **Resolução:** `~(~c → (p ∨ o)) ≡ ~c ∧ ~(p ∨ o) ≡ ~c ∧ ~p ∧ ~o` (**MANÉ** + De Morgan).
- **Pegadinha:** as demais mantêm o *"se…então"* ou trocam *"não chove"* por *"chove"*.

### Q2 — (VUNESP / EBSERH 2020) • *Negação do OU exclusivo*
> Negação de *"Rosana é vulnerável ou necessitada, mas **não ambos**"*:
- **Gabarito: A** → *"Rosana é vulnerável **se, e somente se,** ela é necessitada."*
- **Resolução:** `~(p ⊻ q) ≡ p ↔ q`. *(Na Q1 da pág. 169 do PDF cai a mesma ideia: `~(j ⊻ p) ≡ j ↔ p`.)*

### Q3 — (FGV / ALE-GO 2026) • *Condicional → OU com conjunção no antecedente*
> *"Se a bola é branca **e** a caixa **não** é azul, então a ficha é vermelha."*
- **Gabarito: C** → *"A bola não é branca **ou** a caixa é azul **ou** a ficha é vermelha."*
- **Resolução:** `(b ∧ ~a) → f ≡ ~(b ∧ ~a) ∨ f ≡ (~b ∨ a) ∨ f` (`~p ∨ q` + De Morgan).
- **Pegadinha (alternativa D):** esqueceu de aplicar dupla negação em `~a` (`~~a = a`).

### Q4 — (Instituto Verbena UFG / IFS 2024) • *Contrapositiva*
> **P:** *"Se n² é par, então n é par."*
- **Gabarito: A** → *"Se n não é par, então n² é ímpar."*
- **Resolução:** contrapositiva `~q → ~p` (no domínio dos naturais, *"não par"* equivale a *"ímpar"*).

---

## 7. 🎯 Roteiro Prático no PDF

1. **PDF principal (173 págs):** [3 Equivalências Lógicas.pdf](file:///home/caio/Documentos/%28E%29%202026_2_%20P%C3%93S%20-%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Racioc%C3%ADnio%20L%C3%B3gico%20para%20UFMS/3%20Equival%C3%AAncias%20L%C3%B3gicas.pdf)
2. **Mapa Mental (2 págs, 5 min):** [3.1 Mapa Mental](file:///home/caio/Documentos/%28E%29%202026_2_%20P%C3%93S%20-%20UFMS%20%28Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Racioc%C3%ADnio%20L%C3%B3gico%20para%20UFMS/Equival%C3%AAncias%20L%C3%B3gicas/3.1%20Equival%C3%AAncias%20e%20Nega%C3%A7%C3%B5es%20L%C3%B3gicas%20-%20Mapa%20Mental%20-%20Racioc%C3%ADnio%20L%C3%B3gico%20-%20Estrategia%20academy%20-%20Equival%C3%AAncias%20L%C3%B3gicas.pdf)
3. **Leia só:** páginas **4** (resumo 3.1), **81–82** (resumo 3.3) e **126–127** (resumo 3.5). **Pule** a teoria longa (págs. 5–47, 83–109, 128–153) e vá às questões.
4. **Ordem das baterias:**
   1. **3.2** (págs. 48–79) → *Múltipla Escolha `A–E`* primeiro (Verbena, FGV, VUNESP, Consulplan).
   2. **3.6** (págs. 154–167) e **3.4** (págs. 110–124).
   3. **CEBRASPE Certo/Errado** em modo *Flashcard de Velocidade* (10 s por item).
   4. **3.7** (págs. 168–173) + PDFs extras da pasta (Exercícios de Fixação Parte 04 e 3.2 Questões Multibancas Parte 01).
5. **Meta:** **30 a 40 questões**, priorizando negação de condicional, contrapositiva, `p→q ≡ ~p∨q` e De Morgan. Registre cada erro no **Caderno de Erros**.
6. **Regra de ouro na prova:** na dúvida, teste com **tabela-verdade de 4 linhas** ou com valores V/F concretos para eliminar alternativas.

---

## 📊 Resultado da Prática de Questões (24/11/2026)

- **Pontuação:** **3 / 6 (50%)** nas questões respondidas *(Q7 enviada, sessão encerrada antes da resposta)*.

| # | Banca / Ano | Subtópico | Sua Resposta | Gabarito | Resultado |
| :-: | :--- | :--- | :---: | :---: | :---: |
| **Q1** | FUNDATEC / PC-RS 2026 | Equivalência da condicional (Contrapositiva × *"somente se"*) | `B` | `E` | ❌ |
| **Q2** | AOCP / Polícia Penal-PR 2024 | Negação da conjunção + forma condicional (`~(q∧p) ≡ p→~q`) | `E` | `E` | ✅ |
| **Q3** | VUNESP / CM São José dos Campos 2021 | Negação do OU exclusivo (`⊻`) com termo já negado | `C` | `D` | ❌ |
| **Q4** | VUNESP / TJ-SP 2021 | Conjunção de condicionais — antecedente comum (`(p→q)∧(p→~r)`) | `E` | `C` | ❌ |
| **Q5** | VUNESP / RioPretoPrev 2026 (TI) | Contrapositiva com conjunção no antecedente | `E` | `E` | ✅ |
| **Q6** | VUNESP / RioPretoPrev 2026 (TI) | De Morgan em cascata (3 termos) | `B` | `B` | ✅ |

### 📌 Pontos de Revisão Sugeridos
1. **Ordem na tradução de `p → q` e *"somente se"* (Q1):** mantenha sempre a ordem `antecedente → consequente` antes de trocar por letras e lembre que *"`A` somente se `B`"* significa `A → B`. Use a **Técnica da Única Linha Falsa** para bater o martelo.
2. **Negação de `⊻` quando já existe `~` (Q3):** negar os **dois** lados (`p ⊻ ~q` → `~p ⊻ q`) gera uma **equivalência** (`(!p != q) == (p != !q)`). Para negar `⊻`, inverta **exatamente um** lado (`~p ⊻ ~q` ou `p ⊻ q`).
3. **Fatoração booleana em `(p→q) ∧ (p→~r)` (Q4):** abra para `(~p ∨ q) ∧ (~p ∨ ~r)`, coloque `~p ∨` em evidência para obter `~p ∨ (q ∧ ~r)` e volte para `p → (q ∧ ~r)` (atenção para não inverter `∨` de fora com `∧` de dentro).
4. **Pré-requisito no cronograma:** você sentiu falta da **Aula 02 (Estruturas Lógicas II — Tabela-Verdade e Negações)** antes da Aula 03 (Equivalências). O cronograma será reorganizado para respeitar a ordem natural das matérias com pré-requisitos!
