# deep-learning-challenge analysis


Overview:

The goal was to create a tool to help an organization select  applicants for funding with the best chance of success in their ventures. Features in a 
provided dataset were used to create a binary classifier to can predict whether applicants will be successful if funded by Alphabet Soup. The data contains 
more than 34,000 organizations that have received funding from Alphabet Soup over the years, with metadata about each organization.


Pre-processing:

Our target variable was "IS_SUCCESSFUL", a binary measure of whether the funded business was successful. The 9 features included:

APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested

Two columns in the dataset (EIN and NAME) were excluded, as they are merely identifiers. Low-frequency category values for APPLICATION_TYPE and 
CLASSIFICATION columns were converted into an "other" category.


Model Compilation & Training:

To begin with, 2 hidden layers were used with 9 neurons each (the number of features) because the dataset is fairly simple. The rectified linear 
unit activation function (ReLU) was used first because it is most common. Three further attempts at optimizing the model were attempted, though 
none achieved the goal accuracy of 75%. The second attempt used 12 neurons in each hidden layer and increased the epochs from 200 to 300. The third
attempt kept these changes, but changed the activation function to SELU (scaled exponential linear unit). The final attempt reverted to 200
epochs, but added a 3rd hidden layer with 16 neurons.


Summary:

The model was unable to achieve an accuracy of 75% - all 4 attempts with varying parameters resulted in accuracy scores from 72-73%. Hypertuning 
was mostly ineffective at improving accuracy, though more optimization, possibly with more hidden layers and neurons, could be done. Another potential
option to explore would be using a random forest classifier. This model may reduce overfitting to improve accuracy.
