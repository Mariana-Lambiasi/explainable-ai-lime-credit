# explainable-ai-lime-credit

Explainable AI: LIME aplicado à Classificação de Crédito

Este projeto apresenta a criação de um modelo de classificação de risco de crédito e o uso da técnica LIME (Local Interpretable Model-Agnostic Explanations) para explicar decisões do modelo de forma clara e interpretável. O objetivo é garantir transparência e justiça na tomada de decisões automatizadas.

🎯 Objetivo

Analisar dados de clientes para prever se um solicitante de crédito tem maior probabilidade de ser:

1 → Bom pagador

0 → Mau pagador

Além disso, explicar por que o modelo toma determinada decisão, utilizando o LIME.

📊 Distribuição da Variável Alvo
Classe	Significado	Quantidade	Proporção
1	Bom pagador	700	70%
0	Mau pagador	300	30%
🤖 Modelo Treinado

Foi treinado um modelo de classificação supervisionado usando dados financeiros, demográficos e comportamentais de crédito.
O modelo aprende padrões para prever o risco de inadimplência.

✅ Resultados do Modelo

Matriz de Confusão:

[[ 36  55]
 [ 12 197]]

Métrica	Valor
Acurácia	0.7767
Precisão	0.7817
Recall	0.9426
F1-Score	0.8547

O modelo apresenta bom recall para a classe Bom Pagador, sendo útil em decisões de crédito onde minimizar falsos negativos é importante.

🔍 Explicação LIME da Predição
Probabilidades previstas:
Classe	Probabilidade
Mau Pagador (0)	0.16
Bom Pagador (1)	0.84

➡️ Predição Final: Bom pagador

Principais Fatores que levaram à decisão:
Variável	Impacto	Interpretação
status_account	↓ risco	Conta sem restrições
credit_history	↓ risco	Histórico confiável
savings	↓ risco	Possui reserva financeira
duration	↓ risco	Prazo curto do empréstimo

Esses fatores contribuíram para classificar o cliente como de baixo risco.

📦 explainable-ai-lime-credit
 ┣ model_training.ipynb        → Notebook completo do Colab
 ┣ german_credit.csv           → Base de dados
 ┣ lime_explanation.html       → Visualização interativa da explicação LIME
 ┣ lime_explanation.png        → Gráfico da explicação (imagem estática)
 ┣ requirements.txt            → Dependências do projeto
 ┗ README.md                   → Documentação do projeto


💻 Como Executar

Instalar dependências:

pip install -r requirements.txt


Abrir o notebook:

jupyter notebook notebooks/model_training.ipynb

✨ Autoria

Projeto desenvolvido por Mariana Lambiasi, com foco em interpretabilidade e ética em IA.

📬 Contato

👩‍💻 Mariana Lambiasi de Carvalho 
📧 mariana.carvalho.80804@a.fecaf.com.br





