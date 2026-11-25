# taVNS & Mindfulness: 2 × 2 Factorial HRV & Attention Pipeline

[![Open In Colab](https://google.com)](https://google.com)


A reproducible Python pipeline simulating and analyzing physiological (heart rate variability) and behavioral (reaction time) outcomes across a **2 × 2 factorial design** (`Stimulation`: Active vs. Sham taVNS × `App Condition`: Mindfulness vs. No Mindfulness, *N* = 40).

## Repository Contents
* `experiment/` — Experimental paradigm design and task parameters.
* `analysis/hrv_2x2_anova.ipynb` — Jupyter/Colab notebook for Kubios-style RR-interval artifact filtering, HRV feature extraction (`RMSSD`, `SDNN`, `pNN50`, `LF/HF`), automated quality control (`<= 5%` artifact cutoff), and Type II 2 × 2 ANOVA.
* `synthetic_2x2_hrv.csv` — Simulated cohort dataset (*n* = 10 per cell).
* `tavns_mindfulness_2x2_results.png` — Two-panel interaction plot showing vagal tone reactivity (Δ RMSSD) and attention speed changes (Δ RT).

## Results Preview
![2x2 Factorial HRV and Reaction Time Results](tavns_mindfulness_2x2_results.png)

## Limitations & Future Directions

* **Synthetic Data Assumptions:** The current dataset (`N = 40`, `n = 10` per cell) is synthetically generated under controlled parametric assumptions (e.g., normal error distributions and predefined effect sizes) to validate the preprocessing and statistical pipeline. Real-world psychophysiological recordings typically exhibit greater inter-individual baseline variability and non-normal artifact bursts.
* **Simulated vs. Raw ECG/PPG Waveforms:** Preprocessing currently operates on simulated RR-interval series rather than raw electrocardiography (ECG) or photoplethysmography (PPG) signals. Future iterations will incorporate raw waveform peak detection (e.g., NeuroKit2 or MNE-Python) and real-time respiration rate control, as respiratory sinus arrhythmia (RSA) can confound vagally mediated HRV metrics like RMSSD.
* **Statistical Power & Longitudinal Dynamics:** A sample size of `n = 10` per condition provides adequate power only for large interaction effects and does not capture within-session temporal dynamics. Expanding the pipeline to handle mixed-effects models (LME) across multi-block time windows will allow finer tracking of autonomic habituation and sustained attention.
* **Stimulation Parameter Blinding:** In empirical taVNS protocols, sensory perception differences between active cymba conchae stimulation and earlobe sham can affect participant blinding. Future experimental modules will log perceptual rating scales as covariates in the behavioral and autonomic models.
