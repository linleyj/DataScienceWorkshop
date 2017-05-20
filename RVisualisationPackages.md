# R Packages for Data Visualisation

This document contains code to install the required R packages for the Data Visualisation work shop.

To run this code ensure that you have installed R 3.3.3 and a recent release of Rstudio (preferably 1.0.143), then:

* Open Rstudio
* Copy the first section of code into the R console and press Enter/Return and wait for the packages to install
* Copy the second section of code into the R console and press Enter/Return and wait for the packages to install

If you encounter errors, please try re-running the code.
There will be some time available to resolve software issues at the start of the workshop but it is preferable to have the software installed in advance if possible.

## 1 Install packages from CRAN

This code chunk will install contributed R packages from [CRAN](https://cran.r-project.org/) (The Comprehensive R Archive Network)

```
packages <- c("RJSONIO",
              "RColorBrewer",
              "clifro",
              "devtools",
              "data.table",
              "gapminder",
              "ggthemes",
              "ggvis",
              "gridExtra",
              "leaflet",
              "plotly",
              "praise",
              "reshape2",
              "rbokeh",
              "shiny",
              "shinydashboard",
              "swirl",
              "testthat",
              "tidyverse",
              "wordcloud")

install.packages(packages, repos="https://cran.stat.auckland.ac.nz")
```

## 2 Install packages from GitHub

This code chunk will install the latest R packages from [GitHub](https://github.com/) using [devtools](https://github.com/hadley/devtools)

```
## rmarkdown
devtools::install_github("rstudio/rmarkdown")

## knitr
devtools::install_github("yihui/knitr")

## javascript charts
devtools::install_github("ramnathv/rCharts")

## National Climate Database api
devtools::install_github("ropensci/clifro")

## emoji package
devtools::install_github("hadley/emo")
```

## 3 Trouble Shooting on Ubuntu 16

### RStudio not Working

On Ubutu 16+ the RStudio desktop version does not work due to missing deprecated dependencies. There are two options:

- Install RStudio server and run it by using your browser (http://localhost:8787)
- Use this receipe to install the missing dependencies (click)[http://stackoverflow.com/questions/38172943/r-studio-not-working-on-ubuntu-16-04(click)]
When using a fresh Ubuntu 16 install you might find that the dependencies XML and OpenSSL are missing. Before using the above receipe type the following:

```
sudo apt-get install libssl-dev
sudo apt-get install libxml2-dev
```
