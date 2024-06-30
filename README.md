# Module 19 Challenge: Neural Network Challenge 2

## Problem Statement
The task was to create a branched neural network that predicts whether employees are likely to leave a company and might be better assigned to a different department within the company.

## Solution
The solution proceeds through the following steps.
1. Read the data from a `csv` file into a Pandas DataFrame. (This step was provided.)
2. Preprocess the data into appropriate X and y datasets by
   * Determining the number of unique values in each column, ensuring that there are no `null` values in the data, and determining the datatype of each column.
   * Defining the X dataset by droping the target columns 'Attrition' and 'Department.
   * Using `OneHotEncoder` to encode all non-numeric columns of the X dataset.
   * Using `OneHotEncoder` to encode the 'Attrition' and 'Department' target columns.
   * Define two different y datasets for 'Attrition' and 'Department', respectively.
   * Split the X dataset and each y dataset into train and test datasets.
3. As instructed, create, build, and train a branched neural network with the following layers
   * Input layer,
   * Two shared hidden layers,
   * One hidden layer abd one output layer each for the 'Attrition' and the 'Department' branches.

**Notes:**
1. Since none of the classes of the non-numeric columns exhibit a clear order, we use `OneHotEncoder` to encode all columns.
2. We use a utility encoding function to avoid having to copy code. That makes the code easier to understand and more maintainable.

## Results
We find that the model predicts the Department with an accuracy of 97% for the test data. It overfits the 'Attrition' with an accuracy of 1.0 on the train data versus an accuracy of 0.82 for the test data.