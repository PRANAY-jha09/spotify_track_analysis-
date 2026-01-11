
# 🧾 Spotify Tracks Analysis – Popularity & Audio Features

_Analyzing Spotify's top tracks for trends in popularity, genres, and audio attributes using SQL, Python, and Tableu._


## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project dissects Spotify's top tracks dataset to uncover drivers of popularity, genre trends, and audio feature correlations. Built a complete pipeline with SQL ETL, Python stats/ML insights, and Power BI visuals for music industry decisions.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Spotify aims to boost user engagement via playlists, recommendations, and artist promotions. Key challenges:
- What audio features drive virality?
- Explicit content's impact on reach
- Genre-specific trends (energy, danceability, BPM)
- Top artists/albums for partnerships
- Happiness/energy correlations for mood playlists

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Spotify top tracks CSV (~30K+ tracks from 50+ regions)
- Features: track_id, artists, album, popularity, duration, explicit, danceability, energy, valence (happiness), tempo (BPM), genres
- Sourced from Spotify API/public datasets

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Aggregations, Joins, Pivots)
- Python (Pandas, Matplotlib, Seaborn, SciPy, Scikit-learn)
- Power BI (Scatterplots, Histogram, DAX)
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
spotify-tracks-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Spotify Tracks Report.pdf
│
├── notebooks/                  # Jupyter notebooks
│   ├── exploratory_data_analysis.ipynb
│   ├── spotify_popularity_analysis.ipynb
│
├── scripts/                    # ETL scripts
│   ├── data_ingestion.py
│   └── tracks_summary.py
│
├── dashboard/                  # Power BI
│   └── spotify_dashboard.pbix
│
└── data/                       # CSVs
    ├── spotify_tracks.csv
    └── tracks_features.csv
```

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Dropped duplicates/invalids (~2%)
- Normalized genres/artists (string cleaning, lowercase)
- Handled outliers: BPM >250, duration >15min
- Feature engineered: Explicit binary, normalized scales (0-1)
- Aggregated: Genre avgs, top-N lists

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Distributions:**
- Popularity: Mean 65/100; skewed to 70-90
- Explicit: 25% of tracks
- Audio Features: Danceability mean 0.62; Energy 0.68; Valence 0.47

**Outliers:**
- Highest BPM: 200+ EDM tracks
- Longest: Epic rock suites

**Correlations:**
- Danceability & Popularity (0.35 strong)
- Energy & Popularity (0.28)
- Explicit tracks avg pop 68 vs non 64 (t-test p<0.05)

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Explicit Impact**: Explicit tracks 5% higher avg popularity despite smaller share
2. **Top Genres Energy/Dance**: Pop/Latin lead danceability (0.75); Metal highest energy (0.85)
3. **Top 10 Artists**: Taylor Swift, Drake, Bad Bunny → 30% total popularity share
4. **Top Albums**: Folklore, Un Verano Sin Ti dominate
5. **Scatter Insights**: High dance/energy clusters at pop>80
6. **Valence by Genre**: Pop happiest (0.55); Hip-Hop lowest (0.40)
7. **BPM Trends**: EDM ~130 avg; slower for R&B (90)
8. **Hypothesis**: Danceability predicts 12% popularity variance (R²=0.12)

---
<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

Power BI dashboard features:
- Popularity vs Features scatters
- Genre bars (energy/dance/BPM/valence)
- Top artists/albums
- Explicit pie & comparisons

<img src="SCREENSHOT OF DASHBOARD/Screenshot 2025-11-02 170337.png" width="600">

---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone repo:
```bash
git clone https://github.com/yourusername/spotify-tracks-analysis.git
```
2. Install:
```bash
pip install -r requirements.txt
```
3. Process data:
```bash
python scripts/data_ingestion.py
python scripts/tracks_summary.py
```
4. Notebooks:
   - `notebooks/exploratory_data_analysis.ipynb`
   - `notebooks/spotify_popularity_analysis.ipynb`
5. Dashboard:
   - `dashboard/spotify_dashboard.pbix`

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- **Playlist Optimization**: Prioritize high dance/energy (pop>75) for viral mixes
- **Explicit Strategy**: Promote selectively – boosts pop but limits family audiences
- **Genre Focus**: Latin/Pop for global; invest in high-valence for mood playlists
- **Artist Partnerships**: Top 10 (Drake/Swift) for collabs; scout rising EDM
- **Production Tips**: Target 120-140 BPM, 0.7+ danceability for charts
- **A/B Test**: Explicit vs clean versions on engagement

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Ayushi Mishra**  
Data Analyst  
📧 Email: Pranayjha535@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/pranay-jha09/)  

