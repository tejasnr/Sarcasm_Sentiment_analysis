# 🎮 Steam Game Reviews Sentiment Analysis

**Author:** Tejas NR  
**Date:** June 2025

## 📌 Project Summary

This project focuses on performing binary sentiment analysis on Steam game reviews using two models:

- 🧠 **TF-IDF + Logistic Regression** (Classical ML approach)
- 🤖 **DistilBERT** (Transformer-based deep learning)

The goal is to classify each review as either **Recommended** (Positive) or **Not Recommended** (Negative), and to compare the performance, interpretability, and strengths of each approach.

---

## 📂 Dataset Details

- **Source:** `steam_reviews.csv`  
- **Total Records:** 19,931  
- **Labels:**  
  - `1` → Recommended  
  - `0` → Not Recommended

---

## 🧹 Preprocessing

### Common Steps:
- Lowercasing all text
- Removing special characters and digits
- Removing stopwords
- Tokenization

### TF-IDF Pipeline:
- Used `TfidfVectorizer` with `ngram_range=(1, 3)`
- Removed terms with very low document frequency
- Max features limited to 15,000

### BERT Pipeline:
- Tokenized using `DistilBertTokenizer`
- Truncated to `max_length=256`
- Encoded into PyTorch Dataset

---

## 🧪 Model Training

### Logistic Regression:
- TF-IDF Vectorizer + GridSearchCV tuning
- Best ROC AUC: **0.9149**
- Accuracy: **84.8%**

### DistilBERT:
- Fine-tuned on 13,951 samples with 4 epochs
- Final Test ROC AUC: **~0.9194**
- Accuracy: **88.5%**

---

## 📊 Performance Metrics

| Metric          | Logistic Regression | DistilBERT |
|-----------------|---------------------|------------|
| Accuracy        | 84.8%               | 88.5%      |
| ROC AUC         | 91.49%              | 91.94%     |
| Precision       | 91% (pos)           | 91.1%      |
| Recall          | 87% (pos)           | 92.79%     |
| F1 Score        | 89% (pos)           | 91.94%     |

---

## 📈 Visualizations

- 📌 Word Clouds for Positive and Negative Sentiment
- 🔠 Top 20 Words by Coefficient in Logistic Regression
- 🤖 Confusion Matrix for both models
- 📉 Error Distribution Plots
- 📊 Model Performance Comparison Charts

---

## 💡 Observations

- **Logistic Regression** is interpretable, performs well, and is fast to train.
- **DistilBERT** outperforms LR in overall accuracy and F1, especially for subtle reviews.
- Logistic Regression struggles more with nuanced or sarcastic language.
- Transformer-based models capture contextual meaning better but require GPU and more training time.

---

## 🚀 How to Run

1. Clone the repository  
   `git clone https://github.com/your-repo/steam-sentiment-analysis.git`

2. Install dependencies  
   `pip install -r requirements.txt`

3. Run notebooks in order:
   - `notebooks/data_preprocessing.ipynb`
   - `notebooks/logistic_regression_pipeline.ipynb`
   - `notebooks/distilbert_training.ipynb`

4. Explore visualizations and metrics

---

## 🧰 Tech Stack

- Python 3.10
- Scikit-learn
- Pandas, Matplotlib, Seaborn
- HuggingFace Transformers
- PyTorch + CUDA (GPU support)
- Google Colab / Jupyter

---

## 🧠 Future Work

- Use more advanced models like RoBERTa, XLNet
- Incorporate multi-class sentiment labels (e.g., Neutral)
- Real-time sentiment API integration
- Include sarcasm and humor detection

---

## 📜 License

This project is open-sourced for educational purposes under the MIT License.

---

