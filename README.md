# Beta_Bank_Customer_Retention
Beta Bank customers are leaving: little by little, chipping away every month. We need to predict whether a customer will leave the bank soon.

## Goal
Build a model with the maximum possible F1 score. Additionally, measure the AUC-ROC metric and compare it with the F1.

## Data Description

 Features

- RowNumber — data string index
- CustomerId — unique customer identifier
- Surname — surname
- CreditScore — credit score
- Geography — country of residence
- Gender — gender
- Age — age
- Tenure — period of maturation for a customer’s fixed deposit (years)
- Balance — account balance
- NumOfProducts — number of banking products used by the customer
- HasCrCard — customer has a credit card
- IsActiveMember — customer’s activeness
- EstimatedSalary — estimated salary

 Target

- Exited — сustomer has left

## Conclusion
For this project we completed the following:

   Data Preperation:
   - Handled missing values in the `Tenure` column.
   - Looked at distribution of quantitative columns.

    
   Model Creation:
   - Encoding completed since strings were present in our features
   - Split the data into features and target. Our target column was the `Exited` column since we were identifying customers who left.
   - After transforming the features we continued onto scaling them to standardize them.
   
   Model Training:
   - Random Forest: 
       Had an accuracy of 86% before adding adjustments.
       F1 score was 52% before adjustments. 58.9% after.
       AUC-ROC value was 85%.
       
  - Decision Tree:
      Received the accuracy rate of 84%.
      The F1 score before adjustments was 52%. After upsmapling, 53%. With weight class adjustments, 56%.
      The AUC-ROC value is 81%.
      
  - Logistic Regression:
      81% Accuracy rate.
      F1 score of 27%, very low.
      The AUC-ROC value is 75%. Comparing this to the value of the other models, this will most likely not be the preferred model.
      
      
   Final Model Test:
   - The Random Forest had our highest F1 score so we used this model for our final model test.
   - F1 score: 60%
   - Accuracy: 78%
   - AUC-ROC: 78%
      
      
Conclusion:

The Random Forest model seems to be the best in predicting whether customers stay or not with Beta Bank. This most creates a significan number of True Negatives (0), this shows that many customers are likely to stay. This was most likely because of the number of products used and the activity level of the customers at the bank.
