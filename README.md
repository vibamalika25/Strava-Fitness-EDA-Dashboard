# FitTrack: Strava Fitness Analysis Dashboard

##  Project Overview

**FitTrack** is a comprehensive Exploratory Data Analysis (EDA) project that analyzes user fitness patterns from the Fitabase Strava dataset. The project examines **30+ activity metrics** including step counts, distances, intensity minutes, calories burned, and sleep patterns to uncover behavioral trends, metric correlations, and actionable business insights for fitness platforms.

##  Objectives

- Identify user activity patterns and behavioral trends
- Analyze correlations between fitness metrics (steps, distance, intensity, calories)
- Discover user segmentation based on activity levels
- Provide data-driven recommendations for user engagement and retention
- Create interactive visualizations for business stakeholders

##  Dataset Information

**Source:** Fitabase Strava Fitness Dataset  
**Period:** April–May 2016 (30 days)  
**Users:** 33 unique users  
**Records:** 1,010 rows, 34 columns

### Key Variables:
- **Step Metrics:** TotalSteps, StepTotal
- **Distance Metrics:** TotalDistance, TrackerDistance, LoggedActivitiesDistance
- **Intensity Metrics:** VeryActiveMinutes, FairlyActiveMinutes, LightlyActiveMinutes, SedentaryMinutes
- **Calories:** Daily caloric expenditure
- **Sleep:** TotalSleepRecords, TotalMinutesAsleep, TotalTimeInBed
- **Body Metrics:** WeightKg, BMI (sparse data)

##  Technologies Used

- **Python 3.x** – Core programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Static visualizations
- **Seaborn** – Statistical visualizations
- **Plotly** – Interactive visualizations
- **Missingno** – Missing data visualization

##  Analysis Performed

### Univariate Analysis
- Distribution of step counts, distances, and intensity minutes
- Sleep patterns and data completeness
- Frequency distribution analysis using treemaps

### Bivariate Analysis
- Step count vs. distance relationships
- Activity intensity vs. calories burned
- Tracked vs. logged activity comparisons
- Weekday-weekend activity patterns

### Multivariate Analysis
- Correlation heatmaps (12 key metrics)
- Pair plots for multi-variable relationships
- User segmentation patterns

##  Key Visualizations

| Chart | Description | Key Insight |
|-------|-------------|-------------|
| **Bar Chart** | Step count per day | Weekday peaks, weekend dips |
| **Treemap** | Step/Distance distribution | High variability, 0-step frequency |
| **Countplot** | Sleep records | 51% missing sleep data |
| **Histogram** | Metric distributions | Right-skewed activity data |
| **Stacked Bar** | Tracked vs logged distance | Manual logging rarely used |
| **Stacked Bar** | Steps vs calories | Strong positive correlation |
| **Line Plot** | Top 15 activity peaks | Isolated extreme activity days |
| **Heatmap** | Correlation matrix | Strong metric relationships |
| **Pair Plot** | Multi-variable patterns | User clustering visible |

##  Key Insights

### 1. Activity Patterns
- **High variability:** Step counts range from 0 to 23,186 (mean ~8,236)
- **Weekly cycles:** Higher activity midweek, lower on weekends
- **User segments:** Sedentary, Moderate, Highly Active clusters identified

### 2. Metric Relationships
- **Strong correlations:**
  - TotalSteps ↔ TotalDistance (r ≈ 0.99)
  - TotalSteps ↔ Calories (r ≈ 0.68)
  - VeryActiveMinutes ↔ Calorie burn (r ≈ 0.64)
- **Redundant variables:** TotalDistance/TrackerDistance, StepTotal/TotalSteps can be consolidated
- **Negative correlation:** SedentaryMinutes inversely related to all activity metrics

### 3. Engagement Opportunities
- **Data gaps:** 51% missing sleep data, 93% missing weight data
- **Zero-step days:** Potential disengagement signal
- **Manual logging:** Rarely utilized feature
- **Peak days:** Isolated, not sustained patterns

## 🏢 Business Recommendations

### 1. Personalized Goal Setting
- Implement adaptive step/distance targets based on individual history
- Offer rest day allowances and challenge day opportunities
- Use percentile-based goals (e.g., 25th, 50th, 75th percentiles)

### 2. User Segmentation Strategy
- **Sedentary Users:** Gentle nudges, small challenges, education
- **Moderate Users:** Weekly streaks, mid-level challenges
- **Highly Active Users:** Intensity-based goals, recognition programs

### 3. Engagement Campaigns
- Launch challenges on peak activity days (Tuesday–Thursday)
- Create "Weekend Challenges" to combat weekend activity decline
- Implement automated re-engagement for 0-step days

### 4. Product Simplification
- Consolidate redundant metrics
- Allow users to select preferred primary metric (steps, distance, or active minutes)
- Simplify dashboards to 5–7 core indicators

### 5. Retention Strategy
- Identify at-risk users via declining activity patterns
- Implement proactive re-engagement campaigns
- Celebrate milestones as individual achievements (not daily expectations)

