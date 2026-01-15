# Beats by Dre — Consumer Insights Data Analytics (Capstone)

This project analyzes **Amazon customer reviews** for **Beats Studio+ Buds** and multiple competitor earbuds to uncover actionable consumer insights.  
It combines **data cleaning + EDA + sentiment analysis (TextBlob)** and **Gemini AI-powered insight generation** to identify key pleasure points, pain points, and strategic recommendations.

---

## 📌 Project Goals

- Understand customer sentiment and product feedback for **Beats Studio+ Buds**
- Compare Beats against top competing earbuds
- Identify recurring themes driving positive vs negative reviews
- Generate product + marketing recommendations based on real customer voice

---

## 📊 Dataset

- Reviews collected from **Amazon.com**
- Products include Beats Studio+ Buds + competitors such as Apple AirPods Pro, Bose QuietComfort, Sony WF-1000, Sennheiser Momentum, JBL, OnePlus, Skullcandy, etc.
- Reviews were collected using the **OxyLabs API** (ASIN-based extraction)
- Data was exported and merged into a consolidated dataset for analysis

> ⚠️ Note: Amazon review data may not be included in this repo publicly.  
> You can add your own extracted review files and run the notebook end-to-end.

---

## 🔎 What This Project Does

### ✅ 1) Data Cleaning
- Fill missing values (example: author/product attributes)
- Remove duplicates
- Outlier handling (helpful count filtering)
- Convert categorical columns like `is_verified` → numeric
- Save cleaned data into `cleaned_data.csv`

### ✅ 2) Exploratory Data Analysis (EDA)
- Summary statistics for ratings and review distribution
- Visualization of average ratings across products
- Histogram of ratings for Beats Studio+ Buds
- Descriptive statistics (mean, median, variance, etc.)

### ✅ 3) Sentiment Analysis (TextBlob)
- Score polarity from review text
- Classify each review into:
  - `positive`
  - `neutral`
  - `negative`
- Build a product-wise sentiment summary table
- Compute a “positivity index” and rank products
- Generate word clouds for:
  - all Beats reviews
  - positive Beats reviews

### ✅ 4) AI-Generated Insights (Gemini API)
Using Gemini (`gemini-1.5-flash`), this project generates:
- Sentiment breakdown summary for Beats reviews
- Key pain points from negative reviews
- Pleasure points from high-performing competitor products
- Competitor positioning overview

---

## ⭐ Key Insights (High-Level)

### Beats Studio+ Buds — Strengths
- Strong **sound quality**
- Good **noise cancellation**
- Positive feedback on **design and connectivity**

### Beats Studio+ Buds — Pain Points
- **Microphone / call quality issues**
- **Battery life reliability**
- **Comfort and fit**
- Missing premium features (wireless charging, customization)
- **Price sensitivity** compared to competitor feature sets

### Competitor Trends
Top-performing competitors excel in:
- Premium ANC performance
- Multipoint connectivity
- Custom EQ + feature depth
- Long battery life + strong charging case reliability

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- TextBlob (sentiment polarity)
- WordCloud
- Gemini API (`google.generativeai`)

---

## 🔑 Gemini API Setup (Optional)

Some sections use Gemini AI for insight summarization.
	1.	Get a Gemini API key
	2.	Add it inside the notebook:
  `api_key = "YOUR_API_KEY"`

---

👤 Author

Dyaneswaran Namasivayam
📧 Email: dyaneswaran123@gmail.com
