# Road & Network-aware VANET Traffic Forecasting — Paper Reproduction (RF–GRU)

This repository contains a **paper reproduction / implementation study** of a VANET traffic forecasting approach that combines **road traffic parameters** and **vehicular network features** using a multi-phase pipeline and a hybrid ML/DL model (RF + GRU).

The goal of this project is to reproduce the **reported performance trends** in the reference study by implementing the main stages of the pipeline and evaluating results with standard classification/regression metrics.

---

## Reference Paper
**Network Traffic Prediction Model Considering Road Traffic Parameters Using Artificial Intelligence Methods in VANET**  
(IEEE Access, 2022)

> Note: This project is a *paper reproduction / implementation study*. The paper is not authored by me.

---

## Project Overview
The implementation follows a **three-phase pipeline** inspired by the reference paper:

### Phase 1 — Network Traffic Classification (V2R)
- Preprocessing and cleaning of V2R dataset  
- Feature preparation and traffic classification  

### Phase 2 — Road Traffic Forecasting (V2V)
- Time-series forecasting of road traffic parameters (e.g., sender speed)  
- Implementations with GRU, LSTM, and BiLSTM  
- Optimizer experiments (comparison/tuning)  

### Phase 3 — Feature Fusion + Final Traffic Prediction
- Feature selection and fusion between V2R and predicted road-traffic features  
- Final prediction using hybrid approach (Random Forest + GRU/LSTM-based models)  

---

## Repository Files

### Phase 1
- `journal_phase_1_final_final_modified.py`  
  Data cleaning + V2R traffic classification pipeline

### Phase 2
- `journal_phase2_gru.py`  
- `journal_phase2_lstm.py`  
- `journal_phase2_bilstm.py`  
- `journal_phase2_optimizers.py`  
  Road-traffic forecasting models + optimizer experiments

### Phase 3
- `journal_phase3_feature_selection.py`  
  Feature selection and fusion  
- `journal_phase3_gru.py`  
- `journal_phase3_lstm.py`  
- `journal_phase3_bilstm.py`  
  Final prediction models using fused features

---

## Tools & Libraries
Python, NumPy, Pandas, Scikit-learn, TensorFlow/Keras, Matplotlib

---

## Dataset
The scripts expect CSV files as inputs (example: `lap1.csv`).

> The original dataset used in the reference paper may not be publicly redistributable.  
If the dataset cannot be shared, the code can still remain public.

---

## Author
Elina Shahri  
GitHub: https://github.com/elinashahri
