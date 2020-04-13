# analiseVinhos
Esse repositório trata-se de uma análise e construção de um modelo de predição sobre qualidade de vinhos

A. Como foi a definição da sua estratégia de modelagem?
R: Em um primeiro momento selecionare ordenar as features mais relevantes (selectKBest) e depois testar modelos de classificação diferente que observando aquele que apresenta-se um resultado mais adequado.

B. Como foi definida a função de custo utilizada?
R: Para cada modelo testado, optou-se por utilizar a função de custo padrão da implementada pela ferramenta (scikitlearn) para o modelo

C. Qual foi o critério utilizado na seleção do modelo final?
R: O modelo RandomForest teve o melhor resultado seguido pelo DecisionTreeClassifier. Entretanto o tempo de execução do entre o RandomForest (~ 1.16 min) e DecisionTreeClassifier (~ 0.03 min) é bastante significativo. Considerando o Tempo de treinamento do modelo e valor obtido como fator determinante o modelo escolhido para a tarefa deverá ser o DecisionTreeClassifier.

D. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
R: Para validaço do Modelo optou-se por utilizar o Recall como score. Isso se deve ao fato de que o Recall pode ser utilzado em um situação em que os Falso Negativos são considerados mais prejudiciais que os falsos positivos. O objetivo é encontrar todos os vinhos que possam sinalizar ter uma qualidade ruim, mesmo que no meio do processo alguns vinhos de boa qualidade tenham sido classificados como ruins. O objetivo é priorizar pela qualidade do produto prevendo os que teriam uma qualidade aquem do aceitável.

E. Quais evidências você possui de que seu modelo é suficientemente bom?
R: Mesmo tendo feito um trabalho inicial de pré-processamento dos dados e utilzado uma abordagem que utiliza de vários algortmos de classificação e selecionando o melhor entre eles, os resultados estão longe de um valor ideal. É necessário alguns outras abordagens para melhorar o DataSet (remoção de todos so outliers) e também testar alguns outras abordagens para previsão dos dados (talvés algum rede neural).
