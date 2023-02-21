# deep-learning-challenge

# Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can 
predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup 
over the years. Within this dataset are a number of columns that capture metadata about each organization.

# Step 1: Preprocess Data
  
  1. Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
      
      - What variable(s) are the target(s) for your model?
      - What variable(s) are the feature(s) for your model?
      
  2. Drop the EIN and NAME columns.
  3. Determine the number of unique values for each column.
  4. For columns that have more than 10 unique values, determine the number of data points for each unique value.
  5. Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, 
  and then check if the binning was successful.
  6. Use pd.get_dummies() to encode categorical variables.
  7. Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data 
  into training and testing datasets.
  8. Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform
  function.
  
  # Step 2: Compile, Train, and Evaluate Model
  
  Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict 
  if an Alphabet Soup-funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there 
  are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your 
  binary classification model to calculate the model’s loss and accuracy.
  
  1. Continue using the Jupyter Notebook in which you performed the preprocessing steps from Step 1.
  2. Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
  3. Create the first hidden layer and choose an appropriate activation function.
  4. If necessary, add a second hidden layer with an appropriate activation function.
  5. Create an output layer with an appropriate activation function.
  6. Check the structure of the model.
  7. Compile and train the model.
  8. Create a callback that saves the model's weights every five epochs.
  9. Evaluate the model using the test data to determine the loss and accuracy.
  10. Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity.h5.
 
 # Step 3: Optimize the Model
 
 Using your knowledge of TensorFlow, optimize your model to achieve a target predictive accuracy higher than 75%.
 
 Use any or all of the following methods to optimize your model:
 
 1. Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:
 
  - Dropping more or fewer columns.
  - Creating more bins for rare occurrences in columns.
  - Increasing or decreasing the number of values for each bin.

 2. Add more neurons to a hidden layer.
 3. Add more hidden layers.
 4. Use different activation functions for the hidden layers.
 5. Add or reduce the number of epochs to the training regimen.

# Step 4: Report

1. Overview of the analysis: Explain the purpose of this analysis.
2. Results: Using bulleted lists and images to support your answers, address the following questions:

  - Data Preprocessing
    
    - What variable(s) are the target(s) for your model?
    - What variable(s) are the features for your model?
    - What variable(s) should be removed from the input data because they are neither targets nor features?

  - Compiling, Training, and Evaluating the Model
    
    - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Were you able to achieve the target model performance?
    - What steps did you take in your attempts to increase model performance?


3. Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this 
classification problem, and then explain your recommendation.
