# Module 12 Report Analysis

## Overview of the Analysis
---------------------------

The purpose of this analysis is to utilize machine learning techniques to predict the possibility of loans defaulting for those clients listed as high-risk (`1`).

* We were provided with a dataset of historical lending activity from a peer-to-peer lending services company. This data is comprised of over seventy-seven thousand borrowers and their current laon status. 
* The total number of current healthy loans (`0`) is 75036, and there are a total of 2500 loans at high-risk (`1`) of defaulting.

* We split our data into two variables, X and y so that we can split the loan status column into its own dataframe for our labels. Once we had our data split, we trained and tested the model to see the accuracy of the prediction capability.

* We utilized a Logistic Regression classifier to retrieve the training and testing data score, both of which scored at 99% proving high accuracy for this model. We then ran a secondary Logistic Regression classifier on re-sampled data, to see if there would be a higher probablity of better accuracy in detecting the high-risk (`1`) laons.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1, Logistic Regression using raw data:
  * Balanced_accuracy_score = 0.9442676901753825
  * :---: | Precision | recall | f1-score | support |
    :---: | :--------:| :-----:| :-------:|:-------:|
    0     |  1.00     |  1.00  |  1.00    |  18759  |
    1     |  0.87     |  0.89  |  0.88    |    625  |
    :---: |  :--:     |  :--:  |  :--:    |  :---:  |
    accuracy   |       |    |  0.99    |  19384  |
    macro avg     |  0.94     |  0.94  |  0.94    |  19384  |
    weaighted avg     |  0.99     |  0.99  |  0.99    |  19384  |

  * | Confusion Matrix Results |
    | :----------------------: |
    | True Positive  : 18679 |
    | False Positive : 80    |
    | True Negative  : 558   |
    | False Negative : 67    |

* Machine Learning Model 2, Logistic Regression using raw data and Random Oversampling:


  * Balanced_accuracy_score = 0.9945026387334079
  * :---: | Precision | recall | f1-score | support |
    :---: | :--------:| :-----:| :-------:|:-------:|
    0     |  0.99     |  0.99  |  0.99   |  75036  |
    1     |  0.87     |  0.89  |  0.88    |    75036  |
    :---: |  :--:     |  :--:  |  :--:    |  :---:  |
    accuracy   |       |    |  0.99    |  150072  |
    macro avg     |  0.99     |  0.99  |  0.99    |  150072  |
    weaighted avg     |  0.99     |  0.99  |  0.99    |  150072  |

  * | Confusion Matrix Results |
    | :----------------------: |
    | True Positive  : 74614 |
    | False Positive : 422    |
    | True Negative  : 74633   |
    | False Negative : 67    |

## Summary

Based on the results of both models, there would be a higher accuracy in predictions utilizing the re-sampled data.This will allow a much better overview of which loans to focus on so that there is preventative methods to prevent a defaulted loan. The performance of this model is showing better consistency in determining our healthy loans (`0`) loans over the high-risk (`1`) loans, as the accuracy in predictions were higher/consistent in both the orignal data and the re-sampled data.

Although I do recommend both models for this sort of task, I would have to say, given the substantial difference in healthy loans (`0`) versus high-risk (`1`) loans, it creates the predictatbility to be better in the model. This is because the positive data ( predicted vs. actually predicted ) is so high and easy to capture when processing the information.
