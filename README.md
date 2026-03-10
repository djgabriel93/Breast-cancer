# Modelo de Classificação em base de dados de Câncer de mama

Descrição:
O câncer de mama é o câncer mais comum entre as mulheres no mundo. Ele representa 25% de todos os casos de câncer e afetou mais de 2,1 milhões de pessoas somente em 2015. Começa quando as células da mama começam a crescer descontroladamente. Essas células geralmente formam tumores que podem ser vistos por meio de raio-X ou sentidos como nódulos na região da mama.

O principal desafio na detecção do câncer de mama é como classificar os tumores em malignos (cancerígenos) ou benignos (não cancerígenos).

Fonte: https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset


## Objetivo:
- Compreender o conjunto de dados e realizar a limpeza.
- Construa modelos de classificação para prever se o tipo de câncer é maligno ou benigno.
- Além disso, ajuste os hiperparâmetros e compare as métricas de avaliação de vários algoritmos de classificação.

## Organização do projeto

```
├── .gitignore         <- Arquivos e diretórios a serem ignorados pelo Git
├── ambiente.yml       <- O arquivo de requisitos para reproduzir o ambiente de análise
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
