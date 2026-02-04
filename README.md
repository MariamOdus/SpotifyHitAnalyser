# SpotifyHitAnalyser: A Music Intelligence & Hit Prediction System

An end‑to‑end machine learning project that predicts the hit potential of songs using a combination of Spotify audio features, metadata, and engineered ML features.  
The system integrates Spotify API data, multiple ML models (baseline, tree‑based, and neural), interpretability tools, and a Streamlit (In progress) interface to deliver insights into what makes a song successful.

This project is inspired by real workflows used in music analytics and recommendation systems, combining data science, audio analysis, and product thinking.

---

## Project Goals

- Build a reproducible ML pipeline for predicting hit songs  
- Compare multiple ML models (baseline → tree‑based → neural)  
- Use **SHAP** to interpret model behaviour  
- Provide a simple **Streamlit app** for interactive predictions  

---

## Project Architecture
SpotifyHitAnalyser/
│── README.md
│── requirements.txt
│── data/
│     ├── raw/
│     ├── processed/
│── notebooks/
│     ├── exploration.ipynb
│     ├── model_dev.ipynb
│── src/
│     ├── data/
│     │     ├── fetch_spotify.py
│     │     ├── preprocess.py
│     ├── features/
│     │     ├── audio_features.py
│     │     ├── feature_engineering.py
│     ├── notebooks/
│     │     ├── modelDevelopment.ipynb
│     ├── utils/
│           ├── config.py
│           ├── helpers.py
│── app/
│     ├── streamlit_app.py
│     ├── components/
│── reports/
│     ├── figures/
│     ├── model_results/


---

## Data Sources

### **1. Kaggle Dataset**
Used as the base dataset containing:
- Track metadata  
- Popularity indicators  
- Basic audio features  

---

## Modelling Approach

TrackOracle uses a tiered modelling strategy to compare performance across different ML families:

### **Baseline Model**
- Logistic Regression  
- Establishes a simple benchmark  

### **Tree‑Based Models**
- XGBoost  
- Strong performance on tabular data  

### **Neural Models**
- Simple MLP (feed‑forward network)   

Each model is evaluated using:
- Accuracy  
- F1 score  
- ROC‑AUC  
- Confusion matrix  

---

## Interpretability

Understanding *why* a model predicts a song as a hit is as important as the prediction itself.

TrackOracle uses:
- **SHAP values**  
- **Feature importance plots**  
- **Partial dependence plots**  

These tools help answer:
- *What features drive hit potential?*  
- *How do audio characteristics influence success?*  
- *Which artist or track attributes matter most?*  

---

## Streamlit App

The Streamlit interface allows users to:
- Upload a song or input a track ID  
- Fetch Spotify features in real time  
- Generate a hit‑probability prediction  
- View SHAP explanations  
- Explore similar tracks (future feature)  


---

## Tech Stack

- **Python**   
- **Pandas, NumPy, Scikit‑Learn**  
- **XGBoost**  
- **SHAP**  
- **Streamlit**  

---

## Author

**Mariam Odubayo**  
MSc Artificial Intelligence & Data Analytics  
Passionate about ML, data science, and building intelligent systems that blend analytics with real‑world impact.

