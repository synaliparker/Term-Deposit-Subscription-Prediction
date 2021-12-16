# Term Deposit Subscription Prediction

Completed for the UT Austin McCombs Artificial Intelligence and Machine Learning Post Graduate Program. 

**Course:** Ensemble Techniques - October 2020

**Score:** 51.5/60

## Project Summary
To help the marketing team in identifying the potential customers for subscribing to a term deposit.

### Skills and Tools
EDA, Supervised Learning, Decision Trees, Visualization

## Project Description

### Goal:

Using the data collected from existing customers, build a model that will help the marketing
team identify potential customers who are relatively more likely to subscribe term deposit
and thus increase their hit ratio.
 
### Attribute Information:

#### Bank client data:
- age: Continuous feature
- job: Type of job (management, technician, entrepreneur, blue-collar, etc.)
-  marital: marital status (married, single, divorced)
- education: education level (primary, secondary, tertiary)
- default: has credit in default?
- housing: has housing loan?
- loan: has personal loan?
- balance in account
#### Related to previous contact:
- contact: contact communication type
- month: last contact month of year
- day: last contact day of the month
- duration: last contact duration, in seconds*
#### Other attributes:
- campaign: number of contacts performed during this campaign and for this
            client
- pdays: number of days that passed by after the client was last contacted from a
            previous campaign (-1 tells us the person has not been contacted or contact
            period is beyond 900 days)
- previous: number of times the client has been contacted before for the last
            campaign to subscribe term deposit
- poutcome: outcome of the previous marketing campaign
#### Output variable (desired target):
- Target: Tell us has the client subscribed a term deposit. (Yes, No)

### Conclusion:
Based on the performance of the models, it seems that the Bagging method is the best. Looking at the Confusion Matrix:

- **True Positive:** Those who would subscribe to tram deposit and have done so. 
- **True Negative:** Those who wouldn't subscribe to term deposit and did not.
- **False Positive:** Those who were predicted to subscribe to term deposit but they actually didn't.
- **False Negative:** Those who were predicted to not subscribe to term deposit and did.

In the case of our goal, we would like to have more false negatives than false positives because the results would exceed expectations. For that reason, it is important to factor the weight of the Recall score. Recall will tell us of those who were identified to subscribe term deposit, what is the fraction of those who were correctly identified? This will ensure that we are getting the most accurate prediction of who will subscribe. The Bagging model has the highest Recall and also the highest training and testing scores even though the data may be slightly overfitting. Based on an initial comparison to other models, perhaps it can be improved in further steps. 
