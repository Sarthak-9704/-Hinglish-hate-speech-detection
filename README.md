# -Hinglish-hate-speech-detection

A Natural Language Processing project focused on detecting hate speech in **Hinglish**—a code-mixed language of Hindi and English, written in the Roman script

##  Project Overview

In today's social media landscape, users often communicate in regional languages using the English alphabet. This poses challenges for hate speech detection due to:

- Low-resource language data
- Code-mixing
- Non-standard vocabulary

Our project explores both conventional and deep learning-based NLP approaches to identify hate speech in Hinglish tweets using various features and embedding methods.

## Literature Insight

- Addressed challenges in NLP for Indian low-resource languages
- Evaluated performance of various classical and transformer-based models
- Benchmarked models using multiple datasets and vectorization methods

## Datasets Used

1. **Hate Speech Tweets Dataset**  
   ~4500 annotated tweets (1661 hateful, 2918 non-hateful)  
   [🔗 Link](https://github.com/victor7246/Hinglish_Hate_Detection/blob/2ada87ccff36841c73e75a3ed7651be498839422/data/raw/Hate-speech-dataset/hate_speech.tsv)

2. **Hinglish Profanity Lexicon**  
   ~200 profane words with severity scores (1–10)  
   [🔗 Link](https://github.com/pmathur5k10/Hinglish-Offensive-Text-Classification/blob/68d6d6eacfc2b53530764b48faea532ffeba5d45/Hinglish_Profanity_List.csv)

## Methodology

### 🔹 Preprocessing
- Lowercasing, removal of URLs, mentions, special characters
- Annotating with profanity scores (sum, max, presence, count)

### 🔹 Non-Semantic Models (TF-IDF + Lexicon)
- Logistic Regression
- Multinomial Naive Bayes
- Random Forest

### 🔹 Semantic Models (Embeddings + Lexicon)
- Word2Vec + MLP
- XGBoost with Embeddings
- Fine-tuned **Multilingual BERT**
- **CNN-BiLSTM** with FastText Embeddings

### Evaluation Metrics
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**

## Key Findings

- Transformer-based models (Multilingual BERT) outperformed traditional methods.
- Lexicon features improved performance, but were limited by general profanity focus instead of hate-specific context.
- CNN-BiLSTM underperformed, likely due to small dataset size and static embeddings.

## Results Summary

- Best F1-Score: Multilingual BERT
- Notable gap between semantic and non-semantic models
- Lexicon-based methods worked well in conjunction with embeddings
