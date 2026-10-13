# Projetos
Espaço reservado para projetos e estudos

# Telco Customer Churn Prediction & Business Intelligence

Projeto End-to-End de Ciência de Dados voltado para a previsão de cancelamento de clientes (*Customer Churn*) utilizando o famoso dataset da Telco. O objetivo da solução é identificar clientes com alto risco de evasão e fornecer uma base enriquecida com premissas de Machine Learning para suporte à tomada de decisão via Power BI.


## Arquitetura e Pipeline da Solução

O projeto foi estruturado seguindo as melhores práticas de Engenharia e Ciência de Dados:
1. **Limpeza e Tratamento de Dados (EDA):** Conversão de tipos de dados, tratamento de valores ausentes e normalização da variável alvo (*Churn*).
2. **Modelagem Preditiva:** Treinamento de um classificador baseada em árvore de decisão (*Random Forest*) com codificação de variáveis categóricas (*One-Hot Encoding*) e validação estratificada.
3. **Persistência de Artefatos:** Salvamento do modelo treinado (`.pkl`) para reuso em produção.
4. **Business Intelligence (BI):** Enriquecimento do dataset com as probabilidades preditas de churn, gerando uma base otimizada para dashboards executivos.

---

## Stack Tecnológica

* **Linguagem:** Python 3.10+
* **Manipulação e Análise:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Persistência:** Joblib
* **BI / Visualização de Dados:** Power BI

---

## Estrutura do Repositório

```text
projeto_tian/
│
├── data/
│   ├── processed/
│   │   ├── churn_processed.csv      # Base tratada após a EDA
│   │   └── churn_para_powerbi.csv   # Base enriquecida com predições e probabilidades
│   └── Telco-Customer-Churn.csv     # Dataset bruto (Kaggle)
│
├── models/
│   └── random_forest_churn.pkl      # Modelo Random Forest treinado e serializado
│
├── notebooks/
│   ├── 01_eda_e_limpeza.ipynb       # Notebook de exploração e limpeza de dados
│   └── 02_modelagem.ipynb           # Notebook de treino, avaliação e exportação
│
└── README.md                        # Documentação do projeto