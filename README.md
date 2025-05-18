*pt-BR*

# Árvore AVL ⤵

Este repositório contém uma implementação em C de uma **Árvore AVL (Adelson-Velsky e Landis)**. Uma Árvore AVL é uma **Árvore Binária de Busca (BST) autobalanceada**. Isso significa que, após cada operação de inserção ou remoção, a árvore ajusta sua estrutura (através de **rotações**) para garantir que a diferença de altura entre as subárvores esquerda e direita de qualquer nó (conhecida como **fator de balanceamento**) nunca seja maior que 1 (ou seja, pode ser -1, 0 ou 1).

Essa propriedade de balanceamento é o que torna as Árvores AVL tão eficientes. Em uma BST comum, se os elementos forem inseridos em uma ordem já ordenada (por exemplo, 1, 2, 3, 4, 5), a árvore pode se **degenerar** em uma estrutura semelhante a uma lista encadeada. Nesses casos, as operações de busca, inserção e remoção, que em uma BST balanceada seriam muito rápidas, acabam tendo um desempenho de tempo linear 'O(n)', o que é ineficiente para grandes conjuntos de dados.

Com o balanceamento AVL, mesmo no pior caso de inserção ou remoção, a altura da árvore permanece sempre proporcional ao logaritmo do número de nós. Isso garante que todas as operações fundamentais (busca, inserção e remoção) mantenham uma **complexidade de tempo logarítmica 'O(log n)'**. Em termos práticos, significa que o tempo necessário para realizar essas operações cresce muito lentamente à medida que a quantidade de dados na árvore aumenta, tornando-a uma excelente escolha para aplicações que exigem alto desempenho e escalabilidade.

O código `avl.c` oferece as seguintes funcionalidades principais para manipulação e visualização da Árvore AVL:

* **Inserir**: Adiciona novos elementos à árvore, acionando rotações para manter o balanceamento da Árvore AVL.
* **Percurso (Pré-order)**: Permite visualizar os elementos da árvore na ordem pré-order, útil para inspecionar a estrutura da árvore.
* **Remover**: Remove um elemento da árvore, também realizando rotações para assegurar que a propriedade AVL seja mantida.

---

### Funções Disponíveis

A tabela a seguir detalha cada função, seus parâmetros, o que ela realiza e o formato de saída esperado:

     __________________________________________________________________________________________________
    | opção |  função   |  detalhes                                                                     |
    |-------------------------------------------------------------------------------------------------- |
    |       |           |                                                                               |
    |       |           |  Recebe como parâmetros um número inteiro e um ponteiro para raiz de uma      |
    |   1   |  inserir  |  árvore AVL, retorna o ponteiro para árvore após a inclusão do valor passado  |
    |       |           |  como primeiro parâmetro.                                                     |
    |       |           |                                                                               |
    |-------------------------------------------------------------------------------------------------- |
    |       |           |                                                                               |
    |       |           |  Recebe como parâmetro o ponteiro para uma árvore AVL e imprime na tela       |
    |   2   | pré-order |  todos seus elementos, seguindo a ordem pré-order. Os valores dos elementos   |
    |       |           |  são impressos entre colchetes, sem espaço entre dois elementos.              |
    |       |           |  Acrescenta um ‘\n’ após imprimir todos os elementos. Ex: [20][10][30]        |
    |       |           |                                                                               |
    |-------------------------------------------------------------------------------------------------- |
    |       |           |                                                                               |
    |       |           |  Recebe como parâmetros um número inteiro e a ponteiro para raiz de uma       |
    |   3   |  remover  |  árvore AVL, retorna o ponteiro para árvore após a remoção do valor passado   |
    |       |           |  como primeiro parâmetro.                                                     |
    |       |           |                                                                               |
    |-------------------------------------------------------------------------------------------------- |
    |       |           |                                                                               |
    |  99   |   sair    |  Fecha o programa.                                                            |
    |       |           |                                                                               |
     ___________________________________________________________________________________________________
