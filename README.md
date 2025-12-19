# 🛒 Amharic E-commerce Data Extractor for FinTech Insights

## 📘 Overview

Telegram has become a major platform for **informal e-commerce in Ethiopia**, with thousands of vendors advertising products, prices, and delivery details through unstructured Amharic messages. While this creates opportunity, it also makes it difficult to **analyze vendors at scale** or assess which businesses are reliable enough for financial services such as loans.

This project builds an **end-to-end data extraction and analytics pipeline** that transforms raw Telegram posts into **structured business intelligence**. By fine-tuning a **Named Entity Recognition (NER)** model for Amharic, the system automatically extracts key entities like **products, prices, locations, and contact information**, and uses them to generate a **vendor scorecard** that supports FinTech lending decisions.

The project was completed as part of the **10 Academy – Artificial Intelligence Mastery Program**.


## 🎯 Business Problem

**EthioMart** aims to become a centralized hub for Telegram-based e-commerce in Ethiopia. To support this vision, the company needs a way to:

* Aggregate data from multiple independent Telegram vendors
* Convert unstructured posts into structured, machine-readable data
* Identify **active, high-value vendors** who are good candidates for micro-loans

Manual processing is not scalable. This project addresses that gap using **NLP and machine learning**.


## 📂 Data Sources

* **Telegram e-commerce channels** (real-time messages and images)
* Amharic NER reference datasets for model training
* Channels include vendors with a combined audience of **360,000+ subscribers**

Data types:

* Amharic text messages
* Product images and documents
* Channel and message metadata


## 🔍 What This Project Does

### 1️⃣ Data Ingestion & Preprocessing

* Collected real-time messages from Ethiopian Telegram e-commerce channels using the **Telegram API**
* Cleaned and normalized Amharic text
* Preserved links between text, images, and metadata
* Stored data in structured JSON format for traceability

### 2️⃣ Named Entity Annotation

* Manually labeled Amharic text using the **CoNLL (BIO) format**
* Core entities:

  * **PRODUCT**
  * **PRICE**
  * **LOCATION**
  * **DELIVERY_FEE**
  * **CONTACT_INFO**
* Created a high-quality gold dataset for model training

### 3️⃣ NER Model Fine-Tuning

* Fine-tuned and evaluated three multilingual transformer models:

  * XLM-RoBERTa
  * Multilingual BERT
  * DistilBERT
* **XLM-RoBERTa** achieved the best performance (F1 ≈ 0.89) and was selected

### 4️⃣ Model Interpretability

* Used **SHAP** and **LIME** to explain token-level predictions
* Verified that the model focuses on meaningful Amharic context words
* Improved trust and transparency for business use

### 5️⃣ FinTech Vendor Scorecard

* Aggregated extracted entities at the vendor level
* Computed business metrics such as:

  * Posting frequency
  * Average product price
  * Estimated reach
* Built a **lending score** to identify strong micro-loan candidates


## 📊 Key Insights

* Transformer-based models can reliably extract business entities from informal Amharic text
* Posting frequency and pricing patterns are strong indicators of vendor activity
* A small number of vendors consistently outperform others in business potential
* Automated extraction enables scalable, data-driven lending decisions

## 🚀 Outcome

The final system converts **messy Telegram posts into structured FinTech intelligence**, enabling EthioMart to:

* Centralize Telegram-based e-commerce data
* Evaluate vendors objectively
* Support micro-lending and business growth with data

## 🧰 Tech Stack

* **Python**
* **Hugging Face Transformers**
* **XLM-RoBERTa**
* **NLTK / SpaCy**
* **SHAP, LIME**
* **Telethon (Telegram API)**
* **Pandas, NumPy**
* **Jupyter Notebook**

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.

---
Let's stay in touch! Feel free to connect with me on LinkedIn:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yitbarektesfaye)

