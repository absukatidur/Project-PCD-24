# Analisis Pengaruh Teknik Preprocessing terhadap Klasifikasi Ginjal Normal dan Batu Ginjal Menggunakan Fitur Gray Level Co-occurrence Matrix (GLCM) serta Perbandingan Algoritma Support Vector Machine (SVM), Random Forest, dan K-Nearest Neighbor (KNN)

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis pengaruh berbagai teknik preprocessing terhadap performa klasifikasi citra CT Scan ginjal normal dan batu ginjal menggunakan fitur tekstur **Gray Level Co-occurrence Matrix (GLCM)**. Fitur tekstur citra diekstraksi menggunakan metode GLCM, kemudian dilakukan klasifikasi menggunakan tiga algoritma machine learning, yaitu **Support Vector Machine (SVM)**, **Random Forest**, dan **K-Nearest Neighbor (KNN)**.

Selain membandingkan performa algoritma klasifikasi, penelitian ini juga bertujuan untuk mengetahui pengaruh berbagai teknik preprocessing terhadap kualitas fitur tekstur yang dihasilkan serta akurasi klasifikasi citra ginjal.

---

## Dataset

**Dataset:** CT Kidney Dataset: Normal, Cyst, Tumor and Stone

**Link Dataset:**  
https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone

### Label yang Digunakan

* Normal
* Stone (Batu Ginjal)

### Jumlah Data

| Kelas | Jumlah Citra |
|--------|--------|
| Normal | 100 |
| Stone | 100 |
| **Total** | **200** |

---

## Tahapan Preprocessing

Penelitian ini menggunakan satu skenario baseline dan empat skenario preprocessing.

### Baseline

* Grayscale

### P1

* Grayscale
* Resize

### P2

* Grayscale
* Resize
* Median Filter
* Histogram Equalization

### P3

* Grayscale
* Resize
* CLAHE (Contrast Limited Adaptive Histogram Equalization)
* Sharpening

### P4

* Grayscale
* Resize
* Median Filter
* CLAHE (Contrast Limited Adaptive Histogram Equalization)
* Thresholding

---

## Metode Ekstraksi Fitur

Fitur tekstur citra diekstraksi menggunakan metode **Gray Level Co-occurrence Matrix (GLCM)**.

### Parameter GLCM

* Distance = 1
* Sudut 0°
* Sudut 45°
* Sudut 90°
* Sudut 135°

### Fitur GLCM yang Digunakan

* Contrast
* Homogeneity
* Dissimilarity
* Entropy
* ASM (Angular Second Moment)
* Energy
* Correlation

### Jumlah Fitur

* 7 fitur × 4 sudut
* Total = 28 fitur

---

## Metode Klasifikasi

Penelitian ini membandingkan performa tiga algoritma machine learning.

### Support Vector Machine (SVM)

SVM digunakan untuk mencari hyperplane terbaik yang mampu memisahkan kelas Normal dan Stone secara optimal.

### Random Forest

Random Forest merupakan metode ensemble learning yang menggunakan banyak decision tree untuk meningkatkan akurasi dan stabilitas klasifikasi.

### K-Nearest Neighbor (KNN)

KNN melakukan klasifikasi berdasarkan kedekatan jarak antar data dengan mempertimbangkan sejumlah tetangga terdekat.

---

## Alur Penelitian

```text
Dataset CT Scan Ginjal
          ↓
      Preprocessing
(Baseline, P1, P2, P3, P4)
          ↓
  Ekstraksi Fitur GLCM
       (28 fitur)
          ↓
   Dataset Fitur (CSV)
          ↓
      Klasifikasi
SVM | Random Forest | KNN
          ↓
        Evaluasi
 Accuracy
 Precision
 Recall
 F1-Score
 CV-5Fold
          ↓
      Analisis Hasil
```

---

## Evaluasi Model

Performa model dievaluasi menggunakan metrik berikut.

### Accuracy

Mengukur persentase prediksi yang benar terhadap seluruh data.

### Precision

Mengukur ketepatan model dalam mengidentifikasi citra batu ginjal.

### Recall

Mengukur kemampuan model dalam menemukan seluruh citra batu ginjal yang ada pada dataset.

### F1-Score

Mengukur keseimbangan antara Precision dan Recall.

### 5-Fold Cross Validation (CV-5Fold)

Digunakan untuk mengukur stabilitas dan kemampuan generalisasi model dengan membagi dataset menjadi lima bagian pengujian secara bergantian.

### Tujuan Evaluasi

1. Mengetahui pengaruh setiap teknik preprocessing terhadap kualitas fitur GLCM.
2. Membandingkan performa algoritma SVM, Random Forest, dan KNN.
3. Menentukan kombinasi preprocessing dan algoritma terbaik untuk klasifikasi ginjal normal dan batu ginjal.
4. Mengukur stabilitas model menggunakan metode Cross Validation.

---

## Output Penelitian

Output yang dihasilkan pada penelitian ini meliputi:

* Dataset fitur hasil ekstraksi GLCM dalam format CSV.
* Hasil klasifikasi menggunakan SVM, Random Forest, dan KNN.
* Nilai Accuracy, Precision, Recall, dan F1-Score.
* Nilai 5-Fold Cross Validation (CV-5Fold).
* Grafik perbandingan performa algoritma klasifikasi.
* Analisis pengaruh preprocessing terhadap hasil klasifikasi.
* Penentuan kombinasi preprocessing dan algoritma terbaik.