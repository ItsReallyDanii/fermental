# Methods Notes

## Candidate Feature Families (Bioelectrical/Redox)
- Time-domain dynamics: rise time, decay time, peak amplitude, spike count
- Frequency-domain proxies: power in selected bands
- Nonlinear descriptors: entropy/complexity proxies
- Drift/instability indicators: baseline wander, contact-stability proxies

## Candidate Conventional Features
- Temperature
- Humidity
- Light intensity/photoperiod proxies
- Soil/environmental context variables if present

## Baseline Model Families
- Linear baseline (LogReg)
- Tree-based baseline (Random Forest / Gradient Boosted Trees)
- Optional sequence model (TCN/LSTM) if justified by data volume

## Ablations
- Environmental only
- Bioelectrical only
- Fused
- Fused minus each major bio feature family (family-level ablation)

## Leakage Controls
- Split by session/time/source to prevent duplicate-window bleed
- Strict separation of normalization fit scope (train only)
- No target leakage via post-event aggregations
