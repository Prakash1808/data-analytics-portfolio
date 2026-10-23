# 📊 Gen Z Slang Trends | Social Media Engagement & Sentiment Analytics

### Interactive Power BI Dashboard | Social Media & Audience Analytics Portfolio Project

## 🔍 Project Overview

**Gen Z Slang Trends** is an interactive Microsoft Power BI analytics project that explores how Gen Z slang is used across social media platforms, how its popularity changes over time, and how engagement, sentiment, and audience demographics differ by platform and slang term.

The project analyzes **535,396 simulated social media posts** from **2020–2025**, covering **46 unique slang terms**, **7 usage platforms**, **5 age groups**, and **22 recorded regions**.

Built with **Power BI, Power Query, a manually created DateTable, data modeling, DAX measures, slicers, and interactive visualizations**, the report is organized into three pages: **Executive Overview**, **Slang Term Performance & Sentiment Analysis**, and **Audience Demographics & Engagement Insights**.

The aim is to turn social-media-style activity data into clear, filter-driven insights into slang usage, engagement, sentiment, and virality. **All findings describe the supplied simulated dataset, not verified real-world social media behavior.**

## 🎯 Business Objectives

- Examine how slang-related posting activity changes from 2020 to 2025.
- Track posts, likes, shares, comments, and overall engagement.
- Compare engagement across social media platforms and regions.
- Identify popular slang terms by posts, likes, engagement, and virality.
- Analyze sentiment scores and sentiment-category distributions.
- Examine relationships between intensity and virality scores.
- Understand which audience age groups contribute the most engagement.
- Compare usage contexts, slang categories, and slang lifecycle phases.
- Provide interactive insights with report-level navigation and slicers.

## 📁 Dataset Overview

| Attribute | Details |
|---|---|
| Source file | `genz_slang_usage_2020_2025.csv` |
| Total records / posts | **535,396** |
| Data period | **January 1, 2020 – December 31, 2025** |
| Dataset type | Simulated social media slang usage data |
| Unique slang terms | **46** |
| Slang term categories | **17** |
| Usage platforms | **7** |
| User age groups | **5** |
| Recorded regions | **22** |
| Usage contexts | **17** |
| Fields in source CSV | **22** |

### Key Dataset Columns

| Field | Description |
|---|---|
| `record_id` | Unique post/usage record identifier |
| `timestamp` | Date and time of the recorded activity |
| `slang_term` | Slang term appearing in a record |
| `term_category` | Category such as approval, insult, or identity |
| `term_meaning` | Descriptive meaning of the slang term |
| `origin_platform` | Platform associated with the term's origin |
| `usage_platform` | Platform where the usage was recorded |
| `region` | Recorded geographical region |
| `user_id` | User identifier |
| `user_age_group` | User age bracket |
| `usage_context` | Context such as criticism, humor, or reaction |
| `lifecycle_phase` | Recorded term lifecycle phase |
| `intensity_score` | Numerical measure of slang-use intensity |
| `sentiment` | Positive, neutral, or negative label |
| `sentiment_score` | Numerical sentiment score |
| `ironic_usage` | Boolean indicator of ironic usage |
| `likes`, `shares`, `comments` | Individual engagement measures |
| `virality_score` | Numerical virality score |
| `is_viral` | Boolean viral-post flag |
| `days_since_emergence` | Recorded days since the term's emergence |

**Platforms represented:** TikTok, Instagram, Twitter, YouTube, Reddit, Twitch, and Discord.

## 🧹 Data Preparation & Validation

The project uses Power BI's data preparation and modeling workflow, with calculated measures used in the report. The following characteristics were checked against the supplied CSV:

- Verified **535,396 rows** and **22 source fields**.
- Confirmed **no missing values** in the provided CSV.
- Confirmed `record_id` values are **unique**, with no duplicate complete records.
- Reviewed timestamp coverage and numerical engagement fields.
- Checked categorical consistency for platforms, age groups, sentiment, and lifecycle phases.
- Reviewed Boolean flags (`is_viral` and `ironic_usage`) and numerical scores.

The project description also identifies **Power Query** as the tool used for cleaning and transformations. Detailed Power Query steps and exact DAX expressions are not contained in the CSV or screenshots.

## 🔗 Power BI Data Model

The report uses a main slang usage fact table connected to a **manually created DateTable**. The DateTable supports time-based analysis and filtering by calendar periods.


| Table | Purpose |
|---|---|
| `genz_slang_usage_2020_2025` | Main fact dataset containing post, audience, slang, sentiment, and engagement attributes |
| `DateTable` | Manually created date dimension with a `Date` field |

