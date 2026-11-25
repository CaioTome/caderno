# 🚀 Ramp-Up & Guia de Decorebas — Dia 06 (`25/11/2026`) *(Dia 09 do Cronograma)*

> **Disciplina:** Raciocínio Lógico • **Aula 02:** Estruturas Lógicas II *(Conversão de Linguagem, Tabela-Verdade, Tautologia, Contradição e Contingência)*  
> 🎯 **Foco Estratégico:** **TIER S (Pré-requisito de RLM!)** • **PDF:** 140 páginas (`págs. 3–16` Conversão; `págs. 31–54` Tabela-Verdade; `págs. 84–113` Tautologia/Contradição/Contingência/Implicação; restante = `37` questões comentadas) • **Modo:** `⚡ Fast-Track (Lógica Booleana)`

---

## 1. ⚠️ Alerta de Engenheiro de Software × Banca de Concurso

Não há divergência normativa entre Edital e PDF, mas existe **uma diferença crítica de precedência** entre linguagens de programação e a Lógica Formal cobrada pelas bancas:

| Operação / Regra | Em Programação (C / Java / Python) | Na Lógica de Concursos (PDF págs. 3–7) |
| :--- | :--- | :--- |
| **`∧` (`AND`) vs. `∨` (`OR`)** | `&&` sempre precede `\|\|` | **Mesma precedência!** Resolvem-se na ordem em que aparecem *(esquerda → direita)* |
| **Negação (`~` / `¬`)** | Alta prioridade (`!`) | **1º na fila**, abrangendo o **menor enunciado possível** |
| **Ordem completa sem parênteses** | `!` > `&&` > `\|\|` | **`~`** ➔ **`∧` e `∨`** *(esq.→dir.)* ➔ **`⊻`** ➔ **`→`** ➔ **`↔`** |
| **Vírgula / Ponto e vírgula em frase** | — | Muda a "parentização": a vírgula agrupa o bloco anterior antes do conectivo seguinte *(pág. 6)* |

> 💡 **Decoreba de Precedência (`N - EO - X - SE - SSE`):**  
> `1º ~` (Negação) → `2º ∧ / ∨` (E / OU, quem vier primeiro) → `3º ⊻` (OU exclusivo) → `4º →` (Condicional) → `5º ↔` (Bicondicional).  
> **Atenção:** a condicional (`→`) **precede** a bicondicional (`↔`)! Ex.: `p ↔ q → r` lê-se `p ↔ (q → r)`.

---

## 2. 🔁 Bloco 1 — Conversão de Linguagem Natural para Simbólica *(págs. 3–16)*

1. **Proposição avalia significado, não apenas palavra literal:**
   - *"não é verdade que..."* e *"é falso que..."* negam **toda** a proposição composta seguinte: `~(P ... Q)`.
   - Conectivos informais de causa/consequência (*"com isso"*, *"consequentemente"*, *"portanto"*, *"logo"*) viram **condicional (`→`)** *(págs. 3–4, 31)*.
   - Imperativo com *"e"* em promessa/regra (*"Pague com PIX e ganhe desconto"*) equivale à condicional: `Se pagar com PIX → ganhará desconto`.
2. **Contagem de Proposições Simples × Conectivos:**
   - Conte apenas proposições simples **distintas** (se a mesma frase reaparecer no meio, não duplica `n`).
   - Negação (`~` / `não`) **entra na contagem de conectivos**, mas **não** aumenta o número de proposições simples distintas.

---

## 3. 📊 Bloco 2 — Construção & Contagem da Tabela-Verdade *(págs. 31–54)*

### Fórmula Mestra do Número de Linhas
$$\text{Linhas} = 2^n$$
onde **$n$ = quantidade de proposições simples distintas** *(a negação `~` não altera $n$)*.

| $n$ (proposições simples distintas) | $1$ | $2$ | $3$ | $4$ | $5$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Linhas na Tabela-Verdade ($2^n$)** | `2` | `4` | `8` | `16` | `32` |

### Resumo Express dos 5 Conectivos *(para preencher colunas sem hesitar)*
| Conectivo | Símbolo | Só dá **UM** resultado diferente quando... | Regra Rápida |
| :--- | :---: | :--- | :--- |
| **Conjunção (`E`)** | `p ∧ q` | **Tudo V** → `V` | Basta 1 `F` para dar `F` |
| **Disjunção Inclusiva (`OU`)** | `p ∨ q` | **Tudo F** → `F` | Basta 1 `V` para dar `V` |
| **Disjunção Exclusiva (`OU...OU`)** | `p ⊻ q` | **Diferentes** → `V` *(Iguais → `F`)* | XOR (`p != q`) |
| **Condicional (`SE...ENTÃO`)** | `p → q` | **`V → F`** → `F` *(Vera Fischer!)* | Demais casos → `V` |
| **Bicondicional (`SE E SOMENTE SE`)** | `p ↔ q` | **Iguais** → `V` *(Diferentes → `F`)* | XNOR (`p == q`) |

