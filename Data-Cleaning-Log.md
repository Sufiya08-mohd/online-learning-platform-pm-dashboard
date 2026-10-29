# Data Cleaning Log

Source: `signups_raw.csv` (simulated). Output: `signups_clean.csv`.

| Step | Count |
|---|---|
| raw rows | 300 |
| exact duplicate rows removed | 15 |
| course category values standardized | 22 |
| blank course category -> 'Uncategorized' | 4 |
| traffic source values standardized | 18 |
| blank traffic source -> 'Unknown' | 8 |
| paid/free case fixed | 12 |
| blank completion % (left blank, excluded from averages) | 6 |
| clean rows | 285 |
