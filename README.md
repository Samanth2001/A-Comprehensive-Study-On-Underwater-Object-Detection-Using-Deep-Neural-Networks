# A-Comprehensive-Study-On-Underwater-Object-Detection-Using-Deep-Neural-Networks
This repository presents a comprehensive implementation of underwater object detection using deep learning models, aligned with an IEEE Access publication. The study utilizes the TrashCan 1.0 dataset consisting of 7,212 annotated underwater images and restructures it into two configurations: a 3-class dataset (Trash, Animal, ROV) and a 4-class dataset (Trash, Animal, ROV, Plant).

Separate dataset formats were prepared for YOLOv8 and YOLOv9 architectures to ensure compatibility with their respective training pipelines. Multiple model variants of YOLOv8 (n, s, m, l) and YOLOv9 (t, s, m, c) were trained using two learning rates (0.01 and 0.0001), resulting in a total of 32 experimental configurations.

The repository includes dataset organization, training configurations, model weights, and evaluation results, enabling reproducibility and comparative analysis across architectures, dataset complexities, and hyperparameter settings.
