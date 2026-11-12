<h1 align="center">Aziz Muammer Çetiner</h1>

<p align="center">
  <b>Machine Learning &amp; Artificial Intelligence</b><br>
  Computer Engineering (final year) · Kırşehir Ahi Evran University<br>
  Previously: Software Developer · <a href="https://www.adaptcentre.ie/">ADAPT Centre</a>, Maynooth University (Jul–Sep 2026)
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

**Reproducibility &amp; reliable evaluation.** Taking published models apart and checking whether the reported gains survive contact with a correct evaluation protocol — and building methods whose uncertainty estimates actually hold. Often the gains don't survive.

Recently completed a research position at the ADAPT Centre (Maynooth University). Currently preparing work for journal submission and looking for PhD opportunities starting 2027.

---

## Selected Work

### Re-evaluating the TOP Benchmark
**Reproducibility audit · Clinical trial outcome prediction**

A reproducibility and statistical re-evaluation of HINT and MEXA-CTP, two published models for predicting clinical trial approval, in a unified framework. The headline result: a two-feature historical-rate baseline (ROC-AUC 0.700) exceeds both published methods, and six of seven directional findings fail to replicate.

The audit corrected ten code-level defects in the released implementations, including:

| Defect | Consequence |
|---|---|
| PR-AUC computed on binarized predictions | Metric does not measure ranking quality |
| Attention layers held in plain `dict`, not `nn.ModuleDict` | Parameters never registered, trained, or saved |
| Epoch selection performed on the test set | Reported scores are optimistically biased |

Each model was re-run in an isolated environment and compared through a shared evaluation harness — threshold selection on validation, PR/ROC on continuous scores, bootstrap confidence intervals.

`reproduci
