# Geo-Demographic-Segmentation-model-using-ANN

Building an Artificial Neural Networks (ANN) to access the churn rate of a customer (whether a customer will leave the bank or not)

## Business Problem

Suppose certain bank has seen the unusual churn rate (leaving the company) of customers and what to know why ? The task is to build the model using ann to predict if certain customer has probability to leave the bank or not.

## Dataset

The dataset contains the snapshot of 10000 customer details randomly selected before 6 months. The customer details contains the following features (independent features)

- CustomerID
- Surname
- CreditScore
- Geography (country they belong to (3 countries in this case))
- Gender
- Age
- Tenure
- Balance
- NumOfProducts (no. of products customer own)
- HasCrCard (if customer has credit card or not)
- IsActiveMember
- Estimated Salary

After 6 months, the bank has data if the customer leave the bank or not (dependent feature) Exited column with 1(leaved the bank) and 0(still with the bank)

## Solution

Artificial Neural Network is used for creating this geo-demographic segmentation model.
The following steps was taken in creating the model.

- Data Pre-processing
- Building the ANN
- Making the predictions and evaluating the model
- Testing the model with one customer sample

the confusion matrix and the classification report is shown below.

![cm-ann](https://user-images.githubusercontent.com/14214659/72144119-a5f06300-33a0-11ea-90e3-01d6a796a363.png)

![cr_ann](https://user-images.githubusercontent.com/14214659/72144157-b9033300-33a0-11ea-8977-94c7ddbd543b.png)

The accuracy is found to be 84% which is reasonable without any parameter tuning.

As seen in the notebook, with the information available, the model predicts the new customer will not leave the bank.

## Improvements

As the model shows 84% accuracy, the next time the model is trained, it can show slightly different accuracy which leads to the bias-variance tradeoff. So, k-Fold cross validation can be used to fix the variance problem by splitting the training set. Moreover, the model can be improved using he Dropout Regularization to reduce over-fitting if needed. Furthermore, parameter tuning can be used (using GridSearch) tor tuning the model.
