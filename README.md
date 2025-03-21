# LSTM Stock Price Prediction for SIA

## ⭐ Introduction
This project builds a **Long Short-Term Memory (LSTM)** neural network to predict SIA stock prices.

- The model predicts the **next day's high price** based on the past **52 days of stock performance**.
- 3 models were trained using different **optimizers** (`Adam`, `SGD`, and `RMSProp`) to determine the best-performing model.
- This project was done as part of a machine learning module (ENG335) in my minor coursework.

### 🗂️ Dataset Used
- **Ticker Symbol**: `SIA1.SG`
- **Training** Dataset: **8 years** of **historical stock data (2014-2021)** from Yahoo Finance (`yfinance` API).
- **Testing** Dataset: **2022 stock price data**.

### 📘 Libraries Used
`keras`, `tensorflow`, `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## ⭐ Repository Structure
- 🍞 `lstm-stock-price-prediction.ipynb` – contains data analysis, model training and evaluation
- 🍞 `imgs/` – graphs and visualisations on EDA and comparison of model performance
- 🍞 `requirements.txt ` - lists required Python packages

---

## ⭐ Model Selection & Results
### 📌 Objective
This project evaluates 3 different optimizers (`Adam`, `SGD`, `RMSProp`) to identify the most effective one for **predicting SIA stock prices**.

### 🌟 Best Model: LSTM with RMSProp Optimizer (Model 3)
| **Model** | **Optimizer** | **MSE** | **MAE** | **MAPE** | **R² Score** |  
|-----------|--------------|---------|---------|----------|------------|  
| **Model 1** | Adam | 0.00139 | 0.02801 | 0.00940 | 0.87701 |  
| **Model 2** | SGD | 0.00337 | 0.04675 | 0.01566 | 0.70255 |  
| **Model 3 (Best Model)** | RMSProp | 0.00130 | 0.02645 | 0.00855 | 0.88525 | 

- **Model 3 (RMSProp)** performed the best, achieving the **lowest MSE, MAE, and MAPE**, with the **highest R² Score (0.88525)**.
- **Model 1 (Adam) was a close second**, making it a viable alternative.
- SGD performed the worst, with higher error values and a **noticeable time lag**, where predicted stock prices reacted **slower than actual market trends**.

### 📈 Visualisation of Predicted Stock Prices vs Actual Stock Prices  
![predicted-vs-actual-prices](imgs/model-results.png)

---

## ⭐ How to Run  
### 1. Clone this repository:
```bash
git clone https://github.com/dorcasshee/lstm-stock-prediction.git
cd lstm-stock-prediction
```

### 2. [*Optional*] Create a virtual environment
You may want to use a virtual environment for dependency management. You can run the following commands to create and activate a new virtual environment:
```powershell
python -m venv [venvName] # only run once
[venvName]\Scripts\activate # windows
```

### 3. Install dependencies:  
```powershell
pip install -r requirements.txt
```

### 3. Run `lstm-stock-price-prediction.ipynb` using Jupyter Notebook
Go to Anaconda Prompt and run:
```powershell
jupyter notebook
```
Or if you prefer the **Classic Jupyter Notebook**, follow the instructions at https://github.com/jupyter/nbclassic.

### 4. [*Optional*] Deactivate the virtual environment
```powershell
deactivate
```
