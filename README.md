# Fake News Classification using BERT (bert-base-uncased)

---

## 1. Introduction

Perkembangan teknologi informasi yang sangat pesat telah menyebabkan penyebaran berita menjadi semakin cepat dan masif, terutama melalui platform digital dan media sosial. Namun, fenomena ini juga membawa tantangan besar, salah satunya adalah maraknya **fake news** atau berita palsu. Fake news dapat menyesatkan masyarakat, memengaruhi opini publik, serta berdampak negatif terhadap stabilitas sosial dan politik.

Oleh karena itu, diperlukan sistem otomatis yang mampu **mendeteksi dan mengklasifikasikan berita palsu secara akurat**. Dalam proyek ini, digunakan pendekatan **Natural Language Processing (NLP)** berbasis **Transformer**, khususnya **BERT (Bidirectional Encoder Representations from Transformers)**, untuk melakukan tugas **Fake News Classification**.

---

## 2. Project Objective

Tujuan utama dari proyek ini adalah:

1. Membangun model klasifikasi berita palsu berbasis **Transformer encoder-only**
2. Memanfaatkan **pretrained BERT (bert-base-uncased)** untuk memahami konteks teks berita
3. Mengevaluasi performa model menggunakan metrik klasifikasi standar
4. Menunjukkan efektivitas BERT dalam tugas **binary text classification**

---

## 3. Problem Definition

### Task Type
- **Binary Text Classification**

### Input
- Teks berita (news article)

### Output
- Label kelas:
  - **0** → Fake News
  - **1** → Real News

Masalah ini termasuk ke dalam kategori **supervised learning**, di mana setiap teks berita telah diberi label yang sesuai.

---

## 4. Model Architecture

### 4.1 Transformer Paradigm
Model yang digunakan termasuk dalam kategori:

> **Encoder-only Transformer**

Berbeda dengan model sequence-to-sequence atau decoder-only, encoder-only Transformer sangat cocok untuk tugas:
- Text classification
- Sentiment analysis
- Natural Language Inference (NLI)

### 4.2 BERT (Bidirectional Encoder Representations from Transformers)

BERT merupakan model Transformer yang:
- Dilatih menggunakan **bidirectional context**
- Memahami hubungan antar kata dari kiri dan kanan secara bersamaan
- Menggunakan mekanisme **self-attention**

### 4.3 Model Configuration

- Pretrained Model: `bert-base-uncased`
- Framework: **TensorFlow**
- Model Class: `TFBertForSequenceClassification`
- Number of output labels: **2**
- Classification head: Fully connected layer di atas token `[CLS]`

```python
from transformers import TFBertForSequenceClassification

model = TFBertForSequenceClassification.from_pretrained(
    "bert-base-uncased",
    num_labels=2
)
