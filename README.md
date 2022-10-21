# Neural_Network_Charity_Analysis

## Overview of the Analysis:
Looking at the data provided, there are more than 34,000 organizations that have received funding from Alphabet Soup over the years. Using this data I will create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. To do this I will preprocess the data for a Neural Network Model, compile, train and evaluate the model, and finally, optimize the model.

## Results:
<img width="472" alt="Screen Shot 2022-10-21 at 4 23 05 PM" src="https://user-images.githubusercontent.com/106630710/197304529-d31881e2-8bef-4034-92a0-a008986348b1.png">

#### What variable(s) are considered the target(s) for your model?
  - "IS_SUCCESSFUL"
#### What variable(s) are considered to be the features for your model? 
  - "APPLICATION_TYPE"—Alphabet Soup application type
  - "AFFILIATION"—Affiliated sector of industry
  - "CLASSIFICATION"—Government organization classification
  - "USE_CASE"—Use case for funding
  - "ORGANIZATION"—Organization type
  - "STATUS"—Active status
  - "INCOME_AMT"—Income classification
  - "ASK_AMT"—Funding amount requested
  - "SPECIAL_CONSIDERATIONS"—Special consideration for application
#### What variable(s) are neither targets nor features, and should be removed from the input data?
  - "EIN" and "NAME"—Identification columns. These were dropped as they provide no value to the model. 
  - Attempts at reaching over 75% accuracy included dropping columns: "USE_CASE", "SPECIAL_CONSIDERATIONS" and "ORGANIZATION."
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
##### Initial Attempt:
   - Two hidden layers: 80 neurons in layer 1 and 30 neurons in layer 2. 
   - Relu and sigmoid activation features. Sigmoid is best for binary classifcation problems. Relu is used for for nonlinear datasets.
   - Accuracy: 0.723498523235321
   - <img width="624" alt="Screen Shot 2022-10-21 at 4 47 53 PM" src="https://user-images.githubusercontent.com/106630710/197305891-ca238a59-3893-4ab5-8648-c482fb4d6f9d.png">

#### Were you able to achieve the target model performance?
The closest attempt was the initial attempt which resulted in an accuracy of 0.723498523235321. This was achieved without dropping extra columns, two hidden layers with 80 and 30 neurons respectively, activated with relu and sigmoid functions, at 100 epochs. 

#### What steps did you take to try and increase model performance?
##### Attempt 1:
   - Two hidden layers: 80 neurons in layer 1 and 30 neurons in layer 2. 
   - Relu and sigmoid activation features. Sigmoid is best for binary classifcation problems. Relu is used for for nonlinear datasets.
   - Dropped columns: "USE_CASE", "SPECIAL_CONSIDERATIONS" and "ORGANIZATION."
   - Accuracy: 0.7202332615852356
   - <img width="649" alt="Screen Shot 2022-10-21 at 4 30 31 PM" src="https://user-images.githubusercontent.com/106630710/197304898-1288e2a7-a3ea-4983-bf12-20bce043203d.png">
##### Attempt 2:
   - Three hidden layers: 80 neurons in layer 1, 30 neurons in layer 2 and 10 neurons in layer 3.
   - Relu and sigmoid activation features. Sigmoid is best for binary classifcation problems. Relu is used for for nonlinear datasets.
   - Dropped columns: "USE_CASE", "SPECIAL_CONSIDERATIONS" and "ORGANIZATION."
   - Increased the number of epochs from 100 to 200.
   - Accuracy: 0.719883382320404
   - <img width="616" alt="Screen Shot 2022-10-21 at 4 37 08 PM" src="https://user-images.githubusercontent.com/106630710/197305289-df802ce9-cd97-45a4-9b8b-14251cffb06a.png">
##### Attempt 3:
   - Two hidden layers: 80 neurons in layer 1 and 30 neurons in layer 2. 
   - Relu and sigmoid activation features. Sigmoid is best for binary classifcation problems. Relu is used for for nonlinear datasets.
   - Dropped columns: "USE_CASE", "SPECIAL_CONSIDERATIONS" and "ORGANIZATION."
   - Accuracy: 0.7195335030555725
   - <img width="618" alt="Screen Shot 2022-10-21 at 4 39 09 PM" src="https://user-images.githubusercontent.com/106630710/197305408-f7b36e37-dceb-4372-8d4f-8bf0d215c712.png">
##### Attempt 4:
   - Two hidden layers: 100 neurons in layer 1 and 50 neurons in layer 2. 
   - Tanh, relu and sigmoid activation features. Sigmoid is best for binary classifcation problems. Relu is used for for nonlinear datasets. Tanh is similar to sigmoid but can include a negative range.
   - Dropped columns: "USE_CASE", "SPECIAL_CONSIDERATIONS" and "ORGANIZATION."
   - Accuracy: 0.7206997275352478
   - <img width="618" alt="Screen Shot 2022-10-21 at 4 39 09 PM" src="https://user-images.githubusercontent.com/106630710/197305659-9f4acff3-34cd-4e6f-ab13-805b969c11b8.png">

## Summary: 

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
