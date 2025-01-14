# ﻿Sales Forcasting

### __Methodology:__
1. Data Exploration and Preprocessing: We start by exploring the provided dataset, gaining a deep understanding of the available features, their relationships, and potential challenges. Through careful preprocessing, we handle missing values, encode categorical variables, and prepare the data for further analysis.

2. Exploratory Data Analysis (EDA): Armed with a rich dataset, we embark on an exploratory journey to uncover hidden patterns, trends, and correlations. Engaging visualizations and statistical techniques help us understand the key factors influencing sales, detect seasonal variations, and identify any intriguing trends that may influence business decisions.

3. Time Series Analysis: Equipped with a solid foundation from EDA, we employ time series analysis techniques to capture the temporal patterns within the sales data. Leveraging the power of models like ARIMA (Autoregressive Integrated Moving Average), we aim to build a forecasting model that can capture the complex dynamics of retail sales.


### __Feature Engineering__
1. Combining store and department information: The 'Store' and 'Dept' columns are combined into a new column called 'Store_Dept' by concatenating their values as strings. This allows for better representation of the relationship between store and department in the dataset.

2. Extracting month and year from the Date column: The 'Date' column is parsed into separate columns for month and year. This allows for easier analysis and grouping of data based on these time components.

3. Calculating the total markdown amount: The individual 'MarkDown' columns are used to calculate the total markdown amount for each record. This aggregation provides a consolidated view of the promotional markdowns for a specific store and department.

4. Encoding categorical variables: Categorical variables, such as the 'IsHoliday' column, are encoded to numerical format. In the example provided, the 'IsHoliday' column is converted to integer values (0 for False and 1 for True). This enables the use of these variables in machine learning algorithms that require numeric input.

5. Merging additional features to the train and test datasets: The 'stores' and 'features' datasets are merged with the train and test datasets based on the common columns 'Store' and 'Date'. This combines the relevant additional information (such as store type, size, temperature, fuel price, etc.) with the corresponding records in the train and test datasets.

### EDA Stores
##### __Countplot of Store Types__
![barplot count store type](https://github.com/arduinto/SalesForecasting/assets/142419799/2d4ca978-dfdf-45b1-b927-9522bfd0be41)

##### __Histplot Distribution of Store Sizes__

![barplot dist store sizes](https://github.com/arduinto/SalesForecasting/assets/142419799/382c26cc-865d-4473-810c-e111d21391cd)

##### __Boxplot Store Sizes by Store Type__

![boxplot store size by store type](https://github.com/arduinto/SalesForecasting/assets/142419799/7c97485f-dfac-446c-8b46-e788f1cad604)

##### __Correlation Matrix__

![corr matrix stores](https://github.com/arduinto/SalesForecasting/assets/142419799/a015ebb0-26ac-4374-8707-d73d27f18aeb)

##### __Histplot Distribution of Weekly Sales__

![dist weekly sales](https://github.com/arduinto/SalesForecasting/assets/142419799/82a81702-97cd-4c05-b778-1a9a64f0f4b5)

##### __Boxplot Weekly Sales by Store__

![boxplot weekly sales by store](https://github.com/arduinto/SalesForecasting/assets/142419799/2d47a58b-933d-472c-a1a1-de719229b1a0)


##### __Boxplot Weekly Sales by Department__

![boxplot weekly sales by dept](https://github.com/arduinto/SalesForecasting/assets/142419799/c2f56c73-a97b-44fe-ad38-190991339f8f)

##### __Lineplot Weekly Sales Over Time__

![lineplot weekly sales over time](https://github.com/arduinto/SalesForecasting/assets/142419799/2414c82c-bc66-4e47-a7ca-eaef3f5f03a8)

##### __Scatterplot Weekly Sales vs. Temperature__

![scatter plot weekly sales vs temp](https://github.com/arduinto/SalesForecasting/assets/142419799/b5dcd076-31ff-4bed-9511-b2c24db62261)

##### __Correlation Matrix - Train Dataset__

![corr matriix train dataset](https://github.com/arduinto/SalesForecasting/assets/142419799/f3fce807-e6f4-4ce7-a7e7-d6ad8aee6cad)

##### __Histplot Distribution of Numerical Features__

![histplot dist numerical features](https://github.com/arduinto/SalesForecasting/assets/142419799/d87e5e44-f0c5-416b-91c6-2273b7db426f)
![histplot dist numerical features 2](https://github.com/arduinto/SalesForecasting/assets/142419799/949a0967-d4de-4750-8d9c-9c39375a9938)

##### __Pairplot Features__

![pairplot](https://github.com/arduinto/SalesForecasting/assets/142419799/0a1a9638-3be9-4d95-8e1a-fa57b9249dea)


##### __LinePlot Sales Forecast for Store 1 and Department 1

![sales forecast for store 1 and department 1](https://github.com/arduinto/SalesForecasting/assets/142419799/a75ff3f0-a9e9-4852-8043-2a924adcfb0c)

##### __Lineplot Decomposition Observed, Trend, Seasonal and Residuals__

![plot decomposition](https://github.com/arduinto/SalesForecasting/assets/142419799/24bfe3c6-c9f9-4fbc-bfa8-7effb42d1737)
