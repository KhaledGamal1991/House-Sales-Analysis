# House Sales Analysis

![intro_image](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Intro.jpg)

### Table of Contents

1. [Overview](#Overview)
2. [Business Understanding](#BusinessUnderstanding)
3. [Analysis & Findings](#Findings)
4. [Sale Price Modeling](#Modeling)
5. [Conclusion](#Conclusion)

## Overview <a name="Overview"></a>

Are you interested in buying a house or even selling one? ever wondered what is the best time to buy or sell a house? What is the expected price for your house? then this blog is for you.

In this blog I will analyze the houses sales transactions in Ames city (Ames is a city in Story County, Iowa, United States) using the "Ames Housing dataset". however the concepts of this analysis can be further extended to any house sales dataset.

So let's get started.

## Business Understanding <a name="BusinessUnderstanding"></a>

My objective of this analysis is to answer the following questions:
Q1- What is the best sale time along the year in terms of price and opportunity to sell?
Q2- Which neighborhoods has the highest count of sold units?
Q3- What features affect the sale price and how can we predict it?

In the next section you can find analysis and answers for each of the above questions.

## Analysis & Findings <a name="Findings"></a>

#### *Q1- What is the best sale time along the year in terms of price and opportunity to sell?*

To answer my first question let's have a look at the average sale price and sales count over houses sold time.

From the first figure we notice that average sale price donesn't vary that much over years and months.

![figure_1](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_1.png)

However when we look at the count of sold houses over time we notice that May, Jun and Jul have the highest number of sold houses and this this consistent year after year.

![figure_2](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_2.png)

![figure_3](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_3.png)

From the above we can conclude that May, Jun and Jul time frame is the best time to sell a house and find a buyer soon enough.

#### *Q2- Which neighborhoods has the highest count of sold units?*

If you are buying a house then you might need to make sure that you can sell it back in a short time (secure your investment), so let's have a look at the Neighborhoods with highest sales transactions.

Below count of sales per Neighborhood indicates that some Neighborhoods like "North Ames" has higher demand than other Neighborhoods like "Bluestem" for example.

![figure_4](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q2_1.png)

#### *Q3- What features affect the sale price and how can we predict it?*

Now let's get to the fun part, what features affects the house sale price, and can we predict it.

First le's have a look at the SalePrice distribution, from the below figure we can see that somehow it follows a normal distribution.

![figure_5](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_1.png)

If you were asked, what do you look for when buying a house? I have the following factors in mind which shall affect the sale price (Building Type, Area, Location, quality of building and finishing, utilities, How old it is, has parking or not, Type of sale)

From the dataset, the features that reflect the above factors are:
MSSubClass, MSZoning, Utilities, Neighborhood, BldgType, HouseStyle, OverallCond, HeatingQC, CentralAir, SaleType, YearBuilt --> these are categorical features
GrLivArea, TotRmsAbvGrd, GarageArea

So let's have a look at the above features and see if it really has a relation to the sale price.

1st feature, MSSubClass which Identifies the type of dwelling involved in the sale.
We can see that almost half the dataset are types 20 (1-STORY 1946 & NEWER ALL STYLES) which lies in the upper quartile of average prices 
and 60 (2-STORY 1946 & NEWER) which have the highest average price
both of them are new building (newer than 1946) which might indicate that YearBuilt will be a good feature rather than the MSSubClass itself.

![figure_6](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_2.png)

2nd feature, BldgType: Type of dwelling
Most of the assets are 1Fam "Single-family"
the average price for "TwnhsI", "Duplx", "2FmCon" almsot have the same average price with low count
This might not be a good feature to represent the sales price

![figure_7](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_3.png)

3rd feature, MSZoning which identifies the general zoning classification of the sale.
FV "Floating Village Residential" is the most repeated with highest average price
Although most of the assets are FV, the average price vary from zone to another
Might be a good feature to consider

![figure_8](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_4.png)

4th feature, Neighborhood: Physical locations within Ames city limits
We can notice that the average price vary by neighborhood
Might be a good feature that affects the sale price

![figure_9](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_5.png)

5th feature, Utilities: Type of utilities available
All the assets except one has all utilities, so I'll drop this feature

![figure_10](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_6.png)

6th and 7th features, OverallQual and OverallCond
From the below we notice that OverallQual has strong relation with the price more than OverallCond
I'll consider OverallQual as a feature and drop OverallCond

![figure_11](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_7.png)

![figure_12](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_8.png)

8th feature, HeatingQC: Heating quality and condition
Average price vary per HeatingQC (Heating quality and condition)
I'll consider this feature

![figure_13](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_9.png)

9th feature, CentralAir: Central air conditioning
Most of the assets have central AC, but the average price of Non-centraized AC assets is almot the half of assets with central AC
I'll consider this feature

![figure_14](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_10.png)

10th feature, SaleType: Type of sale
Most of the assets sale type is "Warranty Deed - Conventional", but the average price vary alot between types
I'll consider this feature

![figure_15](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_11.png)

11th feature, YearBuilt: Original construction date
We can see that the prices of new houses are higher in general than old houses
I'll consider this feature

![figure_16](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_12.png)

12th feature, GrLivArea: Above grade (ground) living area square feet
GrLivArea has almost liner relation with the sale price with few exceptions
I will consider this feature
I might just remove the outliers (very huge area more than 4000 and lower saleprice than 200000)

![figure_17](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_13.png)

13th feature, GarageArea: Size of garage in square feet
GarageArea has almost liner relation with the sale price with some exceptions
Some assets have no garage, and in this case the sales price also vary (of course due to other factors)
I will consider this feature

![figure_18](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_14.png)

Now let's see if we missed any features that might be correlated to the sale price.
From the below correlation matrix with numerical features we can find that the sale price is correlated with:
- area (I have selected GrLiveArea to represent this factor)
- YearBuilt (already considered)
- YearRemodAdd (We might have missed this one, let's consider it)
- GarageArea and GarageCars (I have selected GarageArea to represent this factor)

![figure_19](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_15.png)

let's have a look at the YearRemodAdd which indicates remodel date (same as construction date if no remodeling or additions)

![figure_20](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_16.png)

### Sale Price Modeling <a name="Modeling"></a>

Now let go to Sale Price Modeling using the selected features which are ['MSZoning', 'Neighborhood', 'OverallQual', 'HeatingQC', 'CentralAir', 'SaleType', 'YearBuilt', 'YearRemodAdd', 'GrLivArea', 'GarageArea']

Here I have tried two different models (Linear Regression and XGBoost Regressor) and below the two models scores

![figure_21](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q3_17.png)

XGBoost is overfitting with minor difference over the linear regression, so I'll go for the linear regression model for Sale Price modeling.

## Conclusion <a name="Conclusion"></a>

Now let's summarize the findings:
- May, Jun and Jul time frame is the best time to sell a house and find a buyer soon enough.
- Some Neighborhoods has higher demand than other Neighborhoods, so to secure your investment you might need to buy a house in a neighborhood with high demand.
- Features that affects the Sale Price are ['MSZoning', 'Neighborhood', 'OverallQual', 'HeatingQC', 'CentralAir', 'SaleType', 'YearBuilt', 'YearRemodAdd', 'GrLivArea', 'GarageArea'], and we have build a liner regression model to predict the Sale Price with high accuracy which can be used in setting the right price if you are a seller, or checking is a house is over priced if you are a buyer.
- The above analysis can be applied to any Houses Prices dataset from other areas.
