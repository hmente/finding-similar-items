# 🚀 Scalable Detection of Similar Book Reviews Using MinHash and Locality-Sensitive Hashing (LSH)

This repository contains the implementation of a scalable system for detecting similar book reviews in large datasets using **MinHash signatures** and **Locality-Sensitive Hashing (LSH)**. The system is designed to efficiently identify lexically similar texts without performing exhaustive pairwise comparisons.

## 📚 Dataset

The dataset used is the **Amazon Books Review Dataset**, retrieved via the Kaggle API. Each review includes text content, rating, and metadata.

## 🎯 Objective

To detect potentially redundant or near-duplicate reviews by approximating pairwise Jaccard similarity in a scalable manner.

---

## 🔧 Methodology

1. **Text Cleaning & Preprocessing**:
   - Lowercasing
   - Removal of punctuation
   - Optional filtering of short reviews

2. **Shingling**:
   - Character-level shingling with `k=5` is used to convert each review into a set of substrings (shingles).

3. **MinHashing**:
   - Each set of shingles is converted into a MinHash signature using multiple hash functions.
   - Signatures reduce dimensionality while preserving similarity structure.

4. **LSH Bucketing**:
   - Signatures are divided into bands and hashed into buckets.
   - Only review pairs falling into the same bucket in any band are considered candidate matches.

5. **Jaccard Evaluation**:
   - For a selected subset of LSH-detected pairs, the **true Jaccard similarity** is computed and compared to evaluate LSH accuracy.

---

## 📊 Results Summary

- The system identified thousands of highly similar review pairs in under a minute, even for datasets with over 60,000 entries.
- Manual and automatic evaluations showed that many detected pairs had a true Jaccard similarity > 0.98.
- The system avoids expensive \( O(n^2) \) comparisons while maintaining high precision for near-duplicate review detection.

---

## 📂 Project Structure

```bash
├── data/
│   └── amazon_books.csv                # Original dataset (not included)
├── main_analysis.ipynb                 # Jupyter notebook with full pipeline
├── evaluation_top5.csv                 # Sample evaluation of top-matched pairs
├── report.pdf                          # Project report in LaTeX (if applicable)
└── README.md
