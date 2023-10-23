# # Entendendo a análise química para fazer o agrupamento dos vinhos

## Visão Geral

Neste projeto, vamos analisar os dados disponíveis, no conjunto de dados de análise química de vinhos cultivados na mesma região da Itália, mas derivados de três cultivares diferentes.

Você pode conferir o dataset e o projeto na íntegra clicando abaixo:

Link dataset: https://www.kaggle.com/datasets/harrywang/wine-dataset-for-clustering

Link do código do projeto: https://github.com/gustavoptavares/Vinho/blob/main/Vinho_Clusteriza%C3%A7%C3%A3o.ipynb

## Problema e Solução

Vamos analisar os dados o conjunto de dados de análise química de vinhos. Com a análise determinou as quantidades de 13 constituintes encontrados em cada um dos três tipos de vinhos, vamos entender, no detalhe, aspectos relacionados a custos, como:

• Enteder o conjunto de dados com os dados relacionadas a análise dos vinhos.

• Fazer o agrupamento dos vinhos com base em suas características físico-químicas. 

## O Processo

O primeiro passo do projeto foi adquirir os dados. Utilizamos os dados do portal Kaagle, carregando-o no Google Colab, para a exploração e análise dos dados utilizando a linguagem de programação Python e suas bibliotecas, como Pandas, Matplotlib e Scikit-Learn. Foi feita análise exploratória, visualização dos dados, e foi aplicado o modelo de machine learning de clusterização, utilizando o algoritmo de kmeans para fazer agrupamento dos vinhos.

## Resultados

Podemos fazer as seguintes observações:

Cluster 0: Este cluster tem vinhos com níveis relativamente altos de "Malic_Acid" e "Color_Intensity", mas níveis mais baixos de "Flavanoids", "Hue", "OD280" e "Proline".

Cluster 1: Os vinhos deste cluster têm níveis mais altos de "Alcohol", "Total_Phenols", "Flavanoids", "Proanthocyanins", "Hue", "OD280" e "Proline".

Cluster 2: Este cluster parece representar vinhos com características intermediárias, mas com níveis mais baixos de "Alcohol", "Color_Intensity" e "Proline".

Resultados das Métricas para o modelo com 3 clusters:

Silhouette Score: Aproximadamente 0.285. Este valor indica uma estrutura de cluster razoável. Um valor mais próximo de 1 teria sido ideal, mas 0.285 ainda é aceitável, indicando que os clusters não estão muito sobrepostos.

WCSS: Aproximadamente 1277.93. Lembre-se de que queremos minimizar este valor. No contexto do método do cotovelo, observamos que aumentar o número de clusters além de 3 não resultava em uma grande diminuição do WCSS, então 3 foi uma boa escolha.

## Conclusões

Os vinhos foram agrupados em três clusters distintos com base em suas características físico-químicas.

O Cluster 0 parece conter vinhos com níveis mais altos de "Malic_Acid" e "Color_Intensity", mas níveis mais baixos de características como "Flavanoids", "Hue", "OD280" e "Proline".

O Cluster 1 representa vinhos com características premium, com níveis mais altos de "Alcohol", "Total_Phenols", "Flavanoids", "Proanthocyanins", "Hue", "OD280" e "Proline".

O Cluster 2 tem vinhos com características intermediárias, mas com níveis mais baixos de "Alcohol", "Color_Intensity" e "Proline".

O PCA foi útil para visualizar os clusters em um espaço bidimensional, e os clusters estavam bem separados no espaço reduzido, indicando uma boa agrupação. Para um aprofundamento maior, seria interessante também analisar outras técnicas de clusterização e comparar os resultados, bem como considerar outras técnicas de redução de dimensionalidade para visualização e análise.
