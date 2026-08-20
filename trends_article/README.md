# Trends article files

This folder contains everything needed to reproduce the trends article charts:

- `trends_article.ipynb` — the executed plotting notebook.
- `cfsr_megafile_codebook.csv` — survey variable and value labels.
- `cfsrALL_2020_2022.csv.zip` — raw survey rows from 2020 through 2022.
- `cfsrALL_2023_2025.csv.zip` — raw survey rows from 2023 through 2025.

Keep these files together and run `trends_article.ipynb`. The notebook reads both ZIP files directly and combines them automatically; the CSV files do not need to be unzipped or manually recombined.

The notebook requires Python with `pandas`, `numpy`, and `matplotlib`. Generated charts are saved in `trends_article_outputs/`.
