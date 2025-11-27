# 🤖 Bilingual AI-Generated Text Detector

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Jieba](https://img.shields.io/badge/NLP-Jieba-red)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 Project Overview
This project focuses on **Natural Language Processing (NLP)** classification to distinguish between human-written and AI-generated text. A key differentiator of this project is its **bilingual capability**, featuring distinct pipelines for **English** and **Chinese** text analysis.

Using **Random Forest Classifiers** and **TF-IDF Vectorization**, the models achieve high precision, addressing the growing need for content authenticity verification in academic and media settings.

---

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** Scikit-Learn, Pandas, NumPy, Matplotlib, Jieba (for Chinese segmentation)
* **Models:** Random Forest Classifier, Dummy Classifier (Baseline)
* **Techniques:** TF-IDF Vectorization, Undersampling (for class balance)

---

## 📊 Methodology & Results

### 1. English Pipeline
* [cite_start] **Dataset:** Utilized the "Training_Essay_Data" dataset containing human and AI-generated essays.
* [cite_start] **Preprocessing:** Lowercased text and applied **Random Undersampling** to balance the majority class (Human) with the minority class (AI).
* [cite_start] **Features:** Implemented `TfidfVectorizer` (capped at 1000 features) to reduce dimensionality.
* [cite_start] **Model:** Random Forest Classifier (`n_estimators=500`, `class_weight='balanced'`).

### 2. Chinese Pipeline
* [cite_start] **Dataset:** Combined human translations from the **Tatoeba** dataset with a custom `manual_chinese_ai` dataset.
* [cite_start] **Tokenization:** Integrated **Jieba** for specialized Chinese word segmentation.
* [cite_start] **Model:** Random Forest Classifier trained on TF-IDF vectors.

### Performance Metrics
Precision was prioritized as the key metric to minimize False Positives (misclassifying human work as AI).

| Language | Model | Metric | Score |
| :--- | :--- | :--- | :--- |
| **English** | Dummy Classifier (Baseline) | Precision | [cite_start]24.4%  |
| **English** | **Random Forest** | **Precision** | [cite_start]**98.7%**  |
| **Chinese** | Dummy Classifier (Baseline) | Precision | [cite_start]20.2%  |
| **Chinese** | **Random Forest** | **Precision** | [cite_start]**83.9%**  |

---

## 🚀 Installation & Usage

### 1. Clone the repository
```bash
git clone [https://github.com/ZuseGD/Bilingual-AI-Generated-Text-Detector.git](https://github.com/ZuseGD/Bilingual-AI-Generated-Text-Detector.git)
cd bilingual-ai-detector
```
### 2. Unzip Training_Essay_Data.zip
