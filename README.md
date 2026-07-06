# Kidney Stone Detection using YOLOv8

An object detection model that identifies kidney stones in medical images using **YOLOv8 (small variant)**.

## 📌 Overview

This project trains a YOLOv8-small model to detect kidney stones in scan images, covering training, evaluation, and inference in a single pipeline.

## 🎯 Problem Statement

Given a medical scan image, detect and localize kidney stones using bounding boxes — assisting in faster preliminary screening.

## ⚙️ Tech Stack

- **Python**
- **Ultralytics YOLOv8** — object detection model
- **Matplotlib / Pandas** — training metrics visualization

## 📂 Dataset

**Kidney Stone Images Dataset** (Kaggle)
🔗 https://www.kaggle.com/datasets/safurahajiheidari/kidney-stone-images

> Dataset is not included in this repo due to size. Download it from the link above and place it under a `data/` folder, formatted according to `data/detection.yaml`.

## 🔄 Pipeline

1. **Training** — `train_model()` fine-tunes YOLOv8s on the kidney stone dataset (30 epochs, image size 320)
2. **Evaluation** — `evaluate_model()` computes precision/recall metrics, saved to `eval_metrice.txt`
3. **Metrics Visualization** — `show_training_metrics()` plots training curves from `results.csv`
4. **Inference** — `test_image()` runs detection on a user-provided image path

## 🚀 How to Run

```bash
pip install ultralytics pandas matplotlib
```

1. Download the dataset from the Kaggle link above
2. Place it in a `data/` folder and set up `detection.yaml` (class names + train/val paths)
3. Run the notebook cells in order: train → evaluate → visualize metrics → test on a new image

## 📊 Results

~80% detection accuracy on the validation set (update with your exact metrics from `eval_metrice.txt`).

## ⚠️ Note

Model weights (`best.pt`, `last.pt`) are not included in this repo due to file size — train locally or request weights separately.

## 👩‍💻 Author

**Alishba Nadeem**
BS Artificial Intelligence, NUML Islamabad
[GitHub](https://github.com/Alishba-Nadeem1) · [LinkedIn](https://linkedin.com/in/alishba-nadeem-8014b9379)
