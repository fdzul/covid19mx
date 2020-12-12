
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
devtools::install_github("fdzul/covid19mx")
```

Linux

``` r
# install.packages("remotes")
remotes::install_github("fdzul/covid19mx")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
## basic example code
knitr::kable(head(covid19mx::covid19mx))
```

| FECHA\_ACTUALIZACION | ID\_REGISTRO | ORIGEN | SECTOR | ENTIDAD\_UM | SEXO | ENTIDAD\_NAC | ENTIDAD\_RES | MUNICIPIO\_RES | TIPO\_PACIENTE | FECHA\_INGRESO | FECHA\_SINTOMAS | FECHA\_DEF | INTUBADO | NEUMONIA | EDAD | NACIONALIDAD | EMBARAZO | HABLA\_LENGUA\_INDIG | INDIGENA | DIABETES | EPOC | ASMA | INMUSUPR | HIPERTENSION | OTRA\_COM | CARDIOVASCULAR | OBESIDAD | RENAL\_CRONICA | TABAQUISMO | OTRO\_CASO | TOMA\_MUESTRA\_LAB | RESULTADO\_LAB | TOMA\_MUESTRA\_ANTIGENO | RESULTADO\_ANTIGENO | CLASIFICACION\_FINAL | MIGRANTE | PAIS\_NACIONALIDAD | PAIS\_ORIGEN | UCI |
|:---------------------|:-------------|-------:|-------:|------------:|-----:|-------------:|-------------:|---------------:|---------------:|:---------------|:----------------|:-----------|---------:|---------:|-----:|-------------:|---------:|---------------------:|---------:|---------:|-----:|-----:|---------:|-------------:|----------:|---------------:|---------:|---------------:|-----------:|-----------:|-------------------:|---------------:|------------------------:|--------------------:|---------------------:|---------:|:-------------------|:-------------|----:|
| 2020-12-11           | 02ab03       |      2 |     12 |          26 |    1 |           26 |           26 |             30 |              1 | 2020-03-31     | 2020-03-28      | 9999-99-99 |       97 |        2 |   18 |            1 |        2 |                    2 |        2 |        2 |    2 |    2 |        2 |            2 |         2 |              2 |        2 |              2 |          2 |          1 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |  97 |
| 2020-12-11           | 11c483       |      1 |     12 |          29 |    1 |           29 |           29 |             33 |              1 | 2020-04-01     | 2020-03-28      | 9999-99-99 |       97 |        2 |   43 |            1 |        2 |                    2 |        2 |        1 |    2 |    2 |        2 |            2 |         2 |              2 |        2 |              2 |          2 |          2 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |  97 |
| 2020-12-11           | 156b1d       |      1 |      9 |           9 |    1 |            9 |            9 |              4 |              1 | 2020-03-14     | 2020-03-11      | 9999-99-99 |       97 |        2 |   42 |            1 |        2 |                    2 |        2 |        2 |    2 |    1 |        2 |            2 |         2 |              2 |        2 |              2 |          1 |          1 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |  97 |
| 2020-12-11           | 02d87b       |      2 |     12 |           2 |    2 |            2 |            2 |              2 |              1 | 2020-03-18     | 2020-03-17      | 9999-99-99 |       97 |        2 |   40 |            1 |       97 |                    2 |        2 |        2 |    2 |    2 |        1 |            2 |         2 |              2 |        2 |              2 |          2 |          1 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |  97 |
| 2020-12-11           | 05f3d3       |      1 |     12 |           9 |    2 |            9 |            9 |              7 |              2 | 2020-02-27     | 2020-02-22      | 9999-99-99 |        2 |        1 |   36 |            1 |       97 |                    2 |        2 |        2 |    2 |    2 |        2 |            2 |         2 |              2 |        2 |              2 |          1 |          1 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |   1 |
| 2020-12-11           | 058df2       |      2 |     12 |          21 |    2 |            7 |           21 |            114 |              1 | 2020-03-23     | 2020-03-18      | 9999-99-99 |       97 |        2 |   44 |            1 |       97 |                    2 |        2 |        2 |    2 |    2 |        2 |            2 |         2 |              2 |        2 |              2 |          2 |          1 |                  1 |              1 |                       2 |                  97 |                    3 |       99 | México             | 97           |  97 |
