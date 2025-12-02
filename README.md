**1. Klasifikasi Kelulusan Mahasiswa Menggunakan Support Vector Machine (SVM)**
Project ini bertujuan untuk memprediksi status kelulusan mahasiswa berdasarkan atribut akademik menggunakan algoritma Support Vector Machine (SVM). Model dibangun dan diuji menggunakan beberapa konfigurasi train-test split untuk membandingkan performa terbaik.

**2. Deskripsi Dataset**
Dataset berisi data akademik mahasiswa dengan fitur:
- IPS1, IPS2, IPS3, IPS4 — nilai IP per semester
- IPK — Indeks Prestasi Kumulatif
- TOTAL_SKS — total SKS
- MASA_STUDI — lama studi
- STATUS_KELULUSAN — label target
  - 0 = Tidak Lulus Tepat Waktu
  - 1 = Lulus Tepat Waktu
  - 
Dataset disimpan dalam folder:
/data/datakelulusanmahasiswa.csv

**3. Langkah Pengerjaan**
1. Import Library seperti pandas, numpy, sklearn, seaborn, dan matplotlib.
2. Load Dataset, membaca file CSV ke DataFrame.
3. Preprocessing Data
   - Membersihkan missing values
   - Menentukan numeric columns
   - Normalisasi dengan StandardScaler
4. Train-Test Split dengan 4 konfigurasi:
   - 60:40
   - 75:25
   - 80:20
   - 90:10
5. Training Model SVM
   - Menggunakan Pipeline: StandardScaler + SVC
   - Hyperparameter tuning dengan GridSearchCV
   - Parameter grid:
     kernel = ['linear', 'rbf']
     C = [0.1, 1, 10]
     gamma = ['auto', 'scale']
6. Evaluasi Model
   - Accuracy
   - Confusion Matrix
   - Classification Report
7. Analisis perbandingan hasil setiap split


**4. Hasil Evaluasi Model**
Berikut hasil evaluasi pada berbagai train-test split :
 - Split 60:40
   - Best params: C = 0.1, kernel = linear
   - Accuracy: 0.9013
   - Confusion Matrix:
     [[84, 3], [12, 53]]
 - Split 75:25
   - Best params: C = 1, kernel = rbf, gamma = scale
   - Accuracy: 0.8737
   - Confusion Matrix:
     [[46, 8], [4, 37]]
 - Split 80:20
   - Best params: C = 0.1, kernel = linear
   - Accuracy: 0.8947
   - Confusion Matrix:
     [[42, 1], [7, 26]]
 - Split 90:10
   - Best params: C = 10, kernel = linear
   - Accuracy: 0.9210
   - Confusion Matrix:
     [[21, 1], [2, 14]]

**5. Cara Menjalankan Notebook**
1. Clone repository :
   git clone https://github.com/username/repository.git
2. Masuk ke folder repo :
   cd nama-repository
3. Pastikan dataset ada di folder /data.
4. Jalankan Jupyter Notebook :
   jupyter notebook
5. Buka file :
   SVM_kelulusan.ipynb
6. Klik Run All untuk menjalankan seluruh sel.
   
**6. Indentitas Mahasiswa**

Nama           : M. Nurraditya

NPM            : 2457201002362

Kelas          : 3A

Mata Kuliah    : Machine Learning

Dosen Pengampu : Dr. DWI WAHYU PRABOWO, S.Si

