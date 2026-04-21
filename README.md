# Aprendizado de Máquina na Previsão de Cancelamento de Clientes no Setor de Telecomunicações

Este repositório contém o projeto de conclusão de curso (TCC) de **Alisson Felipe Brandão da Silva** para o MBA em Data Science e Analytics pela **USP/Esalq**.
O trabalho consiste no desenvolvimento de modelos preditivos para identificação de *churn*, utilizando uma base de dados realística para orientar decisões estratégicas de retenção no setor de Telecom.

## 📌 Visão Geral
O projeto aborda o problema de evasão de clientes utilizando a base pública *IBM Telco Customer Churn* (7.032 registros). A análise busca entender o perfil do cliente propenso ao cancelamento e validar a eficácia de algoritmos de classificação.

## 🔬 Metodologia e Modelagem
Seguindo os preceitos de **Morettin & Singer (2020)** e **Provost & Fawcett (2016)**, o pipeline de dados foi estruturado em:
1. **EDA (Análise Exploratória):** Identificação de correlações entre tipo de contrato, tenure e churn.
2. **Engenharia de Atributos:** Tratamento de dados nulos e codificação via *OneHotEncoder*.
3. **Validação:** Aplicação de `StratifiedKFold` para lidar com o desbalanceamento das classes.
4. **Algoritmos Testados:**
   - Regressão Logística
   - Random Forest (com análise de importância relativa)
   - Gradient Boosting

## 📊 Principais Resultados
- **Melhor Modelo:** A **Regressão Logística** apresentou o desempenho mais equilibrado para o cenário de negócio proposto.
- **Fator Determinante:** A variável de **tipo de contrato** apresentou a maior importância relativa (aprox. 39,9%), sendo o principal indicador preditivo.
- **Métricas de Foco:** Priorização do **Recall** para minimizar o custo de oportunidade de não identificar um cancelamento real.

## 🛠️ Tecnologias Utilizadas
- **Python 3.10**
- **Bibliotecas:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`.
- **Padronização:** Gráficos configurados com paleta de cores institucional e formatação acadêmica.

## 📂 Estrutura do Repositório
- `churn_tcc_final.ipynb`: Notebook principal com todo o desenvolvimento técnico.
- `WA_Fn-UseC_-Telco-Customer-Churn.csv`: Base de dados utilizada.
- `requirements.txt`: Dependências para reprodução do ambiente.

---
**Autor:** Alisson Felipe Brandão da Silva  
**Orientadora:** Dra. Lilian Silveira  
**Instituição:** USP/Esalq
