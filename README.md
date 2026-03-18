# Diagnóstico de Câncer de Mama com Machine Learning

Este repositório apresenta um projeto de Ciência de Dados focado na classificação de tumores de mama em **Malignos** ou **Benignos**. O objetivo é aplicar o processo de Machine Learning, desde a análise exploratória até a validação de modelos preditivos, utilizando o ecossistema Scikit-Learn.

## 📊 Sobre o Dataset

O projeto utiliza o **Breast Cancer Wisconsin (Diagnostic) Dataset**, disponível no [Kaggle](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset).
* **Instâncias:** 569 amostras.
* **Atributos:** 30 variáveis preditoras numéricas que descrevem características morfológicas das células (raio, textura, perímetro, área, etc.).
* **Target:** Diagnóstico (M = Maligno, B = Benigno).

## 📂 Estrutura do Projeto

O desenvolvimento está dividido em notebooks que seguem o fluxo de trabalho de um projeto de ML:

1.  **`01-gd-eda.ipynb` (Análise Exploratória):** Estudo das distribuições, correlações e identificação de atributos chave.
2.  **`02-gd-metricas.ipynb` e `02-gd-metricas_parte_02.ipynb` (Avaliação de Métricas):** Estudo aprofundado sobre Acurácia, Precisão, Recall, F1-Score e Curva ROC. O foco aqui foi entender o impacto de falsos negativos em um contexto médico, priorizando o **Recall**.
3.  **`03-gd-modelos.ipynb` (Desenvolvimento de Modelos):** Implementação de pipelines com `PowerTransformer` para normalização e comparação entre algoritmos como `LogisticRegression`, `Perceptron` e `SGDClassifier` utilizando `StratifiedKFold`.
4.  **`03-gd-modelos_parte_02.ipynb` (Seleção de Atributos):** Utilização de `SelectKBest` com métodos estatísticos (Chi-Quadrado, ANOVA e Informação Mútua) para otimizar a performance e reduzir a dimensionalidade.

## ⚙️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Modelos, Pipelines, Preprocessing e Metrics)

## 🏆 Resultados

Os modelos de **Regressão Logística** e **Perceptron** apresentaram resultados sólidos, alcançando um **Recall superior a 95%** na validação cruzada. Em diagnósticos médicos, garantir que a maioria dos casos malignos seja detectada (alto Recall) é fundamental para a segurança do paciente.


## Organização do projeto

```
├── .gitignore         <- Arquivos e diretórios a serem ignorados pelo Git
├── breast_cancer.yml       <- O arquivo de requisitos para reproduzir o ambiente de análise
├── LICENSE            <- Licença de código aberto se uma for escolhida
├── README.md          <- README principal para desenvolvedores que usam este projeto.
|
├── dados              <- Arquivos de dados para o projeto.
|
├── modelos            <- Modelos treinados e serializados, previsões de modelos ou resumos de modelos
|
├── notebooks          <- Cadernos Jupyter. A convenção de nomenclatura é um número (para ordenação),
│                         as iniciais do criador e uma descrição curta separada por `-`, por exemplo
│                         `01-fb-exploracao-inicial-de-dados`.
│
|   └──src             <- Código-fonte para uso neste projeto.
|      │
|      ├── __init__.py  <- Torna um módulo Python
|      ├── config.py    <- Configurações básicas do projeto
|      ├── graficos.py  <- Scripts para criar visualizações exploratórias e orientadas a resultados
|      └── models.py    <- Scripts para criar modelos e treinar modelos
|
├── referencias        <- Dicionários de dados, manuais e todos os outros materiais explicativos.
|
├── relatorios         <- Análises geradas em HTML, PDF, LaTeX, etc.
│   └── imagens        <- Gráficos e figuras gerados para serem usados em relatórios
```
