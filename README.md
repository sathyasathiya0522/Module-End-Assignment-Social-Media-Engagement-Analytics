# 📊 Social Media Engagement Analytics Using Python

## 📌 Project Overview

Social media platforms generate large amounts of engagement data such as likes, comments, shares, impressions, watch time, and engagement rates.

This project analyzes a social media engagement dataset using Python to understand content performance, user behavior, engagement patterns, device usage, and sentiment.

The project covers **data cleaning, data transformation, exploratory data analysis (EDA), statistical analysis, visualization, and insight generation**.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Clean and preprocess social media engagement data
- Handle missing values and duplicate records
- Perform exploratory data analysis using Pandas
- Perform statistical analysis using NumPy and Pandas
- Create new features for deeper analysis
- Visualize engagement patterns using Matplotlib and Seaborn
- Create interactive visualizations using Plotly
- Identify important content and user engagement trends
- Generate meaningful business insights

---

## 📂 Dataset

**Dataset Name:** `social_media_engagement_5000.csv`

The dataset contains **5,000 social media records**.

Some of the important features include:

- `user_id`
- `age`
- `gender`
- `country`
- `post_id`
- `post_type`
- `post_category`
- `likes`
- `comments`
- `shares`
- `watch_time_sec`
- `impression_count`
- `posted_at`
- `follower_count`
- `is_verified`
- `device_type`
- `sentiment`
- `hashtags`
- `engagement_rate`

---

## 🛠️ Tools & Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly

---

## 🧹 Data Cleaning

The following data-cleaning operations were performed:

- Checked missing values using `isnull()` and `isna()`
- Filled missing numerical values using the **median**
- Filled missing categorical values using the **mode**
- Checked and removed duplicate records
- Converted `posted_at` to datetime format
- Standardized gender labels
- Standardized sentiment labels
- Checked likes, comments, and shares for unrealistic negative values
- Extracted hashtag counts

---

## 🔧 Feature Engineering

Additional features were created to improve the analysis.

### Engagement Score

The total direct engagement for each post was calculated as:

```python
df['engagement_score'] = (
    df['likes'] +
    df['comments'] +
    df['shares']
)
```

### Hashtag Count

A new `hashtag_count` column was created from the hashtags associated with each post.

### Log Impressions

A log-transformed version of impressions was created using:

```python
df['log_impressions'] = np.log1p(df['impression_count'])
```

Additional features such as **age group** and **posting hour** were also created for final analysis.

---

## 🔍 Exploratory Data Analysis

The following Pandas operations were used:

- `head()`
- `tail()`
- `shape`
- `columns`
- `info()`
- `dtypes`
- `describe()`
- `value_counts()`
- `unique()`
- `nunique()`
- `groupby()`
- Correlation analysis

GroupBy analysis was performed across:

- Post Type
- Post Category
- Country
- Sentiment
- Age Group
- Device Type
- Verification Status

---

## 📈 Statistical Analysis

Descriptive statistics were calculated for:

- Likes
- Comments
- Shares
- Watch Time
- Engagement Rate
- Follower Count

The following statistical measures were analyzed:

- Mean
- Median
- Mode
- Standard Deviation
- Variance
- 25th Percentile
- 50th Percentile
- 75th Percentile
- Skewness
- Kurtosis

---

## 📊 Data Visualization

More than **8 visualizations** were created during the analysis.

### Matplotlib

1. Scatter Plot — Likes vs Impressions
2. Line Chart — Daily Engagement Trend
3. Bar Chart — Posts by Category
4. Pie Chart — Gender Distribution
5. Histogram — Age Distribution
6. Box Plot — Engagement Rate

### Seaborn

7. Count Plot — Post Type
8. Bar Plot — Average Likes by Post Category
9. Violin Plot — Followers vs Sentiment
10. Pair Plot — Numeric Features
11. Heatmap — Correlation Matrix
12. Swarm Plot — Engagement vs Device Type

### Plotly

13. Interactive Scatter Plot — Likes vs Impressions

The Plotly visualization also included post type, engagement score, category, country, and sentiment information.

---

## 💡 Key Findings

### 📱 Content Performance

- **Video** was the highest-performing post type with an average engagement score of approximately **12,664.59**.
- **Music** was the best-performing content category with an average engagement score of approximately **12,788.55**.
- **Brazil** recorded the highest average engagement rate at approximately **1.54**.

### 👥 User Trends

- Users aged **31–40** achieved the highest average engagement score of approximately **12,938.50**.
- The **51–60** age group recorded the lowest average engagement among the analyzed age groups.
- Verified accounts recorded higher average engagement rates and impressions.
- Non-verified accounts recorded a slightly higher average engagement score.

### 📲 Behavioral Insights

- **Mobile** users recorded the highest average watch time at approximately **4,087.83 seconds**.
- Tablet users recorded approximately **3,979.74 seconds**.
- Desktop users recorded approximately **3,974.79 seconds**.
- A meaningful best posting time could not be determined because the dataset did not contain varying time-of-day values in `posted_at`.

### 😊 Sentiment Analysis

- **Negative-sentiment posts** recorded the highest average engagement score at approximately **12,731.50**.
- Negative posts also had the highest average engagement rate at approximately **1.0385**.
- Positive posts generated the highest average impressions at approximately **50,248.11**.
- Neutral posts had the lowest average engagement score at approximately **12,448.16**.

---

## 🏁 Conclusion

The **Social Media Engagement Analytics** project demonstrates how Python can be used to clean, transform, analyze, and visualize real-world social media data.

The analysis identified meaningful differences in engagement across **post types, content categories, countries, age groups, account verification status, device types, and sentiment**.

The results indicate that video and music content performed strongly, users aged 31–40 showed high engagement, mobile users generated the highest average watch time, and sentiment was also associated with differences in engagement.

These insights can support data-driven social media content planning and engagement strategies.

---

## 📁 Project Files

```text
Social-Media-Engagement-Analytics/
│
├── social_media_engagement_5000.csv
├── Social_Media_Engagement_Analytics.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

1. Open the notebook in **Google Colab** or **Jupyter Notebook**.
2. Upload `social_media_engagement_5000.csv`.
3. Install/import the required Python libraries.
4. Run the notebook cells sequentially.
5. Review the outputs, visualizations, and final insights.

---

## 📚 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
```

---

## 👨‍💻 Project Type

**Python for Data Analysis — Module End Assignment**

**Project:** Social Media Engagement Analytics
