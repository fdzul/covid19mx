---
output: github_document
---

<!-- README.md is generated from README.Rmd. Please edit that file -->



# covid19mx

<!-- badges: start -->
[![Build Status](https://travis-ci.org/pages-themes/cayman.svg?branch=master)](https://travis-ci.org/pages-themes/cayman)
[![Gem Version](https://badge.fury.io/rb/jekyll-theme-cayman.svg)](https://badge.fury.io/rb/jekyll-theme-cayman)
![GitHub all releases](https://img.shields.io/github/downloads/fdzul/denhotspots/total?style=social)
<!-- badges: end -->


**covid19mx is a package developed in the department of prevention and control of diseases transmitted by vector of the [Secretary of Health of Veracruz](https://www.ssaver.gob.mx/) and with colaboration of the federal level**

The goal of covid19mx is to provide the Mexican COVID-19 (SARS-COV2) pandemic data into R.

## **overview**

**covid19mx** package has two dataset:

  - **covid19mx20** COVID-19 2020.
  - **covid19mx21** COVID-19 2021.



## Installation

You can install the released version of covid19mx from [CRAN](https://CRAN.R-project.org) with:

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
## covid19mx20 dataset

This is a basic example which shows you how to solve a common problem:


```r
## basic example code
knitr::kable(head(covid19mx::covid19mx20))
```



|FECHA_ACTUALIZACION |ID_REGISTRO | ORIGEN| SECTOR| ENTIDAD_UM| SEXO| ENTIDAD_NAC| ENTIDAD_RES| MUNICIPIO_RES| TIPO_PACIENTE|FECHA_INGRESO |FECHA_SINTOMAS |FECHA_DEF  | INTUBADO| NEUMONIA| EDAD| NACIONALIDAD| EMBARAZO| HABLA_LENGUA_INDIG| INDIGENA| DIABETES| EPOC| ASMA| INMUSUPR| HIPERTENSION| OTRA_COM| CARDIOVASCULAR| OBESIDAD| RENAL_CRONICA| TABAQUISMO| OTRO_CASO| TOMA_MUESTRA_LAB| RESULTADO_LAB| TOMA_MUESTRA_ANTIGENO| RESULTADO_ANTIGENO| CLASIFICACION_FINAL| MIGRANTE|PAIS_NACIONALIDAD |PAIS_ORIGEN | UCI|date       | year|
|:-------------------|:-----------|------:|------:|----------:|----:|-----------:|-----------:|-------------:|-------------:|:-------------|:--------------|:----------|--------:|--------:|----:|------------:|--------:|------------------:|--------:|--------:|----:|----:|--------:|------------:|--------:|--------------:|--------:|-------------:|----------:|---------:|----------------:|-------------:|---------------------:|------------------:|-------------------:|--------:|:-----------------|:-----------|---:|:----------|----:|
|2021-01-13          |071735      |      2|      9|         21|    2|          21|          21|           114|             1|2020-03-18    |2020-03-12     |9999-99-99 |       97|        2|   75|            1|       97|                  2|        2|        1|    2|    2|        2|            2|        2|              1|        2|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-12 | 2020|
|2021-01-13          |1c4583      |      2|     12|          9|    2|           9|           9|             4|             1|2020-03-30    |2020-03-30     |9999-99-99 |       97|        2|   23|            1|       97|                  2|        2|        2|    2|    2|        2|            2|        2|              2|        2|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-30 | 2020|
|2021-01-13          |0d55c9      |      2|     12|          9|    1|           9|           9|            16|             1|2020-03-26    |2020-03-24     |9999-99-99 |       97|        2|   28|            1|        2|                  2|        2|        2|    2|    2|        2|            2|        2|              2|        2|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-24 | 2020|
|2021-01-13          |002371      |      1|      4|          3|    2|           3|           3|             8|             1|2020-03-31    |2020-03-27     |9999-99-99 |       97|        2|   38|            1|       97|                  2|        2|        2|    2|    2|        2|            2|        2|              2|        2|             2|          2|        99|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-27 | 2020|
|2021-01-13          |11fb00      |      1|     12|          9|    2|           9|           9|            15|             1|2020-03-29    |2020-03-25     |2020-04-05 |       97|        1|   54|            1|       97|                  2|        2|        1|    2|    2|        2|            2|        2|              2|        2|             2|          2|         1|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-25 | 2020|
|2021-01-13          |092521      |      1|     12|          9|    1|           9|           9|            17|             1|2020-03-30    |2020-03-28     |9999-99-99 |       97|        2|   49|            1|        2|                  2|        2|        2|    2|    2|        2|            2|        2|              2|        2|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2020-03-28 | 2020|

## covid19mx21 dataset


```r
## basic example code
knitr::kable(head(covid19mx::covid19mx21))
```



|FECHA_ACTUALIZACION |ID_REGISTRO | ORIGEN| SECTOR| ENTIDAD_UM| SEXO| ENTIDAD_NAC| ENTIDAD_RES| MUNICIPIO_RES| TIPO_PACIENTE|FECHA_INGRESO |FECHA_SINTOMAS |FECHA_DEF  | INTUBADO| NEUMONIA| EDAD| NACIONALIDAD| EMBARAZO| HABLA_LENGUA_INDIG| INDIGENA| DIABETES| EPOC| ASMA| INMUSUPR| HIPERTENSION| OTRA_COM| CARDIOVASCULAR| OBESIDAD| RENAL_CRONICA| TABAQUISMO| OTRO_CASO| TOMA_MUESTRA_LAB| RESULTADO_LAB| TOMA_MUESTRA_ANTIGENO| RESULTADO_ANTIGENO| CLASIFICACION_FINAL| MIGRANTE|PAIS_NACIONALIDAD |PAIS_ORIGEN | UCI|date       | year|
|:-------------------|:-----------|------:|------:|----------:|----:|-----------:|-----------:|-------------:|-------------:|:-------------|:--------------|:----------|--------:|--------:|----:|------------:|--------:|------------------:|--------:|--------:|----:|----:|--------:|------------:|--------:|--------------:|--------:|-------------:|----------:|---------:|----------------:|-------------:|---------------------:|------------------:|-------------------:|--------:|:-----------------|:-----------|---:|:----------|----:|
|2021-01-13          |399e57      |      2|      5|         31|    2|           9|          31|            50|             1|2021-01-11    |2021-01-08     |9999-99-99 |       97|        2|   29|            1|       97|                  2|        2|        2|    2|    1|        2|            2|        2|              2|        2|             2|          2|         1|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2021-01-08 | 2021|
|2021-01-13          |3a8055      |      2|      9|         14|    2|          14|          14|            39|             2|2021-01-08    |2021-01-05     |2021-01-09 |        2|        1|   87|            1|       97|                  2|        2|        1|    2|    2|        2|            1|        2|              2|        2|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |   2|2021-01-05 | 2021|
|2021-01-13          |1e97ce      |      1|      4|          3|    1|           3|           3|             1|             2|2021-01-08    |2021-01-06     |9999-99-99 |        2|        2|   77|            1|        2|                  2|        2|        1|    2|    2|        2|            1|        2|              2|        2|             2|          2|         1|                1|             1|                     2|                 97|                   3|       99|México            |97          |   2|2021-01-06 | 2021|
|2021-01-13          |2c5789      |      1|      4|         19|    2|          10|          19|            39|             2|2021-01-08    |2021-01-02     |9999-99-99 |        2|        2|   81|            1|       97|                  2|        2|        1|    2|    2|        2|            1|        2|              2|        1|             2|          2|         1|                1|             1|                     1|                  1|                   3|       99|México            |97          |   2|2021-01-02 | 2021|
|2021-01-13          |1faffe      |      1|     12|         22|    2|          22|          22|            14|             1|2021-01-08    |2021-01-03     |9999-99-99 |       97|        2|   18|            1|       97|                  2|        2|        2|    2|    2|        2|            2|        2|              2|        2|             2|          2|         1|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2021-01-03 | 2021|
|2021-01-13          |248512      |      2|     12|         24|    1|          24|          24|            32|             1|2021-01-08    |2021-01-01     |9999-99-99 |       97|        2|   55|            1|        2|                  2|        2|        1|    2|    2|        2|            1|        2|              2|        1|             2|          2|         2|                1|             1|                     2|                 97|                   3|       99|México            |97          |  97|2021-01-01 | 2021|


