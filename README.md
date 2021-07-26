# RFM
## RFM analysis on raw transaction data

For this project I used the retail transaction and promotion response data set from Kaggle.
The data provides customer and date level transactions for a few years. The data also provides response information of customers to a promotion campaign.

Transaction data provides customer_id, transaction date and amount of purchase. Response data provides the response information of each of the customers. It is a binary variable indicating whether the customer responded to a campaign or not.
Using the provided data I calculated the Recency, Frequency and Monetary values for the dataset. Recency is the number of days since the most recent purchase, Frequency is how many purchases for a number of days and Monetary is total purchase value.

I used RFM as the features and campaign response as the label. I used four different types of models; Decision tree, Linear Regression, Logistic Regression and Random Forest.

The accuracy was very high for every model and the MSE was very low for Linear Regression. The precision and recall for people who did respond to the promotion was very low for most models. This is because of the imbalanced data set. Ten times more people did not respond to the promotion than people who did. 

To account for the imbalanced data set, I used the Balanced Bagging Classifier. The result was less FN (error) for a yes response and more FN (error) for a no response which is what you would expect from a more balanced dataset.

