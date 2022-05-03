# Loan-Defaulter-Predictor
we have data of a BFSI domain containing information about several customers and their loan status.. we want to create a multi-class classification model to predict the status of loan. our major focus will be on weather a customer will be a defaulter or not.

steps done to solve problem

1. Import required libraries
2. check and set correct working directory
3. load the dataset
4. check shape of dataset
5. since max columns were 74 so display set to maxium 80 rows and columns
6. check head to see the initial dataset
7. check column names
8. drop unnecessary columns like- id, member_id, grade(because of subgrade), url, zipcode etc.
9. check data types of each column
10. check 5 point summary of all neumeric columns
11. checking null value/ missing value status of each column
12. check percentage of missing vlaues
13. since there were many varibles containing more than 45% missing values so removed all those columns and again check % of missing values
14. replace missing values of continious columns with median
15. remove/drop categorical missing value obeservations from data.
16. since some obeservations were dropped to index set
17. check unique values and frequency counts of dependent varibale
18. create new dependent varibale list based of loan_status column
19. drop original dependent varibale from dataset
20. check outliers by box plot
21. remove outliers through IQR
22. check unique values and their frequency count of each categorical variable
23. created a list containing continious values of emp_length and replaced it in original dataset
24. check mulicolinearity and remove some independent varibales based on this multicolinearity
25. convert categorical values into numerics through onehot encoding
26. one of the major issue is class imbalace in data. tried several ways to deal with this multicolinearity
    a. created some models on imbalanced data but they were not giving good accuracy
    b. tried undersampling but data got reduced much and it was unable to capture all the information/variety of data so not giving good accuracy
    c. lastly tried SMOTE to oversample the data and it as giving good accuracy. but the only problem was we have created some syntehic data which is not a good practice but we didn't have a choise so we have to do it.
    
27. again check class imbalance
28. converted data into array formate for smoot processing
29. split dataset into tarin and test set
30. scaling is done through standard scaler
31. created random forest model
32. predict output on test set
33. find confusion matrix, precision and recall of all classes
34. exported model and scaler in pickle formate
