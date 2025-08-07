# 📰 Yahoo News Topic Modeling using NLP

> A Social Media Analytics project exploring unsupervised NLP techniques (LDA, NMF, LSA) to extract hidden topics from over 1,000 Yahoo News articles, deployed via an interactive Streamlit app.

## 📌 Overview

This project applies **topic modeling** techniques on a corpus of Yahoo News articles to uncover dominant themes. Using NLP and unsupervised learning methods, we clean, process, and analyze article text using:

- 🧠 **Latent Dirichlet Allocation (LDA)**
- 🔎 **Non-negative Matrix Factorization (NMF)**
- 📚 **Latent Semantic Analysis (LSA)**

An interactive **Streamlit app** was built to visualize topic-word relationships and allow users to explore the topics and related articles.

---

## 🗂️ Contents

- [Project Overview](#-overview)
- [Tech Stack](#-tech-stack)
- [Data Collection](#-data-collection)
- [Preprocessing](#-preprocessing)
- [Topic Modeling](#-topic-modeling)
- [Evaluation](#-evaluation)
- [Streamlit App](#-streamlit-app)
- [Results](#-results)
- [Future Work](#-future-work)
- [How to Run](#-how-to-run)
- [Team](#-team)

---

## 💻 Tech Stack

- Python 🐍
- NLP: NLTK, scikit-learn
- Topic Modeling: gensim, sklearn
- Visualization: matplotlib, seaborn, wordcloud
- Web App: Streamlit
- Web Scraping: newspaper3k

---

## 📰 Data Collection

- Scraped **1126 articles** from [Yahoo News](https://news.yahoo.com) using `newspaper3k`.
- Each article includes:
  - Title
  - Text
  - URL

---

## 🧹 Preprocessing

Performed using a custom `clean_text` function:

- Lowercasing
- Removing punctuations and special characters
- Stopword removal (NLTK)
- Tokenization
- Lemmatization

---

## 🧠 Topic Modeling

We applied and compared the following models:

| Model | Description |
|-------|-------------|
| **LDA** | Probabilistic model that assumes words are generated from a set of latent topics. |
| **NMF** | Matrix factorization-based model that identifies additive combinations of topic features. |
| **LSA** | Uses SVD to find patterns in term-document matrices. |

Each model produced its top 5 topics, which were visualized using bar charts and word clouds.

---

## 📊 Evaluation

We used the following metrics to evaluate topic quality:

- **Perplexity** (for LDA)
- **Topic Coherence**
- **Interpretability**
- **Diversity**
- **Inconsistency**

**NMF** achieved the best balance of coherence and interpretability.

---

## 🌐 Streamlit App

An interactive app was developed that allows users to:

- Select a topic modeling method (LDA, NMF, or LSA)
- View the top topic terms
- Browse associated news articles
- Explore word clouds for each topic

> 📌 Run it locally using the command:
```bash
streamlit run app.py

