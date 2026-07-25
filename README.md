[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/D94-Q8ry)


# AI-Driven Financial News Sentiment Analysis & Stock Market Prediction

An end-to-end data science project designed to predict stock market trends using historical price data and stock news sentiment analysis.

---

### Project Overview

This repository contains the dataset and Jupyter Notebook for analyzing and forecasting stock trends. The project combines quantitative stock data with market news sentiment to build a predictive model.


### Repository Structure

* **`Stocks Prediction.ipynb`**: Jupyter Notebook containing data preprocessing, Exploratory Data Analysis (EDA), feature engineering, model training, and performance evaluation.
* **`stock_news.csv`**: Dataset containing news headlines, publication dates, and sentiment context used to analyze market sentiment impact.

### Data Preprocessing

The preprocessing pipeline cleans and aligns historical market data with news sentiment data:

* **Text Cleaning & Tokenization**: Processed raw headlines from `stock_news.csv` by removing noise, stop words, and converting text to lowercase.
* **Sentiment Feature Extraction**: Calculated daily sentiment polarity scores (Positive, Negative, Neutral) for news headlines using NLP sentiment analyzers.
* **Feature Scaling & Date Alignment**: Standardized numerical stock metrics (Open, High, Low, Close, Volume) using `MinMaxScaler` and merged them with sentiment scores by date.
* **Sequential Train-Test Split**: Divided the dataset chronologically to preserve the time-series order and prevent data leakage.


### Tech Stack & Requirements

This project relies on Python 3.12+ and key machine learning, deep learning, and NLP libraries:
* Core & Data Handling: numpy==1.26.4, pandas==2.2.2, scipy==1.13.1
* Machine Learning: scikit-learn==1.6.1
* NLP & Text Embeddings: gensim==4.3.3, sentence-transformers==3.4.1, transformers
* Deep Learning Frameworks: torch>=1.11.0, tensorflow / keras
* Visualization: matplotlib, seaborn

 ### Model Pipeline & Workflow

### 1. Data Preprocessing & EDA:

* Handled temporal variables (Date parsed to datetime64).
* Evaluated null values, duplicates, and feature distributions across prices, volume, and labels.
* Performed univariate analysis on sentiment polarity classes.

### 2. Feature Engineering & Text Representation:

* Word2Vec (gensim): Extracted dense word vector representations from news text.
* Sentence Transformers (sentence-transformers): Generated context-aware sentence-level embeddings.
* LLM Summarization / Tokens: Integrated T5 model tokenizer/pipelines for text processing.

### 3. Model Development & Classification:

* Random Forest Classifier (scikit-learn): Non-linear baseline classification on feature matrices.
* Neural Networks (Keras/TensorFlow): Sequential Dense architecture with Dropout regularization for sentiment classification and stock trend modeling.

### 4. Evaluation Metrics:

* Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.

### Conclusion

* Successfully combined quantitative stock metrics with news sentiment analysis to predict market trends.
* Including news sentiment provided better insight into short-term price fluctuations compared to relying on technical indicators alone.
* The analysis demonstrated that significant spikes in negative news headlines correlate strongly with sudden market drops.

### Future Scope

* **Real-Time API Integration**: Connect to live financial and news feeds (e.g., Yahoo Finance, Alpha Vantage) for real-time predictions.
* **Deep Learning Architecture**: Implement specialized time-series architectures like **LSTM** or Transformer models like **FinBERT** for complex textual analysis.
* **Multi-Stock Support**: Extend the framework to analyze multiple tickers and sectors concurrently.
* **Interactive Web App**: Deploy an interactive dashboard using **Streamlit** or **Flask** for dynamic visual backtesting.
