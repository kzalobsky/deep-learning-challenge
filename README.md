# deep-learning-challenge
 
# Report on the Neural Network Model
### Deep Learning Charity Funding Outcome Prediction Project using our fine-tuned Nueral Networks

## Overview:
We were tasked to create a tool for Alphabet Soup to help select applicants for funding that have the best chance in success in their endeavors.  We used machine learning and neural networks with the provided dataset to creat a classifier that predicts whether or not an applicant would find success after being funded by Alphabet Soup.  We were given a 75% accuracy target for our model from the team at Alphabet Soup, as well as a dataset of more than 30,000 organizations that have been funded by Alphabet Soup in the past.  Within the dataset, there are columns that collect the metadata for each organization: * **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively

#Analysis Process:
### 1: Data Preprocesing:
*The dataset needed to be checked for null and duplicated values which were then removed
*The EIN and NAME columns were removed because they do not contain information relative to our analysis
*Creation of cutoff points to combine rare data (think outliers) into a new value for both the CLASSIFICATION and APPLICATION_TYPE columns
*The data was converted from categorical data into numeric data with 'pd.get_dummies', then we split the preprocessed data into features and target arrays, and then got our training and testing datasets

###2: Compiling, Training, and Evaluating the Model
The first model wast created with the following parameters, keeping low computation time in mind:
*2 hidden layers with an 80, 30 neuron splite (the input feature was 43, 80 was chosen as the first layer because it is almost double the input_feature).  With a hidden layer activation function for our first model.
*Output node is 1 as it was a binary classification model with only one output - was the funding successful or not?  A Sigmoid layer was applied to the output model as well
*I added another hidden layer at 30 since the model accuracy was below 75%, but the first model was still not at 75% accuracy despite the additional layer.

*The second model used a tanh activation and three hidden layers, and although the accuracy improved it was still not at the 75% required.

###3: Optimization:
The Keras Sequentail model that uses the keras-turner library was used to optimize the model
*The best models from the keras-turn method achieved a 73% prediction accuracy using the sigmoid activation function

###4 Summary:
Through the optimization processes, we can see that the number of epochs and the kind of activations used dramatically impact the accuracy of the prediction models.  
