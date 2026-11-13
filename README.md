# Customer Segmentation · Data Quality, RFM & K-Means

A reproducible customer analytics exercise using **250 synthetic customer records**. It connects data cleaning, recency-frequency-monetary (RFM) scoring, and K-means clustering.

## Workflow

1. Generate synthetic customer, purchase, and spending features with seed 42.
2. Audit missing income, parse registration dates, and filter extreme income and birth-year values.
3. Aggregate spending and purchase counts into RFM features.
4. Assign quantile scores and illustrative segment labels.
5. Standardize five clustering features and inspect inertia and silhouette scores for K=2–6.
6. Fit K=3 and compare clusters with RFM segments.

## Recorded output

The saved run retains **247 records** after filtering. RFM labels include 17 Champions, 83 At Risk, 62 New / Promising, and 85 Standard / Hibernating customers.

## Scope and limitations

All customers are simulated. Segment names are rule-based labels, not validated business outcomes. The final K=3 is explicitly selected in the code; it is not automatically chosen from the diagnostics. Cluster stability and sensitivity to scaling, outliers, and the number of clusters remain useful next steps.

## Open the project

- [Analysis notebook](part1.ipynb)
- [Presentation](Part1_Segmentation.pptx)

## Run locally

Use Python 3 in an isolated environment:

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

Open the notebook and run all cells from top to bottom. Data is generated inside the notebook; no external dataset download is required.

Dependencies are listed without exact version pins; results may vary slightly across library versions.
