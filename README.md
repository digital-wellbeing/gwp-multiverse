# A multiverse analysis of the associations between internet use and well-being

This repository contains the code and simulated dataset associated with "A multiverse analysis of the associations between internet use and well-being" (Vuorre & Przybylski). 

- 

## Data

The Gallup dataset that we used is not publicly available. For researchers who have access to this dataset, place it in `data-raw/gallup/The_Gallup_042722.sav` to exactly reproduce our analyses. For other researchers, we have placed a simulated smaller dataset in `data/synthetic-gallup-data.csv.gz`.

## Reproduce

0a. If you have access to the Gallup dataset, place the provided SPSS data file in `data-raw/gallup/The_Gallup_042722.sav`. 
0b. If you do not have access to the Gallup dataset, change `path <- "data-raw/gwp.rds"` on line 97 of `ms.Rmd` to `path <- "data/synthetic-gallup-data.csv.gz"`
1. Recreate our R environment provided with {renv}: <https://cloud.r-project.org/web/packages/renv/index.html>
2. "knit" the `ms.Rmd` file. (e.g. `rmarkdown::render('ms.Rmd')`.)
3. (Optional) email Matti at m.j.vuorre@tilburguniversity.edu if you are unable to run the code.
