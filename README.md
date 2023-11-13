# A multiverse analysis of the associations between internet use and well-being

- Matti Vuorre
- Andy Przybylski

This repository contains the code and simulated dataset associated with "A multiverse analysis of the associations between internet use and well-being" (Vuorre & Przybylski). 

- preprint: <https://doi.org/10.31234/osf.io/jp5nd>
- repository: <https://github.com/digital-wellbeing/gwp-multiverse>
- archive: <https://doi.org/10.5281/zenodo.7774923>

# Reproduce

## Environment

We coded the analyses in [R](https://www.r-project.org/).

We used [renv](https://cloud.r-project.org/web/packages/renv/index.html) to manage the project's R environment. To ensure that you run computations in the same environment, first restore ours with `renv::restore(prompt = FALSE)`.

### Environment variables

We provide an example `.Renviron` file (`example.Renviron`), which you should rename to `.Renviron` and modify according to your environment.

- `MAX_CORES=8`
  - Change this to use as many CPU cores as you'd like. The real data is big and there's thousands of models so keep that in mind. We used 8 which is the default here.
- `DATA_PATH_GWP="data-raw/gallup/The_Gallup_042722.sav"`
  - Path to the *real* GWP data. Uncomment this and modify to point to your local copy. Keep commented out if you don't have it.
- `DATA_PATH_SYN="data-synthetic/synthetic-data.rds"`
  - Location of the synthetic data file. You probably don't need to touch this.

## Data

If you do not have access to the GWP data, we provide a small simulated dataset for reproducibility. If you do have access, modify environment variables (above) accordingly.

## Run computations

All the code needed for our analyses is in `ms.Rmd`, an R Markdown file that can be "rendered" to a PDF. You can either run code in that file manually, or `rmarkdown::render('ms.Rmd')` to produce the PDF. Note however that you'll need a working LaTeX installation for the latter.

## Help

If all else fails, please email Matti at mjvuorre@uvt.nl.
