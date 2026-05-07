# Arabic News Classification

An NLP assignment for CS365 at IMSIU. The goal is to automatically classify Arabic news articles into predefined categories using traditional machine learning models. A Gradio interface was also built to allow real-time classification.

---

## What This Project Does

Given an Arabic news article, the model predicts which category it belongs to. Three classifiers were trained and compared to find the best performer.

Categories: Health, Economy, Politics, Culture, Sports, Religion, Technology, Other

---

## Dataset

The NADCG dataset was used, which contains 4,000 Arabic news articles collected from various Arabic news sources, each labelled with one of the 8 categories above.

The dataset is not included in this repo. You will need to download it separately.

---

## Approach

**Preprocessing:**
- Removed punctuation, stop words, and diacritics
- Normalised Arabic character variations
- Normalised whitespace

**Feature Extraction:**
- TF-IDF vectorisation with up to 5,000 features (unigrams and bigrams)
- Handcrafted features: article length and unique word count
- Feature selection using Chi-Square, keeping the top 2,000 features

**Models Trained:**
- Support Vector Machine (SVM)
- Random Forest
- Naive Bayes

The data was split 80% training and 20% testing.

---

## Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| SVM | 86.88% | 87.17% | 86.88% | 86.97% |
| Random Forest | 69.87% | 71.87% | 69.87% | 70.34% |
| Naive Bayes | 61.75% | 86.87% | 61.75% | 66.08% |

SVM was the best-performing model. When tested on 10 new articles, it correctly classified 9 out of 10.

---

## Gradio Interface

An interactive web interface was built using Gradio. You can paste any Arabic news article, and the app will return the predicted category, a confidence score, and key extracted keywords in real time.

---
CS365 — Natural Language Processing | Dr. Amal AlSaif | IMSIU
