# 📊 Previsão de Renda com Machine Learning – Adult Income Dataset

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Status](https://img.shields.io/badge/status-completed-success.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Contributions](https://img.shields.io/badge/contributions-welcome-orange.svg)

Este projeto tem como objetivo **prever a faixa de renda de indivíduos** a partir de variáveis socioeconômicas (idade, escolaridade, ocupação, etc.) utilizando diferentes algoritmos de *Machine Learning*.  
O dataset utilizado é o **Adult Income (Census Income)**, amplamente empregado em competições e benchmarks de classificação.

## Principais pontos
- 📂 Estrutura organizada em `data/`, `notebooks/` e `outputs/`
- 🧹 Pré-processamento de dados com `pandas` e `scikit-learn`
- ⚡ Modelos treinados: *Logistic Regression, Random Forest, XGBoost e H2O AutoML*
- 📈 Métricas avaliadas: *Accuracy, Precision, Recall, F1-score, AUC*
- 🔍 Interpretação de modelos com `SHAP`

## 📂 Estrutura do Repositório
```kotlin
├── data/
│   ├── train.csv
│   ├── validation.csv
│   └── test.csv
├── notebooks/ ou scripts/
│   └── ProjetoFinal.ipynb
├── outputs/
│   ├── metrics/
│   └── figures/
├── README.md
├── requirements.txt
└── LICENSE
```

## ⚙️ Tecnologias Utilizadas
- **Python 3.10+**
- **Pandas / NumPy** – manipulação de dados
- **Matplotlib / Seaborn** – visualização
- **Scikit-learn** – pré-processamento, modelos e métricas
- **H2O AutoML 2.0** – geração automática de modelos
- **XGBoost** – modelo baseado em boosting
- **SHAP** – interpretabilidade (XAI)

## 🔎 Metodologia

### 1. Pré-processamento
- **Tratamento de valores ausentes** (`?` → `Not-informed`)
- **Análise e manutenção de outliers**
- **Codificação de variáveis categóricas** com `LabelEncoder`
- **Normalização dos dados** com `StandardScaler`

### 2. Modelagem
- **AutoML (H2O)** para ranking inicial de modelos
- **Modelos manuais testados:**
  - Gradient Boosting (Scikit-learn)
  - Random Forest
  - Naive Bayes

### 3. Avaliação
- Métricas utilizadas:
  - **F1-Score** (principal)
  - Acurácia
  - Precisão
  - Recall
- Matrizes de confusão para análise de erros

### 4. Interpretabilidade
- **SHAP** para análise global (importância das variáveis) e local (explicação de uma predição específica).

## 📊 Resultados

### Ranking final dos modelos
| Ranking | Modelo                                | F1-Score |
|---------|---------------------------------------|----------|
| 🥇 1º   | Gradient Boosting (manual)            | **0.73** |
| 2º      | XGBoost (AutoML)                      | 0.70     |
| 3º      | Extra Trees (AutoML)                  | 0.70     |
| 4º      | Random Forest                         | 0.69     |
| 5º      | Gradient Boosting Annealing (AutoML)  | 0.68     |
| 6º      | Naive Bayes                           | 0.45     |

### Métricas finais do melhor modelo (Gradient Boosting – Teste)
- **F1-Score:** 0.73  
- **Acurácia:** 0.88  
- **Precisão:** 0.79  
- **Recall:** 0.68  

O modelo alcançou **bom equilíbrio entre precisão e recall**, com destaque para evitar falsos positivos (precisão alta).

## 🧠 Interpretabilidade (XAI)

O **SHAP** foi utilizado para:
- **Análise global**: identificar quais variáveis mais influenciam a predição (ex.: horas trabalhadas, nível de educação, capital gain/loss).  
- **Análise local**: explicar as decisões do modelo para casos específicos.

Exemplo de visualizações:
- `shap.summary_plot` – importância das features  
- `shap.force_plot` – explicação de uma predição individual  

## 🚀 Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/carloscesar182/ai_advanced_course.git
   cd ai_advanced_course

2. Crie o ambiente virtual e instale as dependências:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows

   pip install -r requirements.txt

3. Execute o notebook:
   ```bash
   jupyter notebook ProjetoFinal.ipynb

## 📌 Próximos Passos

- Testar técnicas de balanceamento de classes (ex.: SMOTE)
- Explorar diferentes codificações categóricas (OneHot, Target Encoding)
- Pipeline completo com CI/CD ou Dockerização
- Comparar interpretabilidade com outras técnicas (ex.: LIME)

---

## 📜 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](https://github.com/carloscesar182/ai_advanced_course/blob/main/LICENSE) para mais detalhes.

## ✉️ Contato
Autor: Carlos Ferreira

LinkedIn: [https://www.linkedin.com/in/carloscferreira/](https://www.linkedin.com/in/carloscferreira/)

E-mail: [carloscesar182@gmail.com](mailto:carloscesar182@gmail.com)
