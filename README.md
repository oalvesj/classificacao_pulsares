# Classificação de Pulsares com Regressão Logística

Modelo de classificação para identificar estrelas de nêutrons pulsares reais a partir de medições estatísticas de sinais captados por radiotelescópios, diferenciando pulsares de ruído e outras fontes astrofísicas. Feito em Python com Pandas e scikit-learn.

## Etapas

- Análise exploratória e verificação do desbalanceamento das classes
- Preparação e divisão dos dados em treino e teste
- Padronização dos atributos (StandardScaler)
- Treinamento de uma regressão logística
- Avaliação com acurácia, AUC, sensibilidade, especificidade, matriz de confusão e classification report

## Resultados

- A base tem quase 18 mil observações e é desbalanceada: apenas cerca de 9% são pulsares reais.
- Após padronizar os atributos, a regressão logística alcançou **acurácia de cerca de 98%** e **AUC de 0,97**.
- A **especificidade (~99,5%)** é altíssima (quase não gera falsos alarmes) e a **sensibilidade (~83%)** é boa, embora o modelo ainda deixe passar cerca de 17% dos pulsares — algo esperado em uma base desbalanceada.
- A regressão logística se mostrou eficiente e confiável para o problema, pela boa separação das classes e pela simplicidade. Para aumentar a sensibilidade, seria possível ajustar o limiar de decisão ou tratar o desbalanceamento.

## Tecnologias

- Python 3
- Pandas, NumPy, Matplotlib
- scikit-learn
- Jupyter Notebook

## Como rodar

1. Instale as dependências:

```bash
pip install pandas numpy matplotlib scikit-learn notebook
```

2. Abra o notebook `classificacao_pulsares.ipynb`, selecione o kernel Python e execute todas as células.

O arquivo `pulsar.csv` precisa estar na mesma pasta do notebook.
