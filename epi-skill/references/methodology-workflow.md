# Methodology Workflow

Use this workflow for epidemiology, clinical statistics, bioinformatics, and biomedical methods tasks.

## 1. Frame The Claim

Classify the requested claim before choosing methods:

- Descriptive: estimate frequency, distribution, burden, or trend.
- Association: estimate relation between exposure and outcome without causal wording.
- Prediction: estimate future or current outcome probability for individuals.
- Diagnostic/prognostic test: estimate discrimination, calibration, sensitivity, specificity, likelihood ratios, and decision thresholds.
- Causal: estimate effect under an intervention or exposure contrast.
- Mechanistic/bioinformatics: identify molecular patterns, pathways, or biomarkers, usually exploratory unless externally validated.

Define PECO/PICO, time zero, eligibility, exposure window, comparator, outcome window, follow-up, estimand, and analysis population.

## 2. Audit Data Before Analysis

Create an inventory before writing final scripts:

- Source files, tables, sheets, encodings, dimensions, keys, units, and date ranges.
- First rows and codebook for each candidate table.
- Inclusion/exclusion counts and denominator flow.
- Exposure, outcome, covariate, censoring, and follow-up definitions.
- Missingness by variable, group, time point, and outcome status.
- Duplicate records, impossible dates, outliers, batch effects, and coding drift.
- Whether derived variables are reproducible from raw fields.

Do not assume variable names, event definitions, or coding from filenames.

## 3. Choose Design

Use design to control bias before modeling:

- Cross-sectional: estimate prevalence and associations at one time; avoid temporal or causal claims.
- Cohort: define time zero and follow-up; address censoring, competing risk, time-varying exposure, and immortal time.
- Case-control: define source population, sampling, index date, exposure window, matching, and odds-ratio interpretation.
- Trial: define randomization, allocation, adherence, intention-to-treat, per-protocol, safety, and protocol deviations.
- Diagnostic/prognostic: define target condition, reference standard, intended use, threshold, and validation sample.
- Prediction: separate model development, internal validation, external validation, calibration, and clinical utility.
- Bioinformatics: define sample processing, QC, normalization, batch correction, multiple testing, annotation, validation, and biological interpretation.
- Meta-analysis: define eligibility, outcome harmonization, effect measure, heterogeneity, risk of bias, publication bias, and sensitivity.

## 4. Bias And Confounding

For causal or etiologic language, draw or describe a causal structure:

- Confounding: common causes of exposure and outcome, measured before exposure.
- Selection bias: sampling, loss to follow-up, conditioning on colliders, survival/healthy-user effects.
- Information bias: misclassification, detection bias, recall bias, differential measurement, reference-standard errors.
- Time bias: immortal time, time-lag, depletion of susceptibles, reverse causation.
- Model-induced bias: overadjustment, mediator adjustment, collider adjustment, sparse-data bias.

Prefer pre-specified confounders from domain knowledge and DAGs. Do not select confounders only by statistical significance.

## 5. Analysis Plan

Specify before interpretation:

- Primary outcome, primary exposure, primary contrast, and primary effect measure.
- Descriptive table: denominators, missingness, standardized differences when comparing groups.
- Model family: linear, logistic, log-binomial, Poisson/negative-binomial, Cox, flexible survival, mixed model, GEE, ordinal/multinomial, quantile, Bayesian, or nonparametric.
- Time scale and censoring handling for longitudinal/survival outcomes.
- Clustered, repeated, matched, weighted, or survey design handling.
- Nonlinearity, interactions, effect modification, and subgroup rules.
- Multiple testing correction or hierarchy.
- Missing data method: complete-case justification, multiple imputation, inverse-probability weighting, or sensitivity analysis.
- Diagnostics: residuals, influence, proportional hazards, calibration, discrimination, overdispersion, convergence, separation, and influential observations.

## 6. Sensitivity And Robustness

Use sensitivity analyses to test the assumptions most likely to break the conclusion:

- Alternative exposure/outcome definitions.
- Lagged exposure windows and washout periods.
- Additional or restricted confounder sets.
- Negative controls when available.
- E-values or quantitative bias analysis for unmeasured confounding.
- Competing-risk or censoring alternatives.
- Complete-case versus imputed analysis.
- Exclusion of influential observations or high-risk-of-bias studies.
- External validation or replication in independent data.

## 7. Interpretation

Interpret in layers:

- Estimate: direction, magnitude, uncertainty, denominator, time scale, and clinical meaning.
- Identification: assumptions needed for the estimate to answer the target question.
- Robustness: whether sensitivity analyses agree.
- Generalizability: population, setting, measurement, and calendar-time limits.
- Claim boundary: descriptive, associational, predictive, diagnostic, causal, or clinical utility.

Write limitations as methodological constraints, not generic disclaimers.
