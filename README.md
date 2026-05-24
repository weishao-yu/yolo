# Scale Insect Detection with YOLO

本專案為「人工智慧農業應用工作坊」之 YOLO 物件偵測實作紀錄，主題為使用 YOLO 模型偵測釋迦影像中的介殼蟲。

This project is a YOLO object detection practice for detecting scale insects in plant images. It was organized as an image recognition project for a school application portfolio.

---

## Project Background / 專案背景

本次實作源自大二上「演算法」課程，配合教育部智慧雨林產業創生人才育成計畫所舉辦之「人工智慧農業應用工作坊」。

工作坊主題為利用人工智慧技術協助辨識釋迦上的介殼蟲。透過本次實作，我初步接觸 YOLO 物件偵測模型的訓練流程，並理解人工智慧在農業病蟲害偵測中的應用方式。

---

## Project Focus / 專案重點

- Task: Object Detection
- Target class: `Bug`
- Model family: YOLO
- Dataset config: `data_Bug.yaml`
- Application field: AI agricultural image recognition

---

## Files / 檔案說明

- `YOLO_Det_Seg1.ipynb`  
  Main notebook for training and testing the YOLO scale insect detection workflow.

- `check.ipynb`  
  Notebook for checking PyTorch, CUDA, GPU availability, and project setup.

- `data_Bug.yaml`  
  YOLO dataset configuration file. The target class is `Bug`.

- `runs/detect/bug_medium_1024_aug/`  
  Selected training result folder. This folder contains the chosen YOLO training output, including training curves, validation predictions, confusion matrix, and result metrics.

---

## Dataset / 資料集說明

The dataset is not included in this GitHub repository because it was provided during the workshop and may involve course-related data usage restrictions.

由於本專案使用工作坊提供之資料集，基於資料授權與檔案大小考量，未公開上傳原始訓練影像資料。

Expected local dataset path:

```text
Bug_Detection/