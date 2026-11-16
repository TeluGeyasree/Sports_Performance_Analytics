# 🏏 Sports Performance Analytics Using IPL Data

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Interactive_Dashboard-F2C811?style=flat&logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green.svg)

An end-to-end Data Science and Business Intelligence project analyzing 19 editions of the **Indian Premier League (IPL)** from 2008 to present, leveraging real-world ball-by-ball match data from Cricsheet.

---

## 📌 Project Overview
* **Domain:** Sports Analytics & Business Intelligence
* **Dataset:** Official Cricsheet IPL CSV2 Archive (1,243 matches, 295,708 deliveries, 808 players, 19 seasons)
* **Tools & Stack:**
  * **Data Processing & Analysis:** Python, Pandas, NumPy
  * **Exploratory Data Visualization:** Matplotlib, Seaborn
  * **Interactive Business Intelligence Dashboard:** Microsoft Power BI Desktop

---

## 📁 Repository Structure

```text
Sports_Performance_Analytics/
│
├── Dataset/                              # Official Cricsheet raw ball-by-ball archive
│   ├── all_matches.csv
│   └── ipl_csv2.zip
│
├── Cleaned_Data/                         # Standardized datasets
│   ├── matches.csv                       # Standardized franchise names & match outcomes
│   └── deliveries.csv                    # 295,708 legal-annotated deliveries & phases
│
├── Visualizations/                       # High-resolution analytical charts
│   ├── 01_matches_by_season.png
│   ├── 02_match_results_distribution.png
│   ├── 03_top_10_run_scorers.png
│   ├── 04_batting_strike_rate_vs_average.png
│   ├── 05_top_10_wicket_takers.png
│   ├── 06_bowling_economy_vs_strike_rate.png
│   ├── 07_team_wins_leaderboard.png
│   ├── 08_team_win_percentage.png
│   ├── 09_all_rounders_performance.png
│   ├── 10_season_scoring_trends.png
│   ├── 11_venue_scoring_patterns.png
│   ├── 12_toss_decision_win_percentage.png
│   └── 13_innings_phase_run_rate.png
│
├── PowerBI/                              # Power BI Model, DAX & Workbook
│   ├── IPL_Sports_Performance_Analytics.pbix  # Main interactive Power BI dashboard
│   ├── IPL_PowerBI_Complete_Data.xlsx         # Master 7-sheet data source
│   ├── DAX_Measures.dax                       # DAX formula library
│   ├── PowerBI_Dashboard_Guide.md             # Dashboard design specifications
│   ├── Dim_Matches.csv
│   ├── Fact_Batting.csv
│   ├── Fact_Bowling.csv
│   ├── Fact_Team_Performance.csv
│   ├── Fact_Season_Summary.csv
│   ├── Fact_Match_Phase.csv
│   └── Fact_Player_AllRounder.csv
│
├── 01_Data_Loading.ipynb                 # Inspection, shape, head, info, summary stats
├── 02_Data_Cleaning.ipynb                # Missing values, franchise rebrand mapping & cricket rules
├── 03_Match_Analysis.ipynb               # Macro totals, innings scores & match outcomes
├── 04_Batting_Performance_Analysis.ipynb # Top run scorers, strike rate vs average quadrant
├── 05_Bowling_Performance_Analysis.ipynb # Wicket takers, economy vs strike rate, dot ball %
├── 06_Team_Performance_Analysis.ipynb    # Franchise records, win %, defending vs chasing splits
├── 07_Player_Performance_Analysis.ipynb  # Dual-threat all-rounders (500+ runs & 20+ wickets)
├── 08_Season_And_Venue_Analysis.ipynb    # Scoring evolution (8.20 -> 9.50+ RPO) & stadium benchmarks
├── 09_Toss_And_Match_Outcome_Analysis.ipynb # Toss win % (51.5%), bat vs field shift
├── 10_Advanced_Insights.ipynb            # Phase analysis (Powerplay, Middle, Death RPO)
├── 11_PowerBI_Data_Preparation.ipynb     # Star schema verification & export validation
├── .gitignore
└── README.md
```

