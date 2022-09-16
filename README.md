# Facebook adoption and well-being

Code supporting *Estimating the association between Facebook adoption and well-being* (Vuorre & Przybylski, [preprint]()).

This project uses proprietary data which cannot be shared. All the code used to analyse those data are here. This code was used in FB's research environment (FORT). To reproduce our analyses with actual Facebook and synthetic Gallup data, contact Facebook at <ccobb@fb.com> or <ss1-tech-support@fb.com>.

Open code and synthetic datasets: [![DOI](https://zenodo.org/badge/525367459.svg)](https://zenodo.org/badge/latestdoi/525367459)

- `data-prepare.Rmd`
  - Creates clean Gallup and and population datasets, and a synthetic Gallup dataset, to be uploaded to FORT
- `ms.Rmd`
  - Analysis code. Reproducible manuscript source written in R Markdown. This is run in FORT so it can access the FB data.
  
In FORT, open up an R console or notebook and run `rmarkdown::render("ms.Rmd")`.

## Data

### Facebook

If you are conducting the analyses in FORT, you have access to `data-raw/fb.csv`. Otherwise, we have created a simple simulated dataset at `data/fb-synthetic.rds`.

### Gallup

If you have access to Gallup's data, place the SPSS .sav file to `data-raw/Gallup/` and run `data-prepare.Rmd`. Otherwise, we created a synthetic dataset at `data/gwp-synthetic.rds`.

### Population data

Download the "Population by Single Age - Both Sexes (XLSX, 160.91 MB)" from <https://population.un.org/wpp/Download/Standard/Population/> ( <https://population.un.org/wpp/Download/Files/1_Indicators%20(Standard)/EXCEL_FILES/2_Population/WPP2022_POP_F01_1_POPULATION_SINGLE_AGE_BOTH_SEXES.xlsx>) to `data-raw/`. That is processed in `data-prepare.Rmd` to `data-raw/population.rds`, which you can load in the analysis.