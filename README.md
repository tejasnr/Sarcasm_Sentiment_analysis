# Sarcasm-Aware Sentiment Analysis for Steam Reviews

This project implements a sophisticated sarcasm detection system specifically designed for Steam game reviews. It combines traditional NLP techniques with gaming-specific features to identify sarcastic reviews.

## Features

- Advanced sarcasm detection using multiple heuristics
- Gaming-specific pattern recognition
- Sentiment analysis integration
- Multiple machine learning models comparison
- Comprehensive text preprocessing
- Feature extraction tailored for gaming context

## Setup

1. Install the required dependencies:
```bash
pip install -r requirements.txt
```

2. Download NLTK data (this will be done automatically when running the code)

3. Prepare your dataset:
   - Name your dataset file as `steam_reviews.csv`
   - Place it in the same directory as the notebook
   - Ensure it has the required columns (see Dataset section)

## Usage

1. Open and run the Jupyter notebook:
```bash
jupyter notebook sarcasm_analysis.ipynb
```

2. The notebook will:
   - Load Steam reviews dataset
   - Identify sarcastic reviews using sophisticated heuristics
   - Preprocess the text data
   - Extract advanced features
   - Train and compare multiple ML models
   - Show example predictions

## Dataset

The code expects a CSV file named `steam_reviews.csv` with the following columns:
- date_posted: The date when the review was posted
- funny: Number of users who found the review funny
- helpful: Number of users who found the review helpful
- hour_played: Number of hours the reviewer played the game
- is_early_access_review: Whether the review was made during early access
- recommendation: Whether the reviewer recommends the game ("Recommended" or "Not Recommended")
- review: The actual review text

Example row:
```csv
date_posted,funny,helpful,hour_played,is_early_access_review,recommendation,review
2017-04-02,0,0,0,TRUE,Not Recommended,Pretty much same controls and buggy mess as all the other battle royale games.
```

## Models

The system compares three different models:
1. Naive Bayes
2. Logistic Regression
3. Random Forest

The best performing model is automatically selected based on F1-score.

## Features Extracted

- Basic text statistics (word count, character count, etc.)
- Capitalization patterns
- Punctuation patterns
- Sentiment scores
- Gaming-specific patterns
- Contradiction patterns
- And many more...

## Output

The system provides:
- Detailed preprocessing statistics
- Model performance metrics
- Example predictions
- Feature importance analysis
- Sarcasm detection explanations

## Contributing

Feel free to contribute to this project by:
1. Opening issues for bugs or feature requests
2. Submitting pull requests with improvements
3. Adding more gaming-specific patterns
4. Improving the documentation # Sarcasm_Sentiment_analysis
