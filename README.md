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
- `keras`, `tensorflow`, `pandas`, `numpy`, `matplotlib`, `seaborn`
- Random `seed` set to **42** for reproducibility.

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
- Note that depending on the random seed, the model performance could change, and another optimizer could become more appropriate. E.g., `Adam`.

### 📈 Visualisation of Predicted Stock Prices vs Actual Stock Prices  
![predicted-vs-actual-prices](imgs/model-results.png)

---

## ⭐ How to Run  
### 1. Clone this repository:
```bash
git clone https://github.com/dorcasshee/lstm-stock-price-prediction.git
cd lstm-stock-price-prediction
```

### 2. [Optional] Create a virtual environment
You may want to use a virtual environment for dependency management. You can run the following commands to create and activate a new virtual environment:
```powershell
python -m venv [venvName] # only run once
[venvName]\Scripts\activate # windows
```
Replace `[venvName]` with your desired virtual environment name. E.g., `lstm-env`.

### 3. [Recommended] Upgrade `pip`
```powershell
python -m pip install --upgrade pip
```

### 4. Install dependencies:  
```powershell
pip install -r requirements.txt
pip install notebook ipykernel
```

### 5. Install `ipykernel` as `[venvName]`
```powershell
python -m ipykernel install --user --name=[venvName] --display-name "Python ([venvName])”
```

### 6. Run `lstm-stock-price-prediction.ipynb` using Jupyter Notebook
```powershell
jupyter notebook
```
Alternatively, you can run the IPYNB file in **Visual Studio Code** if you have the Jupyter extension. Ensure that the kernel is set to `Python ([venvName])`.

### 7. [Optional] Deactivate the virtual environment
Deactivate the virtual environment if you do not need to use it anymore.
```powershell
deactivate
```

---

## ⭐ Let's Connect!
Thanks for checking out this project!  
If you have any questions, feedback, or collaboration opportunities, feel free to reach out!  

🔗 **LinkedIn:** https://www.linkedin.com/in/dorcasshee/  
📧 **Email:** dorcasshee@outlook.com