# Detecção de Fraudes em Transações de Varejo

Projeto desenvolvido para a disciplina de **Aprendizado de Máquina** com o objetivo de identificar transações fraudulentas utilizando modelos de classificação supervisionada e detecção de anomalias.

---

## Objetivo

Desenvolver um pipeline completo de Machine Learning para:

- Realizar Análise Exploratória dos Dados (EDA);
- Pré-processar o dataset;
- Treinar modelos de classificação;
- Aplicar detecção de anomalias;
- Comparar os modelos por meio de métricas de desempenho.

---

## Dataset

**Retail Intelligence Fraud Detection Dataset**

- 100.000 transações
- 21 atributos
- Classificação binária

**Variável alvo**

- **0** → Transação legítima
- **1** → Transação fraudulenta

---

## Pipeline do Projeto

✔ Análise Exploratória dos Dados (EDA)

✔ Pré-processamento

✔ Divisão em treino e teste

✔ Treinamento dos modelos

✔ Detecção de anomalias

✔ Avaliação dos resultados


## Modelos Utilizados

- Logistic Regression
- Random Forest
- Gradient Boosting
- Isolation Forest

---

## Métricas de Avaliação

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de Confusão

---

**Conclusão dos resultados**

- Os modelos supervisionados apresentaram desempenho superior ao método de detecção de anomalias.
- Logistic Regression, Random Forest e Gradient Boosting obtiveram excelentes resultados.
- O Isolation Forest apresentou desempenho inferior para este conjunto de dados.

---

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

---

## Estrutura do Projeto

```text
Projeto_Deteccao_de_Fraudes/
│
├── Data/
│
├── IMAGENS/
│   ├── distribuicao_fraudes.png
│   ├── distribuicao_valores_transacoes.png
│   └── distribuicao_valores_transc.png
│
├── fraud_detection_project.ipynb
├── fraud_detection_project.py
├── requirements.txt
└── README.md
```

---

## Como Executar

```bash
git clone <URL_DO_REPOSITORIO>

pip install -r requirements.txt

jupyter notebook
```

Abra o arquivo:

```
fraud_detection_project.ipynb
```

---

## Autor

**Felipe Cardoso**
