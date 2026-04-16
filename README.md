# Customer Segmentation and Product Recommendations in E-Commerce

A comprehensive machine learning project that combines customer segmentation with personalized product recommendations to enhance e-commerce business intelligence and customer experience.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements advanced machine learning techniques to:

1. **Segment customers** based on purchasing behavior, demographics, and engagement patterns
2. **Generate personalized product recommendations** for each customer segment
3. **Provide actionable insights** for targeted marketing and sales strategies

By combining clustering algorithms with recommendation systems, this solution helps e-commerce businesses:
- Increase customer lifetime value
- Improve marketing ROI through targeted campaigns
- Enhance customer experience with relevant product suggestions
- Identify high-value customer segments for retention strategies

## ✨ Features

- **Customer Segmentation**: 
  - RFM (Recency, Frequency, Monetary) analysis
  - K-Means clustering for behavioral segmentation
  - Demographic-based profiling
  - Visualization of customer segments

- **Product Recommendations**:
  - Collaborative filtering
  - Content-based filtering
  - Hybrid recommendation approach
  - Personalized recommendations per segment

- **Analytics & Insights**:
  - Segment profiling and characterization
  - Purchase pattern analysis
  - Churn prediction capabilities
  - Business metrics visualization

- **Data Visualization**:
  - Interactive dashboards
  - Segment distribution charts
  - Recommendation performance metrics
  - Customer behavior heatmaps

## 📁 Project Structure

```
Customer-Segmentation-and-Product-Recommendations-in-E-Commerce/
├── README.md
├── requirements.txt
├── data/
│   ├── raw/                 # Original datasets
│   ├── processed/           # Cleaned and preprocessed data
│   └── sample_data/         # Sample datasets for testing
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_customer_segmentation.ipynb
│   ├── 04_product_recommendations.ipynb
│   └── 05_analysis_results.ipynb
├── src/
│   ├── __init__.py
│   ├── data_preprocessing.py
│   ├── segmentation.py
│   ├── recommendations.py
│   ├── visualization.py
│   └── utils.py
├── models/                  # Saved model files
├── results/                 # Output files and reports
└── tests/                   # Unit tests
```

## 🚀 Installation

### Prerequisites
- Python 3.8+
- pip or conda

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/Ambar103/Customer-Segmentation-and-Product-Recommendations-in-E-Commerce.git
cd Customer-Segmentation-and-Product-Recommendations-in-E-Commerce
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

## 💻 Usage

### Running the Full Pipeline

```python
from src.data_preprocessing import preprocess_data
from src.segmentation import CustomerSegmentation
from src.recommendations import RecommendationEngine

# Load and preprocess data
data = preprocess_data('data/raw/customer_data.csv')

# Customer Segmentation
segmentation = CustomerSegmentation(n_clusters=4)
customer_segments = segmentation.fit_predict(data)

# Product Recommendations
recommender = RecommendationEngine(method='hybrid')
recommendations = recommender.recommend(data, customer_segments)
```

### Jupyter Notebooks

Navigate through the analysis step-by-step:

```bash
jupyter notebook notebooks/
```

Start with `01_data_exploration.ipynb` and follow sequentially.

## 📊 Dataset

### Expected Data Format

**Customer Data**: CSV file with columns
- `customer_id`: Unique customer identifier
- `purchase_history`: Array of product IDs purchased
- `total_spent`: Total monetary value
- `purchase_frequency`: Number of transactions
- `last_purchase_date`: Most recent purchase date
- `demographic_features`: Age, location, etc.

**Product Data**: CSV file with columns
- `product_id`: Unique product identifier
- `category`: Product category
- `price`: Product price
- `attributes`: Product features/specifications

### Sample Data

Sample datasets are provided in `data/sample_data/` for testing and demonstration purposes.

## 🔬 Methodology

### Customer Segmentation

1. **Data Preparation**: Cleaning, handling missing values, feature scaling
2. **RFM Analysis**: Calculate Recency, Frequency, Monetary metrics
3. **Clustering**: Apply K-Means algorithm to identify natural customer groups
4. **Profiling**: Characterize each segment with key attributes

### Product Recommendations

1. **Collaborative Filtering**: Find similar customers and recommend products they liked
2. **Content-Based Filtering**: Recommend products similar to user's purchase history
3. **Hybrid Approach**: Combine both methods for optimal results
4. **Ranking**: Score and rank recommendations by relevance

## 📈 Results

Model performance metrics include:
- Silhouette Score for clustering quality
- Precision, Recall, F1-Score for recommendations
- Customer segment characteristics and sizes
- Recommendation coverage and diversity

- <img width="1111" height="581" alt="Screenshot 2026-04-16 190939" src="https://github.com/user-attachments/assets/2a67ff4d-dd11-43a4-b63e-e7861e9da716" />
<img width="1109" height="577" alt="Screenshot 2026-04-16 190930" src="https://github.com/user-attachments/assets/1ad8ba30-3aa5-48c7-9647-f2b06317eeea" />



Detailed results are available in the `results/` directory with visualizations and analytics.

## 🤝 Contributing

Contributions are welcome! Please feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

For questions or suggestions, please open an issue on the repository or contact the project maintainer.

---

**Last Updated**: 2026-04-16 13:37:05
