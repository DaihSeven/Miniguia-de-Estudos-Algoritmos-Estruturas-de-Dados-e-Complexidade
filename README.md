
# Miniguia de Estudos: Algoritmos, Estruturas de Dados e Complexidade

Este repositório contém o resultado do desafio de projeto "Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM" da DIO. O objetivo foi utilizar o NotebookLM para criar um ambiente de aprendizagem ativa focado nos pilares da ciência da computação.

---

## 1. Contexto e Objetivos

**Assunto Escolhido:** Fundamentos de Algoritmos, Estruturas de Dados e Notação Big O.

**Objetivos de Estudo:**
*   Compreender como a escolha da estrutura de dados impacta a performance de um sistema.
*   Dominar os conceitos de complexidade de tempo e espaço (Notação Big O).
*   Identificar padrões de algoritmos comuns (O(n), O(n²), O(log n)) e suas aplicações práticas.

---

## 2. Curadoria de Fontes

Para alimentar o NotebookLM, foram selecionadas as seguintes fontes de alta autoridade:

1.  **IBM:** [O que são estruturas de dados?](https://www.ibm.com/br-pt/think/topics/data-structure) - Visão geral técnica e tipos comuns.
2.  **UDS Blog:** [Estrutura de dados: benefícios para seu sistema](https://uds.com.br/blog/estrutura-de-dados-beneficios-para-seu-sistema/) - Foco em arquitetura e escalabilidade.
3.  **DataCamp:** [Big O Notation & Time Complexity](https://www.datacamp.com/pt/tutorial/big-o-notation-time-complexity) - Guia prático sobre análise de algoritmos.
4.  **Medium (Cezar Antonio):** [Complexidade de Algoritmos: Abordagens O(n²), O(n) e O(n log n)](https://cezarantoniodesouza.medium.com/complexidade-de-algoritmos-abordagens-o-n%C2%B2-o-n-e-o-n-log-n-para-o-mesmo-problema-4b7dc20a9869) - Estudo de caso comparativo.
5.  **Computação UAB/UECE (Mariela Inés Cortés):** [Estrutura de Dados](https://www.uece.br/cct/wp-content/uploads/sites/28/2021/07/Estrutura-de-Dados-2014.pdf)
6.  **Algoritmos e estruturas de dados 1 UFPR**: [Algoritmos e estruturas de dados 1](http://inf.ufpr.br/marcos/livro_alg1/livro_alg1.pdf)
7.  **Fabio Akita:**[Árvores: O Começo de TUDO | Estruturas de Dados e Algoritmos](https://youtu.be/9GdesxWtOgs?si=WytRQiwttc84vUhQ)
8.  **Algoritmos (Prof. Dr. Osvaldo Luiz de Oliveira):**[Análise de Algoritmos e Complexidade da Computação ](https://cc.faccamp.br/docentes/osvaldo/EstruturasDados.pdf)
## 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Abaixo estão registrados os testes realizados no NotebookLM, as respostas obtidas e o raciocínio por trás de cada interação.

---

### Teste 1: Prompt Direto (Definições Fundamentais)

### Pergunta

> **O que é Big O?**

#### Resposta da IA

A notação **Big O** é uma métrica matemática utilizada para descrever a complexidade de um algoritmo, medindo como o tempo de execução (complexidade temporal) ou o uso de memória (complexidade espacial) escalam à medida que o tamanho da entrada (**n**) aumenta.

##### Conceitos Fundamentais

* **Limite Superior:** fornece uma estimativa máxima de crescimento do custo computacional.
* **Pior Cenário:** normalmente analisa o cenário mais pessimista para prever o consumo máximo de recursos.
* **Simplificação Matemática:** constantes e termos menos significativos são ignorados.

  * Exemplo: `4n² + 2n + 7` → **O(n²)**
* **Independência de Hardware:** permite comparar algoritmos independentemente da linguagem, sistema operacional ou máquina utilizada.

##### Principais Categorias de Complexidade

| Complexidade  | Descrição                     |
| ------------- | ----------------------------- |
| O(1)          | Tempo constante               |
| O(log n)      | Tempo logarítmico             |
| O(n)          | Tempo linear                  |
| O(n log n)    | Tempo log-linear              |
| O(n²)         | Tempo quadrático              |
| O(2ⁿ) / O(n!) | Tempo exponencial ou fatorial |

#### Cicatriz

A resposta inicial foi correta, porém excessivamente teórica. Para entender melhor o ponto de partida da IA, solicitei uma explicação sobre as estruturas básicas de programação.

---

### Pergunta

> **Quais são as estruturas básicas de controle como repetição e desvio condicional?**

#### Resposta da IA

As estruturas básicas de controle em algoritmos são:

##### 1. Sequência

Execução de instruções uma após a outra, seguindo a ordem lógica do programa.

##### 2. Seleção (Desvio Condicional)

Permite alterar o fluxo de execução com base em condições lógicas.

Exemplos:

* `if / then`
* `if / then / else`
* `case`

##### 3. Repetição (Iteração)

Permite executar um bloco de código múltiplas vezes.

Exemplos:

* `while`
* `for`
* `repeat / until`

Qualquer algoritmo pode ser construído combinando essas três estruturas fundamentais.

#### Cicatriz

A resposta também foi correta, mas ainda muito conceitual. Percebi que, para compreender a aplicação prática, eu precisava direcionar a IA para comparações específicas presentes nas fontes consultadas.

---

### Teste 2: Prompt de Contexto Fechado (Análise Comparativa)

### Pergunta

> **Com base no artigo da IBM e do DataCamp, crie uma tabela comparativa entre Array e Linked List, destacando a complexidade de inserção e busca para cada uma.**

#### Resposta da IA

##### Tabela Comparativa: Array vs Linked List

| Operação              | Array (Vetor)     | Linked List (Lista Ligada) |
| --------------------- | ----------------- | -------------------------- |
| Busca (Acesso Direto) | O(1)              | O(n)                       |
| Busca por Valor       | O(n)              | O(n)                       |
| Inserção no Início    | O(n)              | O(1)                       |
| Inserção no Final     | O(1)*             | O(n)                       |
| Uso de Memória        | Estático/Contíguo | Dinâmico/Encadeado         |

> * Considerando que exista espaço disponível no array.

#### Análise da IA

##### Arrays

**Vantagens**

* Acesso direto extremamente rápido (`O(1)`).
* Estrutura simples e eficiente para leitura frequente.

**Desvantagens**

* Inserções e remoções podem exigir deslocamento de elementos (`O(n)`).

##### Linked Lists

**Vantagens**

* Inserções e remoções eficientes.
* Crescimento dinâmico.

**Desvantagens**

* Não possuem acesso direto por índice.
* Necessitam percorrer a estrutura para localizar elementos.

#### Implicações Práticas

| Cenário                     | Estrutura Recomendada |
| --------------------------- | --------------------- |
| Leitura frequente de dados  | Array                 |
| Muitas inserções e remoções | Linked List           |
| Tamanho previsível          | Array                 |
| Crescimento dinâmico        | Linked List           |

#### Raciocínio

Este foi o prompt mais eficaz do experimento, pois obrigou a IA a extrair informações técnicas específicas e organizá-las em formato tabular, reduzindo ambiguidades e respostas genéricas.

---

### Teste 3: Prompt de Analogia (Refinamento de Lógica)

### Pergunta

> **Explique a diferença entre O(n) e O(log n) usando uma analogia de procurar um nome em uma lista telefônica.**

#### Resposta da IA

##### O(n) — Busca Linear

Imagine procurar uma pessoa em uma lista telefônica lendo nome por nome desde a primeira página.

* No pior caso, será necessário verificar todos os nomes.
* Se a lista dobrar de tamanho, o trabalho também dobra.

**Exemplo:**

* 1.000 nomes → até 1.000 verificações.
* 1.000.000 de nomes → até 1.000.000 de verificações.

---

##### O(log n) — Busca Binária

Agora imagine abrir a lista exatamente no meio.

* Se o nome procurado estiver antes, você descarta metade da lista.
* Se estiver depois, descarta a outra metade.
* Repete o processo sucessivamente.

A cada etapa, metade dos dados é eliminada.

**Exemplo:**

| Quantidade de Nomes | O(n)                 | O(log n)   |
| ------------------- | -------------------- | ---------- |
| 1.000               | 1.000 passos         | ~10 passos |
| 1.000.000           | 1.000.000 passos     | ~20 passos |
| 1.000.000.000       | 1.000.000.000 passos | ~30 passos |

#### Raciocínio

Este prompt demonstrou como analogias ajudam a transformar conceitos abstratos em exemplos intuitivos. A explicação ficou significativamente mais acessível para quem está iniciando o estudo de análise de algoritmos, permitindo visualizar o impacto do crescimento das complexidades na prática.

---

### Conclusão

Os testes mostraram que a qualidade da resposta está diretamente relacionada ao nível de contexto fornecido ao modelo.

#### Aprendizados

* **Prompts diretos** produzem definições corretas, porém mais genéricas.
* **Prompts de contexto fechado** geram respostas mais precisas e alinhadas às fontes.
* **Prompts com analogias** facilitam o entendimento de conceitos abstratos.
* **Solicitações de tabelas e comparações** tendem a produzir respostas mais organizadas e úteis para estudo.

A principal lição foi que o refinamento do prompt tem impacto direto na profundidade, clareza e aplicabilidade das respostas geradas pela IA.


## 4. Miniguia de Estudo 

### Resumo Estruturado

#### 1. Algoritmos e Estruturas de Dados

Um **algoritmo** é um conjunto de regras não ambíguas que define uma sequência finita de operações capazes de gerar uma saída a partir de uma entrada.

Uma **estrutura de dados** é a forma de organizar e armazenar informações para que possam ser acessadas e manipuladas de maneira eficiente.

Esses conceitos são complementares:

* O algoritmo define **o que fazer**.
* A estrutura de dados define **como armazenar os dados**.
* Uma estrutura adequada potencializa a eficiência e a escalabilidade da solução.

##### Classificação das Estruturas de Dados

###### Estruturas Lineares

Os elementos seguem uma única sequência lógica.

Exemplos:

* Arrays (Vetores)
* Listas Ligadas
* Pilhas (Stacks)
* Filas (Queues)

###### Estruturas Não-Lineares

Os dados são organizados hierarquicamente ou em rede.

Exemplos:

* Árvores (Trees)
* Grafos (Graphs)

---

#### 2. Principais Estruturas de Dados

##### Arrays (Vetores)

Armazenam elementos do mesmo tipo em posições contíguas de memória.

**Características:**

* Acesso direto: `O(1)`
* Tamanho fixo
* Excelente desempenho para leitura

##### Listas Ligadas (Linked Lists)

Estruturas dinâmicas compostas por nós conectados por ponteiros.

**Características:**

* Inserções eficientes
* Crescimento dinâmico
* Busca sequencial: `O(n)`

##### Pilhas (Stacks)

Seguem o princípio **LIFO (Last In, First Out)**.

> O último elemento inserido é o primeiro a ser removido.

##### Filas (Queues)

Seguem o princípio **FIFO (First In, First Out)**.

> O primeiro elemento inserido é o primeiro a ser removido.

##### Árvores (Trees)

Representam relações hierárquicas entre elementos.

###### Árvores Binárias de Busca (BST)

Permitem operações eficientes de busca, inserção e remoção.

| Operação | Complexidade |
| -------- | ------------ |
| Busca    | O(log n)     |
| Inserção | O(log n)     |
| Remoção  | O(log n)     |

---

#### 3. Análise de Complexidade e Notação Big O

A análise de complexidade mede como o consumo de recursos cresce conforme o tamanho da entrada (`n`) aumenta.

##### Tipos de Complexidade

###### Complexidade Temporal

Mede o tempo de execução do algoritmo.

###### Complexidade Espacial

Mede o consumo de memória.

##### Notação Big O

A Notação Big O fornece um limite superior para o crescimento do custo computacional no pior cenário.

##### Principais Classes de Complexidade

| Complexidade | Descrição   | Exemplo                  |
| ------------ | ----------- | ------------------------ |
| O(1)         | Constante   | Acesso a índice de vetor |
| O(log n)     | Logarítmica | Busca Binária            |
| O(n)         | Linear      | Busca Sequencial         |
| O(n log n)   | Log-Linear  | Merge Sort, QuickSort    |
| O(n²)        | Quadrática  | Selection Sort           |
| O(2ⁿ)        | Exponencial | Força Bruta              |
| O(n!)        | Fatorial    | Permutações              |

---

#### 4. Importância Prática

Dominar algoritmos e estruturas de dados permite:

* Construir aplicações mais rápidas
* Reduzir consumo de memória
* Melhorar escalabilidade
* Resolver problemas de forma eficiente

##### Exemplo Prático

Uma escolha inadequada de algoritmo pode fazer com que milhões de registros sejam processados em horas ou dias, enquanto uma solução otimizada executaria a mesma tarefa em segundos ou milissegundos.

---

### Glossário de Conceitos

#### Conceitos Fundamentais

| Conceito                         | Definição                                                                                        |
| -------------------------------- | ------------------------------------------------------------------------------------------------ |
| **Algoritmo**                    | Sequência finita e precisa de instruções utilizada para transformar entradas em saídas.          |
| **Estrutura de Dados**           | Forma de organizar e armazenar informações para permitir acesso e manipulação eficientes.        |
| **Tipo Abstrato de Dados (TAD)** | Modelo conceitual que define os dados e as operações possíveis, sem especificar a implementação. |
| **Variável**                     | Abstração de um endereço de memória identificada por um nome.                                    |
| **Ponteiro (Apontador)**         | Tipo de dado que armazena o endereço de memória de outro dado.                                   |
| **Recursividade**                | Técnica em que uma função chama a si mesma para resolver um problema.                            |

---

#### Análise de Complexidade

| Conceito                      | Definição                                                                                               |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Notação Big O**             | Representação matemática utilizada para descrever o crescimento do custo computacional de um algoritmo. |
| **Complexidade Temporal**     | Quantidade de operações executadas em função do tamanho da entrada.                                     |
| **Complexidade Espacial**     | Quantidade de memória utilizada durante a execução.                                                     |
| **Comportamento Assintótico** | Estudo do crescimento de uma função quando a entrada tende ao infinito.                                 |

---

#### Principais Estruturas de Dados

| Estrutura                      | Descrição                                                                 | Complexidade Principal         |
| ------------------------------ | ------------------------------------------------------------------------- | ------------------------------ |
| **Array (Vetor)**              | Estrutura linear que armazena elementos em posições contíguas de memória. | Acesso: `O(1)`                 |
| **Lista Ligada (Linked List)** | Estrutura dinâmica composta por nós conectados por ponteiros.             | Busca: `O(n)`                  |
| **Pilha (Stack)**              | Estrutura baseada no princípio LIFO (*Last In, First Out*).               | Inserção/Remoção: `O(1)`       |
| **Fila (Queue)**               | Estrutura baseada no princípio FIFO (*First In, First Out*).              | Inserção/Remoção: `O(1)`       |
| **Árvore (Tree)**              | Estrutura hierárquica composta por nó raiz e nós filhos.                  | Busca média: `O(log n)`        |
| **Grafo (Graph)**              | Conjunto de vértices conectados por arestas.                              | Depende do algoritmo utilizado |
| **Tabela Hash (Hash Table)**   | Estrutura que utiliza uma função hash para mapear chaves em índices.      | Busca média: `O(1)`            |

##### Operações em Tabelas Hash

| Operação | Complexidade Média |
| -------- | ------------------ |
| Busca    | `O(1)`             |
| Inserção | `O(1)`             |
| Remoção  | `O(1)`             |

---

#### Algoritmos de Busca e Ordenação

| Algoritmo          | Descrição                                                             | Complexidade |
| ------------------ | --------------------------------------------------------------------- | ------------ |
| **Busca Linear**   | Percorre os elementos sequencialmente até encontrar o valor desejado. | `O(n)`       |
| **Busca Binária**  | Divide repetidamente um conjunto ordenado pela metade.                | `O(log n)`   |
| **Selection Sort** | Posiciona o menor elemento corretamente a cada iteração.              | `O(n²)`      |

---

#### Conceitos Relacionados

| Conceito                     | Definição                                                                         |
| ---------------------------- | --------------------------------------------------------------------------------- |
| **Colisão (Hash Collision)** | Ocorre quando duas chaves diferentes produzem o mesmo índice em uma tabela hash.  |
| **LIFO**                     | *Last In, First Out* — o último elemento inserido é o primeiro a ser removido.    |
| **FIFO**                     | *First In, First Out* — o primeiro elemento inserido é o primeiro a ser removido. |
| **Nó (Node)**                | Unidade básica de estruturas como listas ligadas, árvores e grafos.               |
| **Ponteiro**                 | Referência para o endereço de memória de outro elemento.                          |



### Prompts Reutilizáveis para Revisão
*   *"Resuma os 3 principais benefícios de usar a estrutura de dados correta mencionados na fonte da UDS."*
*   *"Crie um quiz de 5 perguntas de múltipla escolha sobre complexidade de tempo baseando-se no tutorial do DataCamp."*
*   *"Explique para uma criança de 10 anos o conceito de O(n²) usando a fonte do Medium como base."*

---
**Autora:** Daiane das Graças Barbosa Koslowski

**Bootcamp:** Afya - Automação de Dados com IA

**Plataforma:** [DIO](https://www.dio.me)
