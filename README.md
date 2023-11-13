# A multiverse analysis of the associations between internet use and well-being

- Matti Vuorre
- Andy Przybylski

This repository contains the code and simulated dataset associated with "A multiverse analysis of the associations between internet use and well-being" (Vuorre & Przybylski). 

- preprint: <https://doi.org/10.31234/osf.io/jp5nd>
- repository: <https://github.com/digital-wellbeing/gwp-multiverse>
- archive: <https://doi.org/10.5281/zenodo.7774923>

# Reproduce

## Environment

We coded the analyses in [R](https://www.r-project.org/), and used [renv](https://cloud.r-project.org/web/packages/renv/index.html) to manage the project's R environment. To ensure that you run computations in the same environment, first restore it with `renv::restore(prompt = FALSE)`.

### Environment variables

Use the variables in `.Renviron` to e.g. point to a local GWP data file, or use a number of CPUs more appropriate to your machine.

- `MAX_CORES`
  - Number of CPUs to use. 
- `DATA_PATH_GWP`
  - Path to the actual GWP data. 
- `DATA_PATH_GWP_CLEAN`
  - Path to cleaned GWP data
- `DATA_PATH_SYN`
  - Location of the synthetic data file.

## Data

If you do not have access to the GWP data, we provide a small simulated dataset for reproducibility. If you do have access, modify environment variables (above) accordingly.

## Run computations

All the code needed for our analyses is in `ms.Rmd`, an R Markdown file that can be "rendered" to a PDF. You can either run code in that file manually, or `rmarkdown::render('ms.Rmd')` to produce the PDF. Note however that you'll need a working LaTeX installation for the latter.

## Help

If all else fails, please email Matti at mjvuorre@uvt.nl.
