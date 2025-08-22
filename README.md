# Projeto de Machine Learning: Previsão de renda com dataset Annual Adult Income

## Objetivo

Desenvolver um modelo preditivo para classificar a renda (<=50K ou >50K) utilizando técnicas de machine learning, buscando a melhor performance possível com ênfase na métrica **F1 Score**.

---

## Estrutura do Projeto

- Dados: [train.csv](https://github.com/carloscesar182/ai_advanced_course/blob/main/Notebooks/FinalProject/train.csv), [validation.csv](https://github.com/carloscesar182/ai_advanced_course/blob/main/Notebooks/FinalProject/validation.csv), [test.csv](https://github.com/carloscesar182/ai_advanced_course/blob/main/Notebooks/FinalProject/test.csv)
- Código: [script](https://github.com/carloscesar182/ai_advanced_course/blob/main/Notebooks/FinalProject/ProjetoFinal.ipynb) para pré-processamento, modelagem, avaliação e interpretação com XAI
- Resultados: métricas e gráficos de avaliação e explicabilidade

---

## Metodologia

### 1. Pré-processamento dos Dados

- Substituição de valores faltantes representados por '?' por "Not-informed".
- Análise e preservação dos outliers identificados nas variáveis numéricas.
- Codificação de variáveis categóricas com Label Encoding.
- Padronização das features numéricas usando StandardScaler.
- Preparação do target convertido para valores numéricos.

### 2. Modelagem

- Utilização do H2O AutoML para benchmark de modelos.
- Treinamento manual de Gradient Boosting, Random Forest e Naive Bayes com otimização por GridSearchCV.
- Comparação dos modelos segundo F1 Score e outras métricas.

### 3. Avaliação

- Avaliação dos modelos na base de validação.
- Avaliação final do melhor modelo (Gradient Boosting) na base de teste.
- Principais métricas obtidas na base de teste:

| Métrica       | Valor |
|---------------|-------|
| F1 Score      | 0.73  |
| Acurácia      | 0.88  |
| Recall        | 0.68  |
| Precisão      | 0.79  |

### 4. Explainable AI (XAI)

- Implementação de explicações com SHAP para interpretar o impacto das features.
- Visualização global mostra as variáveis mais importantes e seus efeitos.
- Visualização local explica decisões individuais.

---

## Como Executar

Rodar o script respeitando os blocos da ordem criada no colab:
1. Importar os arquivos
2 Atribuir as variáveis
3. Fazer o pré-processamento
4. Criar os modelos
5. Avaliar os modelos
6. Fazer o teste do modelo vencedor
7. Avaliar as métricas do modelo vencedor
8. XAI

---

## Resultados e Insights

- O modelo Gradient Boosting mostrou o melhor desempenho geral.
- Features financeiras e demográficas são os maiores influenciadores.
- XAI trouxe transparência e interpretabilidade essenciais para o projeto.

---

## Publicação

Código e documentação disponíveis neste repositório para reprodução e estudo.

---

# Módulos do Curso
## Fundamentos de Python
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/PythonFundamentals)
- Variáveis e Objetos
- Estruturas de Decisão
- Estruturadas de Repetição
- Listas
- Dicionários, Sets e Tuplas
- Numpy
- Pandas
- Módulos e Pacotes
- Funções
- Funções Padrão

## Algoritmos de machine learning
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/MLAlgorithms)
- Regressão Linear
- Regressão Linear com StatsModels
- Naive Bayes
- Árvore de Decisão
- Random Forest
- k-NN
- k-Means
- Apriori

## Tecnicas avançadas de machine learning
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/MLAdvTechniques)
- Engenharia de Atributos
- PCA
- Seleção de Atributos
- Clusters
- Escolha de melhor agrupador
- Classificação Multilabel
- Balanceamento com SMOTE
- AutoML
- AutoMLH20

## Redes Neurais, Deep Learning e Visão Computacional
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/RNA)
- MLP
- RNA com Keras
- CNN
- Pré Processamento de LSTM
- Autoencoders
- Detecção de Objetos

## Machine Learning Explicável
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/XAI)
- XAI

## Processamento de Linguagem Natural
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/NLP)
- PLN
- NLPR

## LLMs e Inteligencia Artificial Generativa
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/LLMsGenAI)
- Text Generator
- Preenchimento de Máscara
- Gerador de Resumo
- GPT da OpenAI
- GPT do Gemini
- GPT do DeepSeek
- DALL-E
- Stable Diffusion
- Whisper

## Agentes de IA
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/AIAgents)
- Agente via web
- Agente RAG Especializado

## Detecção de Anomalias
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/AnomalyDetection)
- Z-Score
- IQR Method
- LOF
- Isolation Forest
- Autoencoders
- LSTM
- Média Móvel
- Exponential Smoothing
- STD
- ARIMA

## Algoritmos Genéticos
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/GeneticalAlgorithms)
- Binário
- Fitness Function
- Fitness Function com Valor Real

## Busca e Otimização
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/SearchAndOptimization)
- Simulated Annealing com Rosenbrock's Function

## Logica Difusa
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/FuzzyLogic)
- Fuzzy

## Projeto Final
[Files Folder](https://github.com/carloscesar182/ai_advanced_course/tree/main/Notebooks/FinalProject)
- Projeto Final
