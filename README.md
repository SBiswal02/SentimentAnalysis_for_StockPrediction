# Sentiment Analysis for Stock Prediction

A project that combines sentiment analysis of financial news with technical indicators to predict stock price movements using multiple algorithms including Bi-LSTM, SVM, and Random Forest and the comparision of them.

## 🔍 Overview

This project implements the following steps to stock price prediction:

1. **News Scraping**: Automatically collecting financial news from Google News for specific stocks
2. **Sentiment Analysis**: Using NLTK's VADER sentiment analyzer to extract sentiment scores from news headlines and snippets
3. **Technical Analysis**: Computing various technical indicators (CCI, RSI, EVM, Force Index)
4. **Machine Learning**: Training multiple models to predict stock price movements

## ✨ Features

- **Automated News Collection**: Scrapes Google News for real-time financial news
- **Sentiment Analysis**: Extracts sentiment scores using VADER lexicon
- **Technical Indicators**: Implements CCI, RSI, EVM, and Force Index calculations
- **Multiple ML Models**: 
  - Bidirectional LSTM for time series prediction
  - Support Vector Machine (SVM) for classification
  - Random Forest Regressor for regression
- **Data Visualization**: Comprehensive plotting and analysis tools
- **Performance Metrics**: Detailed accuracy and error measurements


## Prerequisites
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- keras
- nltk
- yfinance
- beautifulsoup4
- requests
- lxml


## 🤖 Models

### 1. Bidirectional LSTM (Bi-LSTM)
- **Purpose**: Time series prediction using sentiment and price data
- **Architecture**: Bidirectional LSTM layers with dropout
- **Features**: Price data + sentiment scores
- **Performance**: 89.65% accuracy, MAE: 18.17

### 2. Support Vector Machine (SVM)
- **Purpose**: Binary classification (price up/down)
- **Features**: Open-Close and High-Low price differences
- **Performance**: 62.75% accuracy, MAE: 0.75

### 3. Random Forest Regressor
- **Purpose**: Regression-based price prediction
- **Features**: All available price data (Open, High, Low, Close, Volume)
- **Performance**: 99.29% accuracy, MAE: 1.79

## 📊 Data Sources

### News Data
- **Source**: Google News
- **Stocks**: AAPL, AMZN, MSFT, META
- **Fields**: Date, Ticker, URL, Headline, Source, Snippet

### Stock Data
- **Source**: Yahoo Finance (via yfinance)
- **Period**: 2021-2022
- **Fields**: Open, High, Low, Close, Volume, Adj Close

### Technical Indicators
- **CCI**: Commodity Channel Index
- **RSI**: Relative Strength Index
- **EVM**: Ease of Movement
- **Force Index**: Volume-based momentum indicator

## 📈 Results

### Model Performance Comparison

| Model | Accuracy | MAE | Use Case |
|-------|----------|-----|----------|
| Bi-LSTM | 89.65% | 18.17 | Time series with sentiment |
| SVM | 62.75% | 0.75 | Binary classification |
| Random Forest | 99.29% | 1.79 | Price regression |
