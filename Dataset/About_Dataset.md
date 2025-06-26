# 🗂️ IPL Dataset Overview (2018–2024)

This dataset contains comprehensive information on IPL (Indian Premier League) matches and ball-by-ball deliveries spanning from **2018 to 2024**. It consists of two CSV files: `matches.csv` and `deliveries.csv`.


## 📁 1. `matches.csv`

This file contains match-level data, covering details such as the venue, match outcome, toss decisions, and player awards.

### 🔑 Key Columns

| Column | Description |
|--------|-------------|
| `id` | Unique match identifier |
| `season` | IPL season (year) |
| `city` | City where the match was played |
| `date` | Match date |
| `match_type` | Type of match (e.g., league, eliminator) |
| `player_of_match` | Best performing player |
| `venue` | Stadium name |
| `team1`, `team2` | Participating teams |
| `toss_winner` | Team that won the toss |
| `toss_decision` | Decision made after toss (`bat` or `field`) |
| `winner` | Match-winning team |
| `result`, `result_margin` | Outcome and margin of victory |
| `target_runs`, `target_overs` | Targets for second innings |
| `super_over` | Indicates if a super over occurred |
| `method` | Victory method (e.g., DLS) |
| `umpire1`, `umpire2` | On-field umpires |


## 📁 2. `deliveries.csv`

This file includes granular ball-by-ball data for every delivery in every match.

### 🔑 Key Columns

| Column | Description |
|--------|-------------|
| `match_id` | Reference to match in `matches.csv` |
| `inning` | Inning number (1 or 2) |
| `batting_team`, `bowling_team` | Teams involved |
| `over`, `ball` | Over and ball number |
| `batter`, `bowler`, `non_striker` | Players participating in the delivery |
| `batsman_runs` | Runs scored off the bat |
| `extra_runs` | Runs awarded as extras |
| `total_runs` | Total runs for the ball |
| `extras_type` | Type of extra (e.g., wide, no-ball) |
| `is_wicket` | Whether a wicket fell (1 or 0) |
| `player_dismissed` | Dismissed batter's name |
| `dismissal_kind` | Type of dismissal |
| `fielder` | Fielder involved (if any) |


## 📌 Notes

- Data was cleaned and preprocessed using **Python (Pandas)** and **SQL** before being used for visualization in Tableau.
- These files power an interactive dashboard for analyzing toss decisions and performance trends across IPL seasons.
