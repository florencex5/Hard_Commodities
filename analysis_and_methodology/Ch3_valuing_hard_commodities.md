# Valuing Hard Commodities in Dynamic Climate -- Analysis Report & Methodology

## OBJECTIVE
* Compare and forecast hard commodities using multiple linear regression and machine learning models, incorporating insights from previous chapters.


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
    * Data was split with 30% reserved for testing,maintaining chronological order.
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
1. Strong correlations among supply chain variables, such as weekly imports and refiner production, introduce **multicollinearity risks**. Diversifying feature selection enhances model robustness, but hidden multicollinearity — such as between supply and demand factors — must be carefully managed.
2. Improper **scaling** can lead to data leakage, undermining predictive reliability. Maintaining proportionality between dependent and independent variables is crucial for preserving model performance
3. Enabling **shuffling** during data splitting introduces volatility that benefits XGBoost. For short-term price forecasting, adjusting the sample size by incorporating seasonal patterns (e.g., based on the same quarter) can achieve comparable effect, improving trend recognition and ensuring balanced training and testing datasets.
4. **Assumption violations** in multiple linear regression models affect absolute validity. However, analyzing these violations provides deeper insights into variable interactions, offering a more comprehensive financial perspective on market behavior.
5. LSTM 
    * While extensive **tuning** enhances statistical accuracy, it risks over-smoothing critical climate-related fluctuations. Increasing past data points to estimate current values makes LSTM less adaptive to short-term market shifts compared to multiple regression, but it remains valuable for capturing long-term trends.
    * Determining an appropriate number of past data points (**timesteps**) is key to recognizing seasonal price patterns in hard commodities. Additionally, effective **outlier** handling is vital, as removing them can disrupt sequential dependencies and skew predictions


## ANALYSIS    
* **Introduction**
    * The concept of equity takes on different meanings across disciplines—whether in law, finance, or climate change—yet it consistently emphasizes the importance of balance. In law, equity ensures fairness by providing flexibility when strict legal rules fall short. In finance, it represents ownership and value. In climate discussions, equity focuses on the fair distribution of resources and responsibilities. Similarly, this analysis seeks to balance key factors affecting commodity prices, aiming to enhance forecasting reliability in an increasingly uncertain environment.
    
* **Part 1: Bridging Equity Valuation Components**
    * Equity valuation traditionally follows a structured approach, with the Free Cash Flow to Firm (FCFF) model serving as a fundamental example. This model consists of two key components: the denominator, which includes the Weighted Average Cost of Capital (WACC) and the sustainable growth rate, and the numerator, representing the firm’s free cash flow.
    * **Chapter 1** explored sustainable growth in the context of climate change, highlighting key valuation factors such as workforce distribution, geographic concentration, and demand patterns, all of which directly impact the denominator. Another critical element—**Total Factor Productivity (TFP)**—though not previously discussed, is essential for industries reliant on hard commodities. As renewable energy adoption grows, the efficiency and reliability of emerging technologies will increasingly shape mineral production and price fluctuations, influencing long-term growth projections.
    * Since hard commodity prices are a primary driver of revenue for energy and mining companies, the analysis shifts from evaluating growth sustainability in the denominator to assessing revenue determinants in the numerator. **Chapter 2** examined the interconnectedness of hard commodity prices with market-relevant factors, such as the Consumer Price Index (CPI), to better understand their relationship with profitability. Building on this foundation, **Chapter 3** takes a more direct approach to revenue forecasting, employing multiple regression and machine learning models to refine commodity price predictions.

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
        * For more details on the analysis and model implementation, please refer to [**Quantitative Analysis – Jupyter notebook**](https://github.com/florencex5/Hard_Commodities/blob/main/crudeOil_project_review.ipynb)
        
* **Part 3:Commodities Valuation Model**
    * **Findings**
        * **Overfitting and Volatility Sensitivity**: XGBoost exhibited poor performance across all three hard commodities. While the adjusted R-squared for the training data was within an acceptable range, a significant decline in the testing data suggested potential overfitting. Additionally, the model failed to capture extreme values, instead smoothing out trends, which does not accurately reflect the high volatility in hard commodities prices under dynamic climate conditions.
            * **Data Imbalance Impact**: Disparities in scale and unit size between the dependent and independent variables, such as futures contract prices versus trading volume, contributed to inconsistencies in the model’s predictions.
        * **Multicollinearity in Forecasting**:Despite high VIF values indicating multicollinearity (e.g., USD/EUR at 1873 for natural gas), these variables consistently ranked among the top five in XGBoost feature importance across all selected hard commodities, including WTI and copper, highlighting their significance in forecasting.(Note: The comparison, based on VIF metrics, is limited by differing feature selections for each commodity, as their unique correlation patterns may affect the generalizability of the results.)
        * **RMSE Comparison**: While lower RMSE generally indicates better model performance, the unit of measurement (USD per barrel vs. USD per metric ton) must be considered when comparing models. Crude oil and natural gas displayed lower RMSE values compared to copper in the valuation.
        * **Assumption and Prediction Quality**: In climate-driven markets, assumption violations in multiple linear regression models are common. While these violations may affect the model’s absolute validity, understanding them provides valuable insights into variable relationships. Statistically, they signal issues, but from a financial perspective, they offer a deeper understanding of market dynamics.
    * **Recommendations**
        * **"Shuffling" vs. Seasonal Data Incorporation**: When splitting data for training and testing, shuffling introduces volatility and complexity, which can enhance XGBoost’s performance. Alternatively, manually incorporating seasonal data can replicate this effect, restoring necessary fluctuations for better trend recognition. This approach not only improves prediction accuracy by creating meaningful “waves” in the data but also ensures a balanced expansion of the training and testing datasets.
        * **Addressing Data Imbalance**: Rather than standard scaling, proportionally adjusting dependent variables (e.g., multiplying by 100) can better align their magnitude with independent variables, minimizing discrepancies in scale and unit size.
        * **Timesteps in Forecasting**: selecting the appropriate number of past data points—referred to as “timesteps”—is crucial for effective forecasting.This determines how much historical data the model considers when forecasting future values. For hard commodities with strong seasonal patterns—such as natural gas prices or gold trading volumes—adjusting timesteps helps capture these variations effectively, enhancing the model’s predictive accuracy.
    * **Note**
        * For more details on the analysis and model implementation, please refer to the corresponding Jupyter notebook.
            * [**WTI Crude Oil**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_wti.ipynb)
            * [**Copper**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_cop.ipynb)
            * [**Henry Hub Natural Gas**](https://github.com/florencex5/Hard_Commodities/blob/main/valuation_model_ng.ipynb)   

        

  






