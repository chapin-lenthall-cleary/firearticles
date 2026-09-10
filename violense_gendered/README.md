# Violence datapost plots through 2026

This folder contains a self-contained, GitHub-ready reproduction of the 2026
violence datapost plotting notebook. The recreated notebook reads the
longitudinal megafile directly rather than combining separate historical and
2026 survey files.

## Files

- `violense_datapost_plots_2026.ipynb` — executed notebook with all outputs
- `cfsr_megafile_codebook_2027.csv` — codebook for the longitudinal megafile
- `question_answer_wording_2020_2026.md` — year-by-year violence, ideology,
  and gender question and answer wording, with source and comparability notes
- `cfsrALL_2027.csv.z01` and `cfsrALL_2027.csv.zip` — the two parts of the
  compressed `cfsrALL_2027.csv`
- `SHA256SUMS.txt` — checksums for the packaged files and extracted CSV
- `charts/violense_datapost_plots_2026/` — the 14 exported chart files

The 34 MB compressed archive is split into a 20 MB part and a 14 MB part so
that each file can also be uploaded through GitHub's browser interface. Keep
the two parts together and do not rename either one.

## Reproduce the notebook

From this folder, first join the split ZIP and then extract the data:

```bash
zip -s 0 cfsrALL_2027.csv.zip --out cfsrALL_2027.full.zip
unzip cfsrALL_2027.full.zip
```

Then execute the notebook:

```bash
MPLBACKEND=Agg MPLCONFIGDIR=/tmp/mplconfig \
  jupyter nbconvert --execute --to notebook --inplace \
  violense_datapost_plots_2026.ipynb
```

The notebook expects `cfsrALL_2027.csv` and
`cfsr_megafile_codebook_2027.csv` in its working directory. Their paths can
alternatively be supplied with the `CFSR_MEGAFILE_PATH` and
`CFSR_CODEBOOK_PATH` environment variables.

The notebook requires Python with Jupyter, pandas, NumPy, and Matplotlib.

## Verification

The notebook was executed from start to finish using only the packaged
megafile and codebook. All 11 nonempty code cells ran without errors. Each of
the 14 exported PNG files was byte-for-byte identical to the corresponding
output from the original two-source notebook.

The rejoined archive was tested successfully, and its extracted CSV has this
SHA-256 checksum:

```text
fd6bb5fd4867bc27db8e4581446dcb3e86ab658f39d8f7e40200e6c4746df891  cfsrALL_2027.csv
```
