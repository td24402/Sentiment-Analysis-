# Sentiment-Analysis-of-Amazon-Products

This project analyzes customer sentiment using two complementary approaches:

    VADER (Valence Aware Dictionary and sEntiment Reasoner): a rule-based sentiment analysis tool.

    RoBERTa: a transformer-based deep learning model fine-tuned for sentiment classification.

The goal is to compare traditional lexicon-based and modern deep learning-based sentiment scoring techniques to gain insights into how customers feel about products.

# Dataset 

    Source: Amazon fine food product reviews (Reviews.csv)

    Size: 500 reviews (downsampled for efficiency)

Each review includes:

    Text: the full written review

    Score: star rating (1 to 5)

# Project Overview 

# Step	                              Description
Data Preprocessing	          Tokenization, POS tagging, NER using nltk
Sentiment Analysis	          Performed with both VADER and RoBERTa
Visualization	                Sentiment scores vs star ratings
Model Comparison	            Correlation between VADER and RoBERTa
Outlier Inspection	          Most positive/negative mismatches
Toolkits                      Used	nltk, transformers, matplotlib, seaborn, pandas

# Exploritory Data Analysis 

Star ratings are visualized to understand the distribution.

NLTK is used for:

    Tokenization

    Part-of-Speech Tagging

    Named Entity Recognition

# Sentiment Analysis

VADER (Lexicon-Based)

    Built into NLTK

    Provides 4 scores: pos, neu, neg, compound

RoBERTa (Transformer-Based)

    Model: cardiffnlp/twitter-roberta-base-sentiment

    Returns probabilities: roberta_pos, roberta_neu, roberta_neg

# Visualization 

Compound Score vs Review Score (VADER)

VADER Sentiment Breakdown

Model Score Correlation Comparison

# Results 

Correlation:

    RoBERTa is more confident in positive/negative predictions.

    VADER is more conservative, often assigning high neutral scores.

Outlier Examples:

    Most positive review among 1-star ratings (misalignment)

    Most negative review among 5-star ratings

# Key Takeaways

Lexicon-based models like VADER are fast, interpretable, and rule-based — great for quick sentiment snapshots.

Transformer-based models like RoBERTa provide deeper understanding — more accurate for nuanced language.

Combining both helps validate and explore mismatched or unexpected reviews (e.g., sarcastic 5-star or angry 1-star with kind wording).

# Future Improvements 

Fine-tune RoBERTa on domain-specific Amazon review data

Add sarcasm detection layer

Use multi-class classification (positive, neutral, negative)

Incorporate review metadata 

# Ideal Use Cases 

Customer feedback dashboards

Review flagging for moderation

Sentiment-driven product quality insights

