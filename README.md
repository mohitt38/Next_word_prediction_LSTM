# 🧠 Next Word Prediction Using LSTM

This project is a deep learning-based application that predicts the **next word** in a given sentence using **LSTM (Long Short-Term Memory)** networks. It leverages the language of Shakespeare's *Hamlet* as a dataset and provides a real-time prediction interface using **Streamlit**.

---

## 📚 Project Overview

### 1. **Data Collection**
We use the complete text of Shakespeare’s *Hamlet* as the dataset. Its rich vocabulary and complex sentence structure make it ideal for building a next-word prediction model.

### 2. **Data Preprocessing**
- Tokenization: The text is broken into sequences of words.
- Padding: Sequences are padded to ensure consistent input length.
- Dataset Split: The dataset is divided into training and testing sets.

### 3. **Model Architecture**
The model is a Sequential LSTM-based architecture consisting of:
- An **Embedding Layer** to represent words in a dense vector space.
- Two stacked **LSTM layers** to capture sequential dependencies.
- A **Dense output layer** with **softmax activation** to predict the next most likely word.

> 💡 **To switch to GRU:**  
> You can easily modify the model to use GRU instead of LSTM.  
> Simply replace:
> ```python
> from keras.layers import LSTM
> ```
> with:
> ```python
> from keras.layers import GRU
> ```
> and update the layers:
> ```python
> model.add(GRU(units))
> ```

### 4. **Model Training**
- The model is trained for **100 epochs**.
- **EarlyStopping** is used to avoid overfitting by monitoring validation loss.
- **Note:** The model becomes **more accurate and efficient** when trained for **more epochs**. Training beyond 100 epochs could lead to **even better performance**.

### 5. **Evaluation**
The model is tested using sample sentences. Its ability to generate contextually accurate predictions is verified by evaluating the predicted next word.

### 6. **Deployment**
The model is deployed via a **Streamlit web app**, allowing users to:
- Input a sequence of words.
- Receive real-time predictions for the next word.

---

## 🖼️ Screenshot

Below is a screenshot of the Streamlit web app in action:

![Next Word Prediction Streamlit App](LSTM RNN\img.png)

---

## 🚀 How to Run the Project

### 🔧 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/next-word-lstm.git
   cd next-word-lstm
2. Create a virtual environment and activate it:
   python -m venv venv
venv\Scripts\activate   # Windows
     or
    source venv/bin/activate   # macOS/Linux
3. Install dependencies:
    Install dependencies:
---
## ▶️ Run the Streamlit App
streamlit run app.py
---
## 📁 Files Included
app.py – Streamlit app for interactive prediction

next_word_lstm.keras – Trained model in modern Keras format

tokenizer.pickle – Saved tokenizer object

train_model.py – Script to train the LSTM model

README.md – Project overview and instructions

requirements.txt – Python dependencies

screenshots/app_demo.png – LSTM RNN\img.png
 
 ---

## 🧠 Future Improvements
Train on a larger and more diverse corpus for general-purpose predictions.

Use Bidirectional LSTM, GRU, or Transformer-based models for higher accuracy.

Add beam search or top-k sampling to improve prediction quality.

Deploy using Docker, Gradio, or to a public cloud service.

---