### Passos de Construção *(págs. 32, 38–54)*
1. Contar $n$ proposições simples distintas e calcular $2^n$ linhas.
2. Montar as colunas iniciais alternando metade `V` / metade `F` na 1ª coluna, `2 em 2` na penúltima, `1 em 1` na última.
3. Resolver das operações **internas** (parênteses / negações) até o **conectivo principal**.
4. **Dica Fast-Track para questões que pedem "quantas linhas são V ou F":** em vez de montar a tabela inteira, **procure apenas o caso que gera `F` (na condicional `V → F`) ou `V` (no `∧`)** e conte quantas linhas atendem!

---

## 4. ⚖️ Bloco 3 — Tautologia, Contradição, Contingência & Implicação *(págs. 84–113)*

| Classificação | Última Coluna da Tabela-Verdade | Exemplo Clássico |
| :--- | :--- | :--- |
| **Tautologia** | **100% `V`** *(sempre verdadeira)* | `p ∨ ~p` • `(p ∧ q) → p` • `[(p→q) ∧ ~q] → ~p` |
| **Contradição** | **100% `F`** *(sempre falsa)* | `p ∧ ~p` • `(p → q) ∧ (p ∧ ~q)` |
| **Contingência** | **Mista (`V` e `F`)** | `p → q` • `p ∧ q` • `p ↔ q` |

### Método da Prova por Absurdo *(Atalho de Ouro — págs. 85–86, 102–110)*
Em expressões gigantes (`3` ou `4` letras = `8` ou `16` linhas), **não monte a tabela-verdade inteira**:
1. **Quer testar se é Tautologia?** Tente forçar a proposição inteira a ser **`F`** (`V → F`, no caso de condicional principal):
   - Se conseguir achar uma combinação de `V/F` para `p, q, r` que dê `F` sem contradição → **NÃO é tautologia** (é contingência ou contradição).
   - Se forçar `F` gerar um **absurdo** (ex.: exigir `p = V` e `p = F` ao mesmo tempo) → é **impossível ser falsa ⇒ TAUTOLOGIA!**
2. **Quer testar se é Contradição?** Tente forçar a proposição inteira a ser **`V`**:
   - Se conseguir → **NÃO é contradição**.
   - Se gerar absurdo → **CONTRADIÇÃO!**

### Implicação Lógica (`⇒`) vs. Condicional (`→`) *(págs. 112–113)*
* **`p → q`** é uma **operação/conectivo** (pode ser V ou F dependendo dos valores de `p` e `q`).
* **`p ⇒ q`** (*"p implica q"*) afirma que **a condicional `p → q` é uma TAUTOLOGIA** (nunca acontece `V → F`).
* *Observação do PDF:* algumas bancas usam o símbolo `⇒` informalmente como sinônimo de `→`, mas quando a questão pergunta conceitualmente *"quando A implica B"*, a resposta literal é: **"quando o condicional `A → B`, nessa ordem, for uma tautologia"**.

---

## 5. 🎯 Raio-X FAPEC (Pegadinhas Clássicas do Tema)

1. **Contar letra repetida ou negação no $2^n$:** Em `[(p ∧ ~q) → (~p ∨ r)]`, há apenas **3** proposições distintas (`p, q, r` → $2^3 = 8$ linhas), não `4` nem `5`.
2. **Esquecer a precedência `→` antes de `↔` (ou fazer `∧` depois de `∨`):** Sem parênteses, `∧` e `∨` empatam e seguem da esquerda para a direita; já `→` resolve antes de `↔`.
3. **Confundir `Contingência` com `Contradição`:** Achou **uma única** linha `F` já descarta Tautologia, mas **ainda pode ser Contingência** — precisa checar se também existe pelo menos uma linha `V`.
4. **Ordem na Implicação (`A ⇒ B`):** A condicional que precisa ser tautologia é **`A → B` nessa ordem**, não `B → A` nem `A ↔ B`.

---

## 6. ✅ Questões-Modelo Resolvidas do PDF

### Modelo 01 — Precedência de Conectivos *(SEDUC-SP — pág. 20)*
Dada a proposição composta `p ∨ q → r ↔ s ∧ t`, sua correta interpretação com parênteses é:
- **A)** `(p ∨ q) → (r ↔ (s ∧ t))`
- **B)** `((p ∨ q) → r) ↔ (s ∧ t)`
- **C)** `((p ∨ q) → (r ↔ s)) ∧ t`
- **D)** `(p ∨ q) → ((r ↔ s) ∧ t)`
- **E)** `(p ∨ (q → r)) ↔ (s ∧ t)`

