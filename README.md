# Social-Media-Sentiment-Analysis-
Classified 1,500 brand tweets using TextBlob NLP across 8 brands; achieved ~70% accuracy vs human labels and surfaced brand reputation insights across 12 visualizations.

# 📱 Social Media Sentiment Analysis — Twitter Brand Sentiment

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![TextBlob](https://img.shields.io/badge/TextBlob-NLP-blueviolet)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Evaluation-F7931E?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![openpyxl](https://img.shields.io/badge/openpyxl-Excel%20Dashboard-217346)
![Level](https://img.shields.io/badge/Level-Intermediate-yellow)

---

## 📌 Project Overview

This project analyzes brand perception on Twitter for **8 major consumer brands** using NLP. TextBlob sentiment scoring classifies 1,500 tweets as Positive, Negative, or Neutral, with evaluation against human-labeled ground truth. Results are visualized per brand and exported to an Excel dashboard.

**Business Question:** What do customers say about top brands on social media — and which brands have the strongest and weakest sentiment profiles?

---

## 📂 Project Structure

```
social media/
│
├── twitter_brand_sentiment.csv              # Dataset — 1,500 tweets, 8 columns
├── Social_Media_Sentiment_Analysis.ipynb    # 18-cell analysis notebook
└── README.md
```

---

## 📊 Dataset

| Attribute | Details |
|---|---|
| **Source** | Twitter Brand Sentiment — Kaggle-style synthetic dataset |
| **Records** | 1,500 tweets |
| **Brands** | Netflix, Tesla, Nike, Apple, Samsung, Google, Amazon, Microsoft |
| **File** | `twitter_brand_sentiment.csv` |

**Columns:** `tweet_id`, `date`, `brand`, `tweet`, `sentiment_label` (ground truth), `likes`, `retweets`, `user_followers`

**Ground truth distribution:** Positive: 672 | Negative: 466 | Neutral: 362

---

## 🎯 Project Objectives

1. Apply TextBlob NLP to classify tweets as Positive / Negative / Neutral
2. Evaluate TextBlob accuracy against human-labeled `sentiment_label` column
3. Analyze sentiment distribution per brand
4. Identify top words in positive and negative tweets (word frequency)
5. Compare engagement (likes, retweets) by sentiment
6. Build an Excel dashboard summarizing brand reputation scores

---

## 🔧 Tools & Technologies

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| pandas | Data manipulation and aggregation |
| TextBlob | Sentiment polarity scoring (threshold: >0.1 = Positive, <−0.1 = Negative) |
| scikit-learn | Confusion matrix, classification report |
| Matplotlib | Sentiment charts, confusion matrix heatmap |
| Seaborn | Brand-level bar charts |
| collections.Counter | Word frequency analysis |
| openpyxl | Excel dashboard generation |
| Jupyter Notebook | 18-cell analysis |

---

## 📈 Analysis Workflow (18 Cells)

| Cell | Description |
|---|---|
| 1 | Library imports |
| 2 | Dataset loading and preview |
| 3 | Data cleaning — remove URLs, mentions, special characters |
| 4 | TextBlob sentiment scoring with polarity thresholds |
| 5 | Overall sentiment distribution |
| 6 | Sentiment by brand (grouped bar) |
| 7 | Top 20 words — positive tweets |
| 8 | Top 20 words — negative tweets |
| 9 | Word Cloud — positive tweets |
| 10 | Word Cloud — negative tweets |
| 11 | Engagement analysis (likes/retweets by sentiment) |
| 12 | Monthly sentiment trend |
| 13 | Top 20 most-liked positive tweets |
| 14 | Top 20 most-liked negative tweets |
| 15 | Negative word frequency analysis |
| 16 | Stacked sentiment % per brand (100% bar) |
| 17 | Confusion matrix (TextBlob vs ground truth) |
| 18 | Project summary and key insights |

---

## 📊 Visualizations (12 Charts)

| # | Fig | Chart Type | Insight |
|---|---|---|---|
| 1 | Fig 1 | Donut chart | Overall sentiment distribution — Positive / Negative / Neutral |
| 2 | Fig 2 | Grouped bar | Sentiment breakdown by brand |
| 3 | Fig 3 | Bar chart | Average polarity score by brand |
| 4 | Fig 4 | Line chart | Monthly sentiment trend over time |
| 5 | Fig 5 | Histogram | Polarity score distribution across all tweets |
| 6 | Fig 6 | Bar chart | Average engagement (likes + retweets) by sentiment |
| 7 | Fig 7 | Heatmap | Positive tweet count — Brand × Month |
| 8 | Fig 8 | Scatter | Polarity vs Subjectivity per tweet |
| 9 | Fig 9 | Bar chart | Top 20 words in positive tweets |
| 10 | Fig 10 | Bar chart | Top 20 words in negative tweets |
| 11 | Fig 11 | 100% stacked bar | Sentiment share per brand |
| 12 | Fig 12 | Heatmap | Confusion matrix — ground truth label vs TextBlob prediction |

---

## 🔍 Key Findings (Verified from Dataset + TextBlob)

**Dataset ground truth:**
| Sentiment | Count |
|---|---|
| Positive | 672 (44.8%) |
| Negative | 466 (31.1%) |
| Neutral | 362 (24.1%) |

**TextBlob predictions (computed):**
| Sentiment | Count |
|---|---|
| Positive | 750 (50.0%) |
| Neutral | 453 (30.2%) |
| Negative | 297 (19.8%) |

**TextBlob accuracy against ground truth: 70.1%**

**8 Brands analyzed:** Netflix, Tesla, Nike, Apple, Samsung, Google, Amazon, Microsoft

- Negative tweets generate significantly more engagement — negative feedback spreads faster
- **TextBlob accuracy is 70.1%** — acceptable for rapid brand monitoring, not for clinical/legal use
- The confusion matrix (Cell 17) shows TextBlob over-predicts Neutral vs the ground truth labels

---

## 💡 Brand Strategy Recommendations

1. **Real-time sentiment monitoring** — negative spikes unaddressed within 24h become PR risks
2. **Engage high-follower positive tweets** — amplify organic advocates cheaply
3. **TextBlob is suitable for quick monitoring only** — for higher-stakes decisions, use a fine-tuned transformer (BERT/RoBERTa)
4. Brands with <40% positive sentiment need immediate customer experience intervention
5. Word frequency analysis reveals specific pain points — "slow", "wait" point to fulfillment/service issues

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn textblob scikit-learn openpyxl

# Download TextBlob corpora (run once)
python -c "import nltk; nltk.download('punkt'); nltk.download('averaged_perceptron_tagger')"

jupyter notebook Social_Media_Sentiment_Analysis.ipynb
```

---

## 👤 Author

**[ABITHA ]** | [LinkedIn](https://www.linkedin.com/in/abitha-s-105663399?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) | [GitHub](https://github.com/AbithaSenthil)

