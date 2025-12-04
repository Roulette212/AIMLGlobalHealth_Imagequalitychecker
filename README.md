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
```

## 2. Installation
### Step 1 — Clone this repository

``` text
git clone https://github.com/<your-username>/malaria-image-quality.git
cd malaria-image-quality
```

### Step 2 — Install dependencies
``` text
pip install -r requirements.txt
```
---

## 3. Running the Notebook

### Option A — Jupyter Notebook (Local)
1. Start Jupyter
2. Open the notebook: Model1_ImageQualityChecker.ipynb
3. Confirm the folder layout:
  ``` text
quality/
    sharp/
    blurry/
    test/
```
4. In Jupyter, go to: Kernel → Restart & Run All

### Option B — Google Colab
1. Open the notebook in Google Colab.
2. Upload the quality folder to /content/quality.
3. Update the path inside the notebook if necessary:
``` text
    DATA_ROOT = "/content/quality"
```
4. Run all cells from top to bottom.

---

## 4. Expected Results
The file expected_outputs.pdf contains the output that a correct run should produce, including:
1. Laplacian score distributions
2. Metric vs threshold curves
3. Best threshold details
4. Confusion matrix
5. Example classifications from test images

Use this PDF to verify successful installation.
