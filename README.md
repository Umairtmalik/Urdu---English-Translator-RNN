 # Urdu to English-Translator-RNN
An attention-based encoder-decoder RNN (with LSTM) built from scratch in PyTorch for translating Urdu to English. The project includes custom data handling, training with dynamic loss and BLEU score evaluation (using Moses multi-bleu.perl), and comprehensive result reporting.
**# Urdu-to-English Neural Machine Translation 🇵🇰➡️🇬🇧

This project presents a custom implementation of an **attention-based encoder-decoder RNN model** (with an optional LSTM enhancement) for translating Urdu sentences into English. It aims to provide hands-on experience in building, training, and evaluating a sequence-to-sequence (seq2seq) model from scratch using PyTorch.

---

## 🚀 Project Overview

The goal is to translate sentence-level Urdu text into English using a neural network architecture trained on parallel corpora. This implementation focuses on:

- Building an attention-based encoder-decoder from scratch
- Preprocessing real parallel datasets
- Visualizing learning progress
- Evaluating translation quality using BLEU scores

---

## 🎯 Objectives

### 1. Dataset Preparation

#### 🔗 Data Combination
- Merge two sets of parallel sentence files:
  - One `.dev` pair (Urdu-English)
  - One `.devtest` pair (Urdu-English)

#### 📊 Data Splitting
- Shuffle the combined dataset
- Split into:
  - **70%** Training
  - **15%** Validation
  - **15%** Testing

---

### 2. Model Development

#### 🧠 Custom Attention-based Seq2Seq Model
- Implement an **encoder-decoder RNN** with **Bahdanau-style attention**
- Use **PyTorch**, without relying on high-level RNN libraries
- Backpropagation is handled via PyTorch’s built-in autograd

#### 🌟 Bonus: LSTM Variant
- Swap out vanilla RNN units with **LSTM cells** for potentially improved performance

---

### 3. Training & Evaluation

#### 📈 Training
- Train the model using the training set
- Track metrics per epoch:
  - Training Loss
  - Validation Loss
  - Validation BLEU Score

#### 📉 Evaluation
- Use **Moses `multi-bleu.perl`** to compute BLEU scores on:
  - Validation Set
  - Test Set

---

### 4. Visualization & Analysis

- Plot and analyze:
  - **Training & Validation Loss Curves**
  - **BLEU Score Progression**
- Understand model behavior, overfitting patterns, and convergence

---

## 📓 Example Training Log

```text
Epoch [1/50], Train Loss: 7.4014, Val Loss: 6.9863, Val BLEU: 0.00
Epoch [2/50], Train Loss: 6.6392, Val Loss: 7.0377, Val BLEU: 0.00
...
Epoch [49/50], Train Loss: 0.7452, Val Loss: 9.4111, Val BLEU: 0.84
Epoch [50/50], Train Loss: 0.7110, Val Loss: 9.3564, Val BLEU: 0.82

```
## Cloning the Repo
```bash
git clone https://github.com/tallal02/Urdu-to-English-Translation.git
cd Urdu-to-English-Translation
```
