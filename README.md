# Multilevel Modeling: Principles and Applications with `R`

## Introduction

This 3-day workshop at the University of Bamberg exposed participants to the rigorous application of multilevel models (MLMs) in the `R` statistical environment. Over the course of 3 days, we covered the fundamentals of such hierarchical linear models, starting from simple random-intercept specifications and advancing to more complex ones, which allow us to understand how an effect varies between contexts. During this progression we touched on estimation of MLMs, sample size considerations, and model fit criteria. In the last day of the class we discussed how MLMs can be used to model change over time, under the form of the longitudinal growth model, and practice estimating such a model. The class targeted participants who did not have previous contact with multilevel models, but who wished to gain working knowledge in the topic. The sessions were conducted entirely in
`R`, and the `lme4` and `nlme` packages. The theoretical material was primarily based on selected chapters from Gelman and Hill’s *Data Analysis using Regression and Multilevel/Hierarchical Models*, and Singer and Willett’s *Applied Longitudinal Data Analysis*, as well as shorter methodological articles, where needed.

## Course schedule

### Day 1

We quickly cover a key violation of OLS assumptions (*heteroskedasticity*) and how this frequently a cause for concern in hierarchical data. We extend standard OLS notation to hierarchical data, and show an example of a multilevel model with random intercepts that includes both unit-level and group-level predictors.

Using the example from the previous session, we discuss how the estimation of multilevel models happens, and how to interpret key quantities in the output of such models.

We run a basic random-intercepts model in `R` to show the basics of the `lme4` package: syntax for a multilevel model, and the similarities and differences with syntax for a OLS model. We also cover key aspects related to data management for such models: ID variables, and merging data at multiple levels.

Readings:

- Gelman, Andrew, and Jennifer Hill. 2007. *Data Analysis using Regression and Multilevel / Hierarchical Models*. New York: Cambridge University Press. Chapters 1, 11, and 12.

Optional readings:

- Snijders, Tom A. B., and Roel J. Bosker. 1999. *Multilevel Analysis: An introduction to basic and advanced multilevel modeling*. London: Sage. Chapters 2, 3, and 4.
- Bickel, Robert. 2007. *Multilevel Analysis for Applied Research: It’s Just Regression!* New York: Guilford Press. Chapters 2 and 3.
- Gill, Jeff, and Andrew J. Womack. 2013. “The Multilevel Model Framework.” In Marc A. Scott, Jeffrey S. Simonoff, and Brian D. Marx. *The SAGE Handbook of Multilevel Modeling*. Los Angeles: Sage Publications. Chapter 1 (pp. 3–20).
- Scott, Marc A., Patrick E. Shrout, and Sharon L. Weinberg. 2013. “Multilevel Model Notation—Establishing the Commonalities.” In Marc A. Scott, Jeffrey S. Simonoff, and Brian D. Marx. *The SAGE Handbook of Multilevel Modeling*. Los Angeles: Sage Publications.
Chapter 2 (pp. 21–38).

### Day 2

We advance to more complex specifications, by allowing a coefficient to vary across groups using random slopes. We discuss the interpretation of key estimates from such models, as well as how to present results from them.

We cover how to assess model fit in the multilevel framework, and what minimum/optimal sample sizes are required to run these analyses.

Continuing with the example from the preceding day, we go over how to estimate random slopes specifications in `lme4`, and how to present results for cross-level interactions from these models. Additionally, we show how to assess model fit, and how to export pre-formatted results from these models for quick use in manuscripts.

Readings:

- Gelman, Andrew, and Jennifer Hill. 2007. *Data Analysis using Regression and Multilevel / Hierarchical Models*. New York: Cambridge University Press. Chapter 13.
- McNeish, Daniel M., and Laura M. Stapleton. 2016. “The Effect of Small Sample Size on Two-Level Model Estimates: A Review and Illustration.” *Educational Psychology Review* **28**(2): 295–314.
• Steele, Russell. 2013. “Model Selection for Multilevel Models.” In Marc A. Scott, Jeffrey S.Simonoff, and Brian D. Marx. *The SAGE Handbook of Multilevel Modeling*. Los Angeles: Sage Publications. Chapter 7 (pp. 109–126).

Optional readings:

- Enders, Craig K., and Davood Tofighi. 2007. “Centering Predictor Variables in Cross-Sectional Multilevel Models: A New Look at an Old Issue.” *Psychological Methods* **12**(2): 121–138.
- Snijders, Tom A. B., and Johannes Berkhof. 2008. “Diagnostic Checks for Multilevel Models.” In J. de Leeuw & E. Meijer (Eds.), *Handbook of Multilevel Analysis*. Springer: New York. Chapter 3 (pp. 141–175).
- Raudenbush, Stephen W., and Anthony S. Bryk. 2002. *Hierarchical Linear Models: Applications and Data Analysis Methods*. Advanced Quantitative Techniques in the Social Sciences. Thousand Oaks, CA: Sage Publications. Chapter 9.
- McNeish, Daniel M. 2017. “Small Sample Methods for Multilevel Modeling: A Colloquial Elucidation of REML and the Kenward-Roger Correction.” *Multivariate Behavioral Research* **52**(5): 661–670.
- Snijders, Tom A. B., and Roel J. Bosker. 1999. *Multilevel Analysis: An introduction to basic and advanced multilevel modeling*. London: Sage. Chapter 5.

### Day 3

We discuss simple adaptations to the MLM framework that allow it to capture temporal dynamics, and show the commonalities between this new setup and the previous one using notation. We also focus on a few topics specific to growth curve modeling using MLMs: working with time-varying and time-invariant predictors, how to plot and model trajectories of change, and how to present predictions from these models.

We start from an applied example that will help make us familiar with the data structure, and with how to visualize change over time in our units. We also estimate our first MLM model for temporal change using only time-varying predictors, relying on the additional flexibility provided by the `nlme` package.

In the second part of the lab session, we gradually introduce time-invariant predictors, and use them to explain why growth curves trajectories vary between units.

Readings:

- Singer, Judith D., and John B. Willett. 2003. *Applied Longitudinal Data Analysis: Modeling Change and Event Occurrence*. New York: Oxford University Press. Chapters 3, 4, 5, and 6.

Optional readings:

- Singer, Judith D., and John B. Willett. 2003. *Applied Longitudinal Data Analysis: Modeling Change and Event Occurrence*. New York: Oxford University Press. Chapter 7.
- Laird, Nan M., and Garrett M. Fitzmaurice. 2013. “Longitudinal Data Modeling.” In Marc A. Scott, Jeffrey S. Simonoff, and Brian D. Marx. *The SAGE Handbook of Multilevel Modeling*. Los Angeles: Sage Publications. Chapter 9 (pp. 141–160).
- Núñez-Antón, Vicente, and Dale L. Zimmerman. “Complexities in Error Structures Within Individuals.” In Marc A. Scott, Jeffrey S. Simonoff, and Brian D. Marx. *The SAGE Handbook of Multilevel Modeling*. Los Angeles: Sage Publications. Chapter 10 (pp. 161–182).
- Hox, Joop J. 2010. *Multilevel Analysis: Techniques and Applications*. 2nd edition. New York: Routledge. Chapter 5.
- Goldstein, Harvey. 2011. *Multilevel Statistical Models*. 4th edition. London: Wiley. Chapter 5.