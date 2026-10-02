# ChatGPT_Review_Analysis
This project focuses on analyzing customer reviews of ChatGPT. The objective is to perform a comprehensive sentiment analysis and feature extraction from textual review data to understand user satisfaction and pinpoint positive or critical feedback patterns.

Sentiment, issue and trend analysis of **~193K ChatGPT app reviews** (Jul 2023 – Aug 2024).

**Tools:** Python · pandas · TextBlob · scikit-learn · seaborn · WordCloud

---

## Files

| File | Purpose |
|------|---------|
| `ChatGPT_Review_Analysis.ipynb` | Full analysis: code, charts, insights |
| `chatgpt_reviews.csv` | Dataset (review id, text, rating, date) |
| `requirements.txt` | Python dependencies |

## Data & Method

- **Data:** 196,727 raw reviews → **193,154** after removing 3,573 duplicate IDs and filling 6 empty reviews
- **Sentiment:** TextBlob polarity and subjectivity; Positive (> 0.05), Negative (< −0.05), otherwise Neutral
- **Validation:** text sentiment compared with star ratings
- **Keywords:** top words and phrases in 4–5★ reviews (word cloud) and 1–2★ reviews (log-odds), plus 8 issue themes
- **Trends:** monthly and weekly sentiment, and the monthly mix of complaint themes

## Key Findings

- **Highly positive:** average rating **4.51/5**; 88% of reviews are 4–5★ and 7.8% are 1–2★
- **Text agrees:** ~**76% positive / 21% neutral / 4% negative**
- **Praise is generic:** "good", "best", "helpful", "user friendly", "helpful for students"
- **Top complaints (share of 1–2★ reviews):** errors and crashes **15%**, wrong answers **12%**, login/verification **12%**, pricing **7%**, slow/network **6%**
- **Login problems hurt most:** reviews mentioning them average only **2.1★**
- **Unhappy users write more:** median 8 words in 1–2★ reviews vs 3 words in 4–5★
- **Improving over time:** average polarity rose from ~0.37 (Jul 2023) to ~0.48 (Aug 2024)
- **Complaints shifted:** login issues fell from 31–35% of negatives in mid-2023 to ~5% in 2024, while errors, slowness and pricing rose around Jun 2024

## Recommendations

1. Fix login and verification reliability first
2. Track "error / try later" complaints as a reliability KPI
3. Watch capacity and pricing sentiment as volume grows
4. Improve answer quality and explain limitations clearly
5. Monitor % 1–2★, polarity and complaint themes on a dashboard

## Limitations

- TextBlob misses sarcasm and factual complaints: only ~26% of 1–2★ reviews score as negative, so star ratings are used to find complaints
- 39% of reviews have 2 words or fewer; ~17% contain non-English text or emoji
- Issue themes are keyword-based (~49% of negative reviews match one)


**Author:** <Your Name> · [GitHub](https://github.com/your-username)
