# spatial analysis project
# Opioid deaths in Colorado
- Poisson GLM model of expected overdose deaths by county in Colorado, covariates based on CDC research
- Evidence of Spatial Autocorrelation tested with Moran's-I, global statistic that identifies whether or not spatial autocorrelation is present anywhere
- p-values for Moran's-I calculated based on 500 Monte Carlo simulations
- Clusters identified with cluster evaluation permutation procedure

# Hypotheses
The expected number of overdose deaths for each county were modeled in two ways
1) Constant Risk Hypothesis - assumes all individiduals have teh same risk of overdose regardless of location. This is scaled only for population, no other factors are considered
2) Poisson GLM - expected number of deaths account for factors correlated with deaths from drug overdose. Variables were chosen based on research conducted by the CDC and include only statistically significant variables
![](https://github.com/dani-totten/spatial_stats/blob/main/poisson_vars.png)
