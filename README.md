# Fake News Detection using DistilBERT + BiLSTM

## Descrição

Projeto de Detecção de Fake News utilizando Transfer Learning com DistilBERT para geração de embeddings e BiLSTM como classificador final.

O projeto foi desenvolvido para a Liga de Inteligência Artificial - CIn/UFPE.

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

---

# Dataset

Os arquivos train.csv e test.csv não estão versionados no GitHub devido ao tamanho.

Você pode baixar em:

https://drive.google.com/drive/folders/1qHiZDPJ4NQ0ZyfyC7-QH6vInu9AUYdxE?usp=sharing

Após baixar, envie para o ambiente do Google Colab apenas os arquivos necessários para cada etapa.

---

# Como Reproduzir o Projeto (Google Colab)

## 1° Baixe o repositório

Baixe o projeto no GitHub e abra os notebooks no Google Colab.

---

## 2° Execute no Colab

Envie para o ambiente apenas os arquivos necessários para cada notebook.

---

# Escolha como executar

## 1° Treinar do zero

Notebook:

Treino__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb

### Arquivo necessário

- train.csv

No menu do Colab:

Ambiente de execução → Executar tudo

O notebook irá:

- Limpar os textos  
- Gerar embeddings com DistilBERT  
- Treinar o modelo BiLSTM  
- Ajustar o threshold  
- Salvar os artefatos do modelo  

### Arquivos gerados

- bilstm_classifier.keras  
- model_metadata.pkl  
- Pasta distilbert_tokenizer/ (onde tem o tokenizer.json)

O arquivo test.csv não é necessário para o treinamento.

---

## Rodar apenas Inferência

Notebook:

Inferencia__NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb

### Arquivos necessários

- test.csv  
- bilstm_classifier.keras  
- model_metadata.pkl  
- Pasta distilbert_tokenizer/

Ao executar o notebook, será gerado automaticamente o arquivo:

submission.csv

Este arquivo estará pronto para submissão na plataforma Kaggle.
