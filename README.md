![image](https://www.spinxdigital.com/app/uploads/2022/11/image-airbnb.jpg)
# Deal or No Deal?
## A Comprehensive Analysis of NYC Airbnb Listing
**Author:** Sam Choe

**DISCLAIMER:** THIS PROJECT HAS NOT BEEN SPONSORED BY AIRBNB AND WAS CONDUCTED AS AN ACADEMIC EXERCISE

## Project Overview
In the vibrant landscape of New York City, where towering skyscrapers adorn the skyline and a dynamic tapestry of cultures converges, one aspect remains consistent: the steep cost of accommodations. With the Big Apple consistently topping the charts for the most expensive lodging in the country, finding affordable yet comfortable options can be a daunting task for both tourists and residents alike.

As highlighted by industry reports, New York City boasts not only high average room rates but also a limited availability of affordable options, particularly in prime locations like Manhattan. This disparity between demand and supply leaves many travelers grappling with exorbitant prices, often compromising their budgets or settling for less desirable accommodations.

Amidst this backdrop, the emergence of platforms like Airbnb has offered a glimmer of hope, presenting travelers with a plethora of alternative lodging options beyond traditional hotels. However, navigating the vast landscape of Airbnb listings in NYC can be overwhelming, with thousands of properties vying for attention, each with its own set of amenities, locations, and price points.

With access to an Airbnb dataset comprised of almost 67,000 entries, this project aims to uncover the best Airbnb deals in New York City.

## Business Problem 
Navigating the bustling streets and vibrant neighborhoods of New York City can be both exhilarating and overwhelming for tourists. The city's sheer size and complexity, coupled with its frenetic pace and diverse cultural landscape, present numerous challenges for visitors seeking to make the most of their experience. Finding the right accomodations does not have to be one of those challenges, with Airbnb offering great deals for the budget conscious tourists. This project aims to understand the attributes of Airbnb listings that contribute to better deals.

## Data Understanding
For the project, following dataset was utilized for the analysis:
- Airbnb Dataset from Kaggle (https://www.kaggle.com/datasets/paramvir705/airbnb-data)
  
This dataset with 67,122 entries offers a detailed overview of Airbnb listings across the major cities in the U.S. (NYC, LA, SF, DC, Chicago, Boston), providing information on property features, pricing, reviews, and host characteristics. To conduct the comprehensive analysis, we have focused on only NYC Airbnb listings. To understand each listing better, feature engineering was conducted to create items of interest such as the number of amenities provided at the listing, Airbnb host reliability score, as well as an Airbnb experience quality score (our target variable).

While this dataset is extensive, it is important to note that there were some limitations such as the datset only having listings through late 2017 and most NYC listings being concentrated in the Manhattan and Brooklyn boroughs.

## Modeling and Analysis Results
For the modeling process, the preprocessing steps included standard scaling the numerical columns while one hot encoding the categorical column. Models explored were mainly classification centric, with logistics regression, random forest classifier, gradient boosting, and XG Boost classifiers performed and evaluated. The accuracy score was used to compare performance models as the focus was to know how often these models made correct predictions.

Taking the feature importance from one of our best performing models (XG Boost Classifier - performed best on the test set), it became evident that there were features that mattered more than others when considering Airbnb listings. Most notable were the top three: 1) Number of Reviews, 2) Being Brooklyn based, and 3) Price Per Night of the listing.

Why do these features matter? From our logistics regression modeling, we have come to understand the odds related to securing good experience quality Airbnb listings. More specifically, we have learned that:
- For each 1% increase in number of reviews, the odds of a good listing goes up by 25%
- For a 1% increase in association with Brooklyn, the odds of a good listing goes up by 16%.
- For a 1% increase in the listing’s Price Per Night, the odds of a good listing goes up by 6%.

## Conclusion
Visiting New York City can certainly break the bank, but budget conscious tourists can surely find deals on platforms such as Airbnb.

To have the most success in finding a great Airbnb listing, tourists should:

1. Focus on Brooklyn Airbnb listings
2. Target listings with more than 20 reviews
3. Pay a slight premium of up to 10-20% to secure better deals.

Exhibit 1


Exhibit 2


Exhibit 3


## For More Information
- Detailed Analysis: 
- Presentation Deck: 

## Repository Structure
```
|— data                                                      <- Original dataset and database
    |— Airbnb_Data_Info.txt                                  <- Raw data
|— image                                                     <- Screenshots
    |— XXX.jpg                                    <- Screenshot
    |— XXX.jpg                                     <- Screenshot
    |— XXX                                         <- Screenshot
|— README.md                                                 <- Overview of the Project
|— .gitignore                                                <- List of files to exclude
|— airbnb_notebook.ipynb                                     <- Detailed analysis in Jupyter Notebook
|_ presentation.pdf                                          <- PDF version of the project presentation slides
```
