Decision Trees

Uma arvore de decisao eh construida dividindo (split) todos os conjuntos de dados a partir de um root node em sub conjuntos de dados em children nodes. Para dividir eh necessario entender quais as features que fornecem a melhor divisao do conjunto. Este processo eh repetido de forma recursiva (recursive partitioning). A recursao chega ao fim, quando o conjunto no node em questao tem os mesmos labels ou quando nao eh adicionado mais nada apos a divisao. O node que possui dados unmixed eh chamado de leaf node. 

Decision Tree types:
* Classification Tree
* Regression Tree

Decision tree algorithms:
* ID3 (Iterative Dichotomiser 3)
* C4.5 (successor of ID3)
* CART (Classification And Regression Tree)
* Chi-square automatic interaction detection (CHAID). Performs multi-level splits when computing classification trees.
* MARS: extends decision trees to handle numerical data better.
* Conditional Inference Trees. Statistics-based approach that uses non-parametric tests as splitting criteria, corrected for multiple testing to avoid overfitting. This approach results in unbiased predictor selection and does not require pruning.

* Which features best splits the set of data.
* What coditions for splitting
* When to stop
* Pruning

Gini impurity - Qual a probabilidade de um elemento do meu conjunto de dados ser classificado incorretamente, dado que ele foi classificado aleatoriamente de acordo com a distribuicao de labels usada no meu subconjunto.

To compute the gini impurity we sum, over all classes, the probability p_i of an item being chosen times the incorrect probability of that item.

<img src="https://render.githubusercontent.com/render/math?math=I_G = 1 - \limits _{i=1} ^{J} p_i ^ 2">
$I_G = 1 - \limits _{i=1} ^{J} p_i ^ 2$