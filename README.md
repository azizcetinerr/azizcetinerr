<h1 align="center">Aziz Muammer Çetiner</h1>

<p align="center">
  <b>Machine Learning &amp; Artificial Intelligence</b><br>
  Software Developer · <a href="https://www.adaptcentre.ie/">ADAPT Centre</a>, Maynooth University<br>
  Computer Engineering (final year) · Kırşehir Ahi Evran University
</p>

<p align="center">
  <a href="mailto:cetiner.azizmuammer@ogr.ahievran.edu.tr">
    <img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://github.com/azizcetinerr">
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub">
  </a>
  <!-- <a href="LINKEDIN_URL"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a> -->
  <!-- <a href="SCHOLAR_URL"><img src="https://img.shields.io/badge/Google%20Scholar-4285F4?style=flat-square&logo=googlescholar&logoColor=white" alt="Scholar"></a> -->
</p>

---

## Overview

I work at the intersection of machine learning and scientific rigor. Two threads run through most of what I build:

**Medical imaging.** Deep learning for diagnosis from histopathology and radiology data — architectures, attention mechanisms, and the domain-specific evaluation these problems demand.

**Reproducibility.** Taking published models apart and checking whether the reported gains survive contact with a correct evaluation protocol. Often they don't.

Currently a software developer at the ADAPT Centre (Maynooth University), preparing work for journal submission, and looking for PhD opportunities starting 2027.

---

## Selected Work

### Re-evaluating the TOP Benchmark
**Reproducibility audit · Clinical trial outcome prediction**

A forensic re-evaluation of HINT and MEXA-CTP, two published models for predicting clinical trial approval. The headline result: reported improvements fall below the noise floor, and a base-rate lookup table matches every model on the benchmark.

The audit traced this to concrete defects in the released code:

| Defect | Consequence |
|---|---|
| PR-AUC computed on binarized predictions | Metric does not measure ranking quality |
| Attention layers held in plain `dict`, not `nn.ModuleDict` | Parameters never registered, trained, or saved |
| Epoch selection performed on the test set | Reported scores are optimistically biased |

Each model was re-run in an isolated environment and compared through a shared evaluation harness — threshold selection on validation, PR/ROC on continuous scores, bootstrap confidence intervals.

`reproducibility` · `benchmark-evaluation` · `clinical-trials` · `drug-discovery` · `tabular-foundation-models`

→ Defects reported upstream: [HINT #15](https://github.com/futianfan/clinical-trial-outcome-prediction/issues/15) · [MEXA-CTP #2](https://github.com/murai-lab/MEXA-CTP/issues/2)<br>
→ Preprint in preparation: *Is Progress on the TOP Benchmark Measurable? A Forensic Re-evaluation of HINT and MEXA-CTP* (with Kolawole John Adebayo) · [Code &amp; data](https://github.com/azizcetinerr/top-benchmark-reeval)

<br>

### Fine-Tuning vs. CBAM for Paediatric Pneumonia Detection
**Conference paper · IDAP'26 (IEEE) · Oral presentation**

A controlled comparison of full fine-tuning and Convolutional Block Attention Modules (CBAM) on VGG16, MobileNetV2 and DenseNet121 backbones for paediatric pneumonia detection from chest X-rays. With Ayla Kayabaş.

→ [Repository](https://github.com/azizcetinerr/Deep-Learning-Based-Pneumonia-Detection-from-Chest-X-Ray-Images)

<br>

### Machine Learning for Prostate Cancer Grading
**Survey · Computational pathology**

A survey of automated Gleason grading from histopathological whole-slide images, tracing the field from convolutional baselines to foundation models.

- **CNN architectures** — ResNet, VGG, EfficientNet, DenseNet, ViT
- **Multiple instance learning** — CLAM-MIL, DSMIL, TransMIL, ISMIL
- **Foundation &amp; vision-language models** — UNI, DINOv2, MedGemma, PathChat

<br>

### SICAPv2 / FSConv
**Reimplementation · PyTorch**

The FSConv architecture from Silva-Rodríguez et al., rebuilt from the paper without reference to the original code. Patch-level Gleason grading (NC/GG3/GG4/GG5) with global max pooling, class activation maps for weak localization, patient-wise splits to prevent leakage, weighted cross-entropy for class imbalance, and Cohen's quadratic kappa as the primary metric.

<br>

### PV Plant Fault Monitoring &amp; Energy Forecasting
**TÜBİTAK 1002-A · Time series · Deep learning**

Real-time fault monitoring and deep-learning-based energy production forecasting for photovoltaic plants. Scholarship researcher on a TÜBİTAK 1002-A project.

<br>

### Empowering User Control in Job Matching Systems
**NLP · Recommender systems**

A hybrid matching architecture: SkillNER for résumé parsing and LLM-based scoring of sincerity and trust signals, giving users explicit control over how their profile is matched against opportunities.

→ [Repository](https://github.com/azizcetinerr/EMPOWERING-USER-CONTROL-IN-JOB-MATCHING-SYSTEMS)

---

## Tech Stack

**Languages** &nbsp;
![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white)

**Deep Learning** &nbsp;
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)

**Data &amp; Vision** &nbsp;
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Tooling** &nbsp;
![Git](https://img.shields.io/badge/Git-F05033?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=azizcetinerr&show_icons=true&hide_border=true&theme=tokyonight&hide_title=true" alt="GitHub Stats" height="150">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=azizcetinerr&layout=compact&hide_border=true&theme=tokyonight" alt="Top Languages" height="150">
</p>
