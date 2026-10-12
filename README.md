# CIFAR-10 Image Classification

A deep learning project focused on image classification using the CIFAR-10 dataset. The project explores model performance, regularization, data augmentation, error analysis, and test-time augmentation.

## Overview

The CIFAR-10 dataset contains 60,000 color images across 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. The experiments investigate how different model configurations and augmentation techniques affect classification accuracy and robustness to image corruptions.

## Experiments

- **Part A — Baseline Model:** Establishes baseline performance across multiple random seeds.
- **Part B — Regularization:** Evaluates the effect of regularization on model performance.
- **Part C — Improved Architecture:** Tests an alternative model architecture.
- **Part D — Ablation Study:** Compares geometric augmentation, photometric augmentation, Random Erasing, Mixup, and label smoothing.
- **Part E — Error Analysis:** Examines per-class accuracy, confusion matrices, misclassified images, and robustness to pixelation.
- **Part F — Test-Time Augmentation:** Evaluates averaged predictions from multiple augmented versions of test images.

## Key Results

| Experiment | Result |
|---|---:|
| Part A clean-test accuracy (mean) | 35.18% |
| Part C clean-test accuracy (mean) | 37.34% |
| Best Part D shifted-test accuracy (mean) | 21.80% |
| Clean-test accuracy before pixelation | 39.35% |
| Pixelated-test accuracy | 22.51% |
| Shifted-test accuracy with TTA | 19.39% |

The ablation study found that combining geometric and photometric augmentation achieved the highest mean shifted-test accuracy among the tested configurations. The pixelation experiment showed a substantial performance drop, while test-time augmentation provided only a small improvement.

## Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Dataset

The project uses the [CIFAR-10 dataset](https://www.cs.toronto.edu/~kriz/cifar.html), containing 50,000 training images and 10,000 test images. The notebook handles the dataset loading and preprocessing.

## Reproducibility

Experiments use random seeds **42, 123, and 2026** where specified. Reported results are calculated within the notebook. The test set is reserved for evaluation rather than model selection.

## Notes

This project was developed as part of a machine-learning coursework assignment. All reported results correspond to the experiments documented in the notebook.
