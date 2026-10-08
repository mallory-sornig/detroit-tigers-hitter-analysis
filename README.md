# Detroit Tigers Hitter Analysis

A baseball analytics project evaluating Detroit Tigers hitters using Statcast expected metrics, quality-of-contact indicators, and plate-discipline measures.

## Research Question

**Which Detroit Tigers hitters show the strongest underlying offensive profiles, and whose actual results differ most from expected performance?**

## Project Overview

This project compares traditional offensive production with Statcast expected statistics to identify:

- hitters with strong underlying offensive profiles
- players who may have underperformed their expected results
- players whose actual production exceeded expected metrics
- differences in quality of contact
- differences in plate discipline

The main analysis includes Detroit Tigers hitters with **100+ plate appearances**.

---

## Data

The analysis uses 2026 Detroit Tigers hitting data from **Baseball Savant / Statcast**.

Metrics included:

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

---

## Actual vs. Expected Offensive Performance

![Actual vs Expected](visuals/actual_vs_expected_fixed.png)

This scatterplot compares actual **wOBA** with **xwOBA**.

The diagonal reference line represents:

`wOBA = xwOBA`

- Above the line = expected production was higher than actual production
- Below the line = actual production exceeded expected production
- Near the line = actual and expected results were relatively similar

One of the main goals of this comparison is to identify hitters whose underlying performance may not be fully reflected in their traditional results.

---

## Quality of Contact

![Quality of Contact](visuals/quality_of_contact_python.png)

This chart compares **Hard-Hit %** with **Barrel %**.

Players toward the upper-right of the chart combine frequent hard contact with a higher percentage of barrels, indicating stronger quality-of-contact profiles.

---

## Plate Discipline

![Plate Discipline](visuals/plate_discipline_python.png)

Plate discipline was evaluated using the following ratio:

`BB/K Ratio = BB% ÷ K%`

Higher values generally indicate a stronger walk-to-strikeout profile.

Kevin McGonigle stood out in this analysis with the strongest BB/K Ratio among the selected hitters.

---

## Offensive Sustainability Score

![Sustainability Score](visuals/sustainability_score_python.png)

To summarize several underlying offensive indicators, I created a custom **Offensive Sustainability Score**.

The score combines:

| Metric | Weight |
|---|---:|
| xwOBA | 40% |
| Hard-Hit % | 25% |
| Barrel % | 20% |
| BB/K Ratio | 15% |

Each metric was converted into a percentile rank within the selected Tigers sample.

The final score was calculated as:

```text
Sustainability Score =
100 × [
(xwOBA Percentile × 0.40)
+ (Hard-Hit Percentile × 0.25)
+ (Barrel Percentile × 0.20)
+ (BB/K Percentile × 0.15)
]
