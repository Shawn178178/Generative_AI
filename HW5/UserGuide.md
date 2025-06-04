# User Guide - HW5: LLM + RAG Implementation

This guide walks through the use of LLMs enhanced with RAG for better question answering using datasets, web content, and PDFs.

---

## 📦 Dataset Preparation

- Dataset:  
  [Space Missions Dataset (Kaggle)](https://www.kaggle.com/datasets/sameerk2004/space-missions-dataset/data)

- Description:  
  A structured CSV containing metadata about various space missions, including agencies, dates, mission status, and targets.

---

## 🧠 LLM + Embedding + Retriever Setup

1. Load space mission data
2. Create embeddings (e.g. using OpenAI or HuggingFace models)
3. Store in a vector database
4. Use retriever + Mistral LLM to perform question answering

**Prompt Example:**  
「哪個太空任務成功率最高？」

---

## 🌐 RAG with Web Content (SpaceX)

- External content loaded via:
  ```python
  loader = WebBaseLoader("https://www.spacex.com/mission/")
