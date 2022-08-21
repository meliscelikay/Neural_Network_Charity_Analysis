# Neural_Network_Charity_Analysis

# Project Overview


# Resources

* Dataset from LendingClub: [charity_data.csv]()
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
    
    `EIN` and NAME are non-beneficial ID columns and were dropped from the input data since they do not influence the outcome.


##  Compiling, Training, and Evaluating the Model

    - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    
    The input data has 43 features and 25,724 samples. The first attempt at a model design included 80 neurons for the first hidden layer. 30 layers was chosen for the second hidden layer. A unique neuron '1' used for the output layer. The activation function 'ReLu' used for the hidden layers & 'Sigmoid' used for the output layer as the unique neuron is a binary classification. For the compilation, the optimizer is 'adam' and the loss function is 'binary_crossentropy'. 
    
    - Were you able to achieve the target model performance?
    
    The model accuracy: ~73% which is under the target model performance and could not help to predict the outcome of the charity donations.
    
    - What steps did you take to try and increase model performance?
    
    Applied bucketing to the feature `ASK_AMT` and organized the different values by intervals. The number of neurons on one of the hidden layers increased, a model with three hidden layers used. Also, a different activation function (tanh)tried in order to increase model performance but the model accuracy remain as ~73% and the model's performance not improved.
    

#  Summary