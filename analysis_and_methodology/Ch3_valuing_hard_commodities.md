# Valuing Hard Commodities in Dynamic Climate -- Analysis Report & Methodology

## OBJECTIVE
* Evaluate and compare the performance of multiple linear regression and advanced machine learning models (LSTM, XGBoost)
* Forecast hard commodities, incorporating insights from previous chapters.


## METHODOLOGY
* **Data Selection**
    * *Major Hard Commodities (Dependent Variables)*
        1. WTI Crude Oil
        2. Copper
        3. Henry Hub Natural Gas
    * *Feature Selection (Independent Variables)*
        * Futures Close Price & Trading Volume: Copper, Aluminum, Gold, WTI Crude Oil, Henry Hub Natural Gas
        * Volatility Index (VIX)
        * USD/EUR Exchange Rate
        * Electricity Daily Generation Per Energy Source
        * Electricity Power Operations - Total Interchange
    * *Timeframes*: May 2024 - November 2024
* **Data Preprocessing**
    * Data was split with 30% reserved for testing.
    * MinMax scaling was applied consistently across all models.
* **Analysis Methods**
    * Multiple Linear Regression
    * Machine Learning Model
        * XGBoost
        * Long Short-Term Memory (LSTM)
* **Data Source**
    * U.S. Energy Information Administration (EIA)
    * Yahoo Finance
    * Alpha Vantage
* **Limitations**
    * Different types of models could limit the power of comparison.
    * The choice of splitting and scaling methods can impact results.
    * Variations in library versions (e.g., scikit-learn, XGBoost) can affect outcomes.
    * All findings and recommendations are based on a selected period and features. The results may vary with different datasets, market conditions, or feature selections.


## KEY FINDINGS
1. ...


## ANALYSIS
* **Introduction**
    * ...
    
* **Part 1: Bridging Equity Valuation Components**
    * Equity valuation traditionally follows a structured approach, with the Free Cash Flow to Firm (FCFF) model serving as a fundamental example. This model consists of two key components: the denominator, which includes the Weighted Average Cost of Capital (WACC) and the sustainable growth rate, and the numerator, representing the firm’s free cash flow.
    * **Chapter 1** explored sustainable growth in the context of climate change, highlighting key valuation factors such as workforce distribution, geographic concentration, and demand patterns, all of which directly impact the denominator. Another critical element—**Total Factor Productivity (TFP)**—though not previously discussed, is essential for industries reliant on hard commodities. As renewable energy adoption grows, the efficiency and reliability of emerging technologies will increasingly shape mineral production and price fluctuations, influencing long-term growth projections.
    * Since commodity prices are a primary driver of revenue for energy and mining companies, the analysis shifts from evaluating growth sustainability in the denominator to assessing revenue determinants in the numerator. **Chapter 2** examined the interconnectedness of hard commodity prices with market-relevant factors, such as the Consumer Price Index (CPI), to better understand their relationship with profitability. Building on this foundation, **Chapter 3** takes a more direct approach to revenue forecasting, employing multiple regression and machine learning models to refine commodity price predictions.

* **Part 2: Reviewing Forecasting Approaches**
    * In the [*previous analysis*](https://github.com/florencex5/Crude_Oil_Finance_Project), XGBoost was utilized for crude oil forecasting, but it lacked detailed statistical analysis. To address this, a multiple linear regression model will be applied to better understand the relationships between key factors and their coefficients. While crude oil prices may not exhibit a strictly linear relationship with these factors, this approach will provide a foundational understanding before advancing to more complex models like XGBoost.
    * **Findings**
        * **Multicollinearity**: Strong correlations among supply chain features—e.g., a high positive correlation between weekly imports and refiner production—necessitates more diversified feature selection for robust modeling.
        * **XGBoost vs. Multiple Regression**: XGBoost, which is free from strict assumptions, handles extreme values better, making it suitable for hard commodities amid climate uncertainties. However, its reliance on preprocessing and data selection introduces risks, as dataset scaling before splitting and the use of shuffling led to potential data leakage, compromising predictive reliability.
        * **Outlier Impact**: In hard commodity forecasting, outliers can have lasting effects. In LSTM models, removing outliers disrupts sequential patterns, potentially leading to inaccurate forecasts. Proper handling of outliers—whether through removal or winsorization—requires careful consideration of industry-specific factors.
        * **LSTM Limitations for Hard Commodities**: 
            1. **Tuning vs. Practical Accuracy**: Despite its slightly higher RMSE, one of LSTM’s drawback lies in extensive tuning, which enhances statistical accuracy but weakens its ability to capture climate-related factors and real-world dynamics.
            2. **Over-Smoothing Risk**: Excessive tuning may smooth out critical market volatilities. While multiple regression, depending on feature selection and time horizon, may offer more responsive predictions, LSTM remains valuable for capturing long-term trends.
    * **Note**
        * For more details on the analysis and model implementation, please refer to [**Jupyter notebook**](https://github.com/florencex5/Hard_Commodities/blob/main/crudeOil_project_review.ipynb)
        
* **Part 3:Commodities Valuation Model**
    * **Findings**
        * **Overfitting and Volatility Sensitivity**: XGBoost exhibited poor performance across all three hard commodities. While the adjusted R-squared for the training data was within an acceptable range, a significant decline in the testing data suggested potential overfitting. Additionally, the model failed to capture extreme values, instead smoothing out trends, which does not accurately reflect the high volatility in hard commodities prices under dynamic climate conditions.
            * **Data Imbalance Impact**: The model’s accuracy was likely affected by the imbalance between the dependent variable (e.g., unscaled hard commodities prices) and the independent variables (e.g., scaled trading volume). This disparity could contribute to predictive inaccuracies.
        * **Multicollinearity in Forecasting**: Despite multicollinearity issues, some highly correlated features, such as USD/EUR and daily electricity generation by natural gas, remained influential in XGBoost models, indicating their importance in forecasting models.
        * **RMSE Comparison**: While lower RMSE generally indicates better model performance, the unit of measurement (USD per barrel vs. USD per metric ton) must be considered when comparing models. Crude oil and natural gas displayed lower RMSE values compared to copper in the valuation.
        * **Assumption and Prediction Quality**: In a climate-driven market, violations of assumptions in multiple linear regression models are often unavoidable. However, despite these challenges, multiple linear regression remains a valuable tool for generating meaningful and reliable forecasts. Its strength lies in its ability to analyze the interconnections among independent variables, providing deeper insights into market dynamics.
    * **Recommendation**
        * **"Shuffling" vs. Seasonal Data Incorporation**: When splitting data for training and testing, shuffling introduces volatility and complexity, which can enhance XGBoost’s performance. Alternatively, manually incorporating seasonal data can replicate this effect, restoring necessary fluctuations for better trend recognition. This approach not only improves prediction accuracy by creating meaningful “waves” in the data but also ensures a balanced expansion of the training and testing datasets.
        * **Timesteps in Forecasting**: selecting the appropriate number of past data points—referred to as “timesteps”—is crucial for effective forecasting.This determines how much historical data the model considers when forecasting future values. For hard commodities with strong seasonal patterns—such as natural gas prices or gold trading volumes—adjusting timesteps helps capture these variations effectively, enhancing the model’s predictive accuracy.
        * **...** 
            * ...
            * ...
    * **Note**
        * For more details on the analysis and model implementation, please refer to the corresponding Jupyter notebook.
            * [**WTI Crude Oil**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_wti.ipynb)
            * [**Copper**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_cop.ipynb)
            * [**Henry Hub Natural Gas**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_ng.ipynb)   

        

  






