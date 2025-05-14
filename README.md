# Prediksi Respons Nasabah terhadap Kampanye Deposito Berjangka Menggunakan Machine Learning

Proyek ini merupakan bagian dari Capstone Project Module 3 dalam program pembelajaran Machine Learning. Tujuannya adalah membangun model klasifikasi untuk memprediksi apakah seorang nasabah akan membuka deposito berdasarkan data hasil kampanye pemasaran bank.

## Tujuan Proyek
- Mengembangkan model klasifikasi berbasis machine learning untuk memprediksi kemungkinan nasabah membuka deposito.
- Mengidentifikasi fitur-fitur penting yang memengaruhi keputusan nasabah.
- Memberikan rekomendasi strategis kepada tim pemasaran bank berdasarkan hasil analisis dan prediksi model.

## Dataset
Dataset yang digunakan berisi informasi demografi nasabah dan hasil interaksi kampanye sebelumnya. Target dari dataset ini adalah kolom `deposit` (yes/no).

### Contoh fitur:
- `age`, `job`, `balance`, `housing`, `loan`
- `contact`, `month`, `campaign`, `pdays`, `poutcome`.

## Pendekatan Analitik
- Jenis masalah: Klasifikasi biner
- Model yang diuji:
  - Logistic Regression
  - K-Nearest Neighbors
  - Decision Tree
  - Random Forest (Model terbaik)

## Preprocessing
- Imputasi missing value (median & most frequent)
- Scaling fitur numerik (StandardScaler)
- OneHotEncoding untuk fitur kategorikal
- Tidak menggunakan SMOTE (karena data cukup seimbang)

## Model Terbaik
- Random Forest dengan hyperparameter tuning (GridSearchCV)
- Evaluasi dilakukan pada test set dengan metrik:
  - Accuracy
  - Recall
  - F1-Score (terutama untuk kelas `yes`)
  - ROC AUC

## Hasil Evaluasi
- F1-score kelas `yes`: 0.65
- ROC AUC: 0.74
- Model disimpan dalam format `.pkl` untuk keperluan deployment.

## File Penting
- `data_bank_marketing_campaign.csv` - dataset yang digunakan 
- `014_Capstone Project Module 3_Vanessa Alexandra.ipynb` – seluruh proses analisis dan training model
- `tuned_random_forest_model.pkl` – model terbaik yang disimpan dengan Pickle

## Kesimpulan
Model berhasil memprediksi nasabah potensial secara efektif tanpa perlu balancing tambahan. Pendekatan ini dapat diterapkan oleh tim pemasaran untuk meningkatkan efisiensi kampanye perbankan.

## Rekomendasi
- Gunakan model ini untuk memprioritaskan target campaign
- Lakukan retraining model secara berkala dengan data terbaru
