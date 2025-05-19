# Monte Carlo Simulation for Apparel Demand Forecasting
Developed a Monte Carlo-based forecasting pipeline for XYZ Apparel Ltd. to model multi-source demand uncertainty including order frequency, item selection, quantity, and lead time using time series, classification, and empirical distribution techniques.

## 📋 Overview

This project addresses demand forecasting and uncertainty modeling in the apparel industry using a **Monte Carlo Simulation** approach. The dataset used is transactional in nature and includes customer purchase records over time.

The project has three main components:

1. **Monthly Order Forecasting**  
   Using time-series analysis to predict the number of **distinct monthly orders** based on unique order codes grouped by order dates.

2. **Product Choice Modeling**  
   Building a **classification model** to analyze customer **product selection** behavior. This model incorporates **seasonality** as a key feature, with categorical encoding techniques such as one-hot encoding applied.

3. **Uncertainty Quantification**  
   - Quantity demanded per product is characterized using **empirical quantiles**.
   - Demand **lead time** is similarly analyzed using empirical distributions.
   - These uncertainties are integrated using **Monte Carlo Simulation** to simulate total demand under varied conditions.

---

## 📁 Project Structure

- `215687205_216382558_221167481.ipynb`: Core implementation (data preprocessing, modeling, simulation)
- `data/`: Input datasets
- `results/`: Simulated outputs, plots, and evaluation metrics
- `models/`: Serialized ML models (if applicable)

---

## 🧠 Key Techniques

- **Time Series Analysis** (monthly order forecast)
- **Classification Models**: Logistic Regression, Decision Tree, etc.
- **Seasonality Encoding**: One-hot encoding of seasons
- **Empirical Quantiles**: Using `scipy.stats.mstats.mquantiles`
- **Monte Carlo Simulation**: Synthetic demand generation under uncertainty
- **Evaluation**: Comparison of simulated advance demand with actual advance demand

---

## ⚙️ How to Run

1. Clone this repository and install required packages:
   ```bash
   pip install -r requirements.txt
   ```

2. Launch the notebook:
   ```bash
   jupyter notebook 215687205_216382558_221167481.ipynb
   ```

3. Follow the cell sequence to:
   - Clean & group the dataset
   - Train the time-series & classification models
   - Analyze uncertainties using empirical quantiles
   - Run Monte Carlo simulations
   - Evaluate advance vs urgent demand

---

## 📊 Output Insights

- **Forecasted Order Volumes**: Expected monthly demand trend
- **Product Choice Behavior**: Feature importance in product selection
- **Demand Type Split**:
  - Advance Demand: Known before deadline
  - Urgent Demand: Late-stage demand requiring rush production

---

## 📌 Future Enhancements

- Integrate deep learning for sequential demand modeling
- Real-time inference pipeline for production
- Dynamic seasonality capture using Fourier features

---

## 📚 References

- [scipy.stats.mstats.mquantiles](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mstats.mquantiles.html)
- [Monte Carlo Simulation in Python](https://realpython.com/monte-carlo-simulation-python/)

---

## 🧑‍💻 Authors

- Alekhya Erikipati
- Narotam Daliwali
- Shahand

Final Project for Predictive Modelling  at Schulich School of Business.
