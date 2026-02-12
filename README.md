# AudioTrend-Analytics
AudioTrend Analytics is a Python-based analytics pipeline designed to detect emerging music trends using the Spotify Web API.  Instead of simply pulling track data, this project builds a lightweight "signal engine" that analyzes release recency, cross-query presence, and preview availability to generate a custom trend score for tracks.


## Overview

The goal is to simulate how a data analyst or product analyst might build a discovery or trend detection system from raw API data.

This project demonstrates end-to-end analytics workflow:

API ingestion → data cleaning → feature engineering → scoring algorithm → visualization → BI export.

---

## Project Goals

- Build a real-world data pipeline using an external API (Spotify)
- Design a custom scoring algorithm instead of relying on built-in metrics
- Create reusable analytics outputs for dashboards (Looker Studio)
- Practice production-style data engineering and analysis in Python

---

## Tech Stack

- Python
- Pandas
- Requests
- Matplotlib
- Google Colab
- Spotify Web API
- Looker Studio (BI visualization)

---

## Data Pipeline

### 1. Data Collection

Tracks are pulled from Spotify using multiple artist-based search queries.

Example queries:

- Drake
- Kendrick Lamar
- Travis Scott
- SZA
- Metro Boomin
- Future
- Kanye West
- Chicago artists (G Herbo, Lil Durk, Twista, etc.)

Pagination logic ensures larger datasets beyond default API limits.

---

### 2. Feature Engineering

The system creates custom analytical features:

- days_since_release  
- preview_ok (audio preview availability)  
- query_hits (how often a track appears across searches)

These signals simulate real-world trend indicators such as:

- Recency momentum
- Cross-surface discoverability
- Platform readiness for audio analysis

---

### 3. Trend Proxy Algorithm

A custom trend score is generated:

This approximates how discovery or recommendation systems identify rising content without needing proprietary engagement metrics.

---

### 4. Visualization

Auto-generated charts:

- Top tracks by trend score
- Trend score vs recency analysis
- Query presence impact on trend score

Charts are automatically saved to `/outputs`.

---

### 5. BI Export

Clean dataset exported for dashboarding:


Designed for integration with Looker Studio or other BI tools.

---

## Example Outputs

- outputs/top_tracks_trend_score.png
- outputs/trend_vs_recency.png
- outputs/query_hits_vs_trend.png

---

## Key Skills Demonstrated

- API integration and pagination
- Data cleaning and transformation
- Feature engineering
- Custom scoring algorithms
- Analytical visualization
- BI-ready data modeling

---

## Future Improvements

- Add audio feature extraction when API access allows
- Time-series trend tracking
- Artist growth modeling
- Playlist momentum analysis
- ML-based trend prediction

---

## Why This Project Exists

This project reflects my interest in combining analytics, data science, and real-world systems thinking.

The focus was not just to analyze data, but to design a process that turns raw API responses into actionable signals.

---

## Author

Rasheed Johnson

