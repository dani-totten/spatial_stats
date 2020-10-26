# spatial analysis project
# Opioid deaths in Colorado
- Poisson GLM model of expected overdose deaths by county in Colorado, covariates based on CDC research
- Evidence of Spatial Autocorrelation tested with Moran's-I, global statistic that identifies whether or not spatial autocorrelation is present anywhere
- p-values for Moran's-I calculated based on 500 Monte Carlo simulations
- Clusters identified with poisson spatial scan
- South-Central Colorado has a cluster of excess opioid overdose deaths

# Hypotheses
The expected number of overdose deaths for each county were modeled in two ways
1) Constant Risk Hypothesis - Assumes all individiduals have teh same risk of overdose regardless of location. This is scaled only for population, no other factors are considered,
2) Poisson GLM - Expected number of deaths account for factors correlated with deaths from drug overdose. Variables were chosen based on research conducted by the CDC and include only statistically significant variables. Population weighting was also included in the model.
![](https://github.com/dani-totten/spatial_stats/blob/main/poisson_vars.png)

Residual differences between observed and expected counts of overdose deaths by county are larger for the constant risk hypothesis
![](https://github.com/dani-totten/spatial_stats/blob/main/spatial_side_by_side.png)

# Moran's-I Test of Spatial Autocorrelation
Moran's-I test used to detect global autocorrelation, ie; whether or not autocorrelation is present. Excess deaths modeled by both the CRH and Poisson GLM have significant p-values, signifying that autocorrelation is present and therefore there is some dependency between counties based on their proximity to one another

# Identifying clusters
After identifying the presence of autocorrelation, I used a few methods to identify clusters. Null hypotheses varied slightly, but all tests were in agreement that a cluster of excess overdose deaths was present in south-central Colorado
![](https://github.com/dani-totten/spatial_stats/blob/main/Screen%20Shot%202020-10-26%20at%2011.15.56%20AM.png)
