# Study Design And Modeling Checklists

Use these as reviewer-facing audit lists.

## Observational Etiology

- Is time zero defined before exposure and outcome?
- Is the source population clear?
- Are inclusion/exclusion rules reproducible?
- Are exposure, comparator, outcome, and follow-up windows aligned?
- Are confounders measured before exposure?
- Are mediators, colliders, and post-exposure variables kept out of the primary adjustment set?
- Is the effect measure appropriate: risk difference, risk ratio, odds ratio, rate ratio, hazard ratio, or marginal contrast?
- Are missing data, censoring, and loss to follow-up described by exposure/outcome status?

## Cohort And Survival Analysis

- Define entry date, exit date, event, censoring, competing events, and time scale.
- Check immortal time and delayed entry.
- Check proportional hazards before relying on a single Cox hazard ratio.
- Consider absolute risk, cumulative incidence, restricted mean survival time, or flexible hazards when hazards are non-proportional.
- Use robust variance, frailty, mixed models, or GEE for clustering/repeated events when needed.

## Case-Control

- Define the underlying source population that generated cases.
- Use the same eligibility and exposure opportunity for cases and controls.
- Define index date for exposure ascertainment.
- For matched studies, account for matching in analysis.
- Interpret the odds ratio according to sampling design; do not automatically call it a risk ratio.

## Diagnostic And Prediction Studies

- Define intended use, target population, decision point, and reference standard.
- Split development, internal validation, and external validation.
- Report discrimination and calibration; AUC alone is insufficient.
- Report threshold performance: sensitivity, specificity, PPV, NPV, likelihood ratios, and decision-curve analysis when relevant.
- Avoid leakage: predictors must be available before the prediction time.
- Penalize or shrink high-dimensional models; report optimism correction.

## Clinical Trials

- Define allocation, masking, adherence, protocol deviations, and analysis populations.
- Keep intention-to-treat as the default effectiveness analysis unless the estimand differs.
- Pre-specify primary endpoint and multiplicity handling.
- Report harms, withdrawals, and missing outcomes by arm.
- Distinguish superiority, non-inferiority, equivalence, and exploratory analyses.

## Bioinformatics And Omics

- Inventory samples, phenotypes, batches, platforms, genome/build/annotation versions, and QC thresholds.
- Define normalization, filtering, batch correction, and covariate adjustment before differential analysis.
- Control multiple testing and report effect size with adjusted p value.
- Separate discovery, validation, and biological interpretation.
- Do not treat pathway enrichment or network proximity as clinical evidence without independent validation.

## Meta-Analysis

- Verify that studies, outcomes, time points, and effect measures are genuinely combinable.
- Use PRISMA-style flow and risk-of-bias assessment.
- Harmonize effect direction and units.
- Choose fixed/random effects based on the inferential target, not only I2.
- Report heterogeneity, prediction interval when useful, influence/leave-one-out, publication bias, and subgroup credibility.

## Genetic Epidemiology And MR

- Check instrument relevance and strength; report F statistics or equivalent.
- Harmonize alleles and handle palindromic SNPs.
- Use cis-eQTL/cis-pQTL or other defensible genetic instruments for molecular exposures.
- Do not use TCMSP targets directly as MR exposures.
- Do not use EHR-only data without genotypes as MR outcomes.
- Check pleiotropy, heterogeneity, directionality, colocalization, FDR, and external replication.

## Minimum Reporting Package

- Study design and setting.
- Data source and dates.
- Eligibility flow and final denominators.
- Variable definitions and missingness.
- Primary estimand and effect measure.
- Model specification and diagnostics.
- Sensitivity analyses.
- Assumption-bound interpretation.
