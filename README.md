
<!-- README.md is generated from README.Rmd. Please edit that file -->

# covid19mx

<!-- badges: start -->

[![Build
Status](https://travis-ci.org/pages-themes/cayman.svg?branch=master)](https://travis-ci.org/pages-themes/cayman)
[![Gem
Version](https://badge.fury.io/rb/jekyll-theme-cayman.svg)](https://badge.fury.io/rb/jekyll-theme-cayman)
![GitHub all
releases](https://img.shields.io/github/downloads/fdzul/denhotspots/total?style=social)
<!-- badges: end -->

**covid19mx is a package developed in the department of prevention and
control of diseases transmitted by vector of the [Secretary of Health of
Veracruz](https://www.ssaver.gob.mx/) and with colaboration of the
federal level**

The goal of covid19mx is to provide the Mexican COVID-19 (SARS-COV2)
pandemic data into R.

## **overview**

**covid19mx** .

-   **`gihi()`** calculate gi and hi local spatial statistic.
-   **`bivariate_map()`** generate a bivariate map.
-   **`subset_den()`** is a function for subset de dengue dataset.
-   **`data_geocoden()`** this function creates an address vector and
    replaces incorrect text.
-   **`geocoden()`** this function geocodes the addresses of the sinave
    database using Geocoding API.
-   **`save_geocoden()`** This function generates the RData file where
    it contains the geocoded data and the sinave dataset.
-   **`point_to_polygons()`** this function counts how many events for
    spatial uni.

## Installation

You can install the released version of covid19mx from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("covid19mx")
```

### Development version

To get a bug fix, or use a feature from the development version, you can
install denhotspots from GitHub.

Mac

``` r
# install.packages("devtools")
devtools::install_github("fdzul/denhotspots")
```

Linux

``` r
# install.packages("remotes")
remotes::install_github("fdzul/denhotspots")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
#library(covid19mx)
## basic example code
```
