# Houston Area Crime

### An analysis by: Jose Miguel Boada | Meghan Hull | Liz McDanled

## Purpose:

Analyzing Crime data in the Greater Houston Area Counties to assess what trends and predictions can be made.
## Project Goals

The Greater Houston Area is a large portion of Southeast Texas consisting of 17 counties, and with an estimated population of 7.21 million. Our goal is to look at documented crimes from 2015 to 2020 and their statistics to see how the years, counties, and other factors compare and what factors may determine the crime numbers for different counties. 

### Questions we aim to answer:

- What are the crime rates for the Houston area?

- What crimes are trending/increased over the past couple years?

- Was there a drop in crime, or an increase in crime during the Covid-19 Pandemic?

- If there is another pandemic what prediction can be made about potential crimes?

- What predictions be made about which crimes are more predominant during certain times of the year? 

## Communication protocols 

- Slack

- Zoom

- Google Sheets

Our designated team member roles for this project are:

##### Jose Miguel Boada 
- Responsible for setting up the repository. This includes naming the repository and adding team members. Ensures everyone has his or her own branch to work from. 

##### Meghan Hull 
- Responsible for creating a simple machine learning model. Creating a simple model this early in the design process helps a team better understand where and how a machine learning model will fit into the project. This also grants more time to work out the specifics related to machine learning.

##### Liz McDaneld 
- In charge of the mockup database. Using a SQL-based database, including an ERD of the database and a document pointing out how it is integrated into your database and how it works with the code. 

## Resources

Resources for gathering our data consist of government and city data websites with crime data made available to the public.

### Data Sources & Bespoke Code

1. Link to raw data [^1]

2. Link to code [^2]

[^1]: Texas DPS. "Crime in Texas." [https://min-api.cryptocompare.com/data/all/coinlist](https://crime-data-explorer.app.cloud.gov/pages/home)

[^2]: Jupyter Notebook

## Machine Learning Model

Our current plan for a provisional machine learning model can be found here:

[Machine Learning Preliminary Models](https://github.com/MiguelB512/Harris_Crime_Trends/blob/mhull/MLCode/crime_ML_Models.ipynb)

## Database Integration

For the first segment of this project a mock QDB with keys and data types is created to visualize the direction and goal of the database.

![QuickDB_Crime_Mock_Analysis](https://user-images.githubusercontent.com/103263248/192550650-58f6d0ef-a07d-4a1f-a09b-e0c69f500bf7.png)

A postgresSQL schema was created to create and idea of how the database will look in SQL.

- Yearly_Crime_Table
![Yearly_Crime_Table](https://user-images.githubusercontent.com/103263248/192550848-89ca33ee-2d4b-4c0d-931b-cab71bfc36b0.png)

- Outter_County_Table
![Outter_County_Table](https://user-images.githubusercontent.com/103263248/192550738-129bb2a4-bce8-4b56-adc7-a6e588af7703.png)

- Harris_Crime_Table
![Harris_Crime_Table](https://user-images.githubusercontent.com/103263248/192550913-a3fe9b7b-2222-43ea-b48d-ea11a426f688.png)

From the dataset that was found, explored, and cleaned a sample set of data was pulled and loaded into SQL tables for visualization and provisional machine learning.

- Yearly_Crime_Table
![Yearly_Crime_Table_sample_data](https://user-images.githubusercontent.com/103263248/192551064-8e8519cb-196b-4fe0-a4e4-6fd2fbdac493.png)

- Outter_County_Table
![Outter_County_Table_Sample_data](https://user-images.githubusercontent.com/103263248/192551092-b4dc55ba-6531-41e4-818a-38fc3bf13442.png)

- Harris_Crime_Table
![Harris_Crime_Table_sample_data](https://user-images.githubusercontent.com/103263248/192551106-10a65592-fe19-4fea-aa47-b76dfa95006c.png)


### Software & CDNs

***Table 1: Software & Library Versions***

| Software | Version |
| :--- | :---: |
| Python | 3.7.13 |
| Pandas | 1.3.5 |
| hvplot | 0.7.3 |
| plotly | 5.6.0 |
| SciPy | 1.7.3 |
| Scikit-learn | 1.0.2 |
| Visual Studio Code | 1.70.2 |