---

## 🔬 Jupyter Notebooks Implementation

| # | Notebook | Focus Area & Key Findings |
|---|---|---|
| **01** | `01_Data_Loading.ipynb` | Loads raw Cricsheet data; inspects 1,243 matches, 295,708 deliveries across 19 editions. |
| **02** | `02_Data_Cleaning.ipynb` | Resolves franchise rebrands (e.g. *Delhi Daredevils* ➔ *Delhi Capitals*), isolates super overs, and computes legal ball / bowler wicket attribution. |
| **03** | `03_Match_Analysis.ipynb` | 395,000+ total runs, 14,000+ total wickets, 318 avg match runs. Chasing teams win 52.9% of decisive encounters. |
| **04** | `04_Batting_Performance_Analysis.ipynb` | All-time run scorers led by Virat Kohli (9,336), Rohit Sharma, Shikhar Dhawan, David Warner. Quadrant analysis benchmarks Avg (30.0) vs SR (130.0). |
| **05** | `05_Bowling_Performance_Analysis.ipynb` | Top wicket takers led by Yuzvendra Chahal (205) and Dwayne Bravo (183). Sunil Narine and Rashid Khan maintain sub-6.80 career economies. |
| **06** | `06_Team_Performance_Analysis.ipynb` | Franchise consistency: Mumbai Indians (144 wins, 55.4%) and Chennai Super Kings (138 wins, 57.7%) lead the league. |
| **07** | `07_Player_Performance_Analysis.ipynb` | Identifies elite all-rounders (min 500 runs & 20 wickets) combining batting strike rate with bowling economy. |
| **08** | `08_Season_And_Venue_Analysis.ipynb` | Traces macro IPL scoring progression from 8.20 RPO (2008) to 9.50+ RPO. Highlights high-scoring grounds (Chinnaswamy, Wankhede) vs spin-friendly venues (Chepauk). |
| **09** | `09_Toss_And_Match_Outcome_Analysis.ipynb` | Evaluates toss impact (~51.5% win rate for toss winners) and the modern shift where captains field first in >72% of matches. |
| **10** | `10_Advanced_Insights.ipynb` | Tactical phase segmentation: Powerplay (7.64 RPO), Middle (7.78 RPO), Death (10.37 RPO). Identifies death overs specialists. |
| **11** | `11_PowerBI_Data_Preparation.ipynb` | Star schema modeling, data type verification, master Excel generation, and DAX measures validation. |

---

## 📊 Power BI Interactive Dashboard

The interactive report (`PowerBI/IPL_Sports_Performance_Analytics.pbix`) provides an executive view of the tournament:

* **Top Executive KPIs:** Total Matches (1,243), Total Seasons (19), Total Runs (401K), Total Wickets (15K).
* **Tournament Scoring Progression (Area Chart):** Highlighting the evolution and acceleration in run scoring over 19 seasons.
* **Franchise Wins Leaderboard (Table):** All-time wins across all 15 franchises.
* **Tactical Toss Outcomes (Donut Chart):** Captains' decision to Field First (66.4%) vs Bat First (33.6%).
* **Top 10 Batting Superstars (Bar Chart):** Career run leaders with custom Top N filtering.
* **Top 10 Bowling Legends (Funnel Chart):** Career wicket leaders displayed in a tapered ranking.

---

## ⚡ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Sports_Performance_Analytics.git
cd Sports_Performance_Analytics
```

### 2. Environment Setup
```bash
pip install pandas numpy matplotlib seaborn openpyxl nbformat
```

### 3. Running the Jupyter Notebooks
Open any notebook directly in VS Code or launch Jupyter Lab:
```bash
jupyter lab
```

### 4. Viewing the Power BI Dashboard
Open `PowerBI/IPL_Sports_Performance_Analytics.pbix` directly in **Microsoft Power BI Desktop**.
