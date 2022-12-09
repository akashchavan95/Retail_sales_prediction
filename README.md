# Retail_sales_prediction

Project Title :
Sales Prediction : Predicting sales of a major store chain Apollo Pharmacy

Problem Description
Apollo Pharmacy operates over 4,000 drug stores. Currently, Apollo Pharmacy store managers are tasked with predicting their daily sales for up to 4 weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.
We are provided with historical sales data for around 1000 Apollo Pharmacy stores. The task is to forecast the "Sales" column for the test set.
Data Description
Apollo Pharmacy Stores Data.csv - historical data including Sales
store.csv - supplemental information about the stores¶


Data fields
Most of the features are self-explanatory.
•	The following are descriptions for those that aren't.
•	Id - an Id that represents a (Store, Date) duple within the test set
•	Store - a unique Id for each store
•	Sales - the turnover for any given day (this is what you are predicting)
•	Customers - the number of customers on a given day
•	Open - an indicator for whether the store was open: 0 = closed, 1 = open
•	StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Diwali holiday, c = Christmas, 0 = None
•	SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
•	StoreType - differentiates between 4 different store models: a, b, c, d
•	Assortment - describes an assortment level: a = basic, b = extra, c = extended
•	CompetitionDistance - distance in meters to the nearest competitor store
•	CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
•	Promo - indicates whether a store is running a promo on that day
•	Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
•	Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
•	PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store


Following are the 7 major steps of building Machine Learning Model :
1.	Collecting Data.
2.	Preparing the Data
•	Exploratory Data Analysis.
•	feature engineering.
3.	Choosing a Model
4.	Training the Model.
5.	Evaluating the Model.
6.	Parameter Tuning.
7.	Making Predictions.
#First thing first importing the necessary libraries for EDA and Machine learning algorithim to train our model.
##Following are the libraries:-
•	NumPy
•	Pandas
•	Matplotlib
•	Seaborn
•	Scikit Learn

CONCLUSION
During the time of our analysis, we initially did EDA on all the features of our datset. We first analysed our dependent variable, 'Sales' and also transformed it. Next we analysed categorical variable and dropped the variable who had majority of one class, we also analysed numerical variable, found out the correlation, distribution and their relationship with the dependent variable using corr() Function and for multicollinearity we use VIF Function defined by us. We also removed some numerical features who had mostly 0 values and hot encoded the categorical variables.
Next we implemented 5 machine learning algorithms Linear Regression,lasso,ridge,decission tree, Random Forest. We did hyperparameter tuning to improve our model performance.
1.	The sales in the month of December is the highest sales among others.
2.	The Sales is highest on Monday and start declining from Tuesday to Saturday and on Sunday Sales almost near to Zero.
3.	Those Stores who takes participate in Promotion got their Sales increased.
4.	Type of Store plays an important role in opening pattern of stores. All Type ‘b’ stores never closed except for refurbishment or other reason.
5.	We can observe that most of the stores remain closed during State holidays. But it is interesting to note that the number of stores opened during School Holidays were more than that were opened during State Holidays.
6.	The R Squared score of all Liner Regression Algorithm with or without Regularization are quit good which is 0.76.
7.	the R Squared score of the Decision Tree Regressor model we got 0.83 on test set which is also good.
8.	The Random Forest regressor model perform very well amoung the others.
9.	There is no such over fitting seen.
10.	We can say that random forest regressor model is our optimal model and can be deploy.

