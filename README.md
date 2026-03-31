# chihuahua-muffin-classifier

# 🐶🧁 Chihuahua vs Muffin Classifier (Data-Centric AI with 3LC)

## 📌 Overview

Can you tell a chihuahua from a muffin? This project tackles that challenge using a **data-centric AI approach** with the 3LC platform.

Instead of improving the model architecture, the focus is on **improving the dataset** through:

* Strategic labeling
* Embedding visualization
* Sample weighting

The model used is **ResNet-18 (trained from scratch)**, as required by the competition.

---

## 🧠 What is Data-Centric AI?

> “Data-centric AI is the discipline of systematically engineering the data used to build AI systems.” — Andrew Ng

In this project, performance improvements come from:

* Selecting informative samples from unlabeled data
* Cleaning noisy samples
* Iteratively refining the dataset

---

## 🚀 Approach

### 1. Initial Training

* Started with:

  * 100 labeled images (50 Chihuahua, 50 Muffin)
  * 3,579 unlabeled images
* Trained a baseline ResNet-18 model

---

### 2. Embedding Analysis (3LC Dashboard)

* Visualized embeddings of images
* Identified:

  * Misclassified samples
  * Overlapping clusters
* Used embeddings to guide labeling decisions

---

### 3. Strategic Labeling

* Selected difficult/unlabeled samples
* Focused on edge cases (e.g., muffins resembling dogs)
* Added high-value samples to training set

---

### 4. Sample Weighting

* Used 3LC tables to:

  * Activate useful samples (weight = 1)
  * Ignore noisy samples (weight = 0)

---

### 5. Iterative Improvement

* Re-trained model multiple times
* Improved dataset → improved accuracy

---

## 📊 Results

### 🔹 Accuracy Improvement

* Initial Accuracy: **XX%**
* Final Accuracy: **XX%**

### 🔹 Key Observations

* Better class separation in embeddings
* Reduced misclassification
* Improved generalization

---

## 📸 3LC Dashboard Visualizations

### Embeddings (Before vs After)

![Embeddings Before](assets/embeddings_before.png)
![Embeddings After](assets/embeddings_after.png)

### Accuracy / Metrics

![Accuracy](assets/accuracy.png)

---

## 📂 Project Structure

```
chihuahua-muffin/
│
├── src/                # Training & inference code
├── assets/             # Screenshots (embeddings, accuracy)
├── docs/               # Report / writeup
├── project_zip/        # 3LC project export
├── models/             # Trained model (optional)
├── outputs/            # Submission files
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## ⚙️ How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Register tables (3LC)

```bash
python src/register_tables.py
```

### 3. Train model

```bash
python src/train.py
```

### 4. Generate predictions

```bash
python src/predict.py
```

---

## 📦 Dataset

* Provided via Kaggle competition
* Includes:

  * Labeled training data
  * Unlabeled pool for data-centric improvements

---

## 🛠️ Tools Used

* Python
* PyTorch
* 3LC (Data-Centric AI platform)
* Kaggle

---

## 🏁 Conclusion

This project demonstrates how **data quality and selection** can significantly impact model performance, even when the model architecture is fixed.

---

## 👤 Team Members

- Deepti Mahajan
- Jay Rode
---

## 🔗 Submission Details

* Kaggle Competition: Chihuahua vs Muffin
* Approach: Data-Centric AI using 3LC
