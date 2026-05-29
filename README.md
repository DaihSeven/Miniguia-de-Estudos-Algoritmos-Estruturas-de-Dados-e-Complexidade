
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
---

## 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Durante a interação com o NotebookLM, foram testadas diferentes abordagens para extrair o máximo das fontes:

### Teste 1: Prompt Direto (Baixa Eficácia)
*   **Pergunta:** "O que é Big O?"
*   **Resposta da IA:** Uma definição técnica padrão.
*   **Cicatriz:** A resposta foi genérica. Para melhorar, precisei pedir exemplos baseados especificamente nas fontes fornecidas.

### Teste 2: Prompt de Contexto Fechado (Alta Eficácia)
*   **Pergunta:** "Com base no artigo da IBM e do DataCamp, crie uma tabela comparativa entre Array e Linked List, destacando a complexidade de inserção e busca para cada uma."
*   **Resposta da IA:** Gerou uma tabela precisa citando as fontes 1 e 3.
*   **Raciocínio:** O uso de delimitadores de fonte ajudou a IA a não "alucinar" conhecimentos externos.

### Teste 3: Prompt de Analogia (Aprendizagem Ativa)
*   **Pergunta:** "Explique a diferença entre O(n) e O(log n) usando uma analogia de procurar um nome em uma lista telefônica."
*   **Referência:** Fonte 4.
*   **Dificuldade:** Inicialmente a IA confundiu O(log n) com O(1). Tive que refinar o prompt pedindo para ela focar na técnica de "dividir para conquistar" mencionada nos textos.

---

## 4. Miniguia de Estudo (Entrega Final)

### Resumo Estruturado
1.  **Estruturas de Dados:** São métodos de organizar e armazenar dados para que possam ser acessados e modificados de forma eficiente. Exemplos incluem Arrays (acesso rápido por índice) e Tabelas Hash (busca quase instantânea).
2.  **Complexidade de Algoritmos:** Mede quanto tempo ou espaço um algoritmo consome à medida que o volume de dados (n) cresce.
3.  **Notação Big O:** A linguagem usada para descrever essa complexidade. O objetivo de um bom desenvolvedor é evitar algoritmos O(n²) em grandes bases de dados, preferindo O(n) ou O(log n).

### Glossário de Conceitos
*   **Big O:** Notação que descreve o limite superior da complexidade de um algoritmo.
*   **Time Complexity:** Tempo de execução em função do tamanho da entrada.
*   **Space Complexity:** Memória utilizada pelo algoritmo.
*   **Binary Search:** Exemplo clássico de O(log n), onde o espaço de busca é dividido pela metade a cada passo.

### Prompts Reutilizáveis para Revisão
*   *"Resuma os 3 principais benefícios de usar a estrutura de dados correta mencionados na fonte da UDS."*
*   *"Crie um quiz de 5 perguntas de múltipla escolha sobre complexidade de tempo baseando-se no tutorial do DataCamp."*
*   *"Explique para uma criança de 10 anos o conceito de O(n²) usando a fonte do Medium como base."*

---
**Autor:** Daiane das Graças Barbosa Koslowski
**Bootcamp:** Afya - Automação de Dados com IA
**Plataforma:** [DIO](https://www.dio.me)
