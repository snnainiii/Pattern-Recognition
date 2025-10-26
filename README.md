# 🧠 Penerapan Metode GLCM dan SVM untuk Klasifikasi Autism Spectrum Disorder (ASD)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-4285F4?style=for-the-badge&logo=TensorFlow&logoColor=white)

---

## 📘 Deskripsi Singkat  

**Sistem klasifikasi Autism Spectrum Disorder (ASD)** ini menggunakan pendekatan *pattern recognition* dengan dua tahap utama:
1. **Ekstraksi fitur** dari citra MRI menggunakan **GLCM (Gray Level Co-occurrence Matrix)**.  
2. **Klasifikasi** menggunakan **SVM (Support Vector Machine)**.  

Penelitian ini menganalisis perbedaan pola otak antara penderita ASD dan individu kontrol berdasarkan citra MRI dari **ABIDE Dataset (subset OHSU)**.

---

## ⚙️ Tahapan Penelitian  

### 🔹 1. Business Understanding  
Menentukan tujuan klasifikasi citra otak untuk membantu deteksi dini **Autism Spectrum Disorder** secara non-invasif dan efisien.  

### 🔹 2. Data Understanding  
- Dataset: **ABIDE (Autism Brain Imaging Data Exchange)**  
- Subset: **OHSU (Oregon Health & Science University)**  
- Total data: 28 subjek (13 ASD, 15 kontrol)  
- Format: MRI anatomi (3D) dan fMRI resting (4D)

### 🔹 3. Data Preparation  
- Mengambil **3 slice tengah** dari tiap data MRI.  
- Menggunakan **GLCM** dengan jarak = 1 dan sudut = 0°, 45°, 90°, dan 135°.  
- Fitur yang diekstraksi:
  - Contrast  
  - Correlation  
  - Energy  
  - Homogeneity  

### 🔹 4. Modeling  
Model klasifikasi dibangun menggunakan **SVM (Support Vector Machine)** dengan berbagai kernel:
- Linear  
- Polynomial  
- RBF (Radial Basis Function)  
- Sigmoid  

Eksperimen dilakukan dengan **rasio data training dan testing**:
- 90 : 10  
- 80 : 20  
- 70 : 30  

### 🔹 5. Evaluation  
Evaluasi performa menggunakan **Confusion Matrix** dan metrik:
- Accuracy  
- Precision  
- Recall  
- F1-Score  

### 🔹 6. Deployment  
Model digunakan untuk mengidentifikasi ASD berdasarkan citra MRI.  
Output berupa label klasifikasi: **ASD** atau **Normal**.

---

## 🧩 Dataset  

| Jenis Data     | Dimensi       | Jumlah Slice | Total Data |
|----------------|----------------|---------------|-------------|
| MRI Anatomi    | 160×239×200     | 3             | 84          |
| fMRI Resting   | 64×64×36×82     | 3             | 84          |
| **Total Data** | —               | —             | **168 gambar 2D** |

---

## 💻 Teknologi & Tools  

| Kategori | Teknologi |
|-----------|------------|
| Bahasa Pemrograman | Python |
| Library | NumPy, Pandas, OpenCV, Matplotlib, Seaborn, scikit-learn, Nibabel |
| Framework | Google Colab |
| Perangkat Keras | Intel Core i3 (11th Gen), RAM 8 GB |
| Dataset | ABIDE (Autism Brain Imaging Data Exchange) |

---

## 📊 Hasil & Analisis  

- Metode **GLCM** berhasil mengekstraksi fitur tekstur citra MRI otak.  
- Model **SVM** mampu membedakan antara citra ASD dan kontrol dengan akurasi tinggi.  
- Penggabungan data anatomi + resting menghasilkan performa **lebih baik** dibanding data tunggal.  
- Hasil evaluasi stabil pada berbagai rasio pembagian data.  

📈 **Kesimpulan akhir:**  
Metode **GLCM + SVM** efektif untuk klasifikasi ASD berbasis citra MRI dengan tingkat akurasi yang baik dan potensi aplikasi medis yang tinggi.

---

## 🧠 Kesimpulan  

1. **GLCM** memberikan fitur tekstur signifikan dari citra MRI.  
2. **SVM** terbukti andal sebagai algoritma klasifikasi berbasis fitur GLCM.  
3. Kombinasi keduanya dapat digunakan untuk **diagnosis dini ASD secara non-invasif**.  
4. Hasil klasifikasi menunjukkan perbedaan nyata antara struktur otak penderita ASD dan individu normal.  

---

## 📚 Referensi  

1. W. Yin, S. Mostafa, F. X. Wu (2021) — *CNN and GCN for Autism Diagnosis*  
2. F. Z. Subah et al. (2021) — *Deep Learning with ABIDE Dataset*  
3. S. Raj, S. Masood (2020) — *Comparison of SVM, RF, KNN, GB, ANN for ASD Classification*  
4. ABIDE Official Dataset Documentation  

---

## 🧩 Keyword  

`GLCM` • `SVM` • `Autism Spectrum Disorder` • `MRI` • `Pattern Recognition` • `Machine Learning` • `Feature Extraction`

---

## 👩‍💻 Author  

**Siti Nur Aini**  
📍 Teknik Informatika, Universitas Trunojoyo Madura  
📧 [stnuraini@gmail.com](mailto:stnuraini082@gmail.com)

---
