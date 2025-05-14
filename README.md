# 🧠 Image Categorizer – Product Classification Project

This project implements an image classification pipeline using deep learning techniques to automatically categorize product images into **11 distinct classes**. The model is designed to aid platforms that require efficient and scalable classification of visual product data.

---

## 📦 Dataset

- The dataset contains product images categorized into 11 classes.
- Training and validation data are stored in the `train/` directory, structured by class ID.
- Test images are located in the `test/` folder and are unlabeled.
- To download the dataset, use:


!gdown 1hZK1rshl4dJVEPkUPykU5cZs_ANyTWp-
## 🧠 Model Overview

**Base model:** MobileNetV2 (pre-trained on ImageNet)

**Architecture:**
- Data augmentation: brightness, rotation, zoom, flip
- Dense layers with L1L2 regularization
- Fine-tuned last 25 layers of MobileNetV2

**Optimizer:** Adam with exponential decay learning rate  
**Loss:** Sparse Categorical Crossentropy  
**Evaluation Metric:** Accuracy

---

## ✅ Results

- **Final Validation Accuracy:** 91.90%
- Used `EarlyStopping` and `ModelCheckpoint` for optimization.

---

## 🧪 Prediction

Predictions are generated for test samples and mapped to category IDs using:

python
mapping = {
    0: 0, 1: 1, 2: 10, 3: 2, 4: 3,
    5: 4, 6: 5, 7: 6, 8: 7, 9: 8, 10: 9
}
## Example Output

| image_name             | cat_id |
|------------------------|--------|
| -56lhw2AKjYI0Hnt.jpg   | 0      |
| -6OdHXCBItIArPyk.jpg   | 2      |
| -7241lsvPiVpNVFV.jpg   | 9      |

---

## 📁 Files

- `image_categorizer_1.ipynb` – Full pipeline for training, evaluation, and submission  
- `submission.csv` – Output predictions for test images  
- `result.zip` – Final submission archive

---

## 🚀 How to Run

1. Open `image_categorizer_1.ipynb` in Google Colab  
2. Download the dataset using the provided `gdown` link  
3. Run all cells sequentially  
4. Export predictions from `submission.csv`

---

## 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
