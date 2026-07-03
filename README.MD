# Projeto Final de Aprendizado de Máquina — Detecção de Fraudes em Transações de Varejo

## Descrição do Projeto

Este projeto foi desenvolvido como trabalho final da disciplina de Aprendizado de Máquina.

O objetivo é construir um pipeline completo de Machine Learning para detectar transações fraudulentas em operações de varejo e e-commerce, utilizando técnicas de classificação supervisionada e detecção de anomalias.

O projeto contempla todas as etapas fundamentais de um pipeline de aprendizado de máquina:

- Análise exploratória dos dados (EDA)
- Pré-processamento
- Treinamento de modelos supervisionados
- Aplicação de técnica de detecção de anomalias
- Avaliação e comparação de desempenho
- Discussão dos resultados

---

## Problema

A detecção de fraudes é um problema crítico em sistemas financeiros e operações de varejo, pois transações fraudulentas podem gerar prejuízos financeiros significativos.

Com base em dados históricos de transações, este projeto busca identificar padrões de comportamento associados a fraudes, permitindo prever se uma transação é legítima ou fraudulenta.

---

## Dataset Utilizado

Dataset:

**Retail Intelligence Fraud Detection Dataset**

Características:

- 100.000 registros de transações
- 21 atributos (features)
- Problema de classificação binária

Variável alvo:

- `fraud_flag`
  - `0` → Transação legítima
  - `1` → Transação fraudulenta

Principais atributos presentes:

- Valor da transação
- Método de pagamento
- Tipo de dispositivo
- Localização
- Categoria do comerciante
- Frequência de transações
- Indicadores de comportamento suspeito
- Indicadores de risco

---

## Estrutura do Projeto

```bash
fraud-detection-project/
│
├── data/
│   └── retail_fraud_detection_100k.csv
│
├── notebook/
│   └── fraud_detection_project.ipynb
│
├── src/
│   └── fraud_detection_project.py
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Análise Exploratória de Dados (EDA)

Durante a análise exploratória foram realizadas as seguintes etapas:

- Inspeção da estrutura do dataset
- Análise estatística descritiva
- Verificação de valores ausentes
- Análise da distribuição da variável alvo
- Estudo de correlação entre variáveis

Gráficos gerados:

- Distribuição de fraudes
- Histograma dos valores transacionados
- Mapa de calor de correlação

Principais insights:

Observou-se forte correlação entre fraudes e variáveis relacionadas a comportamentos atípicos, como:

- `velocity_flag`
- `high_risk_device_flag`
- `unusual_location_flag`
- `previous_fraud_flag`

Esses atributos demonstraram alta relevância para a detecção de transações suspeitas.

---

## Pré-processamento dos Dados

As etapas de pré-processamento incluíram:

### 1. Remoção de atributos irrelevantes

Foram removidas colunas de identificação que não agregam valor preditivo:

- `transaction_id`
- `customer_id`
- `transaction_timestamp`

### 2. Codificação de variáveis categóricas

Variáveis categóricas foram convertidas para formato numérico utilizando:

- One-Hot Encoding

### 3. Normalização

Foi aplicada padronização nos atributos numéricos com:

- StandardScaler

### 4. Divisão treino/teste

Os dados foram separados em:

- 80% para treino
- 20% para teste

---

## Modelos de Machine Learning Utilizados

Foram treinados três modelos supervisionados:

### Regressão Logística
Modelo linear utilizado como baseline de comparação.

### Random Forest
Modelo baseado em ensemble de árvores de decisão, capaz de capturar relações não lineares complexas.

### Gradient Boosting
Modelo baseado em boosting com alto poder preditivo.

---

## Detecção de Anomalias

Além dos modelos supervisionados, foi aplicada uma técnica de detecção de anomalias:

### Isolation Forest

Esse algoritmo busca identificar observações anômalas com base em isolamento estatístico, sendo útil em cenários com pouca disponibilidade de rótulos.

---

## Métricas de Avaliação

Os modelos foram avaliados com as seguintes métricas:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de Confusão

Essas métricas são especialmente relevantes em problemas de detecção de fraude, nos quais erros de classificação possuem alto impacto.

---

## Resultados

Após a avaliação dos modelos, observou-se que os modelos supervisionados apresentaram desempenho superior em relação ao método de detecção de anomalias.

Principais observações:

- O Random Forest apresentou o melhor desempenho geral
- A Regressão Logística teve bom desempenho como baseline
- O Gradient Boosting apresentou resultados competitivos
- O Isolation Forest apresentou desempenho inferior

---

## Conclusão

Os resultados indicam que modelos supervisionados são mais adequados para detecção de fraude quando existe disponibilidade de dados rotulados.

Entre os modelos analisados, o Random Forest apresentou o melhor equilíbrio entre precisão e recall, mostrando-se o modelo mais apropriado para este dataset.

Como possíveis melhorias futuras, destacam-se:

- Ajuste fino de hiperparâmetros
- Engenharia de atributos
- Técnicas de ensemble mais avançadas
- Aplicação de Deep Learning

---

## Tecnologias Utilizadas

- Python 3
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}
- :contentReference[oaicite:3]{index=3}
- :contentReference[oaicite:4]{index=4}
- :contentReference[oaicite:5]{index=5}
- :contentReference[oaicite:6]{index=6}
- :contentReference[oaicite:7]{index=7}

---

## Instalação

Clone o repositório:

```bash
git clone <url-do-repositorio>
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

---

## Execução

Execute o Jupyter Notebook:

```bash
jupyter notebook
```

Abra o arquivo:

```bash
notebook/fraud_detection_project.ipynb
```

---

## Autor

Felipe Cardoso
