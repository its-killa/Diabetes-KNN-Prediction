# 🩺 Diabetes Prediction with K-Nearest Neighbors (KNN)

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange?style=flat-square&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-green?style=flat-square&logo=pandas)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

> Proyek machine learning untuk memprediksi apakah seorang pasien menderita diabetes berdasarkan fitur-fitur medis menggunakan algoritma **K-Nearest Neighbors (KNN)**.

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Methodology](#-methodology)
- [Results](#-results)
- [How to Run](#-how-to-run)
- [Technologies Used](#-technologies-used)

---

## 📌 Overview

Diabetes adalah salah satu penyakit kronis yang paling umum di dunia. Proyek ini membangun **model klasifikasi biner** untuk memprediksi risiko diabetes berdasarkan data medis pasien.

**Target variabel:**
- `0` → Tidak Diabetes
- `1` → Diabetes

---

## 📦 Dataset

Dataset yang digunakan adalah **Pima Indians Diabetes Database** dari National Institute of Diabetes and Digestive and Kidney Diseases.

| Info | Detail |
|------|--------|
| Sumber | [Kaggle - UCI ML Repository](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) |
| Jumlah sampel | 768 |
| Jumlah fitur | 8 |
| Target | `Outcome` (biner: 0 atau 1) |

**Deskripsi Fitur:**

| Fitur | Deskripsi |
|-------|-----------|
| `Pregnancies` | Jumlah kehamilan |
| `Glucose` | Kadar glukosa plasma (mg/dL) |
| `BloodPressure` | Tekanan darah diastolik (mm Hg) |
| `SkinThickness` | Ketebalan lipatan kulit trisep (mm) |
| `Insulin` | Kadar insulin serum 2 jam (mu U/ml) |
| `BMI` | Indeks massa tubuh (kg/m²) |
| `DiabetesPedigreeFunction` | Fungsi riwayat diabetes keluarga |
| `Age` | Usia (tahun) |

---

## 🗂 Project Structure

```
diabetes-knn-prediction/
│
├── diabetes_knn_prediction.ipynb   # Notebook utama (EDA + Modeling)
├── diabetes.csv                    # Dataset
└── README.md                       # Dokumentasi proyek
```

---

## 🔬 Methodology

```
1. Load & Explore Data
        ↓
2. Identifikasi nilai tidak valid (0 pada kolom medis)
        ↓
3. Data Cleaning → Imputasi dengan mean
        ↓
4. Feature Scaling → StandardScaler
        ↓
5. Train-Test Split (67% / 33%, stratified)
        ↓
6. KNN Training → Mencari K optimal (K=1 hingga K=14)
        ↓
7. Evaluasi → Confusion Matrix & Classification Report
```

---

## 📊 Results

| Metrik | Nilai |
|--------|-------|
| Algoritma | KNN |
| K Optimal | 7 |
| Accuracy | ~80% |
| Dataset Split | 67% train / 33% test |

**Key Findings:**
- **Glucose** adalah fitur dengan korelasi tertinggi terhadap outcome diabetes
- Ditemukan missing values tersirat (nilai 0 pada kolom medis) pada 5 kolom
- Model KNN K=7 memberikan keseimbangan terbaik antara bias dan varians

---

## 🚀 How to Run

### 1. Clone repository
```bash
git clone https://github.com/username/diabetes-knn-prediction.git
cd diabetes-knn-prediction
```

### 2. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Jalankan notebook
```bash
jupyter notebook diabetes_knn_prediction.ipynb
```

---

## 🛠 Technologies Used

| Library | Kegunaan |
|---------|----------|
| `Pandas` | Manipulasi dan analisis data |
| `NumPy` | Operasi numerik |
| `Matplotlib` | Visualisasi data |
| `Seaborn` | Visualisasi statistik |
| `Scikit-learn` | Preprocessing, modeling, evaluasi |

---

## 🔮 Future Improvements

- [ ] Perbandingan dengan model lain (Random Forest, SVM, XGBoost)
- [ ] Menangani class imbalance menggunakan SMOTE
- [ ] Hyperparameter tuning dengan GridSearchCV
- [ ] Cross-validation (k-fold) untuk evaluasi yang lebih robust
- [ ] Deploy model sebagai REST API menggunakan Flask/FastAPI

---

## 👤 Author

**Akilla Ayuwandewi Putri Edyra**  
📧 akillaayuwandewi11@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/username) | [GitHub](https://github.com/username)

---

## 📄 License

This project is licensed under the MIT License.
