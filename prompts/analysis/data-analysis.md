# Data Analysis Prompt

## Purpose

Perform structured data analysis including exploration, statistical analysis, visualization recommendations, and insight extraction.

## System Prompt

```
You are an expert data analyst skilled in statistical analysis, data visualization, and deriving actionable insights from complex datasets. You communicate findings clearly to both technical and non-technical audiences.
```

## Prompt Template

```
Analyze the following dataset and provide insights.

**Dataset Description:**
{description}

**Columns/Fields:**
{schema}

**Sample Data:**
{sample}

**Analysis Goals:**
{goals}

**Questions to Answer:**
{questions}

Please provide:
1. **Data Overview**: Summary statistics, data quality assessment, missing values
2. **Exploratory Analysis**: Key distributions, correlations, outliers
3. **Statistical Findings**: Hypothesis tests, confidence intervals, trends
4. **Visualizations**: Recommend specific chart types with rationale
5. **Insights**: Key findings in plain language
6. **Recommendations**: Actionable next steps based on findings
7. **Code**: Python/SQL code to reproduce the analysis
```

## Variations

### Quick Summary
```
Summarize this dataset in 5 key insights:
{data}

For each insight, provide: the finding, supporting evidence, and business impact.
```

### Anomaly Detection
```
Examine this time series data for anomalies:
{data}

Identify: unusual spikes or drops, pattern changes, seasonal deviations.
For each anomaly: timestamp, magnitude, possible cause.
```

### Cohort Analysis
```
Perform a cohort analysis on this user data:
{data}

Group users by: {cohort_criteria}
Track: {metric} over {time_period}
Compare retention, engagement, and conversion across cohorts.
```
