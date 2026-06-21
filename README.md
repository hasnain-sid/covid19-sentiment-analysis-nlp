# Comparison of Four Pre-trained Models for Sentiment Analysis on COVID-19 News Headlines

A comparative study benchmarking four sentiment analysis approaches — two transformer-based (**RoBERTa**, **BERT**) and two lexicon/rule-based (**VADER**, **TextBlob**) — on COVID-19 news headlines, evaluated on accuracy, precision, recall, and F1-score.

B.Tech Final Year Research Project · Department of Computer Science & Engineering · Meerut Institute of Engineering and Technology (MIET) · Session 2023–24

---

## Overview

News headlines shape public perception, and during the COVID-19 pandemic they were a primary channel through which people formed opinions about the virus, lockdowns, and vaccines. This project compares how well two transformer-based language models and two simpler rule-based libraries capture sentiment in this kind of short, high-stakes text — and quantifies the trade-off between model complexity and accuracy.

## Problem Statement

Given a COVID-19 news headline, classify its sentiment (positive / negative / neutral) and evaluate which modeling approach — deep transformer-based or lightweight rule-based — performs best for this domain.

## Dataset

- **Source**: A curated dataset of COVID-19 news headlines _(add exact source/size here, e.g. Kaggle dataset name or scraped source, and number of headlines)_
- **Preprocessing**: Text cleaning, normalization, and sentiment label preparation prior to model input.

## Models Compared

| Model | Type | Notes |
|---|---|---|
| **RoBERTa** | Transformer (deep learning) | Robustly Optimized BERT Pretraining Approach |
| **BERT** | Transformer (deep learning) | Bidirectional Encoder Representations from Transformers |
| **VADER** | Lexicon / rule-based | Tuned for social-media-style short text |
| **TextBlob** | Lexicon / rule-based | Lightweight, rule-based polarity scoring |

## Methodology

```
Data Collection → Data Preprocessing → Model Selection → Model Training → Evaluation → Results Comparison → Conclusion
```

Each model was applied to the same preprocessed headline dataset, then evaluated using identical metrics (accuracy, precision, recall, F1-score via `scikit-learn`) for a fair side-by-side comparison.

## Results

| Model | F1 Score | Accuracy |
|---|---|---|
| **RoBERTa** | **80.92%** | **87.85%** |
| BERT | 75.86% | 83.00% |
| TextBlob | 58.00% | 60.00% |
| VADER | 54.00% | 54.00% |

## Key Findings

- Transformer-based models (RoBERTa, BERT) substantially outperformed rule-based models (VADER, TextBlob) on both F1 and accuracy.
- **RoBERTa** achieved the best overall performance, outperforming the strongest rule-based baseline (TextBlob) by roughly **23 points of F1**.
- Rule-based models remain attractive where compute/latency constraints rule out transformer inference, despite the accuracy gap.

## Tech Stack

- **Language**: Python
- **NLP/ML**: Hugging Face Transformers (RoBERTa, BERT), VADER, TextBlob, scikit-learn
- **Data handling**: Pandas, NumPy
- **Environment**: Google Colab

## Repository Structure

```
.
├── notebook/
│   └── sentiment_analysis_covid19.ipynb   # Main analysis notebook
├── data/
│   └── README.md                          # Dataset source/description
├── results/
│   └── classification_reports/            # Per-model sklearn evaluation outputs
├── requirements.txt
└── README.md
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/hasnain-sid/covid19-sentiment-analysis-nlp.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `notebook/sentiment_analysis_covid19.ipynb` in Jupyter or Google Colab and run all cells in order.

## Team & Acknowledgments

This project was completed as a B.Tech Final Year External Practical Exam project (Session 2023–24) at MIET, Meerut, under the guidance of **Prof. Mohd. Shahid**.

**Team members**: Hasnain Akhtar Siddique, Harsh Pratap Tomar, Isha Jindal, Khushi Deewania

## Publication

This work was published as a research paper.

## License

This project is for academic and portfolio purposes.
