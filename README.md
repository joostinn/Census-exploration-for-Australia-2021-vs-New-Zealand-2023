# Census exploration: Australia 2021 vs New Zealand 2023

This project compares workforce industry structure and qualifications using Australia's 2021 Census and New Zealand's 2023 Census. The analysis covers 19 industry divisions and asks whether differences in qualification levels are associated with countries having different industry mixes or with different qualification profiles within the same industries.

The analysis and visualisations are in [`CITS2402-Project-25174009-24754702-25305007.ipynb`](CITS2402-Project-25174009-24754702-25305007.ipynb).

## What the notebook does

- Compares the industry mix of workers with comparable post-school qualifications.
- Examines qualification profiles and Bachelor-level-or-higher shares within each industry.
- Summarises results across four broad sectors.
- Decomposes national qualification-share differences into industry-mix and within-industry effects.
- Checks how classifying New Zealand Level 3 certificates affects the comparison.
- Extends the analysis to the whole workforce, including workers without post-school qualifications.

The notebook includes data checks, charts, interpretations, conclusions, and limitations. Since the data are from different census years and classification systems, the results are descriptive comparisons rather than evidence of cause and effect.

## Data files

All input CSV files are included in the repository and are expected to be in the same directory as the notebook.

| Files | Source and use |
| --- | --- |
| `2021Census_G53A_AUS_AUS.csv`, `2021Census_G53B_AUS_AUS.csv`, `2021Census_G53C_AUS_AUS.csv` | Australian Bureau of Statistics (ABS), 2021 Census General Community Profile tables G53A–G53C; non-school qualifications by industry. |
| `2021Census_G54A_AUS_AUS.csv`, `2021Census_G54B_AUS_AUS.csv`, `2021Census_G54C_AUS_AUS.csv`, `2021Census_G54D_AUS_AUS.csv` | ABS, 2021 Census General Community Profile tables G54A–G54D; employed persons by industry, used for the whole-workforce extension. |
| `STATSNZ_CEN23_EDU_003_1_0_2023_9999___99.csv` | Stats NZ, 2023 Census table CEN23_EDU_003, highest qualification by industry and gender. |

The ABS data are split across multiple wide-format files; the Stats NZ data are in a long-format CSV. The notebook combines and reshapes them for comparison. See the notebook's data and provenance section for details of the source-table selections and harmonisation.

## Run the analysis

Use Python 3 with Jupyter Notebook or JupyterLab. The notebook uses `pandas`, `numpy`, `matplotlib`, and IPython's display utilities.

Install the packages if needed:

```bash
python -m pip install jupyter pandas numpy matplotlib
```

From the repository directory, launch Jupyter and open the notebook:

```bash
jupyter notebook
```

Run the notebook cells from top to bottom. Keep the notebook and all CSV files together in the same directory so its relative input-file paths resolve.

## References

- Australian Bureau of Statistics. (2021). *Census of Population and Housing: General Community Profile, Tables G53 and G54* [Data set]. ABS Census DataPacks.
- Stats NZ. (2023). *2023 Census: Highest qualification, industry, and gender for the employed census usually resident population count aged 15 years and over* [Data set]. Aotearoa Data Explorer.
