# The Interconnectedness -- Analysis Report & Methodology

## THE PROBLEM
* What role does climate change play in reshaping the relationship between major hard commodities?


## METHODOLOGY
* **Data Selection**
    * *Major commodities*
        * Pair 1: Copper v.s. Aluminum
        * Pair 2: Crude Oil v.s. Natural Gas
    * *Market Relevant Factors*
        * Economic Indicators (Monthly Data)
            * Headline Consumer Price Index(CPI),Core CPI,Energy CPI,Energy Service CPI, Energy Commodities CPI,
            * Personal Consumption Expenditure (PCE)
            * Consumer Sentiment Index (Univerisity of Michigan)
        * Digital Assets - Cryptocurrency (Daily Data)
            * Bitcoin
            * Ether
    * *Defined Timeframes*
        * Past Decade: December 2014 – November 2024
        * Five year: December 2019 – November 2024
        * COVID-19 Period: March 2020 – May 2023
        * Post-COVID Period: June 2023 – November 2024
        
* **Data Frequency Considerations**
    * Economic indicators (CPI, CSI, etc.) are reported on a *monthly* basis.
    * Cryptocurrency data for Bitcoin and Ether is available on a *daily* basis.
    * The difference in data frequency will be accounted for in the analysis methodology.

* **Analysis Methods**
   * Time Series Analysis
   * Hypothesis Testing: Correlation (Pearson & Spearman rank)
   * 
    
* **Limitation**
    * A key limitation arises from aligning monthly macroeconomic indicators with daily commodity trading prices. To ensure consistency and comparability, global copper and aluminum prices are used in place of daily futures trading prices for certain segments of the analysis.
    * The post-COVID period is limited to a smaller sample size (less than 30), which may affect the statistical significance of the findings.
    * The differing operating hours between hard commodities and cryptocurrencies complicate data alignment, leading to exclusion of some cryptocurrency data. The merged data will primarily be aligned with the trading calendars of hard commodities.



## KEY FINDINGS
* ..
* ..


## ANALYSIS
* **Part 1: Historical Correlation Trends of Hard Commodities**
    1. *Copper & Aluminum*
         * Over a 30-year period from January 1990 to November 2024, copper and aluminum prices demonstrated a robust positive correlation, with a coefficient of 0.846.This indicates a traditional “complementary” relationship, where an increase in the price of one commodity typically aligns with a rise in the other.
    2. *...*
        * ..

