# VSRD- Viral RNA Silencing Suppressor Database

VSRD is a bioinformatics web application for viral RNA silencing suppressor (VSR) analysis and prediction. The platform integrates VSR-related data browsing, visualization, multi-condition searching, downloading, and machine learning-based functional prediction.

Users can submit amino acid sequences through the web interface, and the backend automatically invokes the integrated XGBoost prediction model to identify potential VSR proteins and return prediction results in real time.

---

## ✨ Features

- 📊 **VSR Dataset Management** - Browse and manage VSR-related data
- 📈 **Interactive Visualization** - Dynamic charts powered by ECharts
- 🔍 **Multi-condition Search** - Flexible filtering and search capabilities
- 💾 **Data Download** - Export datasets for offline analysis
- 🧬 **Sequence Prediction** - Online amino acid sequence analysis
- 🤖 **ML Classification** - ESM-2+XGBoost-based VSR functional prediction
- 🐳 **Dockerized Deployment** - Easy deployment with container technology

---

## 🚀 Quick Start
 - ### Run with Docker

Pull and run the container with a single command:

`docker run -d -p 8000:8000 vsrd:latest`

Then open your browser and visit: http://localhost:8000

- ### Parameter explanation:

-d: Run container in background (detached mode)

-p 8000:8000: Map host port 8000 to container port 8000

---

## 📦 Docker Information

- ### Image Name  ： vsrd

- ### Tag  : latest

- ### Exposed Port  : 8000

- ### Base Image  : python 3.12+

---

## 🛠 Technology Stack

### Frontend 
- HTML

- CSS

- JavaScript

- ECharts - Data visualization library

### Backend 

- Django - Python web framework 

- ESM-2 - Deep feature extraction model

- XGBoost - Machine learning prediction model

---
## 📊 ESM-2+XGBoost Model Information
The prediction model is trained on curated VSR datasets with the following characteristics:

- ### Input: 
Amino acid sequence (FASTA format)

- ### Output: 
Binary classification (VSR / Non-VSR)

- ### Features: 
CLS features extracted by the protein large language model ESM-2

- ### Performance:
 Achieves **96.7%** accuracy, **93.3%** precision, **0.98** AUC , **90.41%** PR AUC, **99.42%** specificity on the validation set. In an independent test set containing 30 samples, the model correctly identified 6 out of 10 VSRs and correctly identified all 20 non VSRs.
