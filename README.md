# SMS-Spam-Detection-Naive-Bayes
# SMS Spam Detection using Naive Bayes

An end-to-end Natural Language Processing (NLP) and Machine Learning project to classify SMS messages as either "Spam" or "Ham" (legitimate). This project demonstrates text preprocessing, feature extraction, and model evaluation using various classification algorithms.

## Problem Statement
The goal of this project is to build a robust predictive model that can accurately identify spam messages. By leveraging NLP techniques, the model reads raw text data, converts it into a structured numerical format, and classifies the intent of the message.

## Dataset
The project utilizes a standard `spam.csv` dataset containing two primary columns:
* **Category**: The label of the message (`spam` or `ham`).
* **Message**: The raw text content of the SMS/Email.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Techniques:** Natural Language Processing (NLP), Bag-of-Words (BoW)

## Methodology
1. **Data Preprocessing:** * Mapped textual labels into binary binary numerical values (`spam` = 1, `ham` = 0).
2. **Feature Extraction (NLP):** * Utilized `CountVectorizer` to convert text into a matrix of token counts.
   * Extracted Unigrams, Bigrams, and Trigrams (`ngram_range=(1,3)`).
   * Applied dimensionality reduction by limiting to the top 8,000 features (`max_features=8000`) and ignoring rare words (`min_df=5`).
3. **Model Training & Comparison:**
   * Trained an initial **Gaussian Naive Bayes** model, achieving ~94% accuracy.
   * Benchmarked against **K-Nearest Neighbors (KNN)** and **Support Vector Classifier (SVC)**.
   * Deployed a **Multinomial Naive Bayes** model, which is mathematically better suited for discrete text counts, resulting in significantly improved classification.

## Results & Evaluation
The **Multinomial Naive Bayes** model outperformed the others, proving highly effective at identifying spam with minimal false positives.

* **Accuracy:** 98.56%
* **Precision:** 95.83%
* **Recall:** 93.24%
* **F1-Score:** 94.52%

The model was also successfully tested on custom, unseen string inputs (e.g., *"Congratulations! You've been selected to receive a FREE iPhone..."*) and accurately classified them.

## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/SMS-Spam-Detection-Naive-Bayes.git](https://github.com/yourusername/SMS-Spam-Detection-Naive-Bayes.git)
