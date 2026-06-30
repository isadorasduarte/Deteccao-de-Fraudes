🚨 Detecção de Fraudes em Transações Financeiras com Machine Learning

Este projeto tem como objetivo construir um sistema de detecção de fraudes em transações financeiras utilizando técnicas de Machine Learning, incluindo Feature Engineering, Balanceamento de Dados, Modelos Preditivos e Explicabilidade com SHAP.

📊 Dataset

O dataset utilizado contém transações financeiras com variáveis como:

valor da transação (amt)
comerciante (merchant)
categoria (category)
localização (city, state)
informações do cliente (idade, profissão, etc.)
variável alvo: is_fraud

🎯 Objetivo

Desenvolver modelos capazes de identificar transações fraudulentas com alta precisão, mesmo em um cenário altamente desbalanceado.

⚙️ Tecnologias utilizadas
Python 
Pandas
NumPy
Scikit-learn
Imbalanced-learn (SMOTE)
XGBoost
Matplotlib
SHAP

🧠 Etapas do Projeto
1. Importação e análise dos dados
Carregamento do dataset
Verificação da distribuição das classes

2. Feature Engineering
Foram criadas novas variáveis a partir de datas:

hora da transação (hour)
dia (day)
mês (month)
dia da semana (weekday)
idade do cliente (age)

3. Pré-processamento
One-Hot Encoding para variáveis categóricas
StandardScaler para variáveis numéricas

4. Balanceamento de dados
Foi aplicado SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar a classe de fraude:

Antes: altamente desbalanceado
Depois: classes balanceadas no conjunto de treino

🤖 Modelos utilizados
📌 Regressão Logística
com class_weight="balanced"
baseline do problema
📌 XGBoost 
modelo principal do projeto
alta capacidade de captura de padrões complexos
📌 Random Forest
otimizado com GridSearchCV
🔧 Otimização de hiperparâmetros

Foi utilizado GridSearchCV para:

Random Forest tuning
busca por melhores parâmetros com validação cruzada

📈 Resultados
🔹 Regressão Logística (com SMOTE)
Recall fraude: ~0.52
Precision fraude: ~0.44
🔹 XGBoost
Recall fraude: ~0.82
Precision fraude: ~0.97
Excelente desempenho geral
🔹 Random Forest (GridSearchCV)
Modelo otimizado com F1-score como métrica principal

📊 Avaliação dos modelos

Foram utilizadas métricas como:

Precision
Recall
F1-score
ROC Curve
Precision-Recall Curve
AUC Score

🔍 Explicabilidade (SHAP)

Foi utilizado SHAP (SHapley Additive exPlanations) para:

entender as variáveis mais importantes
interpretar o impacto de cada feature no modelo
aumentar transparência do modelo

📌 Principais insights
O dataset é altamente desbalanceado
SMOTE melhora significativamente o recall
XGBoost apresentou melhor equilíbrio entre precisão e recall
Variáveis temporais e valor da transação são altamente relevantes

🚀 Conclusão

O projeto demonstra um pipeline completo de Machine Learning aplicado à detecção de fraudes, incluindo:

engenharia de variáveis
tratamento de desbalanceamento
comparação de modelos
tuning de hiperparâmetros
interpretabilidade com SHAP
