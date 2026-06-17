# Assignment-2B-Spam-Message-Detection
Classify SMS or emails as spam or non-spam


```
# 🤖 SMS Spam Message Detection Engine

---

## 📌 Objective
The primary objective of this project is to build and train an end-to-end Machine Learning and Natural Language Processing (NLP) pipeline to accurately classify text messages as either **Spam** or **Ham (Legitimate)**. By analyzing word frequencies and patterns, the model automates the identification of unwanted or malicious messages, providing a foundation for scalable text filtering systems.

---

## 📂 Project Structure
```text
├── advanced_spam_detector.py   # Main Python source application containing pipeline & UI
├── spam.csv                    # Raw downloaded Kaggle/UCI reference text dataset
└── README.md                   # Project documentation architecture

```

---

## 📊 Dataset Details

This project utilizes the classic **SMS Spam Collection Dataset** sourced from the UCI Machine Learning Repository / Kaggle.

* **Total Instances:** 5,572 text messages.
* **Attributes:**
* `label` (Target): Categorized as either `ham` (legitimate text) or `spam` (unsolicited advertisement/phishing).
* `text` (Feature): The raw alphanumeric message content.


* **Class Imbalance:** The data contains a significant real-world class imbalance, with roughly 86.6% legitimate messages (ham) and 13.4% spam messages.

---

## 🛠️ Technologies Used

* **Programming Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning Framework:** `scikit-learn`
* **Natural Language Processing:** `nltk` (Natural Language Toolkit)
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 🔄 Workflow

```
[Raw CSV Data] ➔ [Exploratory Data Analysis Charts] 
                      │
                      ▼
            [Text Preprocessing] ➔ Lowercasing, Regex Cleaning, Stopword Removal, Porter Stemming
                      │
                      ▼
            [Feature Extraction] ➔ TF-IDF Vectorization Matrix
                      │
                      ▼
             [Model Training]    ➔ Multinomial Naïve Bayes Fitting
                      │
                      ▼
            [Evaluation Layer]   ➔ Metrics Calculation & Confusion Matrix Generation
                      │
                      ▼
          [Interactive Deployment] ➔ Continuous Terminal User-Input Parsing Loop

```

---

## ⚙️ Setup and Run

### 1. Install Dependencies

Open your terminal and install the required core packages via pip:

```bash
pip install pandas scikit-learn nltk matplotlib seaborn

```

### 2. Download the Dataset

1. Download `spam.csv` from [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) or [UCI](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).
2. Move the `spam.csv` file directly into your local project directory alongside your python script.

### 3. Execute the Code

Run the application using the following terminal command:

```bash
python code.py

```

---

## 📈 Output and Results

The Multinomial Naïve Bayes model transforms unstructured string patterns into strong probabilistic flags. Performance metrics are calculated using an 80/20 train-test split:

* **Accuracy:** Evaluates overall correctness across both classes.
* **Precision:** Measures the model's reliability when flagging spam (minimizing False Positives to ensure safe emails aren't lost in junk folders).
* **Recall:** Measures the percentage of actual spam messages correctly intercepted by the filter.
* **F1-Score:** The harmonic mean that balances precision and recall into a single unified performance metric.

---

## 🖼️ Output Screenshots

### Window 1: Dataset Distribution Overview

*(This window visualizes the class imbalances through a Countplot and a Pie Chart before data training commences).*
`[Insert your Dataset Countplot & Pie Chart screenshot here]`
<img width="1256" height="490" alt="output" src="https://github.com/user-attachments/assets/d88390b4-6582-4d80-bfe1-3d2d9b977571" />




### Window 2: Model Performance Metrics

*(This window visualizes the structural classification accuracy via a Confusion Matrix Heatmap alongside a Performance Summary Bar Chart).*
`[<img width="1389" height="490" alt="output1" src="https://github.com/user-attachments/assets/b53d8eb5-049f-4405-9fcc-c03fda742c97" /> ]`



---

## 🏁 Conclusion

The project successfully demonstrates how a fast, computationally efficient statistical model like **Multinomial Naïve Bayes** can achieve highly accurate text filtering when paired with a clean NLP pipeline. Implementing **Porter Stemming** and **TF-IDF Vectorization** effectively allowed the mathematical engine to look past grammatical variations and accurately separate legitimate communications from aggressive spam characteristics. Tracking balanced performance markers like Precision and F1-score ensures the engine can easily scale into production pipelines without risking data loss for the user.

```

```
