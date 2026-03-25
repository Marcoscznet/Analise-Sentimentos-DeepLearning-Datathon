# 🚀 Datathon 2026: Análise de Sentimentos e Dores do Cliente com Deep Learning

Este repositório contém a solução completa para o desafio de análise de sentimentos em larga escala, utilizando dados do **CFPB (Consumer Financial Protection Bureau)**. O projeto evoluiu de modelos estatísticos básicos para uma arquitetura de redes neurais profundas, focada em identificar as causas raiz da insatisfação dos clientes bancários.

## 📊 Performance do Modelo
* **Modelo Final:** LSTM (Long Short-Term Memory) com Embedding.
* **Acurácia Alcançada:** **83.38%** (Superando o baseline de 64%).
* **Volume de Dados:** Processamento de 2,5 milhões de registros.

## 🔍 Principais Insights (Dores do Cliente)
Através da análise de **Bigrams** nas predições negativas, o modelo isolou três pilares críticos de insatisfação:
1.  **Integridade de Dados:** Erros em relatórios de crédito e consultas não autorizadas (*Inaccurate Reporting*).
2.  **Segurança e Fraude:** Alto volume de queixas relacionadas a roubo de identidade (*Identity Theft*).
3.  **Atrito no Atendimento:** Falhas de comunicação em processos de cobrança (*Debt Collection - Called/Told*).

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3.10+
* **Deep Learning:** TensorFlow / Keras (LSTM)
* **Processamento de Linguagem Natural (NLP):** Word2Vec, VADER, NLTK.
* **Engenharia de Dados:** Pandas, Pandarallel (Processamento em 8 cores).
* **Visualização:** Matplotlib, Seaborn, WordCloud.

## 📁 Estrutura do Repositório
* `notebooks/`: Scripts detalhando desde a limpeza até o treinamento da LSTM.
* `models/`: Modelo serializado `.keras` e Tokenizer `.pkl` para uso em produção.
* `data_sample/`: Amostra representativa para testes rápidos.

> **⚠️ Nota sobre os Dados:** O dataset completo possui aproximadamente **8 GB** e, por questões de limite de armazenamento do GitHub, não está incluso diretamente neste repositório. 

## 🚀 Como Executar
1. Instale as dependências: `pip install tensorflow pandas scikit-learn matplotlib seaborn wordcloud joblib pandarallel`
2. Carregue o modelo salvo em `models/` para realizar inferências imediatas sem necessidade de re-treino.