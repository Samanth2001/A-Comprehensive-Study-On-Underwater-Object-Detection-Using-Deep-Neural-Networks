#  Dataset Configuration for YOLO Training

🔹 Annotation Format

All images are labeled using the standard YOLO format:

<class_id> <x_center> <y_center> <width> <height>
Coordinates are normalized (range: 0 to 1)
Bounding boxes represent object localization for detection tasks

🔹 Pre-processing Pipeline

The following preprocessing steps were applied uniformly across all images:

Auto-Orientation
Corrected image orientation using EXIF metadata
Removed EXIF orientation flags to ensure consistency
Resizing
All images resized to 640 × 640 resolution
Applied letterbox resizing (fit with padding)
Preserved aspect ratio with black padding where necessary

The data.yaml file defines the dataset structure, class information, and file paths required for training YOLO models. Separate configurations are maintained for the **3-class (C3)** and **4-class (C4)** datasets.

###  Explanation 
* **path** Root directory of the dataset. All other paths are relative to this. 
* **train / val / test** Subdirectories containing images for training, validation, and testing.
* Corresponding label files must exist in:
  labels/train
  labels/val
  labels/test
* **nc (number of classes)** Set to 3 for the C3 dataset and Set to 4 for the C4 dataset.
* **names** List of class labels in order.
* The index of each class corresponds to the class ID in label files:
* * 0 → trash * 1 → animal * 2 → rov * and 3 → plant
    
###  Example data.yaml
path: datasets/yolo_v8 or v9/C3 or C4

train: images/train
val: images/val
test: images/test

nc: 3 or 4

names: ['trash', 'animal', 'rov', and 'plant']
 
