# Fake News Detection using DistilBERT + BiLSTM

## Descrição

Projeto de Detecção de Fake News utilizando Transfer Learning com DistilBERT para geração de embeddings e BiLSTM como classificador final.

O projeto foi desenvolvido para a Liga de Inteligência Artificial - CIn/UFPE.

O pipeline está organizado em três etapas independentes:
- Análise Exploratória de Dados (EDA)
- Treinamento do Modelo
- Inferência e Geração de Submissão

---

# Arquitetura do Modelo

Texto  
→ Tokenizer (DistilBERT)  
→ DistilBERT (Embeddings 768d)  
→ BiLSTM  
→ Dense  
→ Sigmoid  
→ Classificação (Fake / Real)

---

# Estrutura do Repositório

```
Fake-News-Detection-NLP/
│
├── models/
│   ├── bilstm_classifier.keras
│   ├── model_metadata.pkl
│   └── tokenizer.json
│
├── EDA__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb
├── Treino__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb
├── Inferencia__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb
│
├── requirements.txt
└── README.md
```

---

# Dataset

Os arquivos train.csv e test.csv não estão versionados no GitHub devido ao tamanho.

Você pode baixar em:

https://drive.google.com/drive/folders/1qHiZDPJ4NQ0ZyfyC7-QH6vInu9AUYdxE?usp=sharing

Após baixar, envie para o ambiente do Google Colab apenas os arquivos necessários para cada etapa.

---

# Como Reproduzir o Projeto (Google Colab)

O Google Colab já possui as principais dependências necessárias para execução.

---

## 1° Baixe o repositório

Baixe o projeto no GitHub e abra os notebooks no Google Colab.

---

## 2° Execute no Colab

Envie para o ambiente apenas os arquivos necessários para cada notebook.

---

# 1. Rodar a Análise Exploratória de Dados (EDA)

Notebook:

EDA__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb

### Arquivo necessário

- train.csv

### O que será realizado

- Análise da distribuição das classes  
- Correlação entre subject e label  
- Estatísticas do tamanho dos textos  
- Frequência de palavras  

---

# 2. Treinar o Modelo

Notebook:

Treino__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb

### Arquivo necessário

- train.csv

No menu do Colab:

Ambiente de execução → Executar tudo

### O que será realizado

- Limpeza dos textos  
- Tokenização com DistilBERT  
- Geração de embeddings  
- Treinamento do modelo BiLSTM  
- Ajuste do threshold com base no F1-score  
- Salvamento dos artefatos do modelo  

### Arquivos gerados

- bilstm_classifier.keras  
- model_metadata.pkl  
- tokenizer.json 

---

# 3. Rodar apenas Inferência

Notebook:

Inferencia__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb

### Arquivos necessários

- test.csv  
- bilstm_classifier.keras  
- model_metadata.pkl  
- tokenizer.json  

Ao executar o notebook, será gerado automaticamente o arquivo:

submission.csv
