# Steam Reviews Sarcasm Detection

This project implements a sarcasm detection system for Steam game reviews using machine learning and natural language processing techniques.

## Features

- Sarcasm detection using both traditional ML (Naive Bayes) and deep learning (BERT)
- Gaming-specific feature engineering
- Advanced text preprocessing
- Sentiment analysis integration
- Support for both text and behavioral features

## Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Prepare your data:
   - Place your Steam reviews dataset in the root directory as `steam_reviews.csv`
   - Required columns: date_posted, funny, helpful, hour_played, is_early_access_review, recommendation, review

3. Run the analysis:
   - Open `sarcasm_analysis.ipynb` in Jupyter Notebook
   - Run all cells in sequence

## Dataset Format

The system expects a CSV file with the following columns:
- `date_posted`: Review posting date
- `funny`: Number of funny votes
- `helpful`: Number of helpful votes
- `hour_played`: Hours played
- `is_early_access_review`: Early access flag
- `recommendation`: "Recommended" or "Not Recommended"
- `review`: Review text content

## Models

1. **Naive Bayes with TF-IDF**
   - Traditional ML approach
   - Fast training and inference
   - Good baseline performance

2. **BERT-based Model**
   - Deep learning approach
   - Better understanding of context
   - Gaming-specific fine-tuning

## Features Used

- Text-based features (TF-IDF, n-grams)
- Gaming-specific patterns
- Sentiment analysis scores
- Behavioral signals (funny votes, helpful votes)
- Text style analysis (capitalization, punctuation)

## Output

The system provides:
- Sarcasm detection results
- Model performance metrics
- Visualization of results
- Example predictions

## Model Performance

Performance metrics include:
- Accuracy
- F1-Score
- Precision
- Recall

Best model and its performance metrics are saved in the `best_model` directory.

## License

MIT License
