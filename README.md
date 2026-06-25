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

1. **Import Library**

   Jalankan cell pertama untuk mengimpor seluruh library yang diperlukan, seperti Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, dan XGBoost.

2. **Memuat Dataset**

   Jalankan cell load dataset untuk membaca file `insurance.csv` menggunakan Pandas dan menampilkan beberapa data awal.

3. **Memahami Struktur Dataset**

   Jalankan cell yang menampilkan:

   * Dimensi dataset (`shape`)
   * Informasi tipe data (`info`)
   * Statistik deskriptif setiap variabel

4. **Eksplorasi Data (EDA)**

   Jalankan seluruh cell EDA untuk:

   * Memeriksa missing value
   * Memeriksa data duplikat
   * Melihat distribusi variabel kategorik
   * Menampilkan histogram
   * Menampilkan boxplot
   * Menampilkan countplot

5. **Preprocessing Data**

   Jalankan cell preprocessing untuk:

   * Menghapus data duplikat
   * Melakukan Binary Encoding pada variabel `sex` dan `smoker`
   * Melakukan One-Hot Encoding pada variabel `region`

6. **Feature Engineering**

   Jalankan cell feature engineering untuk membuat variabel baru `bmi_age` yang merupakan hasil perkalian antara BMI dan usia.

7. **Analisis Korelasi**

   Jalankan cell heatmap korelasi untuk melihat hubungan antar variabel dan mengidentifikasi fitur yang paling berpengaruh terhadap biaya asuransi.

8. **Membagi Data Training dan Testing**

   Jalankan cell train-test split untuk membagi data menjadi:

   * 80% data training
   * 20% data testing

9. **Standardisasi Data**

   Jalankan proses StandardScaler untuk menstandarkan data yang akan digunakan pada model K-Nearest Neighbor (KNN).

10. **Membangun Model Linear Regression**

    Jalankan cell Linear Regression untuk memperoleh nilai MAE, RMSE, dan R² sebagai model baseline.

11. **Membangun Model KNN Regressor**

    Jalankan cell KNN untuk:

    * Menguji nilai K dari 1 hingga 30
    * Menentukan nilai K terbaik menggunakan metode elbow
    * Mengevaluasi performa model

12. **Membangun Model Random Forest**

    Jalankan cell Random Forest Regressor untuk memperoleh hasil prediksi dan nilai evaluasi model.

13. **Membangun Model XGBoost**

    Jalankan cell XGBoost Regressor untuk membandingkan performanya dengan model lainnya.

14. **Mengevaluasi Seluruh Model**

    Jalankan cell evaluasi untuk membandingkan nilai MAE, RMSE, dan R² dari seluruh model yang digunakan.

15. **Hyperparameter Tuning Random Forest**

    Jalankan GridSearchCV untuk mencari kombinasi parameter terbaik pada model Random Forest.

16. **Melatih Ulang Model Terbaik**

    Gunakan parameter terbaik hasil GridSearchCV untuk membangun model Random Forest yang telah dioptimalkan.

17. **Analisis Feature Importance**

    Jalankan cell feature importance untuk mengetahui variabel yang paling berpengaruh dalam memprediksi biaya asuransi kesehatan.

18. **Menarik Kesimpulan**

    Bandingkan seluruh hasil evaluasi model dan tentukan model dengan performa terbaik berdasarkan nilai MAE, RMSE, dan R².


### Kesimpulan

Berdasarkan hasil penelitian, dataset Insurance tidak memiliki missing value dan hanya terdapat satu data duplikat yang dihapus pada tahap preprocessing. Model yang dibangun menggunakan Linear Regression, KNN, Random Forest, dan XGBoost menunjukkan bahwa Random Forest memiliki performa terbaik. Setelah dilakukan hyperparameter tuning dengan GridSearchCV, model Random Forest memperoleh MAE 2.412,31, RMSE 4.203,34, dan R² 0,9039, sehingga mampu menjelaskan 90,39% variasi biaya asuransi kesehatan. Analisis feature importance menunjukkan bahwa variabel smoker, bmi, age, dan bmi_age merupakan faktor yang paling berpengaruh dalam memprediksi biaya asuransi kesehatan.


---

## Tools 

* Python
* Canva
---
