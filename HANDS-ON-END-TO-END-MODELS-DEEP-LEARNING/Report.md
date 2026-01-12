# Fake News Classification Report using BERT

## 1. Overview
Penelitian ini bertujuan untuk membangun dan mengevaluasi model **Fake News Classification**
menggunakan **BERT (Bidirectional Encoder Representations from Transformers)**.
Model ini melakukan klasifikasi berita ke dalam dua kelas:

- **Class 0** : Real News  
- **Class 1** : Fake News  

Evaluasi dilakukan menggunakan **test set** yang terdiri dari **634 data** dengan distribusi kelas yang seimbang.

---

## 2. Evaluation Metrics
Untuk mengukur performa model, digunakan metrik evaluasi berikut:

- **Precision** : Mengukur ketepatan prediksi model
- **Recall** : Mengukur kemampuan model dalam mendeteksi seluruh data relevan
- **F1-Score** : Rata-rata harmonik antara precision dan recall
- **Accuracy** : Persentase prediksi yang benar secara keseluruhan

---

## 3. Classification Report

| Class | Precision | Recall | F1-Score | Support |
|------|----------|--------|----------|---------|
| 0 (Real News) | 1.00 | 0.96 | 0.98 | 317 |
| 1 (Fake News) | 0.96 | 1.00 | 0.98 | 317 |
| **Accuracy** |  |  | **0.98** | 634 |
| **Macro Avg** | 0.98 | 0.98 | 0.98 | 634 |
| **Weighted Avg** | 0.98 | 0.98 | 0.98 | 634 |

---

## 4. Analysis and Discussion

### 4.1 Overall Performance
Model BERT menunjukkan performa yang sangat baik dengan **akurasi sebesar 98%**.
Hal ini mengindikasikan bahwa model mampu membedakan berita palsu dan berita asli secara efektif.

### 4.2 Class-wise Performance

#### Real News (Class 0)
- **Precision = 1.00** menunjukkan bahwa seluruh prediksi berita asli benar.
- **Recall = 0.96** mengindikasikan terdapat sebagian kecil berita asli yang salah diklasifikasikan sebagai berita palsu.

#### Fake News (Class 1)
- **Recall = 1.00** menandakan seluruh berita palsu berhasil terdeteksi oleh model.
- **Precision = 0.96** menunjukkan adanya beberapa berita asli yang salah diprediksi sebagai berita palsu.

### 4.3 Class Balance
Nilai **macro average** dan **weighted average** yang sama (0.98) menunjukkan bahwa:
- Dataset bersifat seimbang
- Model tidak menunjukkan bias terhadap salah satu kelas

---

## 5. Strengths
- Performa klasifikasi sangat tinggi
- Mampu mendeteksi berita palsu secara optimal
- Cocok digunakan sebagai baseline untuk sistem deteksi fake news

---

## 6. Limitations
- Masih terdapat kesalahan klasifikasi pada berita asli
- Evaluasi hanya dilakukan pada satu dataset uji
- Belum diuji pada data dunia nyata (out-of-distribution data)

---

## 7. Conclusion
Model **Fake News Classification berbasis BERT** berhasil mencapai performa yang sangat baik
dengan **akurasi 98%** dan **F1-score 0.98** pada kedua kelas.
Hasil ini menunjukkan bahwa BERT sangat efektif untuk tugas klasifikasi berita palsu.

---

**Keywords:** Fake News Detection, BERT, Transformer, Text Classification, NLP

