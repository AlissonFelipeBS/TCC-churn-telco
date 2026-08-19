# Predição de Churn em Telecom

Projeto de conclusão do MBA em Data Science & Analytics da **USP/Esalq**, desenvolvido por **Alisson Felipe Brandão da Silva**.

O objetivo é identificar clientes com maior propensão ao cancelamento e transformar os resultados do modelo em informações úteis para ações de retenção.

## Problema de negócio

O churn reduz receita recorrente e aumenta a necessidade de aquisição de novos clientes. Um modelo de classificação pode ajudar a priorizar clientes para ações preventivas, desde que a avaliação considere o custo de não identificar um cancelamento real.

Por isso, o projeto dá atenção especial ao **recall da classe churn**.

## Dados

Foi utilizada a base pública **IBM Telco Customer Churn**, com 7.032 registros após o tratamento dos dados. Ela reúne características como:

- tempo de permanência do cliente;
- tipo de contrato;
- serviços contratados;
- forma de pagamento;
- cobranças mensais e totais;
- situação de churn.

## Metodologia

1. Análise exploratória e verificação da qualidade dos dados.
2. Tratamento de valores ausentes e preparação das variáveis.
3. Codificação de variáveis categóricas com `OneHotEncoder`.
4. Validação com `StratifiedKFold`.
5. Comparação entre:
   - Regressão Logística;
   - Random Forest;
   - Gradient Boosting.
6. Interpretação das métricas e dos fatores associados ao churn.

## Principais resultados

- A **Regressão Logística** apresentou o equilíbrio mais adequado ao cenário analisado.
- O **tipo de contrato** foi o fator de maior importância relativa, com aproximadamente **39,9%**.
- A avaliação priorizou **recall**, reduzindo o risco de deixar de identificar clientes que efetivamente cancelariam.
- Os resultados indicam que clientes com determinados perfis contratuais devem receber atenção especial nas estratégias de retenção.

> As métricas devem ser interpretadas no contexto deste conjunto de dados e não representam, isoladamente, desempenho esperado em produção.

## Tecnologias

- Python 3.10
- pandas e NumPy
- scikit-learn
- Matplotlib e Seaborn
- Jupyter Notebook

## Estrutura do repositório

```text
.
├── TCC-churn-telco.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── requirements.txt
├── .gitignore
└── README.md
```

## Como reproduzir

Clone o repositório e instale as dependências:

```bash
git clone https://github.com/AlissonFelipeBS/TCC-churn-telco.git
cd TCC-churn-telco
python -m venv .venv
```

Ative o ambiente virtual:

```bash
# Linux/macOS
source .venv/bin/activate

# Windows
.venv\Scripts\activate
```

Instale as dependências e abra o notebook:

```bash
pip install -r requirements.txt
jupyter notebook TCC-churn-telco.ipynb
```

## Limitações e próximos passos

- Validar o modelo com dados de outra população ou período.
- Definir limiar de decisão a partir do custo de retenção e do valor do cliente.
- Avaliar calibração das probabilidades.
- Criar um pipeline de inferência e monitoramento.
- Medir o impacto real por meio de testes controlados de campanhas de retenção.

## Autoria

**Autor:** Alisson Felipe Brandão da Silva  
**Orientadora:** Dra. Lilian Silveira  
**Instituição:** USP/Esalq
