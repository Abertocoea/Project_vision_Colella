# 🐛 Silkworm Feeding Classification and Segmentation

## 📋 Overview

This project focuses on the **classification** and **unsupervised semantic segmentation** of images with silkworms, with the goal of identifying the feeding state and separating the main components of the image (worms, leaves, background).

The work is divided into two main tasks:

- **Supervised classification** using lightweight models (MobileViT, MiniCNN)
- **Unsupervised semantic segmentation** using DINO + KMeans

## 🧬 Models

| Task            | Models Used                                  |
| --------------- | --------------------------------------------- |
| Classification  | MobileViT (XXS, XS, S), MiniCNN, ResNet18     |
| Segmentation    | DINO (ResNet50 backbone) + KMeans clustering  |

## 📁 Dataset

The dataset used to train the lightweight networks for the classification task is available at the following link:

> [DATASET LINK HERE](https://drive.google.com/drive/folders/1F7BpqvWrf8E3nh6oaTKEJc09ibT6Igh_?usp=drive_link)

The dataset used to test the unsupervised semantic segmentation method is at the following link:

> [DATASET LINK HERE](https://drive.google.com/drive/folders/13FPSFr3IrRghm8BXj4g5nF28X3keLgwW?usp=drive_link)

Details:

- 1351 high-resolution RGB images (1559×1038 pixels)
- Labels: **feeding** / **non-feeding**

## 🔀 Data Split

The images were divided as follows:

- **70% Training set** (946 images)
- **15% Validation set** (203 images)
- **15% Test set** (202 images)

## 📆 Code:

- **IMPORT**: contains all module imports

- **GLOBAL**: defines paths, image sizes, batch sizes, device, and other global variables

- **UTILS**: utility functions like `accuracy`, `import_data`, `custom_dataset`

- **DATASET**: data preprocessing for training, validation, and testing phases

- **MODELS**: definition of the architectures used (MiniCNN, ResNet18, MobileViT)

- **Training and evaluation function**: functions for training, validation, and full training loop. Includes model saving and early stopping.

- **Top 1 score on various configurations**: training and validation of the models, MobileViT (XXS, XS, S), MiniCNN with different settings.

- **Unsupervised Semantic Segmentation**: full pipeline for feature extraction with DINO and clustering with KMeans

## 📊 Evaluation Metrics

- **Accuracy**, **F1-score**, **Inference Time** (for classification)
- **Silhouette Score** (for unsupervised segmentation)

## 👤 Author

- Alberto Colella  

## 📚 References

- DINO: [https://github.com/facebookresearch/dino](https://github.com/facebookresearch/dino)  
- MobileViT: [https://arxiv.org/abs/2110.02178](https://arxiv.org/abs/2110.02178)

