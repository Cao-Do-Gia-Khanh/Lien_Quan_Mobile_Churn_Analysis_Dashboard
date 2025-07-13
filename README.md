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
##  Key Insights from Churn Analytics Dashboard

The following key insights were derived from the interactive Tableau dashboard built for churn analysis of the Liên Quân Mobile app, based on user reviews and metadata:

---

###  1. Churn rate is moderate but worth monitoring
- Total churned users: **3,348**
- Total retained users: **5,713**
- Approximate churn rate: **37%**

While not alarmingly high, this rate signals the need for deeper monitoring, especially among user segments with negative feedback.

---

###  2. Significant churn spike detected on Day 9
- Churned users jumped from **439 (Day 8)** to **2,097 (Day 9)**
- Retained users also spiked from **1,246 to 3,939**

 **Interpretation**: A major product event or update may have occurred around Day 9, potentially introducing new bugs, instability, or dissatisfaction.

---

### 3. Technical and social issues are the main churn drivers
Top reasons associated with churn include:
- `update` → 685 churned users
- `toxic` (negative in-game behavior) → 352 churned users
- `performance` → 340 churned users
- `lag` → 299 churned users
- `matchmaking` → 247 churned users
- `bug` → 205 churned users


 **Actionable insight**: Address both performance/stability issues and community moderation efforts to reduce user attrition.

---

###  4. Strong correlation between negative sentiment and churn
- Most churned users left **negative** reviews.
- Very few churned users had **positive** feedback.

 This suggests that **sentiment analysis is a strong predictor of churn**, and can be used for early churn warnings or risk scoring.

---

###  5. Version 1.59.1.5 has significantly worse retention metrics
| App Version | Churn Rate | % Negative Sentiment |
|-------------|------------|----------------------|
| 1.58.1.2    | ~0.20      | ~25%                 |
| 1.59.1.5    | ~0.40+     | ~60%                 |

 **Interpretation**: The newer version (1.59.1.5) correlates with **twice the churn rate and negative sentiment** → urgent investigation or rollback may be needed.

---

### Summary
This dashboard reveals churn dynamics across time, app versions, user sentiment, and behavioral triggers. Combined insights can guide:
- Product fixes
- UX improvements
- Targeted retention campaigns

> Built with Tableau | Data Source: Google Play Reviews + Enriched Metadata

