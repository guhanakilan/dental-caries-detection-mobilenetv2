# Dental Caries Detection – MobileNetV2

This repository contains a Jupyter-based workflow for **dental caries (tooth decay) detection** using **MobileNetV2**.  
The primary notebook lives at: `notebooks/FINAL_MODEL.ipynb`.

> 👋 Repo: **guhanakilan/dental-caries-detection-mobilenetv2** — ready to push.

---

## 🧭 Project Overview
- **Model**: MobileNetV2 (transfer learning) for classifying dental radiographs/clinical images.
- **Goal**: Lightweight, fast inference on common hardware while maintaining strong accuracy.
- **Outputs**: Trained model weights, evaluation metrics (accuracy, precision/recall/F1), confusion matrix.

---

## 📁 Structure
```
.
├─ notebooks/
│  └─ FINAL_MODEL.ipynb
├─ requirements.txt
├─ LICENSE
└─ .gitignore
```

---

## ⚙️ Setup
```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab   # or: jupyter notebook
```
Open `notebooks/FINAL_MODEL.ipynb` and run all cells.

> Tip: If the notebook installs extra packages, add them to `requirements.txt` later and commit.

---

## 🏋️ Training (typical flow)
1. Prepare dataset folders (e.g., `data/train`, `data/val`, `data/test`) with class subfolders.
2. In the notebook, set paths and augmentations.
3. Train with MobileNetV2 base (imagenet) + custom head.
4. Save best model weights (e.g., `models/mobilenetv2_best.h5`).

---

## 📈 Evaluation
- Confusion matrix & classification report
- Learning curves (accuracy/loss)
- Precision / Recall / F1, ROC-AUC if applicable

---

## 🚀 Inference
- Load saved weights
- Run prediction on new images / folder
- (Optional) Export to TensorFlow SavedModel / TFLite for mobile

---

## 🤝 Contributing
Pull requests are welcome. Please open an issue first to discuss changes.

## 📝 License
MIT — see `LICENSE`.