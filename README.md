# Kaggle learning from disaster
Here I uploaded (by now) two Jupyter notebooks where I try to have a highest score in each of them.

## First try
It was developed when I was learning about ML and classification. I did not follow a structured data exploration nor shared my insights. \
Mainly, I jumped right to the Decision Tree. Most of missing data were deleted and treatment wasn't specially good. Surprisingly, the model got a nice acc score of 76.5%

## Second Try - When things got real
Here I expended more time exploring and understanding the train dataset, developed a strategy to deal with missing data.\
Modelling was way easier than the first-try, and I also used Randomized Search CV to get some hyperparameter tuning. \
I also got to explore some different models that I leaned in the meantime (and I still learing).
### What I learning diving in the data
* "Women and children first" seems to be accurate and with that Wealth (first class and
more expensive fares) are by far the most impactful features.
* Passengers of lower classes tends to be younger and carries more siblings
Majority of men are from the third class 60%
* Men tend to be travelling alone (working) and women usually are in families (we are
talking about the 1910's)

![image](https://github.com/vinimoti/Titanic-Kaggle/assets/126615931/d747ac0d-a87f-49df-b803-09e7468d6dd2)
I used the mean to infer the missing age data. But ssould i use a more robust model to infer? (that question is really bugging me out).\

![image](https://github.com/vinimoti/Titanic-Kaggle/assets/126615931/425cb6e0-1d88-45e0-8248-99db74a5cebc)
Analyzing the correlation, maybe using 'Fare' and the classes could not be a good idea because of deep correlation between independent variables (X).

### Modelling and Predcting
Dummy classification was a baseline or more like a major red flag for scoring the following classifications. \
My idea to expand how many models is going to be used came from some notebooks from Kaggle. \
The randomized search cross-validation may look 'too random' but It will be faster and more resource efficient than grid search. 
Since I'm doing hyperparameter tuning with Decision Trees and Random Forests time is a major factor even with a small dataset like this one.


#### Used models... and results (so far)
The following are the results for the cross-validation after some tuning. Using only the train dataset.
* Decision Tree Classifier - best accuracy score: 80.58%
* Random Forest Classifier - best accuracy score: 80.36%
* Gaussian Naive-Bayes - best accuracy score: 75.21%
* Logistic Regression for Classification
* K-Neighbors Classifier
* Support Vector Machine (Classifier)

## Submitting to Kaggle and performance
Results after predicting the test dataset and submitting to the competition on Kaggle.
* Decision Tree Classifier - submission score: 77,5%
* Random Forest Classifier - submission score: 76,5%
* Gaussian Naive-Bayes - submission score: 72,2%

## Whats next?
I will keep developing the Second try notebook and use different classification method. I hope i could do some more robust methods for dealing with features. :) 
