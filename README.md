# Scale Insect Detection with YOLO

This project uses YOLO to detect scale insects in plant images. It was organized as an image recognition project for a school application portfolio.

## Project Focus

- Task: object detection
- Target class: `Bug`
- Model family: YOLO
- Dataset config: `data_Bug.yaml`

## Files

- `YOLO_Det_Seg1.ipynb`: main notebook for training or testing the YOLO scale insect detection workflow.
- `check.ipynb`: notebook for checking project setup, data, or detection results.
- `data_Bug.yaml`: YOLO dataset configuration for the scale insect dataset.
- `.gitignore`: excludes datasets, model weights, training outputs, and local cache files.

## Dataset

The dataset is not included in this GitHub repository because image datasets are usually large. The expected local dataset path is:

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

## Notes

Model weights such as `.pt` files and generated results under `runs/` are excluded from GitHub. They can be shared separately through cloud storage if needed.
