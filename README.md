# Deep-learning-challenge
## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With our knowledge of machine learning and neural networks, we used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

We received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

```EIN and NAME```—Identification columns

```APPLICATION_TYPE```—Alphabet Soup application type

```AFFILIATION```—Affiliated sector of industry

```CLASSIFICATION```—Government organization classification

```USE_CASE```—Use case for funding

```ORGANIZATION```—Organization type

```STATUS```—Active status

```INCOME_AMT```—Income classification

```SPECIAL_CONSIDERATIONS```—Special considerations for application

```ASK_AMT```—Funding amount requested

```IS_SUCCESSFUL```—Was the money used effectively

We used  Google Colab for this assignment.

 

## Step 1: Preprocess the Data
Read in the ```charity_data.csv``` to a Pandas DataFrame
Dropped the ```EIN``` and ```NAME``` columns.
Determined the number of unique values for each column.
For columns that have more than 10 unique values, determined the number of data points for each unique value.
Used the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, ```Other```, and then checked if the binning was successful.
Used ```pd.get_dummies() ```to encode categorical variables.
Then split the preprocessed data into a features array, ```X```, and a target array, ```y```. Used these arrays and the ```train_test_split``` function to split the data into training and testing datasets.
Scaled the training and testing features datasets by creating a ```StandardScaler``` instance, fitting it to the training data, then using the ```transform``` function.
## Step 2: Compile, Train, and Evaluate the Model
Using knowledge of TensorFlow, we designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset. Once we completed this step, we compiled, trained, and evaluated the binary classification model to calculate the model’s loss and accuracy.

Continuing with the file in Google Colab in which we performed the preprocessing steps from Step 1.
1. Created a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
2. Created the first hidden layer and chose ```relu``` activation function.
3. We added a second hidden layer with ```sigmoid``` activation function.
4. Create an output layer with ```sigmoid``` activation function.
5. Checked the structure of the model.
6. Compiled and trained the model.
7. Evaluated the model using the test data to determine the loss and accuracy.
8. Saved and exported the results to an HDF5 file. Named the file AlphabetSoupCharity.h5.

## Step 3: Optimize the Model
Using knowledge of TensorFlow, optimized your model to achieve a target predictive accuracy higher than 75%.

Used the following methods to optimize your model:

Dropping more or fewer columns.
Added more neurons to a hidden layer.
Added more hidden layers.
Used different activation functions for the hidden layers.
Used different loss functions
Added or reduced the number of epochs to the training regimen.
### Optimization:

Created a new Google Colab file and named it AlphabetSoupCharity_Opt.ipynb.
* Imported dependencies and read in the charity_data.csv to a Pandas DataFrame.
* Preprocessed the dataset as we did in Step 1.
* Designed a neural network model, and adjusted for modifications that optimized the model to achieve higher than 75% accuracy.
* Saved and exported your results to an HDF5 file. Name the file AlphabetSoupCharity_Optimization.h5.
## Step 4: Write a Report on the Neural Network Model
We wrote a report on the performance of the deep learning model we created for Alphabet Soup.

The report contained the following:

Overview of the analysis: Explained the purpose of this analysis.
Results: Addressed the following questions:
Data Preprocessing
What variable(s) are the target(s) for your model?
What variable(s) are the features for your model?
What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?
Summary: Summarized the overall results of the deep learning model. Included  recommendation for how a different model could solve this classification problem, and then explained the recommendation.