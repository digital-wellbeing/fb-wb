# Facebook adoption and well-being

Code supporting *Title* (Vuorre & Przybylski, [preprint]()).

This project uses proprietary data which cannot be shared. All the code used to analyse those data are here. This code was used in FB's research environment (FORT). To reproduce our analyses with actual Facebook and synthetic Gallup data, contact Facebook at <ss1-tech-support@fb.com>.

- `clean.qmd`
  - Creates clean Gallup and World Bank (population) datasets to be uploaded to FORT
- `ms.Rmd`
  - Analysis code. Reproducible manuscript source written in R Markdown. This is run in FORT so it can access the FB data.
  
In FORT, open up an R console or notebook and run `rmarkdown::render("Manuscript.Rmd", "all")`
