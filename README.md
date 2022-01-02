# Neural_Network_Charity_Analysis
## Analysis Overview

The purpose of this analysis is to develop a machine learning and neural network model with the Python TensorFlow library to predict the amount of funding fulfilled to the Alphabet Soup charitable organization will receive.  The dataset includes several thousand organization records for which the neural network machine learning model iterates through to determine the most successful outcomes of funding by Alphabet Soup. After preporocessing, Compiling, Training and Evaluating the neural network model, Matplotlib library is used to optimize the original model. 

## Results
### Data Preprocessing

- IS_SUCCESSFUL column is considered in the model as the target variable. 
- The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL CONSIDERATIONS and ASK_AMT columns are considered to be the model features.
- Variable that were neither targets or features for the dataset include EIN, NAME because they will no impact on the outcome, and therefore are dropped. 

![Preprocessing](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/85b06cf80ea991bf7b466d8bb755368440cc1626/AnalysisImages/Screenshot%202022-01-02%20at%203.58.02%20PM.png)
![Preprocessing](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/85b06cf80ea991bf7b466d8bb755368440cc1626/AnalysisImages/Screenshot%202022-01-02%20at%203.57.47%20PM.png)

### Compiling, Training, and Evaluating the Model

- The original model has 2 hidden layers. The first and second hidden layer have the activation="relu" function and the activation="sigmoid" function for the output layer,  The first with 80 neurons and the second has 30 along with the output layer. 
- The accuracy for my model was only 69%, and did not reach the 75% target. 
- The steps to try and increase model performance required removing noisy features, additional neurons and hidden layers. After changing the activation functions, the accuracy of my optimized model for predicting donation success resulted in 0.55125 with a loss metric of 1.94214.

![CTE](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/85b06cf80ea991bf7b466d8bb755368440cc1626/AnalysisImages/Screenshot%202022-01-02%20at%204.08.14%20PM.png)
![CTE](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/85b06cf80ea991bf7b466d8bb755368440cc1626/AnalysisImages/Screenshot%202022-01-02%20at%204.08.57%20PM.png)

## Summary 

The original model had an accuracy score of 69% because the model overfitted. In order to optimize the original model by removing more features or adding more neurons and hidden layers to increase accuracy. The random forest model could solve the classification problem by randomly sampling the preprocessed data and building several smaller, simpler decision trees.  The random forest is a more robust model as they are trained on different pieces of the data. It can be used to rank the importance of input variables and it can run efficiently on large datasets. Due to their sufficient number of estimators and tree depth, also they have faster performance than neural networks and could have avoided the data from being overfitted. 

![Output](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/0df781538750ef7c8e2e230eaeb72c508c24a8bc/Model_Accuracy_Output.png)
![Output](https://github.com/MoKmo176/Neural_Network_Charity_Analysis/blob/0df781538750ef7c8e2e230eaeb72c508c24a8bc/Metric_Loss_Output.png)