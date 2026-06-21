# 🍽️ Arabic Restaurant Reviews — Emotion Classification

A Natural Language Processing (NLP) project that detects emotions from Arabic restaurant reviews using multiple classical and deep learning models.

---

## 📌 Overview

This project builds an emotion classifier trained on Arabic restaurant reviews labeled with **6 emotion classes**:

| Label | Emotion |
|-------|---------|
| 0 | Joy |
| 1 | Anger |
| 2 | Sadness |
| 3 | Disgust |
| 4 | Surprise |
| 5 | Neutral |

---

## 📂 Dataset

- **File:** `Arabic_resturant_reviews_with_6emotions.csv`
- **Columns used:** `review`, `emotion_extended`
- Arabic text reviews manually labeled with one of 6 emotions

---

## 🔧 Pipeline

### 1. Preprocessing
- Remove diacritics, Latin characters, and special symbols
- Normalize Arabic letters (`أإآ → ا`, `ى → ي`, `ة → ه`)
- Tokenization using NLTK
- Arabic stopword removal (negation words preserved: `لا، ليس، لم ...`)

### 2. Feature Extraction
- **TF-IDF** — 5,000 features, n-grams (1–3)
- **Keras Tokenizer + Padding** — vocab: 20,000 tokens, max length: 80

---

## 🤖 Models

| Model | Input Features |
|-------|---------------|
| Dense Neural Network (Keras) | TF-IDF |
| LinearSVC + GridSearchCV | TF-IDF |
| CNN (1D Convolutional) | Embedding + Padding |
| FastText (supervised) | Raw tokens |
| BiLSTM (Bidirectional LSTM) | Embedding + Padding |

---

## 📊 Evaluation Metrics

- Accuracy Score
- Precision / Recall / F1-Score (per class)
- Confusion Matrix
- Training & Validation curves (Loss + Accuracy)

---

## 🛠️ Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **ML:** scikit-learn
- **NLP:** NLTK, FastText
- **Data:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn

---

## 🚀 How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

3. Place the dataset CSV in the project directory

4. Open and run the notebook
   ```bash
   jupyter notebook PROVIS_1_.ipynb
   ```

---

## 👩‍💻 Author

**Toqa Mohamed Fathy**  
AI Engineering Student — New Ismailia National University
