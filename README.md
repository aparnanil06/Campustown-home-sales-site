# Median home sale price in 18 college towns

A public website that shows the median sale price of homes sold near 11 US university campuses, by city, from the College-town home sales dataset.

## What this site is for

This site answers one question: what do homes near college campuses sell for, city by city? It is for students and anyone comparing college towns. The page shows a bar chart and a table, both computed from `data/college_town_home_sales.csv` when the page loads. Each bar ends at the median, and a line shows the middle half of sales.

## Live site

https://aparnanil06.github.io/Campustown-home-sales-site/

## Data notes

- **Rule:** sales under $1,000 are left out, as the data description sheet recommends. Four of the 35,442 sales are under $1,000, so 35,438 sales are counted.
- **Median sale price:** for each city, the middle sale price of the counted sales. Where a city has an even number of sales, it is the average of the two middle prices.
- **Middle half of sales:** the 25th and 75th percentiles of the counted sales in each city, using linear interpolation (the same method as Excel's `PERCENTILE.INC`). The line on the chart runs between them.
- **Cities:** each city is grouped by its `city` and `state` values as they appear in the dataset, 18 in all.
- **Sales counted:** the number of sales in each city after the rule is applied.
- **Source:** values are as reported by the collection source in March 2026. They have not been checked against county records.

## Repository contents

| Path | What it is |
|---|---|
| `index.html` | The website: a plain HTML, CSS and JavaScript page |
| `data/college_town_home_sales.csv` | The dataset, version 1.0. The site reads this file. |
| `data/college_town_home_sales.xlsx`, `.sqlite`, `.duckdb`, `.parquet` | The same data in other formats, for checking numbers |
| `docs/data_description_sheet.md` | What every column means, and the problems in the data |
| `AGENTS.md` | Project instructions for the AI coding agent |
| `AGENT_LOG.md` | A log of agent sessions |
| `.github/workflows/pages.yml` | Publishes the site to GitHub Pages on each push to `main` |