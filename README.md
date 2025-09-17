Análise de Desempenho de um Modelo de Classificação com Matriz de Confusão e Relatório de Classificação

Este projeto demonstra a implementação de um modelo simples de classificação utilizando o dataset MNIST e a análise do seu desempenho através da matriz de confusão e do relatório de classificação.

Dataset
O dataset utilizado é o MNIST, um conjunto de dados de dígitos escritos à mão amplamente utilizado para treinamento de modelos de classificação de imagens.

Modelo de Classificação
O modelo de classificação é uma Rede Neural Convolucional (CNN) simples construída com TensorFlow/Keras. A arquitetura inclui:

Camada Convolucional 2D (Conv2D) com 32 filtros, kernel de tamanho (3, 3) e função de ativação ReLU.
Camada de Pooling Máximo 2D (MaxPooling2D) com tamanho (2, 2).
Camada de Achatamento (Flatten) para converter a saída da camada convolucional em um vetor.
Camada Densa (Dense) com 128 neurônios e função de ativação ReLU.
Camada de Saída Densa (Dense) com 10 neurônios (para as 10 classes de dígitos) e função de ativação Softmax para obter probabilidades.
O modelo é compilado com o otimizador Adam, função de perda categorical_crossentropy e métrica de avaliação accuracy.

Treinamento
O modelo é treinado no conjunto de treinamento do MNIST por 3 épocas, com um tamanho de batch de 32 e validação em 20% dos dados de treinamento.

Análise de Desempenho
Após o treinamento, o modelo é avaliado no conjunto de teste utilizando as seguintes métricas:

Matriz de Confusão: Uma tabela que resume o desempenho do modelo em um problema de classificação, mostrando o número de verdadeiros positivos, verdadeiros negativos, falsos positivos e falsos negativos para cada classe.
Relatório de Classificação: Fornece métricas como Precisão, Recall (Sensibilidade), F1-Score e Suporte para cada classe, além de métricas médias (accuracy, macro avg, weighted avg).
Resultados
A matriz de confusão e o relatório de classificação são impressos na saída para análise. A matriz de confusão visualizada também é exibida graficamente.

Bibliotecas Utilizadas
tensorflow: Para a construção e treinamento do modelo de Deep Learning.
sklearn.metrics: Para gerar a matriz de confusão e o relatório de classificação.
numpy: Para operações numéricas.
matplotlib.pyplot: Para visualizar a matriz de confusão.
