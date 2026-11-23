# 2×2 taVNS & Mindfulness Psychophysiology Pipeline

An open-source **PsychoPy** experimental protocol and **Python** preprocessing pipeline modeling a 2×2 factorial study of transcutaneous vagus nerve stimulation (**Active taVNS vs. Sham**) and digital mindfulness (**Mindfulness App vs. Control**).

> **Data & Privacy Note:** To maintain strict IRB compliance and participant confidentiality, this repository uses **self-piloted test logs** and **synthetically generated RR-interval/behavioral datasets (`N = 40`)**. No human subjects data from active lab studies is stored here.

## Experimental Design (2×2 Factorial)

| Condition ID | Stimulation | Mindfulness App | Event Trigger |
| :--- | :--- | :--- | :--- |
| `C1_Active_Mindful` | Active taVNS | Mindfulness App | `101` / `102` |
| `C2_Active_NoMind` | Active taVNS | Control (Rest) | `201` / `202` |
| `C3_Sham_Mindful` | Sham taVNS | Mindfulness App | `301` / `302` |
| `C4_Sham_NoMind` | Sham taVNS | Control (Rest) | `401` / `402` |

## Repository Structure
* `/experiment`: PsychoPy Builder protocol (`session_protocol.psyexp`) and counterbalanced 2×2 `conditions.csv`.
* `/data`: Self-pilot run (`sub-01`) and synthetic 2×2 cohort dataset (`synthetic_2x2_hrv.csv`).
* `/analysis`: Jupyter Notebook (`hrv_2x2_anova.ipynb`) for Kubios-style RR-interval artifact filtering, RT outlier trimming, and 2×2 factorial ANOVA visualization.
