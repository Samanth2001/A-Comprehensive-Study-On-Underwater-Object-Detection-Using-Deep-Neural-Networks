> **Note:** Faster R-CNN, Mask R-CNN, and Cascade Mask R-CNN were initially implemented and evaluated on the **original underwater dataset** as baseline experiments. These experiments were conducted to understand the dataset's characteristics, object distribution, and detection challenges before training the primary models used in this study, **YOLOv8** and **YOLOv9**. Although the implementations were successful, the obtained performance did not meet the desired benchmark due to computational constraints and limited resources for extensive training and hyperparameter optimization. The corresponding code and configurations are included in this repository for documentation, reproducibility, and future research.


## Experimental Models

As part of this research, we evaluated multiple two-stage object detection and instance segmentation models for underwater object detection. Although these models were successfully implemented and trained, the obtained results did not achieve the desired performance due to computational constraints and limited resources available for extensive experimentation and hyperparameter tuning.

The implementations are included in this repository for documentation, reproducibility, and future research.

### Faster R-CNN

**Purpose:** Two-stage object detection

**Backbone:** ResNet-50 / ResNet-101

**Key Components:**

* Region Proposal Network (RPN)
* ROI Pooling
* Bounding Box Regression

**Loss Functions:**

* RPN Classification Loss
* Smooth L1 Bounding Box Regression Loss
* Final Classification Loss

**Remarks:**
Implemented and evaluated on the underwater dataset. Performance was limited by available computational resources and training constraints.

---

### Mask R-CNN

**Purpose:** Object detection with instance segmentation

**Backbone:** ResNet-101 + Feature Pyramid Network (FPN)

**Key Components:**

* ROI Align
* Feature Pyramid Network (FPN)
* Fully Convolutional Network (FCN) Mask Head

**Loss Functions:**

* Classification Loss
* Bounding Box Regression Loss
* Mask Loss

**Remarks:**
Implemented for underwater object detection and segmentation experiments. The obtained results were not adopted as the final model due to limited computational resources and suboptimal performance.

---

### Cascade Mask R-CNN

**Purpose:** Multi-stage object detection with instance segmentation

**Backbone:** ResNet-50 + Feature Pyramid Network (FPN)

**Key Components:**

* Multi-stage Cascade Detection
* Progressive IoU Threshold Refinement
* Instance Segmentation

**Loss Functions:**

* Cascade Classification Loss
* Bounding Box Regression Loss
* Mask Loss

**Remarks:**
Evaluated as part of the comparative study. Although the implementation was successful, the model required significantly higher computational resources, and the achieved performance did not meet the desired benchmark for this study.
