# Chase Coppersmith Data Analytics Portfolio
Different personal analytics projects I've created

## Creating a Bitcoin Price Model using various public datasets
The goal here is to evaluate a wide variety of different publicly available market metrics and examine which (if any) can be used to forecast the price
of Bitcoin. I wanted to test as many metrics as possible, which consisted of also using lagged versions and rolling averages of these metrics. I wanted to create as many potential model features as possible, and get a feel for the relative importance of each group of metrics.

The code performs a number of different tasks to convert various raw data sources into one big data frame, which is then used to model Bitcoin future price over
various time frames. These tasks are briefly outlined below:

- **Read in the data from various sources.**
- **Format data into useable format: Correct date column formats and various data issues, rename columns, aggregate where needed, remove missing values.**
- **Join data togther at various points based on primary key column(s).**
- **Create lagged versions of each numeric column in data frame**
- **Create rolling averages of future Average, High and Low Bitcoin prices to be used as outcome variables.**
- **Create 7 different XGBoost models: 3 day Ceiling and Floor Price, 30 Day Ceiling, Floor, and Average Price, 200 day Ceiling and Floor price:
- **For each model, split data into train and test sets, evaluate different parameters for model and choose most optimal based on RMSE.**
- **Filter out features based on XGBoost built-in Variable Importance function and re-run model building with new set of features.
- **Save model locally for future predictions, as well as final features that are used, so that predictions can be made easily on new data**