* **Part 2:Market Relevant Indicators and Hard Commodity Interconnections**
    * **_Factor 1: Headline CPI_**
        * **Introduction** 
            * The relationship between hard commodities and consumer price indices (CPI) has significantly shifted in today’s climate-driven world, marked by the rapid growth of renewable energy technologies and electric vehicles (EVs). These commodities, essential for green energy infrastructure and EV production, contribute to dynamic trends in the CPI while also being influenced by them.
            * Inflation, as reflected by the CPI, drives commodity prices in futures markets, influencing costs and market sentiment. In turn, the essential role of hard commodities in infrastructure and renewable technologies feeds back into consumer prices. Climate-related policies further complicate this dynamic, introducing additional factors—such as various market indicators—that influence the interconnectedness between hard commodities and economic conditions.
        * **Variability in CPI and PCE**
            * Over the past decade, headline CPI, core CPI, and PCE have exhibited similar trends, particularly during the COVID-19 pandemic, when they displayed a distinct “bump” pattern. However, Energy CPI stands out due to its significantly higher volatility, with a variance of 198.655 compared to headline CPI’s 5.252.
            * Within the Energy CPI category, Energy CPI—which includes gasoline (all types) and fuel oil—is the most volatile component, accounting for approximately 268.13% of the total Energy CPI variance. Notably, Energy Commodities CPI recorded a negative annual percentage change of -1.279% in February 2023, plunging further to -26.925% in June 2023. Although it rebounded slightly by November 2024 to -8.458%, energy commodities remained negative throughout most of 2024, reflecting prolonged oversupply or weakened demand.
        * **Headline CPI vs. Copper and Aluminum Prices** 
            * The comparison with headline CPI is initiated for two primary reasons. First, headline CPI captures a broad spectrum of price changes across the economy. Second, despite the increased fluctuation that comes from its inclusion of energy and food prices, the strong correlation between energy prices and hard commodity prices makes headline CPI an appropriate starting point for analyzing the broader economic implications.     
            * When headline CPI is integrated with copper and aluminum prices, strong positive correlations emerge: 0.735 for copper and 0.830 for aluminum. These values suggest that as commodity prices increase, headline CPI tends to rise correspondingly. However, this relationship presents contradictions. While rising CPI typically reduces purchasing power and curtails demand, simultaneous increases in commodity prices often signal heightened demand—implying the influence of additional factors.These inconsistencies underline the complexity of CPI and commodity price dynamics in a climate-driven world. Variables such as stock market performance, influenced by advancements like AI, may also play a critical role in shaping these interconnections.
              
    * **_Factor 2: Cryptocurrency_**
        * **Introduction** 
            * Cryptocurrencies used to have frequent short-term fluctuations, occupy a unique position in contrast to traditional commodities. Bitcoin, often referred to as “digital gold,” differs from traditional gold in that its supply is driven by technological processes. Unlike copper mining in Chile, which relies on physical extraction, cryptocurrency supply depends on *miners* validating and securing blockchain transactions, aligning with the AI-driven era.
        * **Statistical vs. Financial Significance of Crypto Correlations** 
            * Over a five-year period (Dec 2019–Nov 2024), analysis of the crypto spot market revealed a negligible correlation (0.0779) between Ether spot prices and Bitcoin trading volume. While statistically significant due to the large sample size (1826), this correlation lacks financial relevance. In contrast, a one-year analysis (Dec 2023–Nov 2024/sample size: 365) focusing on both the spot and futures markets found a similarly low correlation (0.0702) between Ether spot prices and Bitcoin futures trading volume, which was not statistically significant. These results highlight the disconnect between statistical and financial significance and raise questions about the other potential drivers behind cryptocurrencies correlations.
            * Given the rapid advancements in AI, the complex structure of cryptocurrency supply and demand, and frequent short-term fluctuations, the following analysis will primarily focus on the past three years to explore the evolving interplay between cryptocurrencies and traditional hard commodities.