The model screenshot shows a **one-to-many (1:*) relationship**, with **DateTable on the “1” side** and the slang usage fact table on the “many” side, with filtering directed from the date dimension to the fact table.

## 📊 Key Performance Indicators

### Executive KPIs

| KPI | Overall Result |
|---|---:|
| **Total Posts** | **535,396** (535K) |
| **Total Engagement** | **38,436,832** (38.44M) |
| **Average Engagement per Post** | **71.79** |
| **Viral Posts** | **717** |
| **Average Sentiment Score** | **0.18** |
| **Unique Slang Terms** | **46** |
| **Top Slang by Posts** | **slay** |
| **Top Slang by Average Virality Score** | **aura** |
| **Top Audience Age Group by Engagement** | **18–24** |
| **Top Usage Context by Post Count** | **criticism** |
| **Ironic Usage Rate** | **10.90%** |

### Engagement Breakdown

| Engagement Type | Total | Share of Engagement |
|---|---:|---:|
| Likes | **32.92M** | **85.64%** |
| Shares | **1.77M** | **4.59%** |
| Comments | **3.75M** | **9.76%** |
| **Total** | **38.44M** | **100%** |

### KPI Definitions

**Total Engagement** = Total Likes + Total Shares + Total Comments

**Average Engagement per Post** = Total Engagement ÷ Total Posts

**Viral Posts** = Count of records where `is_viral = TRUE`

**Average Sentiment Score** = Average of `sentiment_score`

**Ironic Usage Rate (%)** = Records where `ironic_usage = TRUE` ÷ Total Posts × 100

**Top Slang by Posts** = Slang term with the highest record count

**Top Slang by Virality** = Slang term with the highest **average** `virality_score`

**Formatting note:** The audience dashboard displays `0.11` for ironic usage, which represents an approximately **0.109 proportion**, or **10.90%** when expressed as a percentage. It should not be interpreted as 0.11%.

## 📈 Dashboard Pages & Visualizations

### 1. Executive Overview – Gen Z Slang Trends


Provides an overall view of slang-related activity, geographical contribution, engagement, and sentiment.

**Dashboard elements:**

1. **Total Posts by Year** — Posting trends from 2020 to 2025.
2. **Total Posts by Location** — Geographical distribution of slang usage records.
3. **Likes, Shares & Comments** — Donut-chart breakdown of engagement types.
4. **Engagement by Platform** — Platform-level engagement comparison.
5. **Top Regions by Total Engagement** — Treemap highlighting high-engagement regions.
6. **Total Posts by Sentiment** — Comparison of positive, neutral, and negative posts.

**KPI cards:** Total Posts, Total Engagement, Average Engagement, Viral Posts, and Average Sentiment Score.

### 2. Slang Term Performance & Sentiment Analysis


Examines individual slang terms, category distribution, sentiment patterns, and virality-related scores.

**Dashboard elements:**

1. **Average Sentiment Score by Slang Term** — Comparison of mean sentiment scores across slang terms.
2. **Intensity Score vs. Virality Score** — Scatter visualization exploring how the two scores vary alongside engagement.
3. **Total Engagement by Slang Term** — Comparison of combined likes, shares, and comments.
4. **Total Posts by Term Category** — Treemap showing distribution across slang categories.
5. **Top 10 Slang Terms by Total Likes** — Ranking of most-liked slang terms.

**KPI cards:** Unique Slang Terms, Top Slang by Posts, Top Slang by Virality, Average Sentiment, and Average Engagement.

### 3. Audience Demographics & Engagement Insights


Focuses on audience behavior, age groups, lifecycle phases, and sentiment.

**Dashboard elements:**

1. **Total Engagement by Age Group** — Overall engagement across age brackets.
2. **Total Likes by Age Group** — Age-wise likes comparison.
3. **Total Shares by Age Group** — Age-wise sharing activity.
4. **Total Posts by Age Group and Lifecycle Phase** — Distribution of growing, peak, declining, and legacy terms.
5. **Positive, Neutral & Negative Posts by Age Group** — Stacked sentiment comparison.

**KPI cards:** Top Age Group, Highest Likes Age Group, Top Context, Total Engagement, and Ironic Usage Rate.

## 🎛 Interactive Dashboard Features

The Power BI report uses page navigation and slicers for exploring specific segments. Filters visible across the three pages include:

- **Year / Month** — Explore time-based changes.
- **Slang Term** — Focus on individual terms.
- **Term Category** — Compare slang categories.
- **Usage Platform** — Explore individual social platforms.
- **User Age Group** — Examine demographic patterns.
- **Location** — Filter by region.
- **Viral Flag** — Compare viral and nonviral records.

