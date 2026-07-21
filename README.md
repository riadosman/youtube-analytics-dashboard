# 📊 YouTube Analytics Dashboard

An interactive **Streamlit dashboard** for analyzing YouTube channel performance using exported YouTube Analytics CSV reports.

The dashboard provides both **channel-level insights** and **individual video analysis**, allowing creators to compare performance over time, identify trends, and evaluate how videos perform against historical benchmarks.

---

## Features

### 📈 Aggregate Metrics

View overall channel performance with:

- Median performance comparison (Last 6 Months vs Last 12 Months)
- Views
- Likes
- Subscribers
- Shares
- Comments
- RPM (USD)
- Average Percentage Viewed
- Average View Duration
- Engagement Ratio
- Views per Subscriber Gained

Performance values are normalized against the previous year's median, making it easy to identify above-average and below-average videos.

---

### 🎥 Individual Video Analysis

Analyze a single video with:

- Audience distribution
  - Subscriber vs Non-Subscriber
  - USA / India / Other countries
- Cumulative views during the first 30 days
- Comparison against:
  - 20th percentile
  - Median (50th percentile)
  - 80th percentile

This helps determine whether a video's early performance is above or below historical expectations.

---

## Dashboard Preview

You can add screenshots here.

```
images/
├── dashboard.png
├── aggregate_metrics.png
└── individual_video.png
```

Example:

```markdown
![Dashboard](images/dashboard.png)
```

---

## Calculated Metrics

The dashboard computes several additional KPIs from the exported data.

### Engagement Ratio

\[
\frac{\text{Likes + Comments + Shares + Dislikes}}{\text{Views}}
\]

---

### Views per Subscriber Gained

\[
\frac{\text{Views}}{\text{Subscribers Gained}}
\]

---

### Average View Duration

Converted from:

```
HH:MM:SS
```

to total seconds for easier numerical analysis.

---

## Technologies Used

- Python
- Streamlit
- Pandas
- NumPy
- Plotly Express
- Plotly Graph Objects

---

## Project Structure

```
.
├── app.py
├── Aggregated_Metrics_By_Video.csv
├── Aggregated_Metrics_By_Country_And_Subscriber_Status.csv
├── Video_Performance_Over_Time.csv
├── requirements.txt
├── README.md
└── images/
```

---

## Dataset

The dashboard expects the following CSV files exported from **YouTube Studio Analytics**:

- `Aggregated_Metrics_By_Video.csv`
- `Aggregated_Metrics_By_Country_And_Subscriber_Status.csv`
- `Video_Performance_Over_Time.csv`

Place them in the project root before running the application.

---

## Installation

Clone the repository

```bash
git clone https://github.com/riadosman/youtube-analytics-dashboard.git
```

Go to the project

```bash
cd youtube-analytics-dashboard
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the application

```bash
streamlit run app.py
```

---

## Required Packages

```
streamlit
pandas
numpy
plotly
```

or install manually

```bash
pip install streamlit pandas numpy plotly
```

---

## Data Processing

The application automatically:

- Cleans malformed column names
- Parses mixed date formats
- Converts view duration to seconds
- Computes engagement metrics
- Calculates rolling medians
- Generates percentile benchmarks
- Creates cumulative first-30-day view curves

---

## Visualizations

### Aggregate Dashboard

- KPI cards
- Performance comparison table

### Individual Video Dashboard

- Audience segmentation
- Country comparison
- Subscriber analysis
- 30-day cumulative performance chart
- Historical percentile comparison

---

## Future Improvements

- Upload CSV files directly from the UI
- Dark/Light themes
- Export charts as PNG/PDF
- Monthly trend analysis
- Revenue forecasting
- Retention heatmaps
- Click-through rate analysis
- Interactive filtering by publish date
- Channel growth forecasting

---

## License

This project is released under the MIT License.

---

## Author

**Riad Osman**

Software Engineering Student

Building practical AI, Data Analytics, and Software Engineering projects while learning in public.

GitHub: https://github.com/riadosman
LinkedIn: https://www.linkedin.com/in/riad-osman-b54343226/
