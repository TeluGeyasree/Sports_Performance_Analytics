# 📊 Power BI Dashboard Implementation Guide
**Project:** Sports Performance Analytics Using IPL Data  
**Dataset:** Cricsheet Official IPL Dataset  

---

## 🚀 Quick Setup in Power BI Desktop (Single Click)

1. Open **Microsoft Power BI Desktop**.
2. Click **Get data** ➔ **Excel workbook** (or click the green Excel icon on the Home ribbon).
3. Select the file:
   `PowerBI/IPL_PowerBI_Complete_Data.xlsx`
4. In the **Navigator** window, check the box for all 7 sheets:
   - ☑ `Dim_Matches`
   - ☑ `Fact_Batting`
   - ☑ `Fact_Bowling`
   - ☑ `Fact_Team_Performance`
   - ☑ `Fact_Season_Summary`
   - ☑ `Fact_Match_Phase`
   - ☑ `Fact_AllRounders`
5. Click **Load**. All tables will appear in the Data pane immediately!

---

## 📑 6 Dashboard Pages Layout Guide

### Page 1: Overall IPL Dashboard
- **KPI Cards:** Total Matches (1,243), Total Runs, Total Wickets, Total Seasons (19).
- **Clustered Column Chart:** `season` vs `total_runs` (from `Fact_Season_Summary`).
- **Clustered Bar Chart:** `team` vs `matches_won` (from `Fact_Team_Performance`).
- **Cards:** Top Run Scorer (V Kohli), Top Wicket Taker (YS Chahal).

### Page 2: Batting Performance
- **Clustered Bar Chart:** Top 10 Run Scorers (`player` vs `runs`).
- **Scatter Plot:** `batting_average` (X-axis) vs `strike_rate` (Y-axis), size by `runs`.
- **Table:** `player`, `matches`, `innings`, `runs`, `batting_average`, `strike_rate`, `fours`, `sixes`.
- **Slicer:** Filter by `season` or `runs` range.

### Page 3: Bowling Performance
- **Clustered Bar Chart:** Top 10 Wicket Takers (`player` vs `wickets`).
- **Scatter Plot:** `economy_rate` (X-axis) vs `bowling_strike_rate` (Y-axis), size by `wickets`.
- **Table:** `player`, `matches`, `overs_display`, `wickets`, `economy_rate`, `bowling_average`, `dot_ball_percentage`.

### Page 4: Team Performance
- **Horizontal Bar Chart:** `team` vs `win_percentage` (filter `matches_played >= 20`).
- **Grouped Bar Chart:** `team` vs `bat_first_win_percentage` and `chasing_win_percentage`.
- **Matrix / Table:** Complete franchise statistics.

### Page 5: Player Insights
- **Slicer:** Select `player` dropdown.
- **Multi-row Card:** Total Runs, Batting Average, Strike Rate, Wickets, Economy.
- **Table / Bar Chart:** Season-by-season run contribution for the selected player.

### Page 6: Season and Match Analysis
- **Line & Clustered Column Chart:** `season` vs `total_runs` (column) and `overall_run_rate` (line).
- **Column Chart:** Innings Phase scoring rate (`phase` vs `run_rate`).
- **Donut Chart:** Match outcomes by toss decision (`bat` vs `field`).
- **Bar Chart:** Venue average 1st innings scores.
