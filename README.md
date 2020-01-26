# Analysis-of-Rossman-Store-Sales
I. INTRODUCTION
In this project, I have applied machine learning techniques to a real-world problem of forecasting the sales of Rossmann store and compared Time series model with regression models. Rossmann store sales prediction was a Kaggle competition. The aim of this project is to find out if time factor analysis on traditional machine learning algorithms outperforms time series analysis and forecasting with ARIMA. I have trained three conventional regression models and compared them with ARIMA. Used feature selection, model selection to improve forecasting results. To compare the models, I used percentage error and accuracy.
Reason for opting this topic is that this is intuitive to understand. Product sales forecasting is vital topic of purchasing management. Forecast of sales is important in maintaining and determining stock levels and perfectly calculating future demands of products.
The project is divided into two python notebooks
1. ARIMA_Model
2.Comparison_Algorithms

II. DATASET
The publicly available dataset is used for this project and has been obtained from Kaggle. We are provided with historical sales data for 1,115 Rossmann stores. There total size of training data is ~ 1 million. Store information is given separately.
The dataset consists of the following columns: 
1.	Id - an Id that represents a (Store, Date) duple within the test set
2.	Store - a unique Id for each store
3.	Sales - the turnover for any given day (this is what you are predicting)
4.	Customers - the number of customers on a given day
5.	Open - an indicator for whether the store was open: 0 = closed, 1 = open
6.	StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
7.	SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
8.	StoreType - differentiates between 4 different store models: a, b, c, d
9.	Assortment - describes an assortment level: a = basic, b = extra, c = extended
10.	CompetitionDistance - distance in meters to the nearest competitor store
11.	CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
12.	Promo - indicates whether a store is running a promo on that day
13.	Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
14.	Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
15.	PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store


III. ALGORITHMS USED
A. Time series with ARIMA:
Autoregressive Integrated Moving Average Model. An ARIMA model is a class of statistical models for analyzing and forecasting time series data. It explicitly caters to a suite of standard structures in time series data, and as such provides a simple yet powerful method for making skillful time series forecasts.

B. Linear Regression: 
Linear regression is a linear approach to modelling the relationship between a scalar response (or dependent variable) and one or more explanatory variables (or independent variables). The case of one explanatory variable is called simple linear regression. For more than one explanatory variable, the process is called multiple linear regressions. [1] This term is distinct from multivariate linear regression, where multiple correlated dependent variables are predicted, rather than a single scalar variable.
Equation of multiple linear regression:
 
Where Y- Dependent Variable
B0- Intercept, B1….Bn – independent variables


C. Random Forest:
Random forests or random decision forests are an ensemble learning method for classification, regression and other tasks that operates by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees. Random decision forests correct for decision trees' habit of over fitting to their training set.

D. XGBoost: 
XGBoost is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable. It implements machine learning algorithms under the Gradient Boosting framework. XGBoost provides a parallel tree boosting (also known as GBDT, GBM) that solve many data science problems in a fast and accurate way. The same code runs on major distributed environment (Hadoop, SGE, MPI) and can solve problems beyond billions of examples.

IV. CONCLUSION
By these experiments, we can conclude that the traditional machine learning algorithms such as XGBoosting and Random forest aid in more efficient prediction of sale compared to time series analysis with ARIMA. Even though the data was time dependent, we can say that by data wrangling we can apply supervised regression algorithm. After changing the shape of data and separating some columns it is possible to achieve better accuracy at predicting the dependent variable Sales. 
When we compared all the regression models with time series model, some models performed well and could yield accurate result as shown in below table.
Number	Model Name	RMSPE	Accuracy
1	Linear Regression	37.5%	63.5%
2	Random Forest	    33.7%	67%
3	XG Boost	        11%	  89%


