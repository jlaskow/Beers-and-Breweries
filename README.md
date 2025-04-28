# Beers and Breweries
This is a repository for files from the DS 6306 midterm project on beer and brewery data from Budweiser. 

Authors:
  - Joel Laskow
  - Renu Karthikeyan

## Project Summary
This project set out to identify relevant trends hidden within a beer and brewery dataset provided by Budweiser. It is an exercise in exploratory data anaylsis, and uncovers several key trends that warrent further analysis. 


## Data Quality
We have several columns with missing datapoints. 3% of Alcohol by Volume (ABV) and 42% of International Bitterness Units (IBU) are missing.

![image](https://github.com/user-attachments/assets/ab354e42-d86e-4143-8b7b-e35d7b171951)

We impute missing values using the average of each column, however it should be acknowledged that this can skew measurements of bitterness. For instance, median bitterness by State is largely uniform, as again approximately 46% of IBU values were imputed. 

![image](https://github.com/user-attachments/assets/13d1e042-f334-4bca-9d3e-07f81df49acb)




## Observations


### Top States by Number of Breweries

We start by identifying the top 2 states by number of breweries: California (1st) and Colorado (2nd). 

![image](https://github.com/user-attachments/assets/12996070-322f-4e27-9b09-286c3c775f42)

These two states, we speculate, are at the greatest risk of impact from economic fluctuations. Drought, Recession, and Supply Chain Issues in these states in particular could severely hamper production. 


### ABV vs IBU

Despite imputation of missing values, we identify a strong linear trend between alcohol content (ABV) and bitterness (IBU)

![image](https://github.com/user-attachments/assets/2f6065ec-45f8-4048-a8d9-4a216848ec1c)


### Ale Predictions

Using observed correlations between ABV and IBU, we designed a KNN model to classify beers as IPA or Non-IPA. 


![image](https://github.com/user-attachments/assets/b5f81237-4188-4aa8-bfb7-3cf694ebdb8b)

Final model achieved 84% accuracy


### Weak Linear Trends?

To address the missing IBU data, we track IBU misreport percentage compared to the number of brews produced.

![image](https://github.com/user-attachments/assets/f3afc343-e8ba-4e62-a651-1651267bb3a1)

We observe a slight linear trend, however we cannot draw conclusions at this time. Regression analysis is required to draw conclusions. 





## Future Projects
- Evaluate potential linear trends between IBU misreport rate Beer Variety.
- Construct Naive Bayes models to predict likelihood of IBU misreport by state


