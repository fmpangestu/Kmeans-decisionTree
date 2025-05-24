# Proyek Machine Learning: Segmentasi Pelanggan Ritel

Ini adalah submission untuk kelas **[Nama Kelas Dicoding Anda, contoh: Belajar Machine Learning untuk Pemula]** di Dicoding. Proyek ini bertujuan untuk melakukan segmentasi pelanggan berdasarkan data transaksi menggunakan teknik _unsupervised learning_ (Clustering) dan kemudian membangun model klasifikasi untuk memprediksi segmen pelanggan.

![image_2722f0.png](image_2722f0.png)

## Daftar Isi

- [Latar Belakang](#latar-belakang)
- [Tujuan Proyek](#tujuan-proyek)
- [Dataset](#dataset)
- [Metodologi](#metodologi)
  - [Clustering](#clustering)
  - [Klasifikasi](#klasifikasi)
- [Struktur Repository](#struktur-repository)
- [Hasil](#hasil)
- [Instalasi & Penggunaan](#instalasi--penggunaan)

## Latar Belakang

(Jelaskan secara singkat mengapa segmentasi pelanggan itu penting dalam bisnis ritel, seperti yang ada di template Dicoding Anda. Anda bisa copy-paste dari sana atau tulis ulang dengan gaya Anda).

## Tujuan Proyek

- Mengidentifikasi kelompok-kelompok (segmen) pelanggan yang berbeda berdasarkan perilaku transaksi mereka.
- Membangun model K-Means Clustering untuk segmentasi.
- Menginterpretasikan karakteristik dari setiap segmen yang terbentuk.
- Membangun model klasifikasi (seperti Decision Tree) untuk memprediksi segmen pelanggan berdasarkan data transaksi mereka.

## Dataset

Dataset yang digunakan adalah **[Nama Dataset, contoh: Bank Transactions Data]**. Dataset ini berisi informasi transaksi pelanggan yang mencakup fitur-fitur berikut:

- `TransactionID`: ID unik transaksi.
- `AccountID`: ID unik akun pelanggan.
- `TransactionAmount`: Jumlah transaksi.
- `Gender`: Jenis kelamin pelanggan.
- `Age`: Usia pelanggan.
- `CardType`: Jenis kartu yang digunakan.
- `TransactionType`: Jenis transaksi.
- `Latitude`: Garis lintang lokasi transaksi.
- `Longitude`: Garis bujur lokasi transaksi.
- `MerchantID`: ID unik _merchant_.
- `DeviceID`: ID unik perangkat.
- `IPAddress`: Alamat IP.

_(Sesuaikan daftar fitur ini dengan dataset Anda yang sebenarnya)._

## Metodologi

Proyek ini dibagi menjadi dua tahap utama:

### Clustering

1.  **Memuat Data:** Memuat dataset dari sumbernya.
2.  **Exploratory Data Analysis (EDA):** Memahami struktur data, distribusi fitur, dan korelasi.
3.  **Pembersihan & Pra-Pemrosesan:**
    - Menangani nilai yang hilang (NaN).
    - Menghapus data duplikat.
    - Menghapus kolom ID yang tidak relevan.
    - Melakukan _Feature Encoding_ pada fitur kategorikal (misalnya, menggunakan LabelEncoder).
    - Melakukan _Feature Scaling_ pada fitur numerik (misalnya, menggunakan MinMaxScaler).
4.  **Membangun Model Clustering:**
    - Menentukan jumlah _cluster_ optimal menggunakan _Elbow Method_ (KElbowVisualizer).
    - Melatih model K-Means Clustering.
    - (Opsional) Menghitung _Silhouette Score_.
    - (Opsional) Memvisualisasikan hasil _cluster_ menggunakan PCA.
5.  **Interpretasi Cluster:** Menganalisis karakteristik setiap _cluster_ berdasarkan data asli menggunakan fungsi agregasi (min, max, mean, mode).

### Klasifikasi

1.  **Memuat Data Hasil Clustering:** Menggunakan dataset yang sudah diberi label 'Target' dari tahap _clustering_.
2.  **Data Splitting:** Membagi dataset menjadi data latih dan data uji.
3.  **Membangun Model:**
    - Melatih model Decision Tree.
    - (Opsional) Melatih algoritma lain (misalnya, KNN, Random Forest).
4.  **Evaluasi Model:** Mengevaluasi performa model menggunakan metrik seperti Akurasi, Presisi, Recall, dan F1-Score.
5.  **(Opsional) Hyperparameter Tuning:** Mengoptimalkan model menggunakan teknik seperti GridSearchCV.

## Struktur Repository
