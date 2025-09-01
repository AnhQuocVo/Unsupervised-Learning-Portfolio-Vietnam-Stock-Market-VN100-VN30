Dựa trên nội dung bạn cung cấp, tôi sẽ viết lại file **README.md** hoàn chỉnh theo phong cách **professional, súc tích, không icon, không màu mè**, đúng chuẩn cho một project nghiên cứu.

---

# Unsupervised Learning Portfolio: Vietnam Stock Market (VN100)

## Introduction

This project applies Unsupervised Learning techniques to analyze the Vietnam stock market (VN100). The objective is to cluster stocks, uncover hidden patterns, and support data-driven investment decisions. By grouping stocks with similar characteristics, investors can identify outperforming clusters, diversify portfolios, and enhance risk management.

### Significance

* Discover latent structures in the VN100 universe
* Support systematic portfolio construction
* Enable quantitative insights for investment strategies

---

## Project Workflow

### 1. Data Collection

* **Sources**: TradingView (VN100 components), Yahoo Finance (historical data), Fama-French Factors (via `pandas_datareader`)
* **Features Used**: Price, volume, RSI, Bollinger Bands, ATR, MACD, dollar volume (liquidity proxy), rolling returns, Fama-French factor exposures

### 2. Data Preprocessing

* **Cleaning**: Remove missing values, filter stocks with sufficient history
* **Aggregation**: Convert daily to monthly frequency, filter top 150 most liquid stocks
* **Feature Engineering**: Compute rolling returns, technical indicators, factor betas
* **Normalization**: Standardize features for clustering

### 3. Model Application

* **Clustering Algorithms**: K-Means (custom centroids based on RSI), Hierarchical Clustering (optional), PCA for dimensionality reduction
* **Portfolio Construction**: Select high-momentum clusters (e.g., RSI \~70), optimize weights using Efficient Frontier (PyPortfolioOpt)

### 4. Model Evaluation

* **Metrics**: Silhouette Score for cluster quality
* **Visualization**: Cluster scatter plots (RSI vs. returns), portfolio cumulative returns vs. VN100 benchmark

### 5. Final Output

* **Clusters**: Number and characteristics (momentum, volatility, factor exposure)
* **Insights**: Identification of outperforming clusters and diversification benefits
* **Portfolio Performance**: Strategy returns compared to VN100 Buy & Hold

---

## Mathematical Formulas

**Normalization (Z-score)**

$$
z = \frac{x - \mu}{\sigma}
$$

**Min-Max Scaling**

$$
x' = \frac{x - x_{min}}{x_{max} - x_{min}}
$$

**Euclidean Distance (K-Means)**

$$
d(x, y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}
$$

**Principal Component Analysis (PCA)**

$$
C = \frac{1}{n-1} (X - \bar{X})^T (X - \bar{X})
$$

$$
C v = \lambda v
$$

**Silhouette Score**

$$
s(i) = \frac{b(i) - a(i)}{\max(a(i), b(i))}
$$

---

## Results

### Key Findings

* **Clusters Identified**: 4 distinct groups based on technical and fundamental features
* **Momentum Cluster**: High-RSI stocks (\~70) demonstrated persistent outperformance
* **Portfolio Performance**: Unsupervised strategy outperformed VN100 Buy & Hold in backtesting

### Visualization Highlights

| Cluster | Avg RSI | Avg Return | Liquidity | Factor Exposure |
| ------- | ------- | ---------- | --------- | --------------- |
| 0       | 30      | Low        | High      | Defensive       |
| 1       | 45      | Moderate   | Moderate  | Balanced        |
| 2       | 55      | Moderate   | Moderate  | Value           |
| 3       | 70      | High       | High      | Momentum        |

---

## Usage

Clone the repository and run the notebook to reproduce results. Ensure required dependencies are installed.

---

## References

* PyPortfolioOpt
* scikit-learn
* Yahoo Finance
* Fama-French Data Library
*

## Contact

For questions or collaboration, please open an issue or contact the repository owner.


## Disclaimer

This project is for educational and research purposes only. Past performance does not guarantee future results. Invest responsibly.


Bạn có muốn tôi viết thêm **Installation & Requirements** (Python version, thư viện `requirements.txt`) để README này có thể dùng luôn cho GitHub repo không?
