# 📊 Teste Técnico — Cientista de Dados Junior

**Candidato:** Pedro Vicente Moda  
**Posição:** Cientista de Dados Junior  
**Dataset:** `dados_clientes_teste_cientista.csv` — 1.000 clientes de um aplicativo de bem-estar

---

## 📁 Estrutura do Repositório

```
teste_tecnico_ds/
│
├── TesteTecnicoPedroDS.ipynb   # Notebook principal com toda a análise
├── dados_clientes_teste_cientista.csv  # Dataset utilizado
└── README.md
```

---

## 🎯 Objetivo

Analisar o comportamento de cancelamento de serviço (`churn`) de clientes de um aplicativo de bem-estar, passando por todas as etapas de um projeto de ciência de dados: exploração, modelagem supervisionada, não supervisionada e comunicação de resultados.

---

## 🔍 Etapas da Análise

### 1. Análise Exploratória de Dados (EDA)
- Verificação de qualidade dos dados (ausentes, duplicados, tipos)
- Estatísticas descritivas e levantamento de hipóteses
- Identificação de inconsistências (idades suspeitas < 18 anos)
- Análise de correlação entre variáveis e cancelamento
- Visualizações: histograma, boxplots por grupo

### 2. Programação com Python
- Implementação manual do **Robust Scaling** via função customizada
- Simulação de **distribuição binomial** (n=10, p=0.5, 1.000 amostras)

### 3. Estatística e Probabilidade
- **Teste t de Student** para comparação de renda entre sexos
- **Intervalo de Confiança (95%)** para a média de idade dos clientes

### 4. Machine Learning Supervisionado
- Modelo: **Random Forest** com `class_weight=balanced`
- Métricas: Accuracy, F1-Score e ROC-AUC
- Tuning de hiperparâmetros com **GridSearchCV**

### 5. Machine Learning Não Supervisionado
- **PCA** para redução de dimensionalidade e visualização
- **KMeans** com validação por Elbow Method e Silhouette Score

---

## 📈 Principais Resultados

| Métrica | Antes do Tuning | Após Tuning |
|---|---|---|
| Accuracy | 79,00% | 68,50% |
| F1-Score | 0,045 | 0,241 |
| ROC-AUC | 0,500 | 0,479 |

> O modelo apresentou performance insatisfatória, consistente com as correlações próximas de zero observadas na EDA. A conclusão é que as features disponíveis não possuem poder preditivo suficiente para explicar o cancelamento — problema de dados, não de modelo.

**Número ideal de clusters:** 3 — validado tanto pelo Elbow Method quanto pelo Silhouette Score.

---

## 🛠️ Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?logo=scikit-learn)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4C72B0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 🗂️ Versionamento

O projeto foi versionado com **Git** seguindo boas práticas de commits atômicos e mensagens descritivas.
---

## ▶️ Como Executar

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/teste_tecnico_ds.git
cd teste_tecnico_ds

# Instale as dependências
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter

# Execute o notebook
jupyter notebook TesteTecnicoPedroDS.ipynb
```

---

