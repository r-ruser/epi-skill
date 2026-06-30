---
name: epi-skill
description: Research methodology skill for epidemiology, biostatistics, clinical or medical statistics, bioinformatics methods, causal inference, prediction/diagnostic studies, survival/regression modeling, meta-analysis, and manuscript methods auditing. Use when designing, critiquing, analyzing, or reporting biomedical studies; choosing study design or statistical models; controlling confounding and bias; planning sensitivity analyses; reviewing missing data, measurement validity, effect estimates, or reviewer-facing methods/results.
---

# Epi Skill

Use this skill to turn a biomedical research question into a reviewer-defensible methods plan,
analysis audit, or manuscript methods/results critique.

## Default Stance

- Start from the claim: descriptive, association, prediction, diagnostic, causal, mechanistic, or clinical utility.
- Translate the claim into target population, exposure/intervention, comparator, outcome, time zero, follow-up, estimand, and data source.
- Audit real data structure before analysis: file inventory, variable dictionary, missingness, coding, units, time windows, duplicates, eligibility, and outcome ascertainment.
- Treat bias control as part of design, not a post-hoc paragraph. Check selection bias, information bias, confounding, immortal time, collider stratification, reverse causation, and multiplicity.
- Match the model to the estimand and data-generating structure. Do not choose tests by variable type alone.
- Separate association, prediction, diagnosis, causal inference, and clinical decision support. Do not upgrade exploratory or internally validated results into clinical claims.
- Prefer transparent, reproducible outputs: protocol-style methods, analysis plan, tables/figures, code notes, sensitivity checks, and limitations.

## Workflow

1. Define the target claim and estimand.
2. Choose or audit the study design.
3. Build the data audit and variable specification before modeling.
4. Identify bias and confounding structure; use a DAG or target-trial framing when causal language is present.
5. Select effect measures and models that match outcome type, time scale, sampling design, and repeated/clustered structure.
6. Specify primary, secondary, subgroup, interaction, missing-data, and sensitivity analyses before interpreting results.
7. Report effect sizes with uncertainty, denominator, time scale, assumptions, diagnostics, and residual risks.

## References

Load only the reference needed for the task:

- `references/methodology-workflow.md`: full research-methods workflow from question to interpretation.
- `references/study-design-checklists.md`: design-specific and model-specific audit checklists.
- `references/source-scan-provenance.md`: local textbook scan provenance used to distill this skill.

## Output Rules

- For protocol/design tasks: return a structured methods plan plus assumptions and reviewer risks.
- For code/data tasks: run an inventory first, then analysis; save reproducible artifacts.
- For manuscript review: lead with methodological risks and missing analyses, then proposed wording.
- For statistical interpretation: state what the estimate can and cannot support.
- When evidence is weak or design is mismatched, say so directly and downgrade the claim.

## Red Flags

Stop and correct course when any of these appear:

- Outcome, exposure, comparator, time zero, or follow-up are undefined.
- A cross-sectional or uncontrolled analysis is being written as causal evidence.
- A prediction model is described as clinically deployable without external validation and calibration.
- Confounders are selected only by univariable p values.
- Missingness, censoring, competing risk, clustering, multiple testing, or measurement validity is ignored.
- EHR data without genotypes is used as a Mendelian-randomization outcome.
- TCMSP targets are treated as MR exposures without mapping to genetic/protein expression instruments.
