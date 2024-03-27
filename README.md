# Deep Learning Challenge: Charity Funding Predictor

## Overview 

The purpose of this analysis is to assist the nonprofit foundation Alphabet Soup in identifying the most effective tool for selecting applicants who have the best chance of succeeding in their ventures. In this analysis, we apply our knowledge of machine learning and neural networks to develop a tool that predicts whether the applicants will be successful if funded by the foundation.


## Results:

* First and foremost, data preprocessing is essential to eliminate any irrelevant information. For this reason, the columns 'EIN' and 'NAME' are removed from the DataFrame, as they do not provide substantial information that contributes to our analysis. The column 'IS_SUCCESSFUL' is selected as the target variable for the model. This selection is made with the objective of predicting whether applicants will be successful upon receiving funding from the foundation, where a value of 1 indicates success and 0 indicates failure. Consequently, the rest of the columns are designated as feature columns, which will be used to inform the predictions made by our model.

* 'Application_Type' and 'Classification' columns were used as a cutoff to bin variables together. Categorical variables were encoded by get_dummies() after checking to see if the binning was successful. Finally, we splited the data to training and testing sets.

#### Compile, Train and Evaluate the Model

* The first attemp, I chose the model with two hidden layers. The hidden nodes layer 1 is 80 and the hidden nodes layer 2 is 30. Model then got compile and got train. However, the accuracy is only 72%.

/Users/loanho/Desktop/Screenshot 2024-03-27 at 3.28.58 PM.png

/Users/loanho/Desktop/Screenshot 2024-03-27 at 3.36.43 PM.png

* Second attempt was perform with AutoOptimization model to try to get the better performance by using tensorflow and keras library. However, this model is doing just a little bit better with 73% accuracy.

/Users/loanho/Desktop/Screenshot 2024-03-27 at 3.40.09 PM.png

/Users/loanho/Desktop/Screenshot 2024-03-27 at 3.40.44 PM.png

* The third attemp was performed with similar to attemp 1. However, I changed the hidden layer from two to three, change the hidden node layer number. However, the accuracy was still at 72%

/Users/loanho/Desktop/Screenshot 2024-03-27 at 3.58.32 PM.png
/var/folders/ql/zknntgcj1bg90qlc5j5yzk0c0000gn/T/TemporaryItems/NSIRD_screencaptureui_RfMCgh/Screenshot 2024-03-27 at 3.59.05 PM.png

## Summary:

Although the non automized model and the Auto Optimization model could not achive the target. The best accuracy that my model can predict is 73%. In the future, I would try to use auto optimization model with adjust some conditions such as dropping or adding some columns, adjust the number of bin, or adjust the epochs number to get the better model.
