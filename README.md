# Liability Scale Heritability
An R package dervied from the code at https://github.com/svenojavee/LSH
published in the Amerian Journal of Human Genetics in 2022 (doi:
[10.1016/j.ajhg.2022.09.011](https://www.sciencedirect.com/science/article/pii/S0002929722004141)).

The authors have a Shiny webapp at
https://medical-genomics-group.shinyapps.io/h2liab/
# Installation
```R
devtools::install_github("carbocation/LSH")
```

# Usage example
```R
# devtools::install_github("carbocation/LSH")
library("LSH")

observed_scale_heritability=0.035
observed_scale_heritability_se=0.003
population_prevalence=0.10
sample_prevalence=0.25

h2g_liability <- LSH_ascertain(h2Obs=observed_scale_heritability, P=sample_prevalence, K=population_prevalence)

se <- LSH_ascertain_SE(h2Obs=observed_scale_heritability, SEh2Obs=observed_scale_heritability_se, P=sample_prevalence, K=population_prevalence)

print(paste0("liability threshold heritability: ", round(h2g_liability, 3),". std error: ", round(se, 3)))
# [1] "liability threshold heritability: 0.049. std error: 0.004"
```

---------
Original README is below
---------

# Low prevalence liability scale heritability

R convenience functions for calculating the ascertained or unascertained versions of liability scale heritability estimates, standard errors and different types of confidence intervals is available at `convenienceFunctions.R`.
