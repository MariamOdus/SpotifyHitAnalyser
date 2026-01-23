# SpotifyHitAnalyser: A Music Intelligence & Hit Prediction System

An end‑to‑end machine learning project that predicts the hit potential of songs using a combination of Spotify audio features, metadata, and engineered ML features.  
The system integrates real‑time Spotify API data, multiple ML models (baseline, tree‑based, and neural), interpretability tools, and a Streamlit interface to deliver insights into what makes a song successful.

This project is inspired by real workflows used in music analytics and recommendation systems, combining data science, audio analysis, and product thinking.

---

## Project Goals

- Build a reproducible ML pipeline for predicting hit songs  
- Enrich Kaggle metadata with **real Spotify API features**  
- Explore **audio‑driven** and **metadata‑driven** predictors  
- Compare multiple ML models (baseline → tree‑based → neural)  
- Use **SHAP** to interpret model behaviour  
- Provide a simple **Streamlit app** for interactive predictions  
- Present insights into the drivers of song success  

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
│     ├── models/
│     │     ├── train_baseline.py
│     │     ├── train_xgboost.py
│     │     ├── train_mlp.py
│     │     ├── evaluate.py
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

### **2. Spotify Web API**
Used to enrich the dataset with:
- Detailed audio features  
- Artist metadata (followers, genres)  
- Track metadata (release year, popularity)  

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
- Optional: CNN on spectrograms (future work)  

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

##  Key Insights (to be filled as analysis progresses)



---

## Future Work

- Add spectrogram‑based CNN model  
- Build a similarity‑based recommendation engine  
- Deploy Streamlit app publicly  
- Add genre‑specific hit prediction  
- Experiment with transformer‑based audio embeddings  

---

## Tech Stack

- **Python**  
- **Spotify Web API**  
- **Pandas, NumPy, Scikit‑Learn**  
- **XGBoost, LightGBM**  
- **PyTorch / Keras**  
- **Librosa** (optional audio features)  
- **SHAP**  
- **Streamlit**  

---

## Author

**Mariam Odubayo**  
MSc Artificial Intelligence & Data Analytics  
Passionate about ML, data science, and building intelligent systems that blend analytics with real‑world impact.

