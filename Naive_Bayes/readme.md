# Naïve Bayes OCR: Distinguishing Digits 2 and 4

This project implements a simple **Naïve Bayes classifier** to recognize handwritten digits **2** and **4** using binary pixel data. The dataset consists of 16x16 pixel images flattened into 256-dimensional vectors.

---

## Dataset

- **trainX.txt** – Training features (binary pixels: 0 or 1)
- **trainY.txt** – Training labels (2 or 4)
- **testX.txt** – Testing features
- **testY.txt** – Testing labels

Each row corresponds to one 16x16 image, flattened row-wise.

---

## Steps Implemented

1. **Load Data**: Read training and testing features and labels.  
2. **Compute Priors**: Calculate class probabilities \( P(y) \) from training labels.  
3. **Compute Conditional Probabilities**:  
   - \( P(x_i=1|y=c) \) using Laplace smoothing.  
   - \( P(x_i=0|y=c) = 1 - P(x_i=1|y=c) \)  
4. **Prediction**:  
   - Use log probabilities for numerical stability.  
   - Calculate posterior \( P(y|X) \) for each class and choose the max.  
5. **Evaluation**:  
   - Compute **training** and **testing** accuracy.  
   - Class-wise accuracy for digits 2 and 4.

---

## How to Run

```bash
# Install dependencies
pip install numpy matplotlib

# Run the notebook or Python script
jupyter notebook NaiveBayesOCR.ipynb
# or
python naive_bayes_ocr.py
