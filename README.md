# 🚨 Detecção de Fraudes em Transações Financeiras com Machine Learning

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-green)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![SHAP](https://img.shields.io/badge/Explainability-SHAP-purple)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📊 Sobre o Projeto

Este projeto tem como objetivo construir um sistema de **detecção de fraudes em transações financeiras** utilizando técnicas de Machine Learning, incluindo:

- Feature Engineering  
- Balanceamento de dados  
- Modelos preditivos  
- Explicabilidade com SHAP  

---

## 📊 Dataset

O dataset utilizado contém transações financeiras com variáveis como:

- Valor da transação (`amt`)  
- Comerciante (`merchant`)  
- Categoria (`category`)  
- Localização (`city`, `state`)  
- Informações do cliente (idade, profissão, etc.)  
- Variável alvo: `is_fraud`  

---

## 🎯 Objetivo

Desenvolver modelos capazes de identificar transações fraudulentas com **alta precisão**, mesmo em um cenário altamente desbalanceado.

---

## ⚙️ Tecnologias Utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  
- XGBoost  
- Matplotlib  
- SHAP  

---

## 🧠 Etapas do Projeto

### 📌 1. Importação e Análise dos Dados
- Carregamento do dataset  
- Verificação da distribuição das classes  

### 🔧 2. Feature Engineering
Criação de variáveis a partir de datas:

- Hora da transação (`hour`)  
- Dia (`day`)  
- Mês (`month`)  
- Dia da semana (`weekday`)  
- Idade do cliente (`age`)  

### ⚙️ 3. Pré-processamento
- One-Hot Encoding para variáveis categóricas  
- StandardScaler para variáveis numéricas  

### ⚖️ 4. Balanceamento de Dados
Aplicação de **SMOTE (Synthetic Minority Over-sampling Technique)**:

- Antes: dataset altamente desbalanceado  
- Depois: classes equilibradas no conjunto de treino  

---

## 🤖 Modelos Utilizados

### 📌 Regressão Logística
- `class_weight="balanced"`  
- Modelo baseline  

### 📌 XGBoost
- Modelo principal do projeto  
- Alta capacidade de capturar padrões complexos  

### 📌 Random Forest
- Otimizado com GridSearchCV  
- Ajuste de hiperparâmetros  

---

## 🔧 Otimização de Hiperparâmetros

Utilização de **GridSearchCV** para otimizar o Random Forest com validação cruzada.

---

## 📈 Resultados

### 🔹 Regressão Logística (com SMOTE)
- Recall fraude: ~0.52  
- Precision fraude: ~0.44  

### 🔹 XGBoost
- Recall fraude: ~0.82  
- Precision fraude: ~0.97  
- Melhor desempenho geral  

### 🔹 Random Forest (GridSearchCV)
- Modelo otimizado com foco em F1-score  

---

## 📊 Métricas de Avaliação

- Precision  
- Recall  
- F1-score  
- ROC Curve  
- Precision-Recall Curve  
- AUC Score  

---

## 🔍 Explicabilidade (SHAP)

Uso do **SHAP (SHapley Additive exPlanations)** para:

- Interpretar variáveis mais importantes  
- Entender impacto das features no modelo  
- Aumentar transparência do sistema  

---

## 📌 Principais Insights

- Dataset altamente desbalanceado  
- SMOTE melhora significativamente o recall  
- XGBoost apresentou melhor equilíbrio entre precisão e recall  
- Variáveis temporais e valor da transação são altamente relevantes  

---

## 🚀 Conclusão

Este projeto demonstra um pipeline completo de Machine Learning aplicado à detecção de fraudes:

- Engenharia de variáveis  
- Tratamento de desbalanceamento  
- Comparação de modelos  
- Otimização de hiperparâmetros  
- Interpretabilidade com SHAP  
