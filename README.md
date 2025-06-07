# deep-learning-challenge
Chatgpt, expert learning and student collaboration
AlphabetSoup Charity Model Report
What I Did:
The goal of this project was to build a machine learning model that could predict if a charity would be successful in getting funding. I used a dataset that had information about each charity, like what type of organization it was, how much money they asked for, what the money would be used for, and other details.

Data Cleaning:
I started by cleaning the data. There were two columns, EIN and NAME, that I removed because they were just IDs and not helpful for making predictions.

Then I looked at the columns APPLICATION_TYPE and CLASSIFICATION, which had a lot of different values. Some of the values didn’t show up very often, so I grouped those into a single category called “Other” to make the data easier for the model to learn from.

I also turned all the text columns into numbers using pd.get_dummies() because the model can only work with numbers.

Preparing the Data:
After that, I separated the data into features (the inputs) and the target (the result we’re trying to predict, which is whether the charity was successful or not). I split the data into training and testing sets and scaled the features using StandardScaler to make sure all the values were on a similar scale.

Building the Model:
I created a neural network using TensorFlow and Keras. The network had:

Two hidden layers (one with 80 nodes and one with 30)

An output layer that used sigmoid activation because we’re predicting a 0 or 1

I used binary cross-entropy for the loss function and adam as the optimizer.

Training the Model:
I trained the model for 100 rounds (epochs). At first, the model didn’t perform that well — the accuracy started below 50%. But as training continued, the model started doing better.

Results:
After training, I tested the model. It ended up with:

Accuracy: around 70.5%

Loss: around 0.658

This means the model correctly predicted whether a charity was successful about 70% of the time, which is not great but not terrible either.

Saving the Model:
At the end, I saved the model to a file called AlphabetSoupCharity.h5. There was a warning that this file format is a little outdated, but it still works.

Final Thoughts:
The model did okay. If I wanted to make it better, I might try changing the number of layers, testing different activations, or doing more with the data cleanup. But for now, this is a good starting point.