> **Gabarito: B.**  
> **Análise:** Precedência: primeiro `∨` e `∧` → `(p ∨ q)` e `(s ∧ t)`. Ficamos com `(p ∨ q) → r ↔ (s ∧ t)`. Como `→` precede `↔`, resolvemos a condicional antes da bicondicional: **`((p ∨ q) → r) ↔ (s ∧ t)`**.

### Modelo 02 — Preenchimento Parcial de Tabela-Verdade *(FAFIPA / Pref. Araucária — 2025 — Analista de Sistemas — pág. 69)*
A tabela-verdade apresenta valores lógicos ocultos `a`, `b` e `c`:

| `p` | `~p` | `q` | `~p → q` |
| :---: | :---: | :---: | :---: |
| `F` | **`a`** | `F` | **`b`** |
| `V` | `F` | `V` | **`c`** |

Os valores de `a`, `b` e `c` são, respectivamente:
- **A)** `V, F, F` • **B)** `F, F, V` • **C)** `V, F, V` • **D)** `V, V, V` • **E)** `F, V, F`

> **Gabarito: C (`V, F, V`).**  
> **Análise:** Linha 1: se `p = F`, então `~p = a = V`; logo `~p → q` vira `V → F = F`, portanto `b = F`. Linha 2: `~p = F` e `q = V`, logo `F → V = V`, portanto `c = V`.

### Modelo 03 — Classificação & Contagem de Linhas *(CPCON UEPB — 2026 — pág. 115)*
Considere `(P → Q) ∨ (R ↔ P)` e analise:
- `I.` Trata-se de uma proposição composta, formada a partir de 3 outras proposições e mediante o emprego de operadores lógicos.
- `II.` A tabela-verdade correspondente à proposição é composta por 16 linhas.
- `III.` A proposição é tautológica.
- `IV.` A proposição é contingente.

É CORRETO o que se afirma apenas em:
- **A)** `IV` • **B)** `I, II e IV` • **C)** `II e III` • **D)** `I e IV` • **E)** `I e III`

> **Gabarito: D (`I e IV`).**  
> **Análise:** Há 3 proposições distintas (`P, Q, R`), logo **I está correta** e **II está errada** ($2^3 = 8$ linhas, não `16`). Aplicando o absurdo para testar tautologia: para ser `F`, o `∨` exige ambos os lados `F`. Fazemos `(P → Q) = F` (`P = V`, `Q = F`). Para `(R ↔ P) = F` com `P = V`, basta `R = F`. Como existe a linha `(V, F, F)` que torna a fórmula `F` (e claramente `(V, V, V)` a torna `V`), ela é **contingente** (**IV correta**, **III errada**).

---

## 7. 🗺️ Roteiro Prático no PDF

- **PDF Principal:** [2 2 - Estruturas Lógicas II.pdf](file:///home/caio/Documentos/(E)%202026_2_%20P%C3%93S%20-%20UFMS%20(Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Racioc%C3%ADnio%20L%C3%B3gico%20para%20UFMS/2%202%20-%20Estruturas%20L%C3%B3gicas%20II.pdf)
- **Mapa Mental Oficial:** [2.1 Conversão de linguagem — Mapa Mental.pdf](file:///home/caio/Documentos/(E)%202026_2_%20P%C3%93S%20-%20UFMS%20(Analista%20de%20Tecnologia%20da%20Informa%C3%A7%C3%A3o-Gest%C3%A3o%20de%20Projetos%20de%20Software/materias/Racioc%C3%ADnio%20L%C3%B3gico%20para%20UFMS/2%20-%20Estruturas%20L%C3%B3gicas%20II/2.1%20Convers%C3%A3o%20de%20linguagem%20-%20Mapa%20Mental%20-%20Racioc%C3%ADnio%20L%C3%B3gico%20-%20Estrategia%20academy%20-%20Tabela-Verdade%2C%20Tautologia%2C%20Contradi%C3%A7%C3%A3o%20e%20Co....pdf)
- **O que ler / pular (`Modo ⚡ Fast-Track`):**
  - Como você já domina lógica booleana, **pule** os passos longos de construção de tabela-verdade das págs. `38–52` e `92–101`.
  - Leia apenas o método da **prova por absurdo** (`págs. 102–110`) e o bloco de **implicação (`págs. 112–113`)** se quiser revisar exemplos visuais.
  - **Prioridade 1 (Caderno FAPEC):** resolva primeiro as **10 questões `A–E`** selecionadas em [Dia-06-25.11-Estruturas-Logicas-II.md](../../questoes/raciocinio-logico/Dia-06-25.11-Estruturas-Logicas-II.md).
  - **Prioridade 2 (Reforço no PDF):** se errar alguma, ataque as baterias `2.2` (`págs. 17–30`), `2.4` (`págs. 55–83`) e `2.6` (`págs. 114–140`) nos subtópicos correspondentes.

