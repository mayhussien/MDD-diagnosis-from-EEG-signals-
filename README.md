# EEG-Based Depression Detection using Machine Learning

This project focuses on detecting depression using EEG (Electroencephalogram) signals through machine learning techniques. The pipeline involves signal preprocessing, feature extraction (linear, nonlinear, and statistical), feature selection, and classification using multiple ML algorithms.

## 🧪 Project Goal

To develop a machine learning system that classifies EEG signals to detect signs of depression, with a focus on understanding the impact of different feature types and selection methods on classification performance.

---
## 📂 Dataset

The dataset used in this project is the publicly available **[OpenNeuro EEG: Depression Rest Dataset](https://openneuro.org/datasets/ds003790)**.

- Contains resting-state EEG recordings from individuals with and without depression.


## 📁 Project Workflow

### 1. **Signal Segmentation**
- EEG signals were segmented to separate **eyes-open** and **eyes-closed** states.
- Only **eyes-closed** segments were used for modeling and feature extraction.
  

### 2. **Preprocessing & Filtering**
- Removed noise and artifacts using preprocessing techniques.
- Band-pass filtering applied to retain relevant frequency ranges.

### 3. **Channel Selection**
- Selected only specific EEG channels relevant to depression detection.

### 4. **Feature Extraction**
- Converted EEG signals to time series format.
- Extracted:
  - **1 linear feature**
  - **4 nonlinear and statistical features**
- Evaluated performance for each feature type and their combinations.

### 5. **Feature Selection Techniques**
- **PCA (Principal Component Analysis)**
- **ANOVA F-value**
- **Sequential Feature Selection (SFS)**

### 6. **Classification Algorithms**
Tested using **cross-validation** with the following models:
- ✅ Support Vector Machine (SVM) — Linear & RBF Kernels
- ✅ K-Nearest Neighbors (KNN)
- ✅ Linear Discriminant Analysis (LDA)
- ✅ Logistic Regression (LR)
- ✅ Random Forest (RF)
- ✅ Gaussian Naïve Bayes (GNB)

---

## 🧾 Results & Conclusion

- **Nonlinear and statistical features** significantly outperformed linear features.
- **Feature selection** improved classification performance — especially for nonlinear and statistical features.
- **KNN** and **LDA** classifiers yielded the **highest accuracy** across different configurations.

---

## 🛠 Technologies Used

- Python
- NumPy, SciPy
- scikit-learn
- Matplotlib / Seaborn
- EEG signal processing libraries (e.g., MNE or custom filters)

---

## 📊 Possible Improvements

- Incorporate deep learning models like CNNs for raw signal classification.
- Use larger and more diverse EEG datasets.
- Investigate temporal dynamics of EEG signals with RNNs or transformers.

---

## 👩‍💻 Author

**Mai Hussien**  
Bachelor’s Graduation Project – Depression Detection via EEG Signals  
Supervised by [Prof.Seif eldwlatly]  
Year: [2022]

---

