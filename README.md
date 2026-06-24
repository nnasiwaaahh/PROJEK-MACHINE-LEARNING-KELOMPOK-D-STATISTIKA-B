# Analisis Regresi Premi Asuransi Kesehatan dengan Pendekatan Machine Learning

## Deskripsi Project

Proyek ini bertujuan untuk membangun model machine learning yang mampu memprediksi biaya asuransi kesehatan (medical insurance charges) berdasarkan karakteristik peserta asuransi. Dataset yang digunakan memuat informasi mengenai usia, jenis kelamin, indeks massa tubuh (BMI), jumlah tanggungan, status merokok, dan wilayah tempat tinggal peserta asuransi.

Penelitian dilakukan melalui tahapan:

* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Feature Engineering
* Pemodelan Machine Learning
* Hyperparameter Tuning
* Evaluasi dan Interpretasi Model

Beberapa algoritma regresi yang dibandingkan dalam penelitian ini meliputi:

* Linear Regression
* K-Nearest Neighbor (KNN) Regression
* Random Forest Regressor
* XGBoost Regressor

---

## Anggota Tim

| Nama                    | NIM       |
| ----------------------- | --------- |
| Nasywa Putri Maitsa     | K1D024043 |
| Nadia Marsha            | K1D024046 |
| Raditya Akbar Firdaus   | K1D023063 |
| Kezya Aurell Manuela S. | K1D024071 |

Program Studi Statistika
Fakultas Matematika dan Ilmu Pengetahuan Alam
Universitas Jenderal Soedirman

---

## Sumber Dataset

**Medical Cost Personal Dataset (Insurance Dataset)**

Dataset berisi 1.338 observasi dengan 7 variabel:

| Variabel | Deskripsi                         |
| -------- | --------------------------------- |
| age      | Usia peserta asuransi             |
| sex      | Jenis kelamin                     |
| bmi      | Body Mass Index                   |
| children | Jumlah anak/tanggungan            |
| smoker   | Status merokok                    |
| region   | Wilayah tempat tinggal            |
| charges  | Biaya asuransi kesehatan (target) |

Dataset banyak digunakan sebagai studi kasus regresi dalam machine learning karena memiliki kombinasi variabel numerik dan kategorik.

Sumber dataset:
https://www.kaggle.com/datasets/mirichoi0218/insurance

---

## Cara Menjalankan

### 1. Persiapkan Dataset

Pastikan file dataset **insurance.csv** berada pada folder yang sama dengan notebook **PROJECT_ML.ipynb**.

Struktur folder:

```text
project/
│
├── PROJECT_ML.ipynb
└── insurance.csv
```

### 2. Install Library yang Dibutuhkan

Jalankan perintah berikut pada terminal atau command prompt:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### 3. Jalankan Jupyter Notebook

Buka terminal pada folder project lalu jalankan:

```bash
jupyter notebook
```

Kemudian buka file:

```text
PROJECT_ML.ipynb
```

### 4. Jalankan Seluruh Cell Secara Berurutan

Urutan proses dalam notebook:

1. Import Library
2. Load Dataset
3. Exploratory Data Analysis (EDA)
4. Data Preprocessing

   * Menghapus data duplikat
   * Binary Encoding (`sex`, `smoker`)
   * One-Hot Encoding (`region`)
5. Feature Engineering

   * Membuat fitur `bmi_age`
6. Train-Test Split (80:20)
7. Standardisasi Data untuk KNN
8. Pemodelan:

   * Linear Regression
   * KNN Regressor
   * Random Forest Regressor
   * XGBoost Regressor
9. Evaluasi Model
10. Hyperparameter Tuning Random Forest
11. Analisis Feature Importance

### 5. Output yang Dihasilkan

Notebook akan menghasilkan:

* Statistik deskriptif dataset
* Visualisasi distribusi data
* Heatmap korelasi
* Perbandingan performa model
* Hasil hyperparameter tuning
* Nilai evaluasi MAE, RMSE, dan R²
* Feature importance dari model terbaik

### Konfigurasi yang Digunakan

* Train-Test Split : 80% Training, 20% Testing
* Random State : 42
* Scaling : StandardScaler (khusus KNN)
* Hyperparameter Tuning : GridSearchCV (5-Fold Cross Validation)


### Kesimpulan

* Faktor yang paling memengaruhi biaya asuransi kesehatan adalah status merokok (smoker).
* Variabel age, BMI, dan fitur BMI_Age juga memiliki pengaruh yang cukup besar.
* Random Forest hasil tuning memberikan performa terbaik dibandingkan model lainnya berdasarkan evaluasi MAE, RMSE, dan R².
* Machine learning terbukti mampu digunakan untuk memprediksi biaya asuransi kesehatan dengan baik berdasarkan karakteristik peserta.

---

## Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost

---

## Lisensi

Project ini dibuat untuk keperluan akademik pada mata kuliah Machine Learning Program Studi Statistika Universitas Jenderal Soedirman.
