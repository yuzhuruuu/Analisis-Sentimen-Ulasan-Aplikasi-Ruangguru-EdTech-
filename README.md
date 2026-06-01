# Sentiment Analysis of Ruangguru App Reviews (EdTech NLP Project)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge\&logo=tensorflow\&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge\&logo=scikit-learn\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge\&logo=pandas\&logoColor=white)

---

## Project Overview

This project implements a **Natural Language Processing (NLP) pipeline** to analyze and classify user sentiment from **Ruangguru app reviews** on the Google Play Store.

Using a dataset of **10,000+ user reviews**, the system classifies sentiment into:

* **Positive**
* **Neutral**
* **Negative**

The project combines **data scraping, preprocessing, feature engineering, and machine learning/deep learning models**, achieving model accuracy above **92%**.

---

## Objectives

* Extract insights from user-generated reviews in the EdTech domain
* Build a robust sentiment classification system for Indonesian text
* Compare traditional Machine Learning and Deep Learning approaches
* Deliver a reproducible NLP pipeline for real-world applications

---

## Dataset

* Source: Google Play Store (Ruangguru App)
* Total Data: **10,000+ reviews**
* Language: Indonesian
* Characteristics:

  * Real-world noisy text
  * Informal language & slang
  * Class imbalance (handled in preprocessing)

---

## Methodology

### 1. Data Collection

* Scraped **15,000+ reviews** using `google-play-scraper`

### 2. Text Preprocessing

* Case folding
* Cleaning (URL, emoji, punctuation, noise removal)
* Stopwords removal (customized **Sastrawi dictionary**)
* Preserving negation words (*tidak, bukan*) to maintain sentiment context
* Duplicate removal

### 3. Feature Engineering

* **TF-IDF Vectorization** (for ML models)
* **Word Embedding** (for Deep Learning)

### 4. Handling Imbalanced Data

* Applied **Random Over Sampling** on training data

---

## Modeling & Performance

| Scheme | Model                   | Feature   | Split | Accuracy        |
| ------ | ----------------------- | --------- | ----- | --------------- |
| 1      | Logistic Regression     | TF-IDF    | 80:20 | **>93%**        |
| 2      | Multinomial Naive Bayes | TF-IDF    | 70:30 | ~89%            |
| 3      | Deep Learning (GAP)     | Embedding | 80:20 | **>94% (Best)** |

### Best Model

Deep Learning model using **Global Average Pooling** achieved:

* High accuracy (>94%)
* Stable validation performance
* Reduced overfitting via **dropout layers**

---

## Repository Structure

```text id="g4k91s"
├── scraping_dataset.py       # Script for scraping Play Store reviews
├── notebook_pelatihan.ipynb  # Main notebook (EDA, preprocessing, modeling)
├── dataset_ruangguru.csv     # Raw dataset (>10K rows)
└── requirements.txt          # Project dependencies
```

---

## How to Run

### 1. Clone Repository

```bash id="r2jsl1"
git clone https://github.com/username-github-kamu/analisis-sentimen-ruangguru.git
cd analisis-sentimen-ruangguru
```

### 2. Install Dependencies

```bash id="g5k2pa"
pip install -r requirements.txt
```

### 3. (Optional) Scrape New Data

```bash id="k92ms1"
python scraping_dataset.py
```

### 4. Run Notebook

Open `notebook_pelatihan.ipynb` using:

* Jupyter Notebook, or
* Google Colab (recommended)

---

## Key Highlights

* ✅ Real-world dataset (10K+ reviews)
* ✅ Custom Indonesian NLP preprocessing
* ✅ Multi-model comparison (ML vs DL)
* ✅ High accuracy (>94%)
* ✅ End-to-end pipeline (scraping → modeling)

---

## Future Improvements

* Deploy as web app (Streamlit / Gradio)
* Add real-time sentiment API
* Expand dataset with multi-platform reviews
* Fine-tune Transformer models (IndoBERT)

---

## Author

**Annisa Yusri Nur Rochmah**
Information Systems — Universitas Negeri Semarang (UNNES)

**Interests:**
Artificial Intelligence • Machine Learning • NLP • LLMs • Predictive Analytics

---

## 📌 Conclusion

This project demonstrates that combining **data preprocessing, feature engineering, and appropriate model selection** can produce highly accurate sentiment classification systems for Indonesian text.

The Deep Learning approach outperformed traditional models, proving its effectiveness for handling complex linguistic patterns in real-world user reviews.
