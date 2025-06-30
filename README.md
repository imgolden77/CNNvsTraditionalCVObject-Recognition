# CNN vs Traditional CV Object Recognition

# 🧠 CNN vs Traditional CV for Object Recognition

This project compares CNN-based and traditional computer vision algorithms (SIFT, ORB + SVM) on CIFAR-10 and STL-10 datasets, analyzing the effects of image resolution and dataset size.

## 🔍 Overview
- Task: Object recognition
- Methods: CNN (PyTorch), SIFT/ORB + BoVW + SVM (OpenCV, sklearn)
- Datasets: CIFAR-10 (low-res, large), STL-10 (high-res, small)

## 📈 Results
| Method           | CIFAR-10 | STL-10 |
|------------------|----------|--------|
| CNN (Best Model) | 76.81%   | 67.47% |
| SIFT+SVM         | 37.02%   | 39.05% |

## 🏗️ Model Development
- 15 CNN versions iterated to address overfitting
- Optimizer: RMSprop → AdamW (+ weight decay)
- Scheduler: ReduceLROnPlateau
- Data Augmentation: RandomCrop, Flip, Rotation

## 📁 Folder Structure
- `cnn/`: PyTorch code for CNN experiments
- `traditional_cv/`: SIFT/ORB + SVM code
- `results/`: Accuracy, loss plots
- `models/`: (Optional) saved PyTorch model checkpoints

## 📚 Learnings
- Dataset size had greater impact than resolution on CNN
- Traditional CV performed better on high-res small datasets
