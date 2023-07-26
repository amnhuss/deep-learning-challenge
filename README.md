# deep-learning-challenge
 
# deep-learning-challenge
 
Purpose:
The goal of this project was to develop a neural network machine learning tool that will help a non-profit foundation select the applicants to give funding to that have the best chance of success in their ventures.

Data Preprocessing:
1. What variable(s) are the target(s) for your model?
The target variable for the model is 'IS_SUCCESSFUL', which indicates whether or not the charity application was successful.

2. What variable(s) are the features for your model?
The feature variables for the model include 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.

3. What variable(s) should be removed from the input data because they are neither targets nor features?
Variables 'EIN' and 'NAME' were removed from the input data as they are neither targets nor features. They are simply identifiers and do not provide meaningful information for the model.


Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
Optimization 1: This model retained the original structure of two layers but changed the activation functions. The activation function of the first hidden layer was switched to 'tanh', and the second hidden layer used 'LeakyReLU'. 'tanh' was used because it can sometimes perform better in practice compared to 'ReLU' by mapping negative inputs to negative outputs. 'LeakyReLU' was selected to avoid dead neurons, which can occur with 'ReLU' if negative inputs result in a 0 output.

Optimization 2: This model had a more complex architecture with four hidden layers containing 100, 50, 25, and 10 neurons respectively. The additional layers were added in an attempt to capture more complex patterns in the data. The 'ReLU' activation function was used for all the hidden layers due to its efficient computation and its ability to handle the vanishing gradient problem.

Optimization 3: This model had two layers with 80 and 30 neurons respectively, just like the original model. However, it introduced dropout layers for regularization to prevent overfitting. The dropout layers randomly set a fraction of input units to 0 at each update during training time, which helps prevent overfitting. The 'ReLU' activation function was used for the hidden layers.

Optimization 4: The structure of this model was identical to the original model, with two layers containing 80 and 30 neurons. However, the model employed 'SGD' as the optimizer with a learning rate of 0.01, unlike the original model which used 'adam'. Stochastic Gradient Descent (SGD) was used to see if the slower, more robust nature of this optimizer could lead to better performance.


5. Were you able to achieve the target model performance?
No, the model did not achieve the target model performance.

6. What steps did you take in your attempts to increase model performance?
More layers and neurons were added, dropout layers were added to prevent overfitting, and optimier was changed to SGD.


Summary:
The target model performance was not reached despite optimization attempts. Using these attempts, Alphabet Soup cannot make funding decisions for its applicants. 
