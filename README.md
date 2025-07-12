# Lien_Quan_Mobile_Churn_Analysis_Dashboard
Analyze user churn behavior in Liên Quân Mobile using Google Play reviews. Includes sentiment analysis, churn labeling, EDA with PySpark, and interactive Tableau dashboard. Helps uncover churn reasons and optimize user experience.
##  Dataset
- Source: Crawled using `google_play_scraper`
- Size: 9,000+ user reviews  
- Features:
  - Review content
  - Rating
  - Review date
  - App version
  - Sentiment (generated)
  - Reason (keyword-extracted)
  - Churn label (0 = retained, 1 = churned)
  
## Tools & Technologies

- `Python`: Pandas, NumPy, re, Matplotlib
- `PySpark`: SparkSession, DataFrame API
- `Google Play Scraper`
- `Tableau Public`: interactive dashboard with filters
## Key Steps

1. Data scraping from Google Play
2. Data cleaning & preprocessing
3. Sentiment labeling (rule-based or ML)
4. Churn reason extraction
5. Dashboard creation in Tableau
