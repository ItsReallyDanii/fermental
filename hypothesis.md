# Hypothesis

## Primary Falsifiable Statement
In plant stress-state prediction, adding bioelectrical/redox time-series feature families to conventional environmental features improves out-of-distribution robustness and probabilistic calibration versus non-bio baselines.

## Null Hypothesis (H0)
No statistically significant improvement exists in robustness and calibration when bioelectrical/redox features are added to conventional environmental features.

## Alternative Hypothesis (H1)
Bioelectrical/redox feature augmentation produces statistically significant improvements in robustness and calibration over non-bio baselines.

## Success Definition (Phase 1)
- Improvement must exceed predeclared thresholds in `metrics_and_thresholds.md`.
- Improvement must hold under at least one domain-shift condition and one noise condition.
- Calibration must not degrade beyond allowed threshold.
