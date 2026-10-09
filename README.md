# Evidence-Grounded Mitigation of Diagnostic Sycophancy in Large Language Models through Confidence Calibration and Threshold-Based Decision Making

## Overview

This project investigates diagnostic sycophancy in large language models (LLMs) during healthcare consultations, focusing on whether a user's confidence in a self-diagnosis influences the model's diagnostic confidence when the underlying clinical evidence remains unchanged.

Using structured clinical cases from the DDXPlus dataset, the experiment aims to examine how different levels of asserted self-diagnostic confidence affect model responses and whether evidence-grounded confidence calibration and threshold-based decision-making can reduce inappropriate diagnostic confirmation without suppressing evidence-supported agreement.

## Research Question

When the underlying clinical evidence is held constant, to what extent does a user's asserted self-diagnosis inflate an LLM's diagnostic confidence, and can evidence-grounded calibration with a threshold-based decision mechanism reduce this effect without suppressing evidence-supported agreement?

## Objectives

- Investigate the relationship between user-asserted diagnostic confidence and LLM diagnostic confidence.
- Compare model behavior when users assert correct versus incorrect self-diagnoses.
- Examine whether diagnostic confidence remains grounded in clinical evidence as user confidence increases.
- Evaluate confidence calibration and threshold-based decision-making as potential mitigation strategies.
- Assess whether mitigation reduces inappropriate confirmation while preserving justified agreement.

## Dataset

The experiment uses the DDXPlus Dataset (English), a synthetic clinical diagnosis dataset containing patient characteristics, clinical evidence, and diagnostic labels.

###**Dataset citation:**

Fansi Tchango, Arsene; Goel, Rishab; Wen, Zhi; Martel, Julien; Ghosn, Joumana (2023). DDXPlus Dataset (English). figshare. Dataset. https://doi.org/10.6084/m9.figshare.22687585.v2

The experiment uses a 30,000-case subset of DDXPlus. The subset selection procedure and its limitations will be documented as part of the research methodology.

The selected subset includes all 49 diagnostic conditions represented in DDXPlus. The subset was constructed with a cap on the number of cases per condition to improve diagnostic coverage while limiting the dominance of highly represented conditions.

The dataset will be examined and prepared before experimental cases and prompts are constructed.

## Experimental Approach

The planned workflow consists of the following stages:

1. **Data preprocessing:** Inspect dataset integrity, missing values, duplicates, diagnostic coverage, and clinical evidence.
2. **Feature selection and engineering:** Identify relevant clinical inputs, ground-truth labels, and metadata that must be excluded from model prompts.
3. **Experimental construction:** Create matched clinical prompts with different levels of asserted self-diagnostic confidence while holding the underlying clinical evidence constant.
4. **Pilot evaluation:** Validate prompt consistency, response structure, and confidence measurement on a small sample.
5. **Baseline evaluation:** Measure diagnostic behavior and confidence across experimental conditions.
6. **Confidence calibration:** Assess whether model confidence can be better aligned with diagnostic correctness using validation data.
7. **Threshold-based decision-making:** Evaluate whether calibrated confidence can support decisions such as evidence-supported, insufficient evidence, or uncertain.
8. **Comparative analysis:** Compare baseline and mitigated behavior using diagnostic performance, confidence calibration, and inappropriate confirmation metrics.

## Evaluation

Planned evaluation measures include:

- Diagnostic accuracy
- Diagnostic Sycophancy Gap
- False-confirmation rate
- Evidence-supported agreement
- Expected Calibration Error (ECE)
- Brier score
- Abstention and uncertainty rates
- Sensitivity and specificity, where applicable

Final metrics and analysis procedures will be documented as the experimental design is finalized.

## Repository Structure

The repository will be expanded as the project progresses.

- `notebooks/` — Data preprocessing and experimental notebooks
- `data/` — Dataset documentation, data dictionary, and access instructions
- `docs/` — Research methodology, literature review, and experimental protocols
- `experiments/` — Prompt templates, configurations, and pilot procedures
- `results/` — Evaluation tables, figures, and result analysis
- `tests/` — Data integrity and experimental consistency checks

## Current Status

**In progress.**

The dataset has been loaded into the research notebook, and initial data inspection is underway. Feature selection, experimental construction, model evaluation, confidence calibration, and threshold-based mitigation remain planned stages.

Results and conclusions will be added after the corresponding experiments have been conducted.

## Limitations

DDXPlus contains synthetic clinical cases and does not fully represent the complexity, ambiguity, or prevalence of conditions encountered in real-world healthcare consultations. Findings from this dataset may therefore not generalize directly to real patient interactions.

The subset's capped diagnostic representation also differs from natural disease prevalence. These limitations will be considered when interpreting experimental results.

## Reproducibility

The repository will document dataset provenance, preprocessing decisions, prompt templates, model configurations, evaluation procedures, and calibration choices to support reproducibility.

Dataset access and redistribution will follow the applicable dataset license and terms.

## Disclaimer

This project is a personal research experiment. It is not intended to provide medical advice, diagnose individuals, or replace professional clinical judgment.

