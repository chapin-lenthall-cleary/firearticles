# 2026 campus-speech trends follow-up

This package extends the five charts from [the original Expression post](https://expression.fire.org/p/violence-is-up-and-tolerance-is-down) through the 2026 survey wave.

## Files

- `trends_2026_followup.ipynb`: complete analysis and plot code.
- `data/trends_followup_analysis_data_2020_2026.csv.zip`: reduced, de-identified analysis extract from `cfsrALL_2027.csv`.
- `data/cfsr_megafile_codebook_2027.csv`: source codebook.
- `data/source_metadata.json`: source row counts and audited 2026 field dates; exact submission timestamps are excluded from the extract.
- `trends_article_outputs/`: rendered plots and audit tables.
- `trends_2026_followup_datapost.md` and `.docx`: article drafts with the plots in place.

## Reproduce

Run the notebook from this directory. It reads the ZIP in `data/`, validates year counts and key estimates, and rewrites every file in `trends_article_outputs/`.

The article's intended public code URL is [https://github.com/chapin-lenthall-cleary/firearticles/tree/main/trends_article_2026_followup](https://github.com/chapin-lenthall-cleary/firearticles/tree/main/trends_article_2026_followup). The folder must be uploaded there before publication.