* **Part 3: Fluctuations -> Analyzing Shifts in Market Dynamics**
    1. **_Contributions by Indicator Categories_**
    
        * **Economic Indicator: CPI**
           * *Headline and Core CPI*
                * The correlation between headline CPI and hard commodity prices has shifted over time. In both the past decade and the COVID-19 period, positive correlations were observed. However, in the post-COVID period, the relationship reversed, with rising commodity prices coinciding with falling CPI. Due to the limited post-COVID sample size (fewer than 30 data points), statistical significance may be impacted. Spearman’s rank correlation analysis reveals the following:
                    * **Copper**: Significant correlation only with core CPI (r = -0.709).
                    * **Aluminum**: Significant correlations with both headline and core CPI, with the strongest correlation with core CPI (r = -0.763).
                * During the past decade and the COVID-19 period, headline CPI demonstrated stronger correlations with commodity prices. However, in the post-COVID period, core CPI exhibited a stronger negative correlation:
                    * **Copper**: headline CPI (r=-0.391) v.s. core CPI (r= -0.709)
                    * **Aluminum**: headline CPI (r=-0.562) v.s. core CPI (r= -0.763)
                    
            * *Energy CPI and Its Components: Energy Commodities and Energy Services*
                * Energy-related CPI components consistently exhibit positive correlations with hard commodity prices across all analyzed periods: the past decade, the COVID-19 period, and the post-COVID period. Notably, during the post-COVID period, Energy Services CPI—encompassing utility services like piped gas and electricity—showed significant shifts:
                    1. Increased Correlations (compared to the COVID-19 period):
                        * **Copper**: Correlation rose to 0.882, a 64% increase.
                        * **Aluminum**: Correlation increased to 0.802, an 18% rise.
                    2. Energy Services CPI - Sustained Significant Correlations:
                        * Unlike Energy Commodities CPI, which showed no significant correlation, Energy Services CPI maintained its strong linkage with both metals.
                        
        * **Digital Assets: Cryptocurrency**
            * *Roles of Different Cryptoassets*
                * Cryptocurrencies, such as Bitcoin, Ether, and Ripple, each play distinct roles in the market, contributing uniquely to market dynamics. To set the stage for analyzing the relationship between cryptocurrencies and traditional hard commodities, this section begins with a comparison of traditional gold and its digital counterpart, Bitcoin.   
            * *Gold vs. Bitcoin*
                * **Comparison During COVID and Post-COVID Periods:** Bitcoin’s correlation with traditional commodities like gold shifted significantly during the COVID-19 and post-COVID periods. Historically, gold had weak correlations with other commodities and cryptocurrencies. However, both gold and Bitcoin showed strong positive correlations with copper and aluminum in the post-COVID period, with a notable correlation of 0.8537 between gold and Bitcoin. This correlation does not indicate shared market drivers: gold’s recent rise is largely attributed to robust demand in the Chinese market, while Bitcoin’s growth was fueled by shifts in U.S. market sentiment following the presidential election.
                * **Key Differences:** Despite Bitcoin being called “digital gold,” their fundamental differences remain. Gold is a physical commodity, whereas Bitcoin is a digital asset based on a decentralized blockchain. This contrast shapes investor behavior: gold attracts conservative investors seeking stability, often following seasonal patterns (E.g. MoM percentage change in volume), while Bitcoin appeals to investors willing to take on higher risks for higher returns, without a strong seasonal pattern.
                
        * **Section Summary**
           * Different market indicators, such as CPI and cryptocurrencies, impact market fluctuations based on their categories and underlying drivers. For example, while Bitcoin and gold may show correlations during certain periods, their price movements are influenced by separate factors. Similarly, the relationship between CPI and commodity prices highlights the influence of non-inflationary elements in shaping market trends. The post-COVID surge in demand for copper aligns with the global shift toward green energy, emphasizing copper’s importance in electricity infrastructure, including power grids for electric vehicles, as reinforced by COP28’s focus on phasing out fossil fuels.
                
    2. **_Multiple Timeframe Analysis_**
         * **Economic Indicator: CPI**
           * Over the 34-year period from January 1990 to November 2024, the correlation between copper and aluminum prices was 0.846. Narrowing the analysis to the past decade (10 years), the correlation increased to 0.910, aligning with the theory that shorter timeframes reduce noise and improve correlation (all else equal). However, during the COVID-19 period (2 years), the correlation dropped slightly to 0.89, suggesting that the relationship remained strong but did not improve further. In the post-COVID period (1.5 years), the correlation decreased to 0.777, reflecting heightened sensitivity to external factors and economic shifts during this time.
           * For Energy CPI and its components, the trends diverged from general expectations. Comparing the COVID-19 period to the preceding decade:
               * **Energy CPI**: Correlation with copper rose by 34%, and with aluminum by 12%.
               * **Energy Commodities CPI**: Copper’s correlation surged by 46%, and aluminum’s by 15%.
               * **Energy Services CPI**: Correlations decreased slightly, with copper falling by 13% and aluminum by 6%.
           * Transitioning from the COVID-19 period to the post-COVID period, the dynamics shifted again:
               * **Energy CPI and Energy**: Commodities CPI: Correlations declined sharply. Notably, Energy Commodities CPI correlations dropped significantly—by 78% for copper and 86% for aluminum.
               * **Energy Services CPI**: Correlations showed marked increases with both metals.
          * **Digital Assets: Cryptocurrency**
             * ...
          * **Section Summary**
            * These results underscore the rapidly evolving interconnections between hard commodities and market factors. While hard commodity trading might seem distant from everyday consumer concerns, changes in these interconnections—shaped by global energy transitions and post-pandemic economic factors—are reflected in consumer-focused metrics like CPI. This emphasizes the importance of analyzing such shifts to understand broader economic impacts, including consumer sentiment and market confidence.

    3. **_Seasonality in Market Trends_**


    * *...*
        * ...

  * **...**
    1. *...*
         * ..
           * ...
           
    2. *...*
        * ..
    3. *...*
        * ...
---
  * **...**
    * ...






