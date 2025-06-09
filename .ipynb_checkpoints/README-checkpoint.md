Sentiment Classifier for Steam Game Reviews (Optimized for Apple Metal)
This notebook implements a sentiment classification system that labels Steam game reviews as positive or negative. It demonstrates a complete pipeline, from data loading and preprocessing to model training, evaluation, and visualization.

Key Features:
Dual-Model Approach: Compares a traditional machine learning model (TF-IDF + Logistic Regression) against a state-of-the-art fine-tuned transformer (BERT).

Direct Labeling: Uses the review's "Recommended" / "Not Recommended" status as the ground truth for sentiment, providing clear positive/negative labels.

Comprehensive Evaluation: Assesses models using Accuracy, Precision, Recall, and F1-score.

Insightful Visualizations: Generates a confusion matrix to analyze model predictions and word clouds to discover the most prominent terms in positive and negative reviews.

Metal GPU Acceleration: The PyTorch code is configured to use Apple's Metal Performance Shaders (MPS) for a significant speed-up on M1/M2/M3 GPUs.

Pipeline Overview:
Data Loading & Labeling: Load the dataset and use the recommendation column to create positive/negative labels.

Data Preparation: Create a smaller, balanced dataset for efficient training.

Model Training: Train both a Logistic Regression and a BERT model.

Evaluation: Compare the models using standard classification metrics.

Visualization: Plot the confusion matrix, word clouds, and BERT training progress.