TABLEAU LINK:https://public.tableau.com/views/YashvardhankumarSA1IDAI101-240OMH0307UNIT4/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
  IPL Performance & Scoring Evolution Analysis
  Project Overview
Project Title: IPL Performance & Scoring Evolution Analysis
Purpose:This project analyzes Indian Premier League (IPL) data to identify performance trends, team dominance, venue influence, and the evolution of scoring patterns over time.

The objective is to use data visualization to:

 Examine whether IPL scoring has increased across seasons
 Identify topperforming batsmen and bowlers
 Analyze team success patterns
 Evaluate the impact of toss decisions
 Understand venuebased scoring behavior

Target Audience:
Cricket analysts, IPL fans, sports strategists, and decisionmakers interested in performance trends and match dynamics.


  Data Summary
 Data Sources
 `matches.csv` – Matchlevel information (season, venue, toss winner, match winner, etc.)
 `deliveries.csv` – Ballbyball match data (runs scored, wickets, players involved, etc.)
These datasets were connected in Tableau using the `match id` field to ensure accurate aggregation between matchlevel and deliverylevel data.
 Data Preparation & Cleaning
 Established relationship between `matches` and `deliveries` using match ID.
 Used Level of Detail (LOD) expressions to correctly calculate matchlevel metrics.
 Removed null winners (noresult matches) where necessary.
 Ensured proper aggregation (Average instead of Sum) for season and venue analysis.
 Sorted season data chronologically for accurate trend representation.
 Key Metrics Created
 Match Total Runs
  `{ FIXED [id] : SUM([batsman_runs]) }`
  Calculates total runs per match.
 Match Count
  `COUNTD([id])`
  Counts distinct matches.
 Strike Rate
  `(SUM([batsman_runs]) / COUNT([ball]))  100`
 Economy Rate
  `SUM([batsman_runs]) / (COUNT([ball]) / 6)`
 Toss Result Impact
  ```
  IF [toss_winner] = [winner]
  THEN "Won After Toss"
  ELSE "Lost After Toss"
  END
  ```

  Key Insights

  Scoring Trend: IPL scoring has steadily increased over time, with recent seasons showing the highest average total runs per match. This suggests evolution in batting strategies and powerhitting dominance.

  Venue Influence: Certain venues consistently produce higher scoring matches, indicating battingfriendly pitch conditions.

  Player Dominance: A small group of batsmen and bowlers significantly outperform others, demonstrating concentrated performance impact.

 Team Performance: Some franchises show longterm dominance in match wins, reflecting sustained competitive strength.

  Toss Impact: Toss advantage appears minimal, with win probability close to 50%, suggesting limited predictive impact on match outcomes.



Dashboard Features

The Tableau dashboard includes the following visualizations:

 1. Season Trend Analysis

 Line/bar visualization of average total runs per match across seasons.
 Displays scoring evolution over time.

 2️. Team Wins Comparison

 Bar chart showing total match wins by team.
 Sorted in descending order for quick identification of dominant franchises.

 3️. Top 10 Batsmen

 Ranked by total career runs.
 Highlights individual performance leaders.

 4️.Top 10 Bowlers

 Ranked by total wickets taken.
 Identifies consistent wickettaking bowlers.

 5️. VenueBased Scoring Analysis

 Average total runs per match at each venue.
 Highlights battingfriendly grounds.

 6️. Toss Impact Analysis

 Comparison of matches won after winning the toss vs losing the toss.
 Presented as percentage distribution.

 Navigation & Interaction
 Visuals are structured to guide users from macrolevel trends (season analysis) to microlevel insights (player performance).
 Charts are sortable and responsive within Tableau.
 Users can compare categories (teams, venues, seasons) directly through visual ranking.


  Relevant Screenshots

Below are screenshots from the project dashboard:

 🔹 Full Dashboard View


<img width="1508" height="985" alt="Screenshot 2026-02-20 190603" src="https://github.com/user-attachments/assets/3dc1fbde-68d3-4f16-8b15-40952e9d8071" />


 🔹 Season Trend Analysis

<img width="1410" height="943" alt="Screenshot 2026-02-20 190701" src="https://github.com/user-attachments/assets/febfdc6b-e48c-43c6-bf00-5b616264ce45" />


 🔹 Team Wins Analysis

<img width="1454" height="947" alt="Screenshot 2026-02-20 190721" src="https://github.com/user-attachments/assets/ac30e265-f6ce-4ffc-b4c5-b477f020dc14" />


 🔹 Venue Analysis

<img width="1433" height="955" alt="Screenshot 2026-02-20 190759" src="https://github.com/user-attachments/assets/e5825c98-2d89-4640-b6de-8984966fb1df" />


Conclusion

This analysis demonstrates that IPL has evolved into a higherscoring competition over time, driven by strategic batting aggression and tactical advancements. While individual and team dominance remain important, venue conditions significantly influence match outcomes. Toss advantage, however, appears statistically minimal.

Limitations
 The dataset does not account for rule changes across seasons.
 External factors such as weather, pitch preparation, and player injuries were not included.
 Advanced metrics such as pressure situations or match phase impact were not analyzed.

Future Improvements

 Incorporate win probability modeling.
 Add seasonwise strike rate and economy rate trends.
 Include advanced player impact metrics.
 Build interactive filters for dynamic exploration by season or team.



Tools Used

 Tableau (Data Visualization & Analysis)
 GitHub (Project Documentation & Version Control)

Name: yashvardhan kumar IDAI101-240OMH0307 CRS: Artificial Intelligence School: Birla Open Minds International School
