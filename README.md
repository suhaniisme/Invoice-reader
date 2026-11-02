# Invoice Reader 🧾🤖

> An intelligent, automated invoice parsing and document processing application engineered to extract structured data from receipts and invoices using optical character recognition (OCR) and localized machine learning models.
---

## 🎯 About The Project

Manual invoice processing, data entry, and receipt management are time-consuming and prone to human error. **Invoice Reader** is designed to streamline financial workflows for local merchants, small businesses, and developers. 

By combining robust optical character recognition (**EasyOCR**) with intelligent text parsing and optional localized large language models (**Ollama**), this application automates receipt scanning, crops relevant text fields, extracts key line items (such as totals, vendor names, and dates), and formats them for immediate reporting or automated record dispatch.

---

## 🌟 Core Features & Capabilities

* **📷 Smart Image Cropping & Preprocessing**: 
  * Upload receipt or invoice images with built-in tools to crop, align, and optimize image quality for better recognition accuracy.
* **🔍 Automated OCR Data Extraction**: 
  * Powered by **EasyOCR** to accurately scan and parse text elements from varying invoice layouts without relying on expensive third-party cloud APIs.
* **🤖 Local AI-Powered Parsing**: 
  * Integrates local **Ollama** large language models to intelligently structure raw OCR text strings into neat JSON objects, line items, and totals.
* **✉️ Automated Receipt Dispatch**: 
  * Seamlessly format and dispatch parsed invoice receipts directly via structured email workflows.
* **📊 Interactive Dashboard UI**: 
  * Built using **Streamlit** to provide a clean, user-friendly control panel for uploading documents, reviewing extracted data, and exporting reports.

---

## 🛠️ Complete Tech Stack

### **Frontend & User Interface**
* **Framework**: Streamlit (enabling rapid, interactive Python-based web dashboard deployment).
* **Styling & Layout**: Custom CSS and responsive Markdown layouts for clean visual presentation.

### **OCR & Computer Vision**
* **Text Extraction Engine**: EasyOCR / OpenCV for image processing, grayscale conversion, contour detection, and optical character recognition.

### **AI & Natural Language Processing**
* **LLM Orchestration**: Ollama (running local large language models for context-aware receipt structuring and data cleaning).
* **Data Parsing**: Regular expressions (RegEx) and JSON validation wrappers for structured extraction.

### **Data Handling & Dispatch**
* **File Management**: Python file I/O for handling image uploads (`.png`, `.jpg`, `.jpeg`, `.pdf`).
* **Communication**: Built-in Python SMTP / email protocols for automated receipt dispatch.

---

## 🏗️ Project Architecture & Structure

The codebase is organized into a modular structure to separate OCR pipelines, UI components, and parser logic:

```text
Invoice-reader/
│
├── assets/                    # Static images, icons, and sample invoices
├── utils/                     # Helper modules (OCR wrappers, parsers, email dispatch)
├── app.py                     # Main Streamlit application entry point
├── requirements.json /.txt    # Project dependencies
├── .env.example               # Environment variable templates
