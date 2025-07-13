# CIRRHOSIS AI 

End-to-end pipelines for **liver-cirrhosis MRI segmentation** and **clinical-outcome prediction**.  
The project combines computer-vision models in Python (UNet-Lite, SynergyNet) with a tabular fully-connected network (FCNN) to forecast patient status.

---

## Files

| File / Folder | Purpose |
|---------------|---------|
| `notebooks/UNet_Lite_model_D2.ipynb` | Jupyter notebook – data loading, training and evaluation of UNet-Lite. |
| `notebooks/SynergyNet_model_2d_cirrhosis.ipynb` | Notebook – SynergyNet segmentation workflow. |
| `notebooks/fcnn_tabular_classification_.ipynb` | Notebook – tabular pipeline (EDA → preprocessing → FCNN). |
| `src/unet_lite_model_D2.py` | Script version of UNet-Lite notebook (CLI-ready). |
| `src/synergynet_model_2d_cirrhosis.py` | Script version of SynergyNet notebook. |
| `src/fcnn_tabular_classification_.py` | Script version of tabular workflow. |
| `requirements.txt` | Python dependencies (Torch ≥ 2.3, TF ≥ 2.19, etc.). |
| `README.md` | This document. |

> **Datasets are *not* stored in the repository.**  
Datasets are proprietary – please contact the authors or use your own data with the same folder structure.
---

## Summary of Methods & Results

| Task | Best model | Key metric (val) |
|------|------------|------------------|
| MRI segmentation | **SynergyNet** | Dice ≈ 0.83 |
| Tabular prognosis | **FCNN (128-64-32)** | Accuracy ≈ 0.88 |

* UNet-Lite reaches Dice ≈ 0.56 with half the parameters of SynergyNet.  
* Top predictors of mortality: serum albumin, bilirubin, INR.  
* Future work: fuse imaging + labs for improved prognosis.

