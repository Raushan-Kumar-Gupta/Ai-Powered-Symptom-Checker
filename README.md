
# 🤖 AI-Powered Symptom Checker Chatbot in Regional Languages

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![IEEE](https://img.shields.io/badge/published-IEEE-green)

> An AI-powered chatbot that helps users check symptoms and get medical advice in **Hindi**, **Telugu**, and **English**, especially useful for non-English-speaking people in rural areas.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Dataset Description](#dataset-description)
- [Methodology](#methodology)
- [Installation & Usage](#installation--usage)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [Evaluation Metrics](#evaluation-metrics)
- [Screenshots](#screenshots)
- [References](#references)
- [License](#license)
- [Citation](#citation)

---

## 🔍 Overview

This project aims to help people who face language barriers in healthcare. It uses **Natural Language Processing (NLP)** and **Machine Learning (ML)** to understand symptoms written in regional languages and give possible disease predictions with advice.

The chatbot is easy to use, and users can simply type their symptoms in natural language. The system will show:
- Likely diseases
- Disease descriptions
- Precautionary steps

---

## 🧠 Features

- 🌐 Supports **English**, **Hindi**, and **Telugu**
- 🤖 Uses **Random Forest** ML model for disease prediction
- 🩺 Gives **precautions** and **descriptions** for each disease
- 🧾 Handles **free-text input** with typos or mixed languages
- 🖥️ Simple GUI with Tkinter
- 📚 Based on real symptom datasets from **Kaggle**

---

## 🏗️ System Architecture

```
User Input (Regional Language)
        ↓
Text Preprocessing (NLP)
        ↓
Symptom Mapping → Feature Extraction
        ↓
Disease Prediction (Random Forest Model)
        ↓
Output (Disease, Description, Precaution)
```

---

## 🗂️ Dataset Description

| Dataset File              | Purpose                                  |
|---------------------------|------------------------------------------|
| `Training.csv`            | Train ML model on symptom–disease pairs  |
| `Testing.csv`             | Evaluate model predictions               |
| `Symptom_Severity.csv`    | Severity level of each symptom           |
| `Symptom_Precaution.csv`  | Precaution steps in English, Hindi, Telugu |
| `Symptom_Description.csv` | Descriptions of diseases                 |

These datasets were translated from English to regional languages and contain over 100+ common symptoms and 40+ diseases.

---

## ⚙️ Methodology

### NLP Preprocessing
- Removes special characters and stop words
- Tokenizes and lemmatizes text
- Matches input with known symptoms using **fuzzy matching**
- Handles **multi-word symptoms** like "red sore around nose"

### Machine Learning
- Uses **Random Forest Classifier**
- Trained to predict top 3 diseases based on symptoms
- Provides confidence score for each prediction

### GUI Interface
- Built using **Tkinter**
- Real-time chatbot display
- Input box for symptoms
- Shows predicted disease, description, and precautions

---

## 🚀 Installation & Usage

### 1. Clone the repo
```bash
git clone https://github.com/Raushan-Kumar-Gupta/Ai-Powered-Symptom-Checker.git
cd Ai-Powered-Symptom-Checker
```

### 2. Install required libraries
```bash
pip install -r requirements.txt
```

### 3. Run the application
```bash
python main.py
```

> Make sure you have Python 3.8+ and Tkinter installed.

---

## 📊 Results

The chatbot gave over **97% accuracy** during testing.

| Model                  | Accuracy | Precision | Recall | F1 Score |
|------------------------|----------|-----------|--------|----------|
| Random Forest          | **0.970**| 0.980     | 0.970  | 0.975    |
| Logistic Regression    | 0.891    | 0.900     | 0.890  | 0.895    |
| SVM                    | 0.897    | 0.900     | 0.895  | 0.897    |
| K-Nearest Neighbors    | 0.718    | 0.730     | 0.720  | 0.725    |
| Decision Tree          | 0.146    | 0.123     | 0.146  | 0.123    |

---

## 🎯 Future Enhancements

- Add more languages like **Bengali**, **Tamil**, and **Kannada**
- Deploy as **Web or Mobile App**
- Integrate with **LLMs** like GPT for smarter conversation
- Add seasonal awareness for better prediction
- Use speech input for accessibility

---

## 🧪 Evaluation Metrics

- **Accuracy**: Correct disease prediction
- **Precision/Recall/F1**: Balances wrong/missed predictions
- **User Feedback**: How well users understand responses
- **Multilingual Handling**: Accuracy across languages

---

## 📸 Screenshots

> Sample: Add screenshots like these in your `screenshots/` folder

- `English` symptom prediction  
- `Telugu` input chatbot display  
- Predicted disease with precautions shown

---

## 📚 References

- 📄 IEEE Published Paper: [AI-Powered Symptom Checker Chatbot in Regional Languages](https://ieeexplore.ieee.org/document/10985720)  
- 📅 Published in: IEEE IATMSI 2025 Conference  
- 👨‍💻 Authors: Raushan Kumar Gupta, R. Henry Koushal, Venkata Sai Pranav C., K. Hemesh Verma, Nandu C. Nair  

---

## 📝 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

---

## 💡 Citation

If you use this work in your research, please cite:

```bibtex
@INPROCEEDINGS{Gupta2025SymptomChatbot,
  author={Gupta, Raushan Kumar and Koushal, R. Henry and Pranav, Venkata Sai and Verma, K. Hemesh and Nair, Nandu C.},
  booktitle={2025 IEEE International Conference on Interdisciplinary Approaches in Technology and Management for Social Innovation (IATMSI)},
  title={AI-Powered Symptom Checker Chatbot in Regional Languages},
  year={2025},
  doi={10.1109/IATMSI64286.2025.10985720}
}
```

---

> Made with ❤️ to make healthcare accessible to every language speaker.
