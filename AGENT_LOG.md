# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```

## 2026-11-19: Median sale price page with bar chart and table

- **Asked:** "1,000 and include a bar chart as well" (after the agent proposed a page of median sale price by city, computed from the CSV, leaving out sales under the threshold and stating the rule; the user chose the $1,000 rule to match the data description sheet).
- **Agent produced:** `index.html` rewritten as a plain HTML, CSS and JavaScript page. It reads `data/college_town_home_sales.csv` in the browser, leaves out sales under $1,000, computes the median sale price and sales count for each city, and shows a sorted bar chart and table. The page states the rule and the number of sales left out. No numbers are typed in by hand.
- **Checked or changed:** Ran the page in a headless browser and compared its 18 medians with a separate calculation from the CSV: all matched. The first phone-width screenshot showed the bars and value labels running past the right edge, so the chart now sizes itself to its container and redraws on resize. Checked again at 390 px and 900 px wide: no clipped labels and no horizontal page scroll.
