# Malaria Microscopy Image Quality Checker

This repository contains a simple, reproducible pipeline to distinguish *sharp* vs *blurry* malaria microscopy images using a classical Laplacian variance focus metric. It is intended as the image quality gate in a larger malaria parasite quantification workflow.

The goal is to:
- Compute a focus score for each image
- Automatically classify images as *sharp* or *blurry*
- Show how accuracy, precision, recall, and F1 vary with the Laplacian threshold
- Provide example code and data so results can be reproduced end-to-end

---

## 1. Repository structure

```text
malaria-image-quality/
│
├─ Model1_ImageQualityChecker.ipynb   # main notebook with all code and results
├─ README.md                          # this file
├─ requirements.txt                   # Python dependencies
├─ expected_outputs.pdf               # PDF of notebook outputs (for Appendix 1)
│
├─ quality/
│   ├─ sharp/                         # sample sharp images
│   ├─ blurry/                        # corresponding synthetically blurred images
│   └─ test/                          # additional images used only for demo