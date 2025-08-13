# ai-sector-rotation-portfolio-optimization
AI-driven sector rotation strategy combining deep learning forecasting, reinforcement learning decision-making, and modern portfolio theory for portfolio optimization.


# AI-Driven Sectoral Rotation for Portfolio Optimization  
*Leveraging Deep Learning and Market Trends for Smarter Investment Strategies*  

## Overview  
This project implements a **complete AI-driven investment strategy** that predicts key macroeconomic indicators, classifies the economic cycle, and dynamically reallocates investments across sectors to optimize portfolio performance.  

Using **Deep Learning (LSTM & Transformer)** for forecasting, **Reinforcement Learning (Q-Learning)** for decision-making, and **Modern Portfolio Theory (MPT)** for portfolio optimization, this system delivers automated, data-backed sector rotation strategies.  

---

## Objectives  
- Predict **GDP, Inflation, Unemployment Rate, and Interest Rate** using historical macroeconomic data.  
- Classify **economic phases** (Expansion, Peak, Recession, Recovery) based on forecasted indicators.  
- Implement **Q-Learning** to select the best-performing sector for each economic phase.  
- Optimize sector allocation using **Modern Portfolio Theory** to maximize the Sharpe Ratio.  
- Create a **real-time prediction & recommendation system** for sector overweighting.  

---

## Dataset  
Data is collected from **FRED (Federal Reserve Economic Data)**, including:  
- GDP (Billions USD)  
- Inflation (CPI Index)  
- Unemployment Rate (%)  
- Interest Rate (Fed Funds, %)  
- Sector ETF historical prices (Technology, Healthcare, Energy, Financial, etc.)  

---

## Methodology  
1. **Data Collection & Preprocessing**  
   - Fetch macroeconomic & sector ETF data from FRED.  
   - Convert GDP & Inflation to percentage changes for comparability.  
   - Normalize data using **MinMaxScaler** and structure into time-series sequences (12-month windows).  

2. **Exploratory Data Analysis (EDA)**  
   - Summary statistics, correlation heatmaps, rolling averages, and histograms.  
   - Thresholds determined from histograms for phase classification.  

3. **Macroeconomic Forecasting Models**  
   - **LSTM Model** – Captures sequential dependencies via memory cells.  
   - **Transformer Model** – Uses multi-head attention to model long-term dependencies without RNN bottlenecks.  

4. **Model Evaluation & Comparison**  
   - Metrics: RMSE, MAE, R².  
   - Transformer achieved **higher accuracy** (RMSE=0.0507, R²=0.9455) vs. LSTM (RMSE=0.0825, R²=0.8479).  

5. **Reinforcement Learning – Q-Learning for Sector Allocation**  
   - States: Economic Phases  
   - Actions: Sector Overweighting Decisions  
   - Learned Policy:  
     - Expansion → Industrial  
     - Peak → Technology  
     - Recession → Healthcare  
     - Recovery → Financial  

6. **Portfolio Optimization (MPT)**  
   - Objective: Maximize Sharpe Ratio while minimizing risk.  
   - Optimized Portfolio: Sharpe Ratio = **1.86**, Annual Return = **7.70%**, Volatility = **3.60%**.  

7. **Real-Time Prediction & Recommendation**  
   - Latest macroeconomic data → Forecast using Transformer → Classify phase → Recommend sector.  
   - High alignment between predicted & actual values.  

---

## Results  
- **Best Performing Model:** Transformer  
- **Predicted Economic Phase:** Peak  
- **Recommended Sector:** Technology  
- **Portfolio Performance:**  
  - Annualized Return: **7.70%**  
  - Annualized Volatility: **3.60%**  
  - Sharpe Ratio: **1.86**  

---

## Visuals  
- Correlation Heatmap of Macroeconomic & Sectoral Data  
- Rolling Mean & Standard Deviation of Sector Performance  
- Histogram Distribution of GDP Growth & Inflation Rate  
- Transformer vs LSTM GDP Prediction Comparison  
- Predicted vs Actual Macroeconomic Indicators (Bar Chart)  

---

## Tech Stack  
- **Languages:** Python  
- **Libraries:** TensorFlow, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy  
- **Data Source:** FRED (Federal Reserve Economic Data)  
- **ML Techniques:** LSTM, Transformer, Q-Learning, Modern Portfolio Theory  

---

## Future Enhancements  
- Integrate **more macroeconomic indicators** (e.g., Manufacturing PMI, Consumer Sentiment).  
- Use **advanced Transformers** (e.g., Informer, Temporal Fusion Transformer).  
- Expand to **global economic data** for international portfolio diversification.  
- Deploy as a **web dashboard** for real-time portfolio recommendations.  

---

## Contact  
Nikita Patil  
Email: nikitabpatil2804@gmail.com  
LinkedIn: https://www.linkedin.com/in/nikita-patil-2a9203251/
GitHub: https://github.com/NikitaPatil7

---

*This project demonstrates the integration of AI, financial modeling, and reinforcement learning to develop an adaptive, data-driven sector rotation strategy capable of optimizing returns under different economic conditions.*
