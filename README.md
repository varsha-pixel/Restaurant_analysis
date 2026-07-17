# Zomato Restaurant Data Analysis

An exploratory data analysis (EDA) project over real restaurant data: cuisine popularity, price vs. rating, and geographic distribution. No modeling — the goal is to show you can extract clean, business-relevant insight from a messy real-world dataset.

**Problem statement**

A restaurant aggregator wants to understand its own marketplace: which cuisines are most popular vs. highest-rated, whether price predicts quality, and which restaurants represent the best value. You're handed the raw restaurant table and asked to answer those questions with evidence.

**Dataset**

**Kaggle**: Zomato Restaurants Data (slug: shrutimehta/zomato-restaurants-data — note this differs from the slug commonly circulated online, shrutimechlearn/..., which no longer resolves)

**Domain**: food delivery & restaurant analytics

**Size**: 9,551 restaurants across 15 countries (~91% India, concentrated in Delhi NCR), 21 columns
Ships with a bonus Country-Code.xlsx lookup table (the main CSV only has a numeric country code)

**Tools & Technologies**
**SQL Server** – Data querying and analysis
**Power BI** – Dashboard development
**Python (Pandas)** – Data cleaning and preprocessing
**Jupyter Notebook** – Data preparation

**Analysis walkthrough & key findings**

**1.Geographic distribution** — the dataset is ~91% Indian and dominated by Delhi NCR (New Delhi, Gurgaon, Noida). Any city/cuisine conclusion should be read as "true for Delhi NCR", not global.

**2.Cuisine popularity vs. quality diverge** — North Indian, Chinese, and Fast Food are the most common cuisines, but Brazilian, International, and Indian (as a standalone label) rate highest on average (min. 20 restaurants per cuisine, to avoid small-sample noise).

**3.Price vs. rating** — raw cost for two barely correlates with rating (Pearson r = 0.077), but Zomato's own 1-4 price tier correlates much more strongly (r = 0.403). Market segment predicts quality better than the sticker price does.

**4.Operational features** — restaurants with table booking rate noticeably higher on average (3.59 vs. 3.41) than those without; online delivery shows almost no relationship. Read as correlation (booking as a proxy for an established, higher-end restaurant), not causation.

**5.Best value** — a rating / cost_for_two score (restricted to restaurants already rated ≥ 4.0) surfaces high-quality, low-cost restaurants that a simple "top rated" list would miss.

