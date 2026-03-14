## [Live demo →](https://adrymmm.github.io/pca-visualiser)

# PCA Visualiser

Interactive exposition of Principal Component Analysis. Upload a CSV and step through the algorithm on your own data, with plain-English intuition and NumPy equivalents at each stage.

## Sections

1. **Upload** — CSV input; numeric columns detected automatically, dates and IDs excluded
2. **Data matrix** — raw data with notation
3. **Standardisation** — columns scaled to mean 0, std 1; before/after comparison
4. **Covariance matrix** — heatmap with hover tooltips
5. **Eigen-decomposition** — eigenvalues, scree plot, loadings, projection, and a 2D geometric illustration
6. **Summary** — full pipeline in one place

## Running

No build step. Open `index.html` directly, or serve locally:

```bash
python3 -m http.server 8000
```

## Data format

- CSV with a header row
- At least 2 numeric columns and 5 rows
- Missing values (`NA`, `NaN`, `null`) dropped row-wise
- Year, ID, and constant columns excluded automatically

Three sample datasets are built in (Iris, Wine quality, Body measurements).

## Notes

- Only dependency is [KaTeX](https://katex.org/) for math, loaded from CDN
- Eigen-decomposition uses the [Jacobi algorithm](https://en.wikipedia.org/wiki/Jacobi_eigenvalue_algorithm)
- All computation is client-side
