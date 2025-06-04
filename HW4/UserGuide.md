# User Guide - HW4 LLM Fine-Tuning and Deployment

This document provides instructions for running and customizing the customer churn prediction model.

---

## 📌 Task Overview

- **Used ChatGPT** to search academic literature via prompt.
- **Fine-tuned an LLM** on customer churn data from Kaggle.
- **Deployed the model locally** using Hugging Face + Ollama.

---

## 🔧 How to Use the Colab Notebook

1. Open the notebook:  
   [Colab Notebook](https://colab.research.google.com/drive/1SUFgHhwx6pdwGGJawFbORflBfLZwIQ-h?usp=sharing)

2. Upload the dataset from Kaggle:  
   [Telco Customer Churn](https://www.kaggle.com/datasets/palashfendarkar/wa-fnusec-telcocustomerchurn/data)

3. Format the prompt examples:
   ```python
   "[[The gender of customer is {gender}.]]"
   "[[His/her PaymentMethod is {payment_method}.]]"

  Prediction target:
  "Churn" (Yes / No)

In terminal:
ollama create churn_mistral -f Modelfile
ollama run churn_mistral