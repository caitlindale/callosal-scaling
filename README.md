# callosal-scaling
This repository contains analysis code investigating the relationship between brain size and the proportions of the corpus callosum, using outputs derived from structural MRI data.

Full analysis code is available for the manuscript:

> **Scaling down: proportionally smaller corpora callosa in larger brains**  
> *(Dale, Kurth & Luders, 2025)*

## 🧠 Overview

This project investigates how **corpus callosum (CC) volume** scales with total intracranial volume, as a proxy for **brain size**, focusing on **proportional callosal volume (CC volume / total intracranial volume)** as the outcome of interest. We examine the role of possible moderators sex, age and handedness.

All analyses were conducted in **R 4.4.0** within a **Jupyter Notebook (.ipynb)** using the **UK Biobank RAP** platform.

---

## 📊 Statistical Model

The primary model tests whether proportional callosal volume decreases with increasing brain size and whether this scaling relationship varies by **sex**, **age**, or **handedness**.

The model can be expressed as:

\[
\text{CC}_{\text{prop}_i} = \beta_0 + \beta_1 \text{TIV}_i + \beta_2 \text{TIV}_i^2 + \beta_3 \text{Sex}_i + \beta_4 \text{Age}_i + \beta_5 \text{Handedness}_i + \beta_6 (\text{TIV}_i \times \text{Sex}_i) + \beta_7 (\text{TIV}_i \times \text{Age}_i) + \beta_8 (\text{TIV}_i \times \text{Handedness}_i) + \epsilon_i
\]

Where:
- **CC_prop** = Corpus callosum volume / Total intracranial volume
- **TIV** = Total intracranial volume (linear and quadratic terms)
- **Sex**, **Age**, **Handedness** = covariates
- **ε** = residuals

Model diagnostics confirmed that all assumptions for linear regression were adequately met.

---

## 📁 Contents

| File | Description |
|------|-------------|
| `CC_TIV_analysis.ipynb` | Jupyter notebook with all data preprocessing, statistical modelling, and diagnostic checks |
| `README.md` | This file |

---

## 🛠️ Notes

- Conducted on the **UK Biobank Research Analysis Platform (RAP)**.
- Uses an R kernel (R version 4.4.0).
- Corpus callosum volumes and TIV values were taken from **T1-weighted IDPs** in the UKB imaging dataset.
- Statistical assumptions (linearity, independence, normality of residuals) were explicitly tested and reported.

---

## 📜 Citation

If using this codebase or building on these methods, please cite the associated manuscript once published.

---

## 🧬 Author

**Caitlin Dale**  
PhD Candidate, University of Auckland  
[Contact via GitHub](#)

---

