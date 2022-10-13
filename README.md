# Texas Crime Analysis

### An analysis by: Jose Miguel Boada | Liz McDaneld

## Project Presentation
Click [here](https://miguelb512.github.io/Texas_Crime_Trends/) for a website prensentation of out project. 


[<img src="https://user-images.githubusercontent.com/60283799/195472758-d3287a57-5eef-4588-90b2-b355f574db02.png">](https://miguelb512.github.io/Texas_Crime_Trends/)


## Project Goals and Purpose 

The Greater Houston Area is a large portion of Southeast Texas consisting of 17 counties, and with an estimated population of 7.21 million. The goal is to look at documented crimes from 2015 to 2020 and their statistics to see how the years, counties, and other factors compare and what factors may determine the crime numbers for different counties. Our analysis looks at an overview of all Texas counties, with a focus on Harris County and the Greater Houston area. 

### Questions we aim to answer:

- What are the crime rates for the Houston area?

- What crimes are trending/increased over the past couple years?

- What predictions be made about which crimes are more predominant during certain times of the year?

- Which counties across Texas look similar in crime rates, and what other similarities may they have?

- Have crime rates slowed down the growth of larger Texas counties?

## Project Preplanning

For the first segment of this project a mock QDB with keys and data types is created to visualize the direction and goal of the database.

![QuickDB_Crime_Mock_Analysis](https://user-images.githubusercontent.com/103263248/192550650-58f6d0ef-a07d-4a1f-a09b-e0c69f500bf7.png)

A postgresSQL schema was created to create and idea of how the database will look in SQL.

- Yearly_Crime_Table
![Yearly_Crime_Table](https://user-images.githubusercontent.com/103263248/192550848-89ca33ee-2d4b-4c0d-931b-cab71bfc36b0.png)

- Outter_County_Table
![Outter_County_Table](https://user-images.githubusercontent.com/103263248/192550738-129bb2a4-bce8-4b56-adc7-a6e588af7703.png)

- Harris_Crime_Table
![Harris_Crime_Table](https://user-images.githubusercontent.com/103263248/192550913-a3fe9b7b-2222-43ea-b48d-ea11a426f688.png)

## Database

Our final dataset consisted of all index crimes reported for Texas by County and their reporting agencies. This data was cleaned and explored in our [Crime Data Analysis](https://github.com/MiguelB512/Texas_Crime_Trends/blob/main/Crime_Data_Analysis.ipynb) notebook.
 In our analysis we looked at the data types, changing the year data column to an object to not interfere with the other integer functions. Datetime would be an idea datatype, but with only having the year listed in our raw data, this was the solution found. Columns were renamed to exclude spaces. 

![df](https://user-images.githubusercontent.com/103263248/195412607-e16c94cd-f12e-45de-91a5-b632b3153092.png)

Agencies were counted to get a count of how many agencies reported their crime information for each county and saved to a new DataFrame. 

![reporting_agencies_per_county_per_year](https://user-images.githubusercontent.com/103263248/195412676-6996b099-85c0-4c4e-a72a-6d63b23354d9.png)

A classification of violent and non-violent crimes was created and saved as violent_offenses and nonviolent_offenses columns to hold this information. 

![violent_nonviolent_offenses](https://user-images.githubusercontent.com/103263248/195412695-b23865d9-eba3-4440-b363-79889a9b774f.png)

Then the data is merged back into one main Crime DataFrame to hold the original raw data with the new agency count, violent offenses, and nonviolent offenses columns.

![df_final](https://user-images.githubusercontent.com/103263248/195412718-393a57bd-3322-4a0c-b6df-6e1b1d1d529a.png)

Once the Crime DataFrame was completed and ready to be stored it was exported to CSV files for later use and a SQL table. 

-Crime_Data_table

![crime_table](https://user-images.githubusercontent.com/103263248/195412759-b8fca48b-f1d3-427e-bb8a-1eca9cdc122c.png)

## Machine Learning Model

Our current plan for a machine learning model is using Clustering with K-means and Linear Regression models.
Our feature selections will be looking at the crime rates compared to the population rates of the counties in Texas with a focused comparison on violent to nonviolent crimes. We also took a close look on the Greater Houston, TX Area.
The reason for selecting our model is due to the data not being a fit for supervised machine learning models. When run through supervised machine learning with ensemble and resampling the data was split to small for training and testing purposes.
With unsupervised machine learning and clustering with K-means and Linear regression the data can be split, scaled, fit, and trained with no numerical value issues. 
The data is preprocessed and checked for null values, and duplicate values. A new DataFrame is made to hold the county names separately. The data us then standardized with StandarScaler(). PCA is used to reduce dimension to three principal components, and a new PCS DataFrame is created with them. An Elbow Cure is created to find the best value for K. Predictions are run after initializing the KMeans model. A new Clustered DataFrame is created and data from the Crime DataFrame, and PCS DataFrame, including the predictions held in the 'Class' column, are concatenated on the same columns. 
A 3D Scatter Plot is used to visualize the PCA data and clusters with popup on hover to see crypto data information. 

![Clustering_3d](https://user-images.githubusercontent.com/103263248/195412878-d7ab4e9e-af74-45f7-9d7c-5331cf6ed332.png)

A table with the crime reporting counties is created with the option to sort and select the data. 

![selectalbe_table_ML](https://user-images.githubusercontent.com/103263248/195412949-c35647b9-b922-423f-9873-32bfa55782ac.png)

The data is scaled with MinMaxScaler().fir_transform and a new Plot DataFrame is created to hold the scaled data with the Clustered DataFrame index. A scatter plot is created using hvplot.scatter using x="Violent_Offenses" and y="NonViolent_Offenses" with popups on hover to display data information.

![crime_data_clustering](https://user-images.githubusercontent.com/103263248/195413018-79134d54-59e4-4548-8519-8b76e369cf7a.png)


Our models can be found on our [Machine Learning ](
https://github.com/MiguelB512/Texas_Crime_Trends/tree/main/ML_Models) folder.

Our exploration on trying different supervised machine learning can be found in our [Machine Learning exploration](https://github.com/MiguelB512/Texas_Crime_Trends/tree/main/ML_Exploring) folder.


### Raw Data Sources

[Federal Bureau of Investigation Crime Data Explorer](https://crime-data-explorer.fr.cloud.gov/pages/explorer/crime/crime-trend)

## Communication protocols 

Our communication protocols for how we communicated across this project are as follows:

- Slack

- Zoom

- Google Sheets
### Software & CDNs
| Python |
| Pandas |
| hvplot |
| seaborn |
| plotly |
| SciPy |
| Scikit-learn |
| Visual Studio Code |
| postgresSQL |
| AWS RDS |
| HTML5 |
| CSS |
| Github pages |


