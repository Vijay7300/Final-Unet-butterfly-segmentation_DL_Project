# Final-Unet-butterfly-segmentation_DL_Project

# 🦋 Butterfly Image Segmentation using U-Net

## 📖 Overview

This project focuses on **image segmentation of butterflies** using a deep learning approach based on the **U-Net architecture**. The goal is to accurately separate the butterfly from the background by predicting pixel-wise masks.

The model is trained on the **Leeds Butterfly Dataset**, where each image has a corresponding segmentation mask.

---

## 🚀 Key Features

* Implementation of **U-Net from scratch using TensorFlow/Keras**
* Custom data loading and preprocessing pipeline
* Supports **image-mask pairing automatically**
* Performance evaluation using:

  * Dice Coefficient
  * Mean IoU (Intersection over Union)
* Visualization of:

  * Original Image
  * Predicted Mask
  * Ground Truth Mask
  * Final Segmented Output
* Efficient inference (~0.02–0.06 sec per image)

---

## 🗂️ Dataset

* Dataset: **Leeds Butterfly Dataset**
* Contains:

  * RGB images
  * Corresponding segmentation masks
* Images and masks are matched using naming conventions:

  * Example: `image.png → image_seg0.png`

---

## ⚙️ Methodology

### 1. Data Preprocessing

* Images resized to **256×256**
* Masks converted to **binary format**
* Train-validation split (80:20)

### 2. Model Architecture

* U-Net with:

  * Encoder (Downsampling)
  * Bottleneck
  * Decoder (Upsampling with skip connections)
* Uses:

  * Convolution + ReLU
  * Batch Normalization
  * Dropout (for regularization)

### 3. Training

* Loss Function: Binary Crossentropy
* Optimizer: Adam
* Callbacks:

  * Early Stopping
  * ReduceLROnPlateau
  * Model Checkpointing

---

## 📊 Evaluation Metrics

### Dice Coefficient

Measures overlap between predicted and ground truth masks.

### Mean IoU

Measures intersection over union for segmentation quality.

---

## 📈 Results

* Fast inference: ~0.02–0.06 seconds per image
* Up to **50+ images per second**
* Good segmentation performance on validation data

---

## 🖼️ Output Visualization

The model outputs:

* Original image
* Predicted segmentation mask
* Ground truth mask
* Final segmented butterfly

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* OpenCV
* Matplotlib
* PIL

---

## 📌 Future Improvements

* Use Dice Loss or Combined Loss
* Data augmentation for better generalization
* Try advanced architectures (Attention U-Net, UNet++)
* Deploy as a web app

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone <repo-link>
cd <repo-name>
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run training

```bash
python train.py
```

---

## 💡 Conclusion

This project demonstrates how U-Net can be effectively used for **semantic segmentation tasks** with high accuracy and fast inference, making it suitable for real-time applications.

---

## 🙌 Acknowledgements

* Leeds Butterfly Dataset
* TensorFlow & Keras community

---
