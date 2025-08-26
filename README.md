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
##  Key Highlights

- **Architecture**: Utilizes MobileNetV2 — a lightweight yet powerful CNN model with inverted residuals and linear bottlenecks, ideal for mobile and low-resource environments.  [oai_citation:0‡Wikipedia](https://en.wikipedia.org/wiki/MobileNet?utm_source=chatgpt.com)
- **Objective**: Identify carious lesions in intraoral or radiographic imagery with high accuracy, efficient inference, and low computational overhead.

---

##  Use Cases & Applications

1. **Early Detection in Low-Resource Settings**  
   Deployable on smartphones or low-cost devices, enabling timely oral health screening in rural clinics or school screenings where dentists might not be immediately available.  [oai_citation:1‡arXiv](https://arxiv.org/abs/2308.15705?utm_source=chatgpt.com)

2. **Clinical Decision Support**  
   Augment dentists’ diagnostic accuracy by highlighting potential lesions, reducing subjectivity and missed cases, particularly for subtle early-stage caries. AI has shown to outperform clinical exams in consistency.  [oai_citation:2‡Lippincott Journals](https://journals.lww.com/jcde/fulltext/2025/05000/revolutionizing_the_diagnosis_of_dental_caries.2.aspx?utm_source=chatgpt.com) [oai_citation:3‡MDPI](https://www.mdpi.com/2306-5354/11/9/936?utm_source=chatgpt.com)

3. **Mass-Screening & Epidemiological Studies**  
   Offers scalable, automated analysis of dental images, facilitating large-scale survey studies and public health assessments.  [oai_citation:4‡Lippincott Journals](https://journals.lww.com/jcde/fulltext/2025/05000/revolutionizing_the_diagnosis_of_dental_caries.2.aspx?utm_source=chatgpt.com) [oai_citation:5‡ecommons.roseman.edu](https://ecommons.roseman.edu/cgi/viewcontent.cgi?article=1628&context=researchsymposium&utm_source=chatgpt.com)

4. **Mobile Health (mHealth) Integration**  
   With model optimizations (e.g., quantization, mixup, fine-tuning), this pipeline can power smartphone apps that deliver near real-time diagnostics.  [oai_citation:6‡Wikipedia](https://en.wikipedia.org/wiki/MobileNet?utm_source=chatgpt.com) [oai_citation:7‡Lippincott Journals](https://journals.lww.com/jcde/fulltext/2025/08000/artificial_intelligence_for_dental_caries.9.aspx?utm_source=chatgpt.com)

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
