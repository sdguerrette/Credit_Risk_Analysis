# Overview
This project utilized supervised machine learning techniques to train a model on a dataset made of credit-lending information provided for free by Learning Tree. Supervised machine learning was chosen due to the known output of the model - whether a lending candidate should be labeled as High Risk or Low Risk. Due to the fact that this is a very unbalanced dataset, with vastly more Low Risk candidates than High Risk, we decided to apply a variety of oversampling, undersampling, combination sampling, and random forest algorythms to balance the data and make our analysis more usueful.

# Analysis
The following shows the results of each out the sampling methods we tested on this dataset.
- ### Random Oversampling
  - Random Oversampling produced a balanced accuracy score of 64.03% with the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 18 42 PM](https://user-images.githubusercontent.com/100643755/179444806-e97fcaba-c2c9-4ec2-a507-701bb99937bb.png)
  - Random Oversampling also produced a 1% precision score for High Risk, with a recall score of 66%. 
  
  ![Screen Shot 2022-07-17 at 9 23 57 PM](https://user-images.githubusercontent.com/100643755/179445142-6f41300c-a2bc-460a-bf56-222dad517445.png)
- ### SMOTE Oversampling
  - SMOTE Oversampling producted a balanced accuracy score of 65.14% with the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 26 38 PM](https://user-images.githubusercontent.com/100643755/179445319-230346c9-3600-45b4-94c6-5930f6c08b1a.png)
  - SMOTE Oversampling also resulted in a 1% precision score for High Risk, with a recall score of 61%
  
  ![Screen Shot 2022-07-17 at 9 27 38 PM](https://user-images.githubusercontent.com/100643755/179445385-f57e924c-7d04-46c6-aca4-b015738b5a12.png)
- ### Undersmapling 
  - Undersampling using the Cluster Centroids method resulted in an a balanced accuracy score of 54.40% with the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 29 52 PM](https://user-images.githubusercontent.com/100643755/179445563-fa5b6348-9dae-47c6-9040-b6d6fc76e256.png)
  - Cluster Centroids also resulted in a 1% precision score, as well as a 69% recall score.
  
  ![Screen Shot 2022-07-17 at 9 30 40 PM](https://user-images.githubusercontent.com/100643755/179445624-b0a9d18d-0ebd-468d-8782-e1c783569f25.png)
- ### Combined Sampling
  - The SMOTEENN method combines oversampling and undersampling in an attempt to mitigate the risks of each. For our dataset, it resulted in a balanced accuracy score of 65.50% and produced the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 32 45 PM](https://user-images.githubusercontent.com/100643755/179445756-3d221ad2-fe77-47ec-b863-df099be12d3d.png)
  - SMOTEENN resulted in a precision score of 1% for High Risk, with a recall score of 75%.
  
  ![Screen Shot 2022-07-17 at 9 33 44 PM](https://user-images.githubusercontent.com/100643755/179445821-28707734-27ae-4619-8e41-a52ffea470ac.png)
- ### Balanced Random Forest Classifier
  - The Balanced Random Forest Classifier, a type of ensemble learner, provided a balanced accuracy score of 78.85% with the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 36 04 PM](https://user-images.githubusercontent.com/100643755/179445959-66da6317-0f5f-4b9b-aca4-f416defea632.png)
  - Balanced Random Forest Classifier also resulted in a 3% precision score and a 70% recovery score.
  
  ![Screen Shot 2022-07-17 at 9 37 12 PM](https://user-images.githubusercontent.com/100643755/179446039-3972c8d0-e3f4-40f2-80ee-a87a9fdd9a08.png)
  - Another feature of this method is the ability to see which of the features (or dataset columns) was most important in determining which result to predict. The following are the top-10 features by importance:
  
  ![Screen Shot 2022-07-17 at 9 38 42 PM](https://user-images.githubusercontent.com/100643755/179446166-c2fb807e-3333-4b5c-b1d3-23a9215215c3.png)
- ADABoost Classifier
  - The Easy Ensemble ADABoost classifier produced a balanced accuracy score of 93.16% with the following confusion matrix:
  
  ![Screen Shot 2022-07-17 at 9 40 06 PM](https://user-images.githubusercontent.com/100643755/179446271-7a1885e6-b861-4f10-9b73-57d127b84b24.png)
  - ADABoost also produced a precision score of 9% for High Risk, as well as a recovery score of 92%
  
  ![Screen Shot 2022-07-17 at 9 41 00 PM](https://user-images.githubusercontent.com/100643755/179446340-146155b0-4c47-42a8-86f2-928087c9c685.png)


  


# Summary
