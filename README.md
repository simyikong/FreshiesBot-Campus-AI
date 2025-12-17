# FreshiesBot: Campus Onboarding Assistant 🎓🤖

[![Framework](https://img.shields.io/badge/Core-Rasa_Open_Source-purple.svg)](https://rasa.com/)
[![Model](https://img.shields.io/badge/NLU-Google_BERT-red.svg)](https://huggingface.co/)
[![Algorithm](https://img.shields.io/badge/Clustering-KMeans-green.svg)]()
[![Integration](https://img.shields.io/badge/API-Google_Geocoding-blue.svg)]()

> **Collaborator:** University of Malaya Student Union (KMUM)  
> **Focus:** Hybrid NLU Pipeline (Unsupervised Clustering + Supervised Classification)

---

## Overview
FreshiesBot is a **24/7 campus onboarding assistant** developed to support the **University of Malaya Student Union (KMUM)** during the peak “Freshies” registration period. The system automates high-volume enquiries related to residential colleges, course registration, and campus navigation.

Unlike conventional chatbots that rely solely on manually labelled intents, FreshiesBot implements a **hybrid data-driven NLU pipeline**. It first applies **K-Means clustering** to discover latent intent groups from raw student query logs, which are then used to train a **BERT-based classifier** for precise and scalable intent recognition.

---

## System Architecture
FreshiesBot employs a multi-stage NLP architecture that combines unsupervised learning for intent discovery with supervised learning for robust intent classification, alongside external API integration for location-based assistance.

### Core Components
- **Unsupervised Intent Discovery:** K-Means clustering on historical student queries
- **NLU Engine:** Rasa Open Source with Google BERT embeddings
- **Entity Recognition:** Transformer-based NER for campus-specific entities
- **Location Services:** Google Geocoding API for real-time navigation guidance
- **Frontend Interface:** Web-based interface for student interaction

---

## Key Technical Features
- **Automated Intent Discovery:**  
  Implemented K-Means clustering to group semantically similar student queries, significantly reducing manual labelling effort for intent definition.

- **Transformer-Based NLU:**  
  Utilises Google BERT embeddings for robust intent classification and named entity recognition, effectively handling campus-specific terminology and informal student language.

- **Geocoding Integration:**  
  Integrates Google Geocoding services to provide real-time navigation assistance for locating residential colleges and campus facilities.

- **Text Preprocessing Pipeline:**  
  Custom preprocessing workflow including tokenisation, lemmatisation, and stop-word removal to reduce noise and improve clustering quality.

---

## Impact
- **Stakeholder Deployment:**  
  Designed in collaboration with KMUM to support student onboarding during intake periods, offloading repetitive administrative enquiries.

- **Operational Benefit:**  
  Validated by Student Union members as an effective tool to reduce manual workload and improve response consistency during high-demand periods.

---

## Tech Stack
- **Frontend:** React.js (Web Application)  
- **NLU Engine:** Rasa Open Source, Google BERT  
- **Machine Learning:** Scikit-learn (K-Means), Pandas  
- **External APIs:** Google Maps / Google Geocoding Service  

---

## Installation

### Install Dependencies
```bash
pip install rasa transformers scikit-learn
````

### Train the Model

```bash
rasa train
```

### Run the Action Server (Geocoding)

```bash
rasa run actions

