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

### 1. Clone Repository

```bash
git clone https://github.com/username/nama-repository.git
cd nama-repository
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### 3. Jalankan Notebook / Script

Jika menggunakan Jupyter Notebook:

```bash
jupyter notebook
```

Buka file notebook dan jalankan seluruh cell secara berurutan.

Atau jika menggunakan Python Script:

```bash
python main.py
```

### 4. Tahapan Pemrosesan

1. Load dataset
2. Exploratory Data Analysis (EDA)
3. Encoding variabel kategorik
4. Feature Engineering (BMI_Age)
5. Scaling data
6. Split data train-test (80:20)
7. Training model
8. Hyperparameter tuning
9. Evaluasi model
10. Analisis feature importance

---

## Ringkasan Hasil

### Hasil EDA

* Dataset tidak memiliki missing value.
* Ditemukan 1 data duplikat yang dihapus pada tahap preprocessing.
* Variabel charges memiliki distribusi right-skewed.
* Mayoritas peserta merupakan non-perokok.
* Variabel smoker menunjukkan hubungan paling kuat terhadap biaya asuransi kesehatan.

### Feature Engineering

Dibuat fitur baru:

```text
BMI_Age = BMI × Age
```

Fitur ini menunjukkan korelasi yang cukup kuat terhadap biaya asuransi kesehatan.

### Modeling

Model yang diuji:

* Linear Regression
* KNN Regression
* Random Forest Regressor
* XGBoost Regressor

### Hyperparameter Tuning

Dilakukan tuning pada Random Forest menggunakan GridSearchCV dengan:

* n_estimators = 100, 200, 300
* max_depth = 3, 4, 5
* min_samples_split = 2, 5, 10
* min_samples_leaf = 1, 2, 4

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
