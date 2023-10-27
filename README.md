## Classificação de Fraude com TensorFlow

<img src="https://www.modalmais.com.br/wp-content/uploads/2020/02/fraude_cartoes.jpg"/>

Este repositório contém um exemplo de um modelo de classificação binária para detectar fraudes em transações de cartão de crédito usando TensorFlow e Keras.

## Pré-requisitos

Antes de executar o código, certifique-se de ter instalado as seguintes bibliotecas:

- TensorFlow
- pandas
- matplotlib
- numpy
- scikit-learn

Você pode instalá-las usando o `pip`:

```bash
pip install tensorflow pandas matplotlib numpy scikit-learn
```

## Visão Geral
O código realiza o seguinte:

- Carrega os dados de transações de cartão de crédito do arquivo "creditcard.csv" e realiza limpeza dos dados, removendo valores ausentes.

<img src="creditcard table.png"/>

- Divide os dados em recursos (X) e rótulos (Y), onde X contém as informações da transação e Y contém a classe (fraude ou não fraude).

- Divide os dados em conjuntos de treinamento e teste usando train_test_split.

- Aplica a padronização aos dados usando StandardScaler.

- Define um modelo de rede neural sequencial com camadas densas e função de ativação "relu" para as camadas ocultas e "sigmoid" para a camada de saída.

- Compila o modelo com otimizador "Adam" e função de perda "mae" (Mean Absolute Error) para fins de demonstração, embora "binary_crossentropy" seja mais comum para problemas de classificação binária.

- Treina o modelo usando os dados de treinamento com um número especificado de épocas.

<img src="creditcard model.png"/>

- Avalia o modelo nos conjuntos de treinamento e teste para medir o desempenho.

- Plota a curva de perda e a curva de acurácia durante o treinamento.

<img src="creditcard metrics.png"/>

- Realiza previsões no conjunto de teste e compara os rótulos reais com as previsões, plotando um gráfico de dispersão para visualização.

<img src="creditcard preds.png"/>

- Usa um limite (threshold) para transformar as probabilidades em rótulos.

## Melhorias Potenciais
Para melhorar o desempenho do modelo, você pode considerar as seguintes melhorias:

- Ajustar hiperparâmetros, como o número de camadas, unidades ocultas e taxa de aprendizado.
- Experimentar diferentes funções de perda, como "binary_crossentropy".
- Balancear classes se houver desequilíbrio entre fraudes e transações normais.
- Realizar engenharia de recursos para criar novas features relevantes.


## Executando o Código
Você pode executar o código fornecido em um ambiente Python. Certifique-se de que os dados de transações de cartão de crédito estejam no arquivo "creditcard.csv" e siga as etapas no código para treinar e avaliar o modelo.

```python
python Credit_Card_Fraud.py
```
## Resultados
Os resultados do modelo, incluindo métricas de desempenho e visualizações, podem ser encontrados no arquivo do Jupyter Notebook (ou script) associado.
