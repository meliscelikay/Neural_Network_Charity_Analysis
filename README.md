# Neural_Network_Charity_Analysis

# Project Overview

The main goal of this project is to provide clear data points and success rates to Alphabet Soup Company, which will be used to decide which companies will funded. I will deployed machine learning neutral networks with TensorFlow model in Phython to analyze large dataset consisting of 34,000 companies.  

# Resources

* Dataset from LendingClub: [charity_data.csv](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/charity_data.csv)
* Software: Python 3.9.7, Anaconda Navigator 1.10.0, Conda 4.13.0 and Jupyter Notebooks 6.4.12

# Results

##  Data Preprocessing

   - What variable(s) are considered the target(s) for your model?
    
   The column `IS_SUCCESSFUL` contains a value of 1 refering if the funding was used effectively. This variable considered as the target for the deep learning neural network.
    
   - What variable(s) are considered to be the features for your model?
    
   The following columns were used as feature variables:
    
   `APPLICATION_TYPE
    AFFILIATION
    CLASSIFICATION
    USE_CASE
    ORGANIZATION
    STATUS
    INCOME_AMT
    SPECIAL_CONSIDERATIONS
    ASK_AMT`
    
   - What variable(s) are neither targets nor features, and should be removed from the input data?
    
   `EIN` and `NAME` are non-beneficial ID columns and were dropped from the input data since they do not influence the outcome.
   
   ![charity_data_head.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/charity_data_head.png)
   
   ![charity_data_dropped.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/charity_data_dropped.png)


##  Compiling, Training, and Evaluating the Model

   - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    
   The input data has 43 features and 25,724 samples. The first attempt at a model design included 80 neurons for the first hidden layer. 30 layers was chosen for the second hidden layer. A unique neuron '1' used for the output layer. The activation function `ReLu` used for the hidden layers & `Sigmoid` used for the output layer as the unique neuron is a binary classification. For the compilation, the optimizer is `adam` and the loss function is `binary_crossentropy`. 
   
   ![x_train_scaled.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/x_train_scaled.png)
   
   ![define_model.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/define_model.png)
    
   - Were you able to achieve the target model performance?
    
   The model accuracy: ~73% which is under the target model performance and could not help to predict the outcome of the charity donations.
    
   ![AlphabetSoupCharity.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/AlphabetSoupCharity.png)
    
   - What steps did you take to try and increase model performance?
    
   Applied bucketing to the feature `ASK_AMT` and organized the different values by intervals. The number of neurons on one of the hidden layers increased, a model with three hidden layers used. Also, a different activation function `Tanh` tried in order to increase model performance but the model accuracy remain as ~73% and the model's performance not improved.
   
###### The number of neurons on one of the hidden layers increased   
   ![neurons_added.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/neurons_added.png)

###### A model with three hidden layers used
   ![layer_added.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/layer_added.png)

###### `Tanh` activation function used
   ![Tanh_function.png](https://github.com/meliscelikay/Neural_Network_Charity_Analysis/blob/5b0f6a9450ff547033c4c0e7675cdf2eb6da8a24/Resources/Tanh_function.png))


#  Summary

The target goal of 75% accuracy could not be reached, on average 73% was the highest result. I did not think increased quantity of neurons had a positive impact. I would recommend using more detailed data with more features subjects to create a more accurate model, instead of data accumulated across so many different companies. I believe using a supervised machine learning model with relevant classifiers may improve the accuracy rate.
