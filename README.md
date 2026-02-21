# 📰 Fake News Detection using DistilBERT + BiLSTM

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Embeddings-red)
![TensorFlow](https://img.shields.io/badge/TensorFlow-BiLSTM-orange)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![Colab](https://img.shields.io/badge/Google-Colab-F9AB00)
![Status](https://img.shields.io/badge/Status-Complete-success)

Projeto de **Detecção de Fake News** utilizando Transfer Learning com **DistilBERT** para geração de embeddings e **BiLSTM** como classificador final.

O projeto foi desenvolvido para a **Liga de Inteligência Aritifical - CIn/UFPE**.

---

# 🧠 Arquitetura do Modelo
Texto → Tokenizer (DistilBERT)
→ DistilBERT (Embeddings 768d)
→ BiLSTM
→ Dense
→ Sigmoid
→ Classificação (Fake / Real)

---

# 📂 Estrutura do Repositório
Fake-News-Detection-NLP/
│
├── models/
│ ├── bilstm_classifier.keras
│ ├── model_metadata.pkl
│ └── distilbert_tokenizer/
│
├── NLP_Ligia_Luiz_Miguel_Gonzaga.ipynb
├── requirements.txt
└── README.md


---

# 📊 Dataset

Os arquivos `train.csv` e `test.csv` não estão versionados no GitHub devido ao tamanho.

Você pode baixar em:

[<Google Drive >](https://drive.google.com/drive/folders/1qHiZDPJ4NQ0ZyfyC7-QH6vInu9AUYdxE?usp=sharing)

🏆 Kaggle  
👉 <COLOCAR_LINK_KAGGLE_AQUI>

Após baixar, envie para o ambiente do Colab:
train.csv
test.csv


---

# 🚀 Como Reproduzir o Projeto

## 1️⃣ Clone o repositório

```bash
git clone <COLOCAR_LINK_GITHUB_AQUI>

Ou abra diretamente no Google Colab:
👉 <COLOCAR_LINK_COLAB_AQUI>
