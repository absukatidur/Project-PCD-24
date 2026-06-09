# Analisis Pengaruh Teknik Preprocessing terhadap Klasifikasi Ginjal Normal dan Batu Ginjal Menggunakan Fitur Gray Level Co-occurrence Matrix (GLCM) serta Perbandingan Algoritma Support Vector Machine (SVM), Random Forest, dan K-Nearest Neighbor (KNN)

## Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis pengaruh berbagai teknik preprocessing terhadap performa klasifikasi citra CT Scan ginjal normal dan batu ginjal. Fitur tekstur citra diekstraksi menggunakan metode **Gray Level Co-occurrence Matrix (GLCM)**, kemudian dilakukan klasifikasi menggunakan tiga algoritma machine learning, yaitu **Support Vector Machine (SVM)**, **Random Forest**, dan **K-Nearest Neighbor (KNN)**.

---

## Dataset
**Dataset:** CT Kidney Dataset: Normal, Cyst, Tumor and Stone
**Link Dataset:**
https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone

### Label yang Digunakan
* Normal
* Stone (Batu Ginjal)

### Jumlah Data

| Kelas  | Jumlah Citra |
| ------ | ------------ |
| Normal | 100          |
| Stone  | 100          |
| Total  | 200          |

---

## Tahapan Preprocessing
Empat skenario preprocessing yang digunakan dalam penelitian ini adalah:

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

### Fitur GLCM yang Digunakan
* Contrast
* Correlation
* Energy
* Homogeneity
* Dissimilarity
* ASM (Angular Second Moment)

---

## Metode Klasifikasi
Penelitian ini membandingkan performa tiga algoritma machine learning:
1. Support Vector Machine (SVM)
2. Random Forest
3. K-Nearest Neighbor (KNN)

---

## Alur Penelitian
```text
Dataset CT Scan Ginjal
        ↓
    Preprocessing
        ↓
Ekstraksi Fitur GLCM
        ↓
Pembentukan Dataset Fitur
        ↓
Klasifikasi
(SVM, Random Forest, KNN)
        ↓
Evaluasi Performa
(Accuracy, Precision, Recall, F1-Score)
```

---

## Evaluasi Model
Performa model dievaluasi menggunakan metrik berikut:
* Accuracy
* Precision
* Recall
* F1-Score

Hasil evaluasi digunakan untuk:
1. Mengetahui pengaruh setiap teknik preprocessing terhadap kualitas fitur GLCM.
2. Membandingkan performa algoritma SVM, Random Forest, dan KNN.
3. Menentukan kombinasi preprocessing dan algoritma terbaik untuk klasifikasi ginjal normal dan batu ginjal.
