# Grammys Website Analytics

Python analysis of whether splitting one website into grammy.com and recordingacademy.com improved user engagement.

**Notebook:** [Analyzing-Website-Performance-Grammys.ipynb](Analyzing-Website-Performance-Grammys.ipynb)

This is a training project from the Global Career Accelerator program, completed for the **Python & Data (The Grammys Project) Certification**. The scenario and data come from the program. It is not work done for, or endorsed by, the Recording Academy.

## Context

In February 2022 the Recording Academy split its single site into two: grammy.com for the awards and fans, and recordingacademy.com for members and the music industry. The question was whether the split helped engagement, and what the Academy should do next. The analysis compares daily web traffic for the combined site before the split with each of the two sites after it.

## Tools and skills

- Python, pandas, Plotly Express, Jupyter
- Loading and previewing CSV data
- Splitting a time series at a cutoff date
- `groupby` comparisons, loops over several DataFrames, a small reusable function
- Combining data with `concat` and `merge`, renaming and dropping columns
- Line charts and grouped bar charts
- Turning results into a written business recommendation

## Approach

1. Charted daily visitors to see when traffic spikes.
2. Compared award nights with all other days.
3. Split the grammy.com data at 2022-02-01 into the combined site (before) and grammy.com alone (after).
4. Calculated pages per session, bounce rate and average time on site for the combined site, grammy.com and recordingacademy.com.
5. Combined the two age-demographics files and compared the sites with a grouped bar chart.
6. Wrote a recommendation memo for the Recording Academy.
7. LevelUp: merged the desktop and mobile visitor files, calculated the device split, and compared grammy.com with figures for the American Music Awards website.

## Key findings

- **Show night drives traffic.** Award nights averaged about 1.36 million more visitors than other days, and sessions ran longer (154 vs 98 seconds). Smaller spikes come when nominations are announced.
- **Bounce rate fell after the split.** 33.67% for recordingacademy.com and 40.16% for grammy.com, against 41.58% for the combined site.
- **Time on site moved in opposite directions.** recordingacademy.com rose to 128.5 seconds and grammy.com fell to 82.99 seconds, from 102.85 seconds on the combined site.
- **Pages per session went up after the split**, more for recordingacademy.com than for grammy.com.
- **The audiences differ by age.** recordingacademy.com draws more visitors aged 25 to 54. grammy.com draws more aged 18 to 24 and 55+.
- **Against the AMAs website**, grammy.com has a lower bounce rate (40.16% vs 54.31%), but AMA visitors stay much longer (353 vs 83 seconds). The AMA figures come from a dashboard screenshot supplied by the program, which is not included in this repo. Time on site and pages per session are the metrics grammy.com most needs to improve.

**Recommendation:** keep the two sites separate. The main trade-off is the cost of running two sites. grammy.com should add more recommended content to hold engagement outside nomination and award season, and borrow what keeps bounce rates low and pages per session high on recordingacademy.com.

## How to run

The data files are not included (see [datasets/README.md](datasets/README.md)). The notebook keeps its saved outputs, so it can be read on GitHub without running anything.

To run it yourself:

1. Place the six CSV files in `datasets/`.
2. Open `Analyzing-Website-Performance-Grammys.ipynb` in Jupyter and run the cells from the top.

Requirements: Python 3 (the notebook was saved with Python 3.10.6), pandas, plotly and Jupyter. Package versions were not recorded.

The AMAs dashboard image used in the LevelUp section is not included, so it shows as broken on GitHub (see [figs/README.md](figs/README.md)).

## Repo structure

```
grammys-website-analytics-python/
├── Analyzing-Website-Performance-Grammys.ipynb   analysis notebook with saved outputs
├── datasets/
│   └── README.md                                 which data files go here
└── figs/
    └── README.md                                 note on the image that is not included
```
