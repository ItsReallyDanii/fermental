# Metrics and Thresholds

## Primary Task
Stress-state classification (extendable to regression variants if data requires).

## Core Metrics
1. Predictive Quality: Macro-F1 (primary) and AUROC (secondary)
2. Robustness: Relative degradation under noise/domain shift
3. Calibration: Expected Calibration Error (ECE) or Brier score

## Suggested Pass/Fail Thresholds (edit if needed)
- Macro-F1: >= 5% relative lift vs environmental-only baseline
- AUROC: >= +0.03 absolute improvement vs environmental-only baseline
- Robustness: <= 20% relative performance drop under defined shift condition
- Calibration: ECE not worse than baseline by > 0.01; preferred improvement >= 0.01

## Statistical Plan
- Paired bootstrap confidence intervals for key deltas
- Multiple-seed repeats (>=5) for stability
- Correct for multiple comparisons where applicable

## Minimum Sample Guidance
- Enough held-out events/classes for stable CI width and class coverage
- If class imbalance is high, stratified evaluation required
