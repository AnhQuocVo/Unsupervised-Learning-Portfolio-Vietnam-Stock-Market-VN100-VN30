# Unsupervised Learning Portfolio: Vietnam Stock Market (VN100&VN30)

## Introduction
This project applies Unsupervised Learning techniques to analyze the Vietnam stock market (VN100 & VN30). The objective is to cluster stocks, uncover hidden patterns, and support data-driven investment decisions. By grouping stocks with similar characteristics, investors can identify outperforming clusters, diversify portfolios, and enhance risk management.
### Significance
* Discover latent structures in the VN100 universe
* Support systematic portfolio construction
* Enable quantitative insights for investment strategies


## Project Workflow

### 1. Data Collection

* **Sources**: TradingView (VN100&VN30 components), Yahoo Finance (historical data), Fama-French Factors (via `pandas_datareader`)
* **Features Used**: Price, volume, RSI, Bollinger Bands, ATR, MACD, dollar volume (liquidity proxy), rolling returns, Fama-French factor exposures

### 2. Data Preprocessing

* **Cleaning**: Remove missing values, filter stocks with sufficient history
* **Aggregation**: Convert daily to monthly frequency, filter most liquid stocks
* **Feature Engineering**: Compute rolling returns, technical indicators, factor betas
* **Normalization**: Standardize features for clustering

### 3. Model Application

* **Clustering Algorithms**: K-Means (custom centroids based on RSI)
* **Portfolio Construction**: Select high-momentum clusters (RSI >= 70), optimize weights using Efficient Frontier (PyPortfolioOpt)

### 4. Model Evaluation

* **Metrics**: Silhouette Score for cluster quality
* **Visualization**: Cluster scatter plots (RSI vs. returns), portfolio cumulative returns vs. VN100/VN30 benchmark

### 5. Final Output

* **Clusters**: Number and characteristics (momentum, volatility, factor exposure)
* **Insights**: Identification of outperforming clusters and diversification benefits
* **Portfolio Performance**: Strategy returns compared to VN100 Buy & Hold

---

## Results
![VN100](assets/image.png)
![VN30](assets/image-1.png)
