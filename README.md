# 📚 Finding Similar Book Reviews using Jaccard Similarity

This repository contains the code, report, and data processing workflow for the project:  
**“Finding Similar Book Reviews using Jaccard Similarity”**  
conducted as part of the course *Algorithms for Massive Data* in the Master in Data Science for Economics program at Università degli Studi di Milano.

## 👩‍💻 Author

- Hilal Mente 
- Academic Year 2024/25

## 🧠 Project Description

This project focuses on finding lexically similar book reviews using the **Jaccard Similarity** metric on a scalable subset of the Amazon Books Review dataset.  
Key goals:
- EDA of review length distribution
- Preprocess large-scale review data
- Detect pairs of reviews with overlapping word tokens
- Interpret similarity
- Ensure reproducibility and scalability

## 📊 Dataset

- Source: [Amazon Books Reviews – Kaggle](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews)
- Preprocessing steps include:
  - HTML entity cleaning
  - Unicode normalization
  - Duplicate removal
  - Trimming reviews to ≤ 200 words

## ⚙️ Technologies Used

- Python 3.9
- Libraries: `pandas`, `numpy`, `matplotlib`, `re`, `unicodedata`, `html`
- Notebook: Jupyter (Google Colab compatible)

## 📁 File Structure

```bash
.
├── notebook.ipynb          # Main Jupyter Notebook (Colab-compatible)
├── requirements.txt        # Required Python packages
├── HilalMente_Report.pdf   # Final PDF report
├── top_jaccard_pairs.csv   # Exported table of top 100 Jaccard review pairs
├── distribution_of_review_lengths.png
├── box_plot_of_review_lengths.png
├── cumulative_distribution_of_review_lengths.png
└── README.md