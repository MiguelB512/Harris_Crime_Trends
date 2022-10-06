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

## Resources

Resources for gathering our data consist of government and city data websites with crime data made available to the public.

## Google Slides Overview
Click Here: [Google Slides Presentation](https://docs.google.com/presentation/d/1Psy_9680WhK3Fl6l-vSwBj8kEAoRhaeSkPDeJF36BqE/edit?usp=sharing) for a short presentation about the overview of our project 

## Machine Learning Model

Our current plan for a provisional machine learning model is using Clustering with K-means and Linear Regression models.
Our feature selections will be looking at the crime rates compared to the population rates of the counties in Texas with a focused comparison on violent to nonviolent crimes. We also took a close up look on the Houston TX Area.

Our models and exploration of other machine learning models can be found on our [Machine Learning Branch](
https://github.com/MiguelB512/Harris_Crime_Trends/tree/Machine_Learning/ML_Exploring).

- Clustering Crime with K-Means for Texas Counties:

![bokeh_plot](https://user-images.githubusercontent.com/103263248/194184834-b508ff95-5a2d-4ce7-a50a-9bbfb0982ba3.png)

- Clustering Crime with K-Means for Texas Counties in the Greater Houston Area:

![bokeh_plot (1)](https://user-images.githubusercontent.com/103263248/194185501-444e96a6-0645-4e55-b38b-4181ba36aae3.png)

Our Linear Regresion plotting can be found [here](https://github.com/MiguelB512/Harris_Crime_Trends/blob/Machine_Learning/ML_Exploring/Linear_Regression_Plot_Models.ipynb).

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


### Raw Data Sources

(Federal Bureau of Investigation Crime Data Explorer)[https://crime-data-explorer.fr.cloud.gov/pages/explorer/crime/crime-trend]

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
