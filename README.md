# Neural Network Charity Analysis
Mod 20 Neural Network Challenge

## Overview
The purpose of this analysis is to use a neural network to predict whether applicants will be successful if funds are recieved from Alphabet Soup. This analysis uses python's TensorFlow library to create, train, and evaluate data gathered from previous loans.


## Results
### Data Preprocessing
#### Data Columns consist of: 
###### - EIN and NAME—Identification columns
###### - APPLICATION_TYPE—Alphabet Soup application type
###### - AFFILIATION—Affiliated sector of industry
###### - CLASSIFICATION—Government organization classification
###### - USE_CASE—Use case for funding
###### - ORGANIZATION—Organization type
###### - STATUS—Active status
###### - INCOME_AMT—Income classification
###### - SPECIAL_CONSIDERATIONS—Special consideration for application
###### - ASK_AMT—Funding amount requested
###### - IS_SUCCESSFUL—Was the money used effectively


1. What variable(s) are considered the target(s) for your model?
    - The target variable is the "IS_SUCCESSFUL" column since we are trying to determine which investments will be successful. 
  
2.  What variable(s) are considered to be the features for your model?
    - The remaining columns became the features for the model.

3.  What variable(s) are neither targets nor features, and should be removed from the input data?
  - EIN, NAME were removed since did not offer any relevant data that could help the model perform better.

### Compiling, Training, and Evaluating the Model

#### Optimization Attempt 1
![image](https://user-images.githubusercontent.com/114044192/221378072-02ed9b22-dc91-4de6-9b9b-3e08d9fda15e.png)

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - 2 hidden layers with 80 & 30  with ReLu for  input and Sigmoid for output
  - Used Relu and Sigmoid Activations Functions since sigmoid is best for binary classifcation problems as this and relu is for nonlinear datasets.

2. Were you able to achieve the target model performance?
  - No - Accuracy was 63.04
![image](https://user-images.githubusercontent.com/114044192/221379575-cbf24009-2e85-44bb-9add-fef212baea4d.png)

3. What steps did you take to try and increase model performance?
  - Removed additional columns to reduce "noise":STATUS, SPECIAL_CONSIDERATIONS
  - Increased neurons to 80 and 30

#### Optimization Attempt 2
![image](https://user-images.githubusercontent.com/114044192/221378512-3b6ac325-8572-4fe5-baff-7c16db32376f.png)

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - 3 hidden layers with 80 & 30 & 15  with ReLu for  input and Sigmoid for output
  - Used Relu and Sigmoid Activations Functions since sigmoid is best for binary classifcation problems as this and relu is for nonlinear datasets.
2. Were you able to achieve the target model performance?
 - No - Accuracy was 57.87
![image](https://user-images.githubusercontent.com/114044192/221379517-9af7b75d-1118-4e1e-8950-1c64917e5b19.png)

3. What steps did you take to try and increase model performance?
  - Removed additional columns to reduce "noise":STATUS, SPECIAL_CONSIDERATIONS
  - Increased hidden layers to 3
  - Kept first 2 layers the same: neurons to 80 and 30; added 15 neurons for third layer. 
  
#### Optimization Attempt 3
![image](https://user-images.githubusercontent.com/114044192/221379287-15c7c9bc-ee1e-4028-b639-46c8905f64c0.png)

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - 2 hidden layers with 120 & 50  with ReLu for  input and Sigmoid for output
  - Used Relu and Sigmoid Activations Functions since sigmoid is best for binary classifcation problems as this and relu is for nonlinear datasets.

2. Were you able to achieve the target model performance?
  - No - Accuracy was 54.44
 ![image](https://user-images.githubusercontent.com/114044192/221379353-4657126a-7804-4899-87a5-0332fa17f840.png)

3. What steps did you take to try and increase model performance?
  - Returned to original data set without STATUS & SPECIAL_CONSIDERATIONS removed. 
  - Added 3rd hidden layer. 
  - Reduced neurons to 35 and 15 and set 3rd layer at 5
  - Reduced Epochs to 50
  
## Summary
I was unable to achieve 75% accuracy with the changes I made. I believe this is due to not finding the optimum layers and neurons. My accuracy actually decreased with each change I made after my first attempt. I believe that studying the data set a bit more to determine more accurately what data can be removed, and possibly changing the activation functions could increase accuracy. 
