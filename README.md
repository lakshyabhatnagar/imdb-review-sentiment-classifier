# 🎬 IMDB Movie Review Sentiment Classifier

This is a Streamlit web app that classifies movie reviews as **positive** or **negative** using a **Simple RNN** model trained on the IMDB dataset.

---

## 🚀 Demo

Paste a movie review into the text box, and the model will classify the sentiment as **Positive** or **Negative**, along with a prediction confidence score.

---

## 🧠 Model Overview

- **Dataset**: IMDB Movie Reviews (`tensorflow.keras.datasets.imdb`)
- **Vocabulary Size**: 10,000 most frequent words
- **Preprocessing**:
  - Word index mapping from IMDB
  - Lowercasing and splitting on spaces
  - Padding to length 500
- **Architecture**:
  - `Embedding(input_dim=10000, output_dim=128, input_length=500)`
  - `SimpleRNN(128, activation='relu')`
  - `Dense(1, activation='sigmoid')`
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam

---

## 🖥️ How to Run

### 1. Install dependencies

```bash
pip install streamlit tensorflow

### 2. Make sure the model file is in the same directory:

simple_rnn_imdb.h5

### 3. Run the app

streamlit run app.py