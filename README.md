# Japeto AI Response Categorizer (Internal Project)

> 🧠 Internal machine learning system for tagging AI-generated chatbot responses on the Japeto Chat platform.

---

### 📊 Project Overview

This project delivers a classification pipeline designed for Japeto's proprietary chatbot system, **Japeto Chat**, enabling accurate categorisation of AI-generated responses. This improves analytics insight for chatbot owners by mapping generative responses to relevant topics.

---

### 🔍 Use Case

Japeto’s current analytics system only tracks categories for scripted responses. This model enables categorisation of **AI-generated responses**, enhancing topic-level analytics for AI chatbot interactions.

> Target Accuracy: **≥ 85%**  
> Final Accuracy Achieved: **~85.2%**

---

### 📁 Dataset

- 1500 total messages (manual and synthetic)
- Each message includes:
  - `user_message`
  - `chatbot_response`
  - `response_source` (scripted or AI-generated)
  - `category` (labelled)
  - `session_id`, `timestamp`

📌 Only AI-generated responses were used for model training.

---

### 🧪 ML Pipeline

| Step | Description |
|------|-------------|
| **1. Preprocessing** | Lowercasing, punctuation & stopword removal, null filtering |
| **2. Vectorization** | TF-IDF with 1–2 n-grams |
| **3. Train-Test Split** | Stratified 75/25 |
| **4. Models** | Logistic Regression, Multinomial Naive Bayes, Random Forest |
| **5. Evaluation** | Accuracy, Precision, Recall, F1, Confusion Matrix, Confidence Score |

---

### ⚙️ Models Used

- **Logistic Regression**  
  > ✅ Achieved best accuracy and generalization  
- **Multinomial Naive Bayes**  
  > ⚡️ Fastest to train, slightly lower accuracy  
- **Random Forest**  
  > 🌲 Strong handling of complex patterns, slightly slower

---

### 📉 Evaluation Results

| Model | Accuracy | Notes |
|-------|----------|-------|
| Logistic Regression | 85.2% | Best overall performance |
| Naive Bayes | 82–84% | Lightweight, fast |
| Random Forest | 83–85% | Robust but slower |

Low-confidence predictions (<50%) were flagged for manual review to improve quality assurance.

---

### 🖼️ Screenshots

> Replace these with real screenshots before final submission.

<p align="center">
  <img src="screenshots/data-preprocessing.png" width="600" alt="Data Preprocessing Step"/>
</p>

<p align="center">
  <img src="screenshots/model-evaluation.png" width="600" alt="Evaluation Results"/>
</p>

<p align="center">
  <img src="screenshots/confusion-matrix.png" width="600" alt="Confusion Matrix"/>
</p>

---

### 📌 Deployment & Integration

This classification model is intended for **internal deployment** within the Japeto Chat platform to improve the analytics dashboard.  

It can be integrated into the response logging pipeline to tag AI-generated messages in real-time or asynchronously.

---

### 🧠 Future Improvements

- Fine-tune models with additional labelled data
- Expand category definitions
- Explore deep learning alternatives (e.g., BERT)
- Implement active learning to auto-suggest low-confidence labels

---

### 🔒 License & Usage

> **This project is confidential and intended for internal use by Japeto Ltd. Not licensed for external or public distribution.**

---

