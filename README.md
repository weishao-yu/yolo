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
Expected local dataset path:

```text
Bug_Detection/
```

Expected YOLO dataset structure:

```text
Bug_Detection/
  train/
    images/
    labels/
  val/
    images/
    labels/
```

---

## Selected Training Result / 精選訓練成果

本專案保留較佳的一組訓練結果於：

```text
runs/detect/bug_medium_1024_aug/
```

該實驗使用 YOLO11m 模型進行訓練，主要設定如下：

| Item | Setting |
|---|---|
| Model | YOLO11m |
| Epochs | 100 |
| Image Size | 1024 |
| Batch Size | 4 |
| Target Class | Bug |
| Dataset Config | data_Bug.yaml |

第 100 epoch 的驗證結果如下：

| Metric | Value |
|---|---:|
| Precision | 0.69288 |
| Recall | 0.72185 |
| mAP50 | 0.76088 |
| mAP50-95 | 0.34531 |

---

## Result Files / 成果檔案說明

The selected training result folder includes:

```text
runs/detect/bug_medium_1024_aug/
```

Important files:

- `results.png`：Training curves and validation metrics.
- `results.csv`：Training and validation metrics for each epoch.
- `confusion_matrix.png`：Confusion matrix of the validation result.
- `BoxPR_curve.png`：Precision-Recall curve.
- `val_batch*_pred.jpg`：Model prediction results.
- `val_batch*_labels.jpg`：Ground-truth label comparison images.

---

## Reflection / 學習反思

本次實作中，模型在 mAP50 上約達 0.76，代表模型已能初步辨識部分介殼蟲目標。然而，mAP50-95 約為 0.35，顯示在更嚴格的定位標準下仍有改善空間。

透過這次實作，我理解到 AI 模型的效果不只取決於模型架構本身，也受到資料數量、標註品質、影像角度、訓練參數與資料多樣性影響。這次經驗讓我更加認識 YOLO 物件偵測流程，也讓我了解人工智慧如何應用於農業病蟲害辨識等跨領域問題。

---

## Notes / 備註

Model weights such as `.pt` files are not included in this repository to avoid large file uploads.

本專案主要作為 YOLO 物件偵測與 AI 農業應用之學習紀錄，並非完整商業化模型。