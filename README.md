🧠 Simple RNN — IMDB Sentiment Analysis
An end-to-end deep learning project that uses a Simple Recurrent Neural Network (RNN) to classify IMDB movie reviews as positive or negative.

📌 Project Overview
This project demonstrates how to build, train, and save a text classification model using a SimpleRNN architecture on the IMDB movie review dataset.

📂 Project Structure
simple-rnn-imdb/
├── simpleRNN.ipynb       # Main notebook with full pipeline
├── simple_rnn_imdb.h5    # Saved trained model
└── README.md             # Project documentation

🗂️ Dataset

Source: Keras built-in IMDB dataset
Size: 50,000 movie reviews (25,000 train / 25,000 test)
Labels: Binary — Positive (1) / Negative (0)
Vocabulary Size: 10,000 most frequent words


🏗️ Model Architecture
LayerTypeOutput ShapeParametersEmbeddingEmbedding(None, 500, 128)1,280,000SimpleRNNSimpleRNN(None, 128)32,896DenseDense(None, 1)129

Total Parameters: 1,313,025 (~5.01 MB)
Activation (Output): Sigmoid


⚙️ Training Configuration
ParameterValueOptimizerAdamLoss FunctionBinary CrossentropyEpochs10 (max)Batch Size32Validation Split20%Early Stoppingpatience=5, monitor=val_loss

🛠️ Tech Stack
Python 3.12
TensorFlow / Keras
NumPy
Google Colab (GPU: T4)
