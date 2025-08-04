# Modelling-U.S.-Home-Prices-Using-Bayesian-Hierarchical-Regression
Modelling U.S. Home Prices Using Bayesian Hierarchical Regression
Overview
In this project, developed in collaboration with a fellow coursemate, we analyzed the variation in U.S. home prices using a Bayesian hierarchical modeling approach. The dataset included over 20,000 observations from neighborhoods across North America, with variables covering socio-demographics, housing characteristics, and geographical proximity to the ocean.

The primary goals were to:

Investigate how ocean proximity affects median house values.

Model the effect of covariates (e.g., income, housing age) across groups using Bayesian hierarchical regression.

Methods
We applied two main modeling frameworks:

1. Hierarchical Model (Varying Intercepts Only)
Groups based on ocean proximity levels.

Posterior estimation via Gibbs Sampling.

Parameters: group-specific means, common variance, between-group variance.

2. Hierarchical Linear Regression
Group-specific intercepts + shared slopes (β) across all groups.

Priors placed on all model components, including a Wishart prior on the precision matrix of the regression coefficients.

Inference through Gibbs Sampling with custom update steps for each parameter.

Other methods and techniques:

Exploratory data analysis: boxplots, smoothed trends by group.

Convergence diagnostics: traceplots, ACF, and Geweke test.

Posterior predictive checks and simulation for new hypothetical neighborhoods.

Main Findings
Median house values varied significantly by ocean proximity: Inland areas had notably lower prices.

Income, housing age, and household size were among the most impactful covariates, with clear and significant posterior effects.

Posterior estimates were stable and showed good convergence properties.

The Bayesian approach allowed for group-level structure and uncertainty quantification not captured in standard regression.

Dataset Source
The data was sourced from Kaggle and originally published on Zenodo by researchers. Each row corresponds to a U.S. neighborhood in 2012, with the following variables:

Median house value (response)

Housing median age

Total rooms and bedrooms

Population and households

Median income

Ocean proximity (categorical)

Notes
All code is implemented in R.

Sampling and diagnostics can be replicated via the included .R scripts.

The project demonstrates the use of Bayesian hierarchical modeling for grouped regression problems with real-world interpretability.
