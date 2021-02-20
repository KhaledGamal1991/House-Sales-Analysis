# House Sales Analysis

![intro_image](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Intro.jpg)

## Overview

Are you interested in buying a house or even selling one? ever wondered what is the best time to buy or sell a house? What is the expected price for your house? then this blog is for you.

In this blog I will analyze the houses sales transactions in Ames city (Ames is a city in Story County, Iowa, United States) using the "Ames Housing dataset". however the concepts of this analysis can be further extended to any house sales dataset.

So let's get started.

## Business Understanding

My objective of this analysis is to answer the following questions:
Q1- What is the best sale time along the year in terms of price and opportunity to sell?
Q2- Which neighborhoods has the highest count of sold units?
Q3- What features affect the sale price and how can we predict it?

In the next section you can find analysis and answers for each of the above questions.

## Analysis & Findings

#### *Q1- What is the best sale time along the year in terms of price and opportunity to sell?*

To answer my first question let's have a look at the average sale price and sales count over houses sold time.

From the first figure we notice that average sale price donesn't vary that much over years and months.

![figure_1](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_1.png)

However when we look at the count of sold houses over time we notice that May, Jun and Jul have the highest number of sold houses and this this consistent year after year.

![figure_2](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_2.png)

![figure_3](https://github.com/telayat/House-Sales-Analysis/blob/main/Pics/Q1_3.png)

From the above we can conclude that May, Jun and Jul time frame is the best time to sell a house and find a buyer soon enough.

#### *Q2. What is the average availability each month ?*

For this question, I wanted to analyze the occupation of the residences in Boston throughout the year so I measured the availability each month and plotted it as well in the figure below.

![figure_2](https://github.com/fatma-hassanein/BostonAirBNB_Dataset_Analysis/blob/main/images/figure2.png?raw=true)

It shows that the occupation decrease during almost the same months that the prices increased.
This indicates one of two conclusions, either that Boston is not one of the targeted destinations during Winter and Holidays season or the increase in the prices during this time affected the reservation using AirBNB and the renters used another way to find a resident in the city. 

A significant finding as well is that the occupation in Boston is almost 50% on average throughout the year so this make us question the reason for that and study another aspects in the residence.

In my next three questions, I wanted to figure out the aspects that can affect the price or the renters satisfaction and their willingness to rent in Boston. So, I made some analysis to study some of the properties in the dataset and correlate its relation to the price if needed.

#### *Q3. What is the most used cancelation policy in Boston ?*

Well, I looked at the cancellation policies to find if there is a specific policy used mostly around Boston and then, I checked as well if the cancelation policy is correlated with the prices offered for this residence. 

The below figure showed that strict policy was the mostly used at that time followed by the flexible and the moderate policies.

![figure_3](https://github.com/fatma-hassanein/BostonAirBNB_Dataset_Analysis/blob/main/images/figure3.png?raw=true)

Moreover, in the second figure below, it is obvious that the policies become more strict when the price of the resident is more expensive which some how makes sense since as a resident owner, the place is probably more valuable and affecting more his/her revenue in case of cancelation.

![figure_4](https://github.com/fatma-hassanein/BostonAirBNB_Dataset_Analysis/blob/main/images/figure4.png?raw=true)

#### *Q4. What is the average review score for Boston residences ?*

Analysis was done on the available reviews scores in Boston. 
The results as shown below in the figure were very positive showing that most renters are very satisfied with theier residences which is a very encouraging indicator to recommend AirBNB as an option for residences renting in Boston. 

![figure_5](https://github.com/fatma-hassanein/BostonAirBNB_Dataset_Analysis/blob/main/images/figure5.png?raw=true)

#### *Q5. Is the reviews correlated with the price ?*

Further analysis was done to correlate the relation between reviews and prices but turned out to be a bit disappointing. 
That is because as shown in the below figure, price is not that related to the customer satisfaction and his/her review about the residence.

![figure_6](https://github.com/fatma-hassanein/BostonAirBNB_Dataset_Analysis/blob/main/images/figure6.png?raw=true)

## Conclusion

Suming all up after these long analysis:
* Boston is a touristic destination and a targeted city for education and enterpreneurship. 
* The rentals in Boston during Winter are over-priced which can be affecting the occupation.
* The cancellation policies are divided almost equally between strict and moderate to flexible but the policy can be a great indicator for the offered price since they turned to be correlated.
* The reviews average is significantly great in Boston rentals but it is not related to the price of the resident so that means that the residences in Boston are satisfying.
* There are missing revenue oppurtunities for AirBNB since the average occupation is 50% and the renters are satisfied so further analysis is required to find the reasons behind the low occupation despite the good service. 
* Pricing techniques sepcially during different seasons can be a reason for low occupation which can increase by performing more analysis to find aspects that affect the price and encourage owners and AirBNB to follow a scientific way to specify each residence price.