The report also uses visual cross-filtering and navigation buttons between **Overview**, **Slang Analysis**, and **Audience Insights**. KPI cards and charts respond to the applicable report filters.

## 💡 Key Analytical Findings

### 1. Slang posting activity peaks in 2023.

| Year | Posts |
|---|---:|
| 2020 | 52,592 |
| 2021 | 91,597 |
| 2022 | 101,347 |
| **2023** | **114,006** |
| 2024 | 112,845 |
| 2025 | 63,009 |

Posting activity grows through 2023, remains close to its peak in 2024, and is lower in 2025 in the supplied simulated data.

### 2. TikTok contributes the most engagement.

| Platform | Total Engagement |
|---|---:|
| **TikTok** | **22.65M** |
| Instagram | 5.61M |
| Twitter | 5.05M |
| YouTube | 2.63M |
| Reddit | 1.68M |
| Twitch | 0.63M |
| Discord | 0.18M |

TikTok contributes approximately **58.94%** of total dataset engagement.

### 3. Likes dominate overall engagement.

Likes account for **85.64%** of engagement events, compared with **9.76%** for comments and **4.59%** for shares.

This indicates that the dataset's engagement volume is driven primarily by likes.

### 4. The 18–24 age group generates the most engagement.

| Age Group | Total Engagement | Total Likes | Total Shares |
|---|---:|---:|---:|
| **18–24** | **15.67M** | **13.41M** | **728.43K** |
| 13–17 | 13.06M | 11.14M | 618.51K |
| 25–30 | 6.68M | 5.72M | 301.18K |
| 31–40 | 2.20M | 1.90M | 88.51K |
| 41+ | 0.84M | 0.74M | 29.25K |

The **18–24** segment accounts for approximately **40.76%** of total engagement, making it the largest contributing age group in the data.

### 5. “slay” is the leading slang term by post count and engagement.

The term **slay** appears in **19,004 posts**, receives approximately **1.31M likes**, and generates approximately **1.54M total engagements**.

Other high-engagement terms include **bussin**, **rizz**, **gaslighting**, and **delulu**.

### 6. “aura” has the highest average virality score.

**aura** ranks highest by *average* `virality_score`, at approximately **0.01265**. This differs from the count of posts flagged `is_viral = TRUE`; the two metrics should not be treated as interchangeable.

### 7. Positive sentiment has the largest share of posts.

| Sentiment | Total Posts | Share |
|---|---:|---:|
| Positive | **254,777** | **47.59%** |
| Neutral | 169,863 | 31.73% |
| Negative | 110,756 | 20.69% |

The overall mean sentiment score is approximately **0.18**, reflecting a slightly positive average according to the dataset's sentiment values.

### 8. Approval is the largest slang category.

The **approval** category contains **106,901 posts**, approximately **19.97%** of the dataset. Other common categories include insult, identity, humor, and appearance.

### 9. California is the highest-engagement recorded region.

California produces approximately **4.50M** engagements, followed by New York (**3.84M**) and Texas (**3.54M**).

The `region` field mixes US states and country-level locations, so these are source-defined regions rather than a consistent country ranking.

### 10. Criticism is the most frequent context, but not the highest-engagement context.

**criticism** has the greatest post count (**31,758**), narrowly ahead of commenting (**31,746**). In contrast, **reaction** has the highest total engagement among usage contexts (approximately **2.37M**).

These findings describe associations and distributions in the simulated dataset; they do not demonstrate causal effects or real-world platform performance.

## 🛠 Tools & Technical Skills

**Microsoft Power BI | Power Query | DAX Measures | Manual DateTable | Data Modeling | One-to-Many Relationships | Data Validation | KPI Reporting | Interactive Slicers | Report Navigation | Time-Series Analysis | Sentiment Analysis | Audience Segmentation | Social Media Analytics | Data Visualization**

The README embeds the actual three dashboard screenshots and the Power BI data-model image using local paths within this repository.

## 🚀 Project Outcome

Created a three-page Power BI report demonstrating the ability to:

- Explore and validate a dataset of more than **535K** social media activity records.
- Design a date-based relational model using a **manually created DateTable**.
- Analyze social media engagement and audience demographics.
- Define and report consistent engagement, sentiment, and virality KPIs.
- Build interactive navigation, filters, charts, treemaps, and geographic visuals.
- Compare posting activity over time and across platforms, age groups, and regions.
- Communicate data-driven findings while recognizing the limits of synthetic data.

## 👤 Author

**Prakash Ananda Shelake**  
Data Analyst | SQL | Python | Power BI | Tableau | Advanced Excel  
GitHub: [Prakash1808](https://github.com/Prakash1808)
