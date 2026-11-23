# taVNS & Mindfulness: 2 × 2 Factorial HRV & Attention Pipeline

A reproducible Python pipeline simulating and analyzing physiological (heart rate variability) and behavioral (reaction time) outcomes across a **2 × 2 factorial design** (`Stimulation`: Active vs. Sham taVNS × `App Condition`: Mindfulness vs. No Mindfulness, *N* = 40).

## Repository Contents
* `experiment/` — Experimental paradigm design and task parameters.
* `analysis/hrv_2x2_anova.ipynb` — Jupyter/Colab notebook for Kubios-style RR-interval artifact filtering, HRV feature extraction (`RMSSD`, `SDNN`, `pNN50`, `LF/HF`), automated quality control (`<= 5%` artifact cutoff), and Type II 2 × 2 ANOVA.
* `synthetic_2x2_hrv.csv` — Simulated cohort dataset (*n* = 10 per cell).
* `tavns_mindfulness_2x2_results.png` — Two-panel interaction plot showing vagal tone reactivity (Δ RMSSD) and attention speed changes (Δ RT).

## Results Preview
![2x2 Factorial HRV and Reaction Time Results](tavns_mindfulness_2x2_results.png)
