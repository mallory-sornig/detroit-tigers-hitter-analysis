# Detroit Tigers Offense Analysis
Detroit Tigers Hitter Analysis
Project Overview
This project analyzes Detroit Tigers hitters using traditional offensive statistics, Statcast expected metrics, quality-of-contact measures, and plate-discipline indicators.
The goal is to evaluate which hitters showed the strongest underlying offensive profiles and identify players whose actual results differed meaningfully from their expected performance.
Research Question
Which Detroit Tigers hitters show the strongest underlying offensive profiles, and whose actual results differ most from expected performance?
Data
The analysis uses 2026 Detroit Tigers hitting data from Baseball Savant / Statcast.
The primary analysis includes hitters with at least 100 plate appearances to reduce the impact of extremely small samples.
Metrics Used
- AVG
- OBP
- SLG
- OPS
- HR
- BB%
- K%
- Exit Velocity
- Hard-Hit %
- Barrel %
- wOBA
- xwOBA
- xBA
- xSLG
Methodology
Actual vs. Expected Performance
Three gap metrics were calculated:
xwOBA Gap
xwOBA - wOBA
A positive value indicates that expected offensive production was higher than actual production.
A negative value indicates that actual production exceeded expected production.
xSLG Gap
xSLG - SLG
AVG Gap
xBA - AVG
Players were classified as:
- Underperforming Expected Results: xwOBA Gap ≥ 0.025
- Outperforming Expected Results: xwOBA Gap ≤ -0.025
- Results Match Expectations: xwOBA Gap between -0.025 and 0.025
Plate Discipline
Plate discipline was evaluated using:
BB/K Ratio = BB% ÷ K%
Higher values generally represent stronger walk-to-strikeout profiles.
Offensive Sustainability Score
A custom Sustainability Score was created to summarize several underlying offensive indicators.
Each metric was converted to a percentile rank within the selected Tigers hitter sample.
The final score uses the following weights:
- xwOBA — 40%
- Hard-Hit % — 25%
- Barrel % — 20%
- BB/K Ratio — 15%
Formula:
100 × [(xwOBA Percentile × 0.40) + (Hard-Hit Percentile × 0.25) + (Barrel Percentile × 0.20) + (BB/K Percentile × 0.15)]
The Sustainability Score is a relative evaluation tool created for this project. It is not a predictive model or official MLB metric.
Visualizations
Actual vs. Expected Offensive Performance
This scatterplot compares actual wOBA with xwOBA.
The diagonal reference line represents:
wOBA = xwOBA
Players above the line produced less than their expected metrics suggested, while players below the line produced more than expected.

Quality of Contact
This chart compares Hard-Hit % and Barrel % to identify hitters producing the strongest contact.

Plate Discipline
This chart ranks hitters by BB/K Ratio.

Offensive Sustainability Score
This chart ranks Tigers hitters using the custom Sustainability Score.

Key Findings
- Riley Greene ranked first overall in the Sustainability Score, showing the strongest combined underlying offensive profile in the sample.
- Eduardo Valencia ranked second overall and displayed exceptional contact-quality metrics, although his actual offensive production substantially exceeded his expected metrics.
- Dillon Dingler ranked third, showing a balanced combination of expected production and quality of contact.
- Kevin McGonigle led the group in BB/K Ratio, demonstrating the strongest plate-discipline profile among the hitters analyzed.
- Matt Vierling had the largest positive xwOBA gap, meaning his expected offensive performance was notably stronger than his actual results.
- Eduardo Valencia had the largest negative xwOBA gap, suggesting his actual production significantly exceeded what his expected metrics indicated.
- Most hitters in the sample finished relatively close to their expected offensive performance.
Limitations
This analysis has several limitations:
- Rankings are relative only to the selected Detroit Tigers hitters, not all MLB hitters.
- Players had different numbers of plate appearances.
- Smaller samples are inherently less stable.
- Injuries and changes in playing time are not included.
- Park effects are not modeled.
- Opponent quality is not included.
- Platoon splits are not considered.
- Baserunning and defensive value are excluded.
- Expected statistics are descriptive estimates, not guarantees of future performance.
- Sustainability Score weights were selected specifically for this project.
Tools Used
- Microsoft Excel
- Baseball Savant / Statcast
- GitHub
