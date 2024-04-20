# Group 14 CMSE202 Final Project
By:
    Michael Facchinello
    Chungmin Lee
    Karen Sandy

# Data Set
hmeq.csv data set link from kaggle
https://www.kaggle.com/datasets/lchipham/home-equity-loan-default

# Presentation Slides link
https://docs.google.com/presentation/d/1GdUMv_dCpzKqR-GrFElH0Ui5J2GA7bIJ/edit#slide=id.p1

# How to Run the Code:

- Run the code cell by cell as you move along through the notebook.
- The hmeq.csv data set is required for this notebook
- This code requires you to use pip install to download the imbalance-learn module. This is built into the notebook.
- Note that the SVM classifier can potentially take a few minutes

# Contributor Roles

Michael Facchinello
- Abstract (Question and Methods)
- Loading in, cleaning, and preliminary data overview (Correlation Matrix, Boxplots, Multivar regressions)
- Solved Imbalanced Classes Issue
- Implemented standard scaler in SVM
- worked on slide show

Chungmin Lee
- Abstract (Discussion)
- Primarily responsible for support vector machine classifier
- Secondarily responsible for multivar regression
- Worked on slide show

Karen Sandy
- Abstract (Results and Conclusion)
- Responsible for logistic classifiers
- Worked on slide show





# Abstract

## Question

The question we aim to answer within our project is, can we build a classifier that successfully predicts whether a borrower defaults or successfully pays off a home equity loan using a dataset containing various borrower financial factors that banks have access to? Secondarily, the project aims to examine the most relevant features or variables that cause defaults. 

## Methodods

Our methodology consists of a preliminary data analysis where we examine relationships within our data, see multivariate regressions and correlation matrices, and determine the impact of outliers and class balance. This preliminary look at the data gives us the information needed to build our classifiers, which consists of 2 logistic classifiers, one with all features and one with only the statistically significant features. An SVM classifier was built as well with a Standard Scaler and grid search to compute the best hyperparameters. 

## Results 

Beginning with a summary, our analysis reveals that the SVM Model exhibited superior predictive performance compared to our logistic classifiers. Utilizing data derived from home equity loans, we embarked upon an analytical journey encompassing a Correlation Matrix examination, multiple regression analysis, logistic regression, and SVM classification.

The first thing we did was run a correlation matrix on our data to see if there were any promising links within our data. However, this yielded nothing for us, as we saw there were no good connections. 

Following up with the correlation matrix, a multiple regression was run, and results were not the best too. Our model had an R-squared value of 0.310. Showing That our model is not best. However, from this we did pin out features that were irrelevant to our investigation. These being Loan, Mortgage due, and value. 
Such a low R squared value did have us investigate more into outliers in our data. We removed outliers and ran the regression again. However, this made our R-squared value even lower. In conclusion we stuck to our original data for onwards investigation.

We ran Logistic regression on our data and our results gave us an overall accuracy of 72 %, mainly because the prediction of our defaulted lenders was extremely low at 55%. This regression was run again without the irrelevant feature, this however, gave us worse results with an accuracy of 53%. 

The SVM classifier we ran gave much better accuracy than the Logistic model, yielding an accuracy of 81% overall. This also gave us fewer false positives and negatives as compared to the Logistic model.

## Discussion

Based on the results what we have done so far would be great for lenders. Assisting them to make decisions on potential borrowers in the future based on their data. Further helping them maximize profits but also not have too many clients' defaults. 

## Conclusions

In conclusion, our analysis of home equity loans data aimed to develop predictive models for identifying future defaulters. Through the application of logistic regression and SVM classification techniques, we determined that the SVM model outperformed logistic regression in terms of predictive accuracy. However, further refinement and optimization of the model are warranted to enhance its predictive capabilities.