#  Credit Card Anomaly Detection

This project implements an anomaly detection system using univariate Gaussian modeling to identify fraudulent credit card transactions. It includes full preprocessing, visualization, density-based anomaly detection, and evaluation using confusion matrix and F2-score.

 Features:
- Univariate Gaussian anomaly detection
- KDE-based feature selection
- Log transformation of skewed features
- Time decomposition into day/hour/minute
- Evaluation using Accuracy, Precision, Recall, F2-Score, and MCC
- Visualizations: histograms, KDE plots, confusion matrices

 Repository Structure:
- creditcardanomaly.csv          # Dataset file
- anomaly_detection.ipynb        # Jupyter notebook with full pipeline
- requirements.txt               # Python dependencies
- README.md                      # Project overview

 How to Run:
git clone https://github.com/Indhusrikrishnaraj/credit-card-anomaly-detection.git && cd credit-card-anomaly-detection
pip install -r requirements.txt
jupyter notebook anomaly_detection.ipynb

 Preprocessing Highlights:
- Handled large file size and memory usage via `psutil` and `gc`
- Applied log transformation to `Amount`
- Dropped irrelevant features like `Time`, `Second`, `Day`
- Decomposed time to derive `Hour`, improved interpretability
- Selected features via domain knowledge and KDE comparison

 Data Summary:
- Total records: 284,807
- Features: 30
- Class distribution: Extremely imbalanced
- Train: Only normal (class 0)
- Validation/Test: Balanced with fraud (class 1)

 Model Performance:
- Optimal epsilon (ε): 0.009
- F2-Score: 0.81
- Confusion Matrix plotted using Seaborn
- Accuracy: 99.67%
- Precision: 79.8%
- Recall: 82.1%
- F1-Score: 80.9%
- MCC: 0.808

 Libraries Used:
- numpy, pandas — Data handling
- seaborn, matplotlib, plotly — Visualization
- scikit-learn — Train/test split
- psutil, time, os, gc — System monitoring
- tqdm — Progress bars

 Future Improvements:
- Extend to multivariate Gaussian modeling
- Real-time fraud detection with Streamlit/Flask
- Add SHAP explainability for interpretability

 Notes:
- Runs locally on Jupyter
- Compatible with Python 3.10
- Notebook: `anomaly_detection.ipynb`

