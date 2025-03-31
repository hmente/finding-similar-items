# 📚 Finding Similar Book Reviews using Jaccard and TF-IDF

This project was developed for the "Algorithms for Massive Data" course, part of the Master's in Data Science for Economics at the University of Milan (2024/25). The goal is to detect similar book reviews from the Amazon Books dataset using scalable similarity algorithms.

---

## 🔍 Objective

To identify semantically or lexically similar book reviews using two methods:
- **Jaccard Similarity** (token set overlap)
- **TF-IDF Cosine Similarity** (vectorized semantic similarity)

---

## 🗂️ Project Structure
### 📁 root/
### ── FindingSimilarItems.ipynb: Main implementation (Colab compatible)
### ── requirements.txt: Required Python packages
### ── tfidf_similar_pairs.csv
### ── jaccard_vs_tfidf.csv
### ── jaccard_vs_tfidf_plot.png
### ── report.tex: LaTeX source of final report
### ── README.md            # This file

---

## 🧪 Methods

### ✅ Jaccard Similarity
- Based on the intersection-over-union of word tokens
- Simple and efficient for detecting surface-level matches

### ✅ TF-IDF Cosine Similarity
- Captures deeper semantic similarities
- Uses `sklearn` to vectorize reviews and compute pairwise cosine distances

---

## ⚙️ Setup & Usage

1. Clone this repository:
```bash
git clone https://github.com/your-username/finding-similar-reviews.git
cd finding-similar-reviews 
``` 


2. Upload your Kaggle API credentials as kaggle.json::
```bash
mkdir ~/.kaggle
cp kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```

## 📊 Results
- Jaccard and TF-IDF return very different matches
- IDF provides more semantically accurate results
- jaccard_vs_tfidf_plot.png for a comparison scatter plot

## 📝 Report
- The full report is available in the `report.tex` file

## 🧑‍💻 Author

Hilal Mente
Master in Data Science for Economics
University of Milan – 2024/25