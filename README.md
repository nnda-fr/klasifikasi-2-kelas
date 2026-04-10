# Citrus Classification: Oranges vs. Grapefruits 

[](https://www.python.org/)
[](https://keras.io/)
[](https://scikit-learn.org/)

Proyek ini menggunakan **Artificial Neural Networks (ANN)** untuk mengklasifikasikan buah jeruk ke dalam dua kategori: **Orange (Jeruk)** atau **Grapefruit (Jeruk Besar)** berdasarkan karakteristik fisik seperti diameter, berat, dan nilai warna (RGB).

## Ringkasan Model

Model dibangun menggunakan arsitektur *Deep Learning* sederhana dengan **Keras Sequential API**. Berdasarkan data pelatihan, model ini mampu mencapai akurasi sekitar **92-93%** pada data pengujian.

### Dataset

Dataset terdiri dari **10.000 sampel** buah dengan fitur-fitur berikut:

  * `diameter`: Diameter buah.
  * `weight`: Berat buah.
  * `red`, `green`, `blue`: Nilai rata-rata warna dalam skala RGB.
  * `name`: Label target (Orange atau Grapefruit).

## Langkah Eksperimen

### 1\. Preprocessing Data

  * **Label Encoding**: Mengubah label tekstual (`orange` & `grapefruit`) menjadi nilai numerik (0 dan 1).
  * **Feature Scaling**: Menggunakan `MinMaxScaler` untuk menormalkan rentang nilai fitur agar model konvergen lebih cepat.
  * **Train-Test Split**: Membagi data dengan rasio **70% Pelatihan** dan **30% Pengujian**.

### 2\. Arsitektur Neural Network

Model terdiri dari tiga lapisan *Dense*:

  * **Input Layer**: 32 neuron, aktivasi ReLU.
  * **Hidden Layer**: 32 neuron, aktivasi ReLU.
  * **Output Layer**: 1 neuron, aktivasi Sigmoid (untuk klasifikasi biner).

### 3\. Kompilasi & Pelatihan

  * **Optimizer**: Stochastic Gradient Descent (SGD).
  * **Loss Function**: Binary Crossentropy.
  * **Epochs**: 100.

## Hasil Evaluasi

Setelah proses pelatihan selama 100 epoch, model memberikan performa yang sangat solid:

| Metric | Score |
| :--- | :--- |
| **Training Accuracy** | \~92.8% |
| **Test Accuracy** | **92.3%** |
| **Test Loss** | 0.1855 |

## Cara Penggunaan

1.  Pastikan kamu memiliki library yang dibutuhkan: `pandas`, `scikit-learn`, dan `keras`.
2.  Muat dataset `citrus.csv`.
3.  Jalankan notebook `klasifikasi_dua_kelas.ipynb`.

-----
