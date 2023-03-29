# deep-learning-challenge

# Purpose

The purpose of this analysis is to use a neural network model to predict whether a charity will be successful based on various features. 
This analysis can help predict whether applicants will be successful if funded by Alphabet Soup.  
The target is to get the accuracy of this analytical tool to more than 75% and the funded applicants success rate by using most of the remaining features after preprocessing.

# Data Preprocessing

The csv file was read into the notebook as Pandas dataframe.
The "NAME" and "EIN" identification columns were dropped from the table.
The feature variables were defined as the rest of the columns: application_type, affiliation, classification, use_case, organization, status, ask_amt, income_amt, and special_considerations
The columns containing categorical data were converted to numeric data types using the get_dummies function for one-hot encoding.
The dataset was  split into testing/training datasets and scaled by creating a StandardScaler instance, fitting it to the features dataset, and scaling both training and testing datasets. 

# Compiling, Training, and Evaluating the Model

Neural network was used to compile, train and evaluating this model in both optimizations.

In the optimization 1 I have removed 2 columns and used 2 nodes & 2 layers. 

![image](https://user-images.githubusercontent.com/115423610/228502987-82769d10-99e0-4392-9186-53946d38763c.png)

![image](https://user-images.githubusercontent.com/115423610/228503086-828440c3-03c4-49f6-843f-3db4f7645563.png)


This model has not achieved a target predictive accuracy higher than 75%. Achieved accurancy was 72 % . Second Optimization had to be carry on.

![image](https://user-images.githubusercontent.com/115423610/228503780-8cf3854f-9057-4c01-9a18-fdaef6a530d4.png)


For the next optimization, I had to add more layers with different node levels to achieve an accuracy of +77%. To achieve this I had to increase the no. of layers and the epoch up to 150.

![image](https://user-images.githubusercontent.com/115423610/228504375-6b18ad7e-b81b-4227-a672-598200b73739.png)

![image](https://user-images.githubusercontent.com/115423610/228504485-ee97afc4-f0bf-43d0-8c37-a9cdc39c023d.png)

This model built, tested and trained has achieved a target predictive accuracy higher than 75%. The Accuracy is 77.7%. 

![image](https://user-images.githubusercontent.com/115423610/228504610-6c5285d9-fc88-463e-a868-d86c1634b0d1.png)

# Summary & Recommendations
Overall, the optimized model met the 75% accuracy.

By trying different models and layers along with removal of unnecessary columns is helping. Training and testing on different epoch level result in reducing the bias and will help the model perform with better accuracy. 

We could also continue to adjust some of the binning thresholds for the "name", "classification", and ""application_type" value counts to further optimize the current model.



