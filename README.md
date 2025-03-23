## **Comparative Analysis of Machine Learning Stock Selection Models with Embedded-Wrapper Coordinated Screening**
   
## Author: Annie
### **Introduction**
Constructed a 29-dimensional factor matrix,  spanning six key dimensions: value investing (EP/BP/SP/CFP), financial health (Debt-to-Equity Ratio/Cash Ratio/Current Ratio), profitability (GPM/ROE/ROA), growth potential (Sales_Qtrly_Growth/Profit_Qtrly_Growth), technical momentum (RSI/MACD/ARBR), and liquidity features (5D_Volume/60D_Volume/20D_Skewness). In our developed Embedded-Wrapper hybrid screening framework, Random Forest's Gini importance analysis revealed:

Profitability factors dominate predictive power (GPM importance weight=10, ROE/ROA weights exceeding industry mean by 3.2x)
Nonlinear synergistic effects exist between financial leverage (Financial_Leverage weight=9) and asset turnover efficiency (Asset_Turnover weight=8)
Technical indicators exhibit hierarchical stratification - momentum indicator MACD (weight=1) and volatility measure ATR14 (weight=2) show significant negative correlation.
LASSO path recursive tracking at the Wrapper layer further identified: When valuation factors EP/BP (combined weight=1) co-occur with cash flow metric Net_Operating_Cash_Flow (weight=5), the model achieves 13.6% marginal Sharpe ratio enhancement.

The XGBoost delivers 8.51% annualized return (44.2% alpha over benchmark) with Sharpe ratio 0.87  in out-of-sample testing, while reducing maximum drawdown by 8.8% versus baseline. These results validate the structural advantages of multi-factor ecosystems in systematic risk premium capture.


### **Installation**

This project uses JQData, but I have already downloaded the required data, so there is no need to read external data again. The data is solely for testing the framework. The project uses Python 3.11.

 Install conda, then create a virtual environment. 

 ```shell
 conda create --name=ml_stock python=3.11
 ```
 
 After setting up the virtual environment, install the project dependencies.

 ```shell
pip install -r requirements.txt
 ```

Open the notebook:
 ```shell
jupyter lab
 ```
