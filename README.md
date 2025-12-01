# SVM_kelulusan

Proyek Klasifikasi Kelulusan Mahasiswa dengan Support Vector Machine (SVM)
1. Judul Proyek
Klasifikasi Status Kelulusan Mahasiswa Menggunakan Algoritma Support Vector Machine (SVM)

2. Deskripsi Dataset
Dataset ini berisi data historis mahasiswa yang digunakan untuk memprediksi status kelulusan (Lulus atau Belum Lulus). Data terdiri dari berbagai atribut yang mencerminkan performa akademik dan status kemahasiswaan.

## 📊 Deskripsi Fitur Dataset

| Fitur                   | Tipe Data              | Deskripsi                                                  |
|-------------------------|------------------------|------------------------------------------------------------|
| IPK                     | Numerik (float)        | Indeks Prestasi Kumulatif terakhir.                       |
| Total SKS               | Numerik (int)          | Total SKS yang telah ditempuh.                            |
| Umur                    | Numerik (int)          | Usia mahasiswa.                                            |
| Lama Studi (Semester)   | Numerik (int)          | Jumlah semester yang telah dijalani.                      |
| Status Kehadiran        | Kategorikal            | Status keaktifan mahasiswa (contoh: Aktif, Cuti).         |
| Keaktifan Organisasi    | Numerik (int)          | Indikator keaktifan organisasi (1 = Aktif, 0 = Tidak).    |
| Nilai MK Tertentu       | Numerik (float)        | Nilai pada mata kuliah kunci.                             |
| Label (Target)          | Kategorikal (Biner)    | Lulus / Belum Lulus.                                      |

3. Langkah Pengerjaan (Metodologi)Proyek ini dilaksanakan melalui tahapan standar data science:3.1. Eksplorasi Data (EDA) 📊Memeriksa struktur data, tipe, dan statistik deskriptif.Mengidentifikasi bahwa IPK dan Lama Studi adalah fitur yang paling membedakan status kelulusan.3.2. Preprocessing Data 🧹Penanganan Missing Values: Menggunakan Imputasi Median pada kolom IPK.Encoding: Variabel kategorikal di-encode (Label Encoding untuk Target, One-Hot Encoding untuk Status_Kehadiran).Scaling: Seluruh fitur numerik distandarisasi menggunakan StandardScaler, yang krusial untuk kinerja SVM.Split Data: Data dibagi menjadi 80% Latih dan 20% Uji.3.3. Training dan Tuning Model ⚙️Model Support Vector Classifier (SVC) dilatih menggunakan kernel Linear dan RBF.Dilakukan hyperparameter tuning dasar pada C dan gamma untuk menemukan konfigurasi optimal.4. Hasil Evaluasi ModelModel terbaik yang diidentifikasi adalah SVM RBF Kernel dengan parameter optimal $C$ dan $\gamma$ (gamma). Hal ini menunjukkan adanya pola non-linear dalam data kelulusan.Metrik Model Terbaik (SVM RBF)

## 📈 Evaluasi Model SVM

| Metrik      | Hasil              | Interpretasi                                                   |
|-------------|--------------------|----------------------------------------------------------------|
| Akurasi     | [Nilai Tertinggi]% | Tingkat prediksi yang benar secara keseluruhan.               |
| Precision   | [Nilai]            | Keakuratan model dalam memprediksi kelas **Lulus**.           |
| Recall      | [Nilai]            | Kemampuan model menemukan seluruh kasus yang sebenarnya Lulus.|
| F1-Score    | [Nilai]            | Keseimbangan antara Precision dan Recall.                     |

5. Cara Menjalankan Notebook
5.1. Kebutuhan Pustaka
Pastikan Anda telah menginstal pustaka berikut di lingkungan Python Anda:

Bash

pip install pandas numpy scikit-learn matplotlib seaborn
5.2. Langkah Eksekusi
Unduh file svm_kelulusan_mahasiswa.ipynb dan data_kelulusan.csv.

Buka notebook menggunakan Jupyter Notebook atau Google Colab.

Jalankan semua cell secara berurutan.

Gunakan fungsi predict_status() di akhir notebook untuk menguji model dengan data input baru.

6. Identitas Mahasiswa
## 👤 Identitas Mahasiswa

| Detail         | Informasi                   |
|----------------|-----------------------------|
| Nama           | [Nama Lengkap Mahasiswa]    |
| NIM            | [Nomor Induk Mahasiswa]     |
| Mata Kuliah    | [Nama Mata Kuliah]          |
| Program Studi  | [Nama Program Studi]        |

