# A-Comprehensive-Study-On-Underwater-Object-Detection-Using-Deep-Neural-Networks
#  Underwater Object Detection using YOLOv8 & YOLOv9

##  Overview

This repository presents a comprehensive implementation of underwater object detection using deep learning models, aligned with an IEEE Access research publication. The study focuses on detecting marine debris and underwater objects in complex environments using state-of-the-art real-time object detection models.

The experiments are conducted on the TrashCan 1.0 dataset (7,212 underwater images) and restructured into multiple configurations to evaluate model performance across varying levels of complexity. A total of **32 experimental configurations** were designed by combining different model variants, dataset structures, and learning rates.

---

##  Dataset

### 🔹 Source

* **Dataset**: TrashCan 1.0
* **Total Images**: 7,212
* The dataset contains annotated underwater images including marine debris, animals, and operational objects.

>  The dataset is **not included** in this repository. Please refer to the original source for access and licensing.

---

### 🔹 Custom Dataset Configurations

To improve training efficiency and reduce class imbalance, the dataset was restructured into two configurations:

####  3-Class Dataset (C3)

* Classes: **Trash, Animal, ROV**
* Train: 3,959 images
* Validation: 1,133 images
* Test: 554 images

####  4-Class Dataset (C4)

* Classes: **Trash, Animal, ROV, Plant**
* Train: 4,051 images
* Validation: 1,154 images
* Test: 568 images

---

### 🔹 Dataset Formatting

Separate dataset formats were prepared for:

* YOLOv8
* YOLOv9

Each dataset version is compatible with its respective training pipeline.

---

## Methodology

### 🔹 Models Used

#### YOLOv8 Variants

* Nano (**n**)
* Small (**s**)
* Medium (**m**)
* Large (**l**)

#### YOLOv9 Variants

* Tiny (**t**)
* Small (**s**)
* Medium (**m**)
* Compact (**c**)

---

### 🔹 Training Configurations

| Parameter      | Values           |
| -------------- | ---------------- |
| Dataset Types  | C3, C4           |
| Learning Rates | 0.01, 0.0001     |
| Epochs         | 100              |
| Task           | Object Detection |

---

### 🔹 Total Experiments

A total of **32 experimental configurations** were conducted:

| Factor         | Count  |
| -------------- | ------ |
| Model Variants | 8      |
| Dataset Types  | 2      |
| Learning Rates | 2      |
| **Total**      | **32** |

---

## Results Summary

* **YOLOv9c** achieved the best performance on the **3-Class dataset (C3)**
* **YOLOv8l** performed best on the **4-Class dataset (C4)**
* Models trained on the **3-class dataset generally performed better** due to reduced class complexity
* Higher-capacity models (YOLOv8l, YOLOv9c) demonstrated superior precision, recall, and mAP performance

---

## Repository Structure

```
Underwater-Object-Detection/
│
├── datasets/
│   ├── yolo_v8/
│   ├── yolo_v9/
│
├── models/
│   ├── yolov8/
│   ├── yolov9/
│
├── configs/
│   ├── yolov8/
│   ├── yolov9/
│
├── results/
│   ├── tables/
│   ├── plots/
│   ├── predictions/
│
├── scripts/
│   ├── train.py
│   ├── evaluate.py
│   ├── inference.py
│
├── paper/
│   └── IEEE_Access_Paper.pdf
│
└── README.md
```

---

## How to Run

### 🔹 Training Example

```bash
python scripts/train.py --model yolov8m --dataset C3 --lr 0.01
```

### 🔹 Evaluation

```bash
python scripts/evaluate.py
```

### 🔹 Inference

```bash
python scripts/inference.py
```

---

## Results & Outputs

The repository includes:

* Model evaluation metrics (Precision, Recall, mAP)
* Training curves
* Sample predictions
* Comparative analysis across models

---

## Research Paper

This work is based on an IEEE Access publication:

**"A Comprehensive Study on Underwater Object Detection Using Deep Neural Networks"**

> Add paper link here (IEEE / DOI)

---

## Notes

* Dataset is not included due to size and licensing constraints
* Model weights may be provided separately (or via external links)
* Ensure correct dataset formatting before training

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

##  Citation

If you use this work, please cite:

```bibtex
@article{yourpaper2025,
  title={A Comprehensive Study on Underwater Object Detection Using Deep Neural Networks},
  author={Samanth, K. et al.},
  journal={IEEE Access},
  year={2025}
}
```

---

## Acknowledgements

* TrashCan 1.0 Dataset
* YOLOv8 & YOLOv9 frameworks
* IEEE Access publication support

---
