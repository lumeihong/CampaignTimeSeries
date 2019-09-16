# Solution Explained

Solutions are listed under folders:

* **clean_data**
* **task1 solution**
* **task2 solution**
* **task3 solution**
* **task4 solution**

# Getting Started

## <ins>clean_data</ins>

It contains the data merged and cleaned.

## <ins>task1 solution</ins>

### create dataset sql.docx:

* It contains all SQL for 1. creating table, 2. inserting data using batch insertion 
* SQL was written in MySql console in pythonanywhere: https://www.pythonanywhere.com/user/meihong/databases/
* Postgres was not available for pythonanywhere free account

### data_cleaning.ipynb:

* fill empty values
* clean missing data
* merge multiple csv files
* save to campnew file in clean_data folder

### data_analysis.ipynb:

* plot impressions, total clicks, conversions by country, channel_name, and business_vertical
* plot top 20 sum of impressions and clicks partitioned by channel_name and region for strategy_id =3718750
* plot cumulative sum of impressions and clicks over date in ascending order for strategy_id =3718750
* plot cumulative sum of impressions and clicks by channel_name and region over date in ascending order for strategy_id =3718750
* plot some findings

### other_EDA.ipynb:

* plot impressions, total clicks, conversions histograms

## <ins>task2 solution</ins>

### forecast_analysis_ver1.ipynb:

* analyse trend for impressions, clicks and conversions. Focus on impressions only for now. Analyze all channels
* decompose impressions by its trend, seasonality, and noise
* choose ARIMA model as it is currently the most popular timeseries foracst model
* try to find I by differencing impressions by 1 and 2
* try to find AR and MA (p and q) by plotting ACF and PACF charts
* try to fit the ARIMA model using estimated variables
* try to train the dataset and test the dataset
* try prediction and plot the prediction result
* first prediction result is: 
  * model ARIMA(4,1,6)
  * test MSE: 441642.836, :expressionless: which means in average the model is wrong by about 441642.836 impressions for each prediction made

![Prediction plot](https://github.com/lumeihong/data_science/blob/master/task2%20solution/prediction_ver1.jpg)

### forecast_analysis_ver2.ipynb:

* analyze impressions and only Mobile channel for period before 26Sep2018. Same analysis process as forcast_analysis_ver1.ipynb
* Test MSE: 490615.495
![Prediction plot](https://github.com/lumeihong/data_science/blob/master/task2%20solution/prediction_ver2.jpg)
* forecast result: he impressions for Mobile channel at 2018-10-02 is 1.620175, at 2018-10-09 is 1.688434

| Date  | Impressions |
| :---:  | :---:  |
| 2018-09-26  | 1.804699  |
| 2018-09-27  | 1.420678  |
| 2018-09-28  | 2.203231  |
| 2018-09-29  | 1.841132  |
| 2018-09-30  | 1.573274  |
| 2018-10-01  | 1.657311  |
| 2018-10-02  | 1.620175  |
| 2018-10-03  | 1.702276  |
| 2018-10-04  | 1.716765  |
| 2018-10-05  | 1.690648  |
| 2018-10-06  | 1.688740  |
| 2018-10-07  | 1.680014 |
| 2018-10-08  | 1.683780  |
| 2018-10-09  | 1.688434  |

### forecast_analysis_ver3.ipynb:

* analyze impressions and only Display channel for period before 26Sep2018. Same analysis process as forcast_analysis_ver1.ipynb
* Test MSE: 77272.631
![Prediction plot](https://github.com/lumeihong/data_science/blob/master/task2%20solution/prediction_ver3.jpg)
* forecast result: he impressions for Display channel at 2018-10-02 is -43.852396, at 2018-10-09 is -57.017579
* comment: this forecast result is wrong, the model has to be tried with other pdq variables and trained, which requires more time

| Date  | Impressions |
| :---:  | :---:  |
| 2018-09-26  | -59.572501 |
| 2018-09-27  | -11.221328  |
| 2018-09-28  | 2.125909  |
| 2018-09-29  | -26.901917  |
| 2018-09-30  | -58.436155  |
| 2018-10-01  | -59.436806  |
| 2018-10-02  | -43.852396  |
| 2018-10-03  | -41.451798  |
| 2018-10-04  | -53.603554  |
| 2018-10-05  | -61.283525  |
| 2018-10-06  | -56.877207  |
| 2018-10-07  | -50.803637 |
| 2018-10-08  | -52.093063  |
| 2018-10-09  | -57.017579  |

## <ins>task3 solution</ins>

### Click Analysis.jpg:

* It shows visualization of number of clicks by country, channel_name, business_vertical respectively. It was done in Tableau. https://public.tableau.com/profile/meihong2019#!/vizhome/Campdataanalysis/ClicksAnalysis 

### Conversion Analysis.jpg:

* It shows visualization of number of conversions by country, channel_name, business_vertical respectively. It was done in Tableau. https://public.tableau.com/profile/meihong2019#!/vizhome/Campdataanalysis/ConversionsAnalysis

### Impression Analysis.jpg:

* It shows visualization of number of impressions by country, channel_name, business_vertical respectively. It was done in Tableau. https://public.tableau.com/profile/meihong2019#!/vizhome/Campdataanalysis/ImpressionsAnalysis

### Impressions and Clicks Trend.jpg:

* It shows visualization of cumulative increase of impressions and clicks by channel_name and region over time. It was done in Tableau. https://public.tableau.com/profile/meihong2019#!/vizhome/Campdataanalysis/ImpressionsClicksTrend

### Total Spend CPM.jpg:

* It shows visualization of total spend CPM by country. It was done in Tableau. https://public.tableau.com/profile/meihong2019#!/vizhome/Campdataanalysis/TotalSpendCPM

#### as it was developed using Tableau Community version, the analysis would be published online before saving. If required, I will delete the results from online

## <ins>task4 solution</ins>

### databricks_spark_sql.ipynb:

* Online databricks community was registered first in order to run python and spark sql: https://community.cloud.databricks.com/?o=686829070189825#notebook/2759158575234159/command/2759158575234174.
* Simple sql data selection and spark dataframe are practiced using MovieLens data.

### ml-latest:

* MovieLens full set of data downloaded from https://grouplens.org/datasets/. 
