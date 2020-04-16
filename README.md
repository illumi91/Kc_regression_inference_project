# Kc House Inference Regression Project by Luigi Fiori

# Files

kc_house_data: raw data for kc_house
kc_house_project.ipynb: notebook for EDA
column_names.md: description of the column names
presentation.pdf: Slide presentation

# Approach to the Project

### -Data Mining: Collect necessary data for our project
### -Data Cleaning: Fix data inconsistencies and handle missing values
### -Business Understaning: Ask relevant questions and define the desired outcome
### -Data Exploration: Create data Visualizations to understand your data and make the necessary hypotheses
### -Predictive Modelling: Train Models, evaluate their performance and use them to create predictions



## Introduction

For this project we will be dealing with a regression problem, through the kc_house dataset that contains price, nr. of rooms and others for several zipcodes in the US market.

It's an inference project so the main aim is to evaluate which predictor between our variables is more valuable when calculating the price of a house.

The model I will be using is linear regression.


## Data cleaning

Looking at the histograms we can see that the dataset is composed by many categorical varibles.

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/cat_var.PNG)

The main issue to deal with has been the creation of several dummies variables for each zipcode in order to succesfully implement a linear regression model.

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/dummies.PNG)


## Business understanding

I checked the price over time for each single zipcode trying to get an initial visual understanding.

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/Capture.PNG)


## Data exploration

To respect the normality assumptions I plotted the histograms for each variable.

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/hist.PNG)

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/matrix.PNG)


## Predictive modelling

I applied feature stepwise selection to select the most valuable features.

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/stepwise.PNG)

This one is the best model obtained:

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/final_model.PNG)

Here we can see the top fatures we have found:

![awesome](https://raw.githubusercontent.com/illumi91/Kc_regression_inference_project/master/kc_dataset_images/most_imp_feat.PNG)



# Conclusions

R-squared adj. is 0.58 meausuring a decent 'goodness of fit' of our fitted line.
P-values are all < 0.05 so statistically significant.
An additional bathroom would increase house prices of $85600 so if possible we advise to add an additional bathroom before selling a house.