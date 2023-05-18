# Optimizing a Deep Learning Algorithm
The purpose of this analysis is to create a model that will help the nonprofit foundation AlphabetSoup choose applicants for funding with the best chance of success in their ventures. I have created a binary classifier to help AlphabetSoup predict whether applicants will be successful if funded by this company.
<img width="1310" alt="Screenshot 2023-05-17 at 6 05 01 PM" src="https://github.com/katherinewinder1/deep-learning-challenge/assets/112666732/4e822877-a354-4643-90d7-8e6345276fb7">

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

The target variable is the "IS_SUCCESSFUL" column.
The features are "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS" "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and  "ASK_AMT". 
There were two columns that had irrelevant data that were neither the targets nor the features which were "EIN" and "NAME". I removed these columns from the input data and discovered that with either of these columns included in the dataset, the session crashed due to exceeding Google Colab's RAM usage limit.
<img width="1244" alt="Screenshot 2023-05-17 at 6 05 38 PM" src="https://github.com/katherinewinder1/deep-learning-challenge/assets/112666732/005cd289-4296-4ba0-949a-7b3e60611594">

Compiling, Training, and Evaluating the Model

Originally, I selected 3 layers for the model with 7, 14, and 1 neuron in each layer. These were arbitrary and were used as a starting point for the model. The target accuracy of at least 75% was not achieved by this model with 100 epochs.
I tried adding another hidden layer, adding more neurons to each layer, adding more columns from the original data, using fewer and more epochs, and changing the binning and cutoff values to optimize the model and increase it's performance, but in the allotted time given my model was not able to reach the targetted 75% accuracy. 

Summary

The most accurate model I observed had only 3 hidden layers with 7, 14, and 1 neurons in each layer. This model had a cutoff value of 500 for application types and a cutoff of 100 for classification and ran over 100 epochs. This model achieved 73% accuracy. I tried adding more layers and neurons, changing the epochs, and adding lower cutoffs for binning however the accuracy only decreased. I also tried running the model with all of the original columns to the dataset but the session crashed. A model with fewer features, similar layers and neurons, and higher cutoffs would most likely solve the classification problem that I faced. 
<img width="621" alt="Screenshot 2023-05-17 at 5 57 26 PM" src="https://github.com/katherinewinder1/deep-learning-challenge/assets/112666732/b96cbfc2-8fd8-4dde-9ba2-acb860f08377">
