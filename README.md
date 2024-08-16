# sms_spam_detector
## Overview
This project involves building an SMS spam detector using a Support Vector Classification (SVC) model and hosting it as a web application using Gradio. The goal is to classify SMS text messages as either "spam" or "ham" (not spam). The project is divided into three parts: creating the SMS classification function, implementing the prediction logic, and developing a Gradio interface for users to test the model.

## Repository Structure
sms_spam_detector/
│
├── data/
│   ├── SMSSpamCollection.csv
│
├── notebooks/
│   ├── gradio_sms_text_classification.ipynb
│   ├── sms_text_classification_solution.ipynb
│
├── README.md
│
└── app/
    ├── app.py

## Instructions
### Part 1: Create the SMS Classification Function
Objective: Build a function that constructs, trains, and returns a linear Support Vector Classification (SVC) model for classifying SMS text messages.

Load Data:

Load the SMSSpamCollection.csv file into a Pandas DataFrame.
Set the features variable to the text message column of the DataFrame.
Set the target variable to the label column, which contains either "spam" or "ham" labels.
Split Data:

Split the data into training and testing sets using train_test_split. Set the test_size to 33%.
Build a Pipeline:

Construct a machine learning pipeline that:
Vectorizes the text data using TfidfVectorizer.
Applies a linear SVC model to classify the messages.
Train the Model:

Fit the model to the transformed training data.
Return the Model:

Return the trained model for further use in prediction.
Output: The sms_classification function that returns a trained model.

### Part 2: Create the SMS Prediction Function
Objective: Implement the logic to predict whether a new SMS text message is spam or not, using the trained model.

Make Predictions:

Create the sms_prediction function that takes a trained model and new text as input.
Determine Message Type:

Use a conditional statement to check if the prediction is "ham" or "spam".
Return the Result:

If the message is "ham", return:
f'The text message: "{text}", is not spam.'
If the message is "spam", return:
f'The text message: "{text}", is spam.'
Output: The sms_prediction function that returns a classification message.

### Part 3: Create the Gradio Interface Application
Objective: Develop a Gradio web interface that allows users to input SMS messages and see whether they are classified as spam or not.

Create Gradio Interface:

Create a Gradio interface with a textbox for input (SMS text) and a textbox for output (prediction result).
Configure Labels:

Ensure that the input textbox is labeled with "Enter SMS Text" and the output textbox is labeled with "Prediction Result".
Launch the Application:

Launch the Gradio app and provide the shareable URL for users to access the application.
Test the Application:

Test the application using the following sample text messages:
"You are a lucky winner of $5000!"
"You won 2 free tickets to the Super Bowl."
"You won 2 free tickets to the Super Bowl. Text us to claim your prize."
"Thanks for registering. Text 4343 to receive free updates on medicare."
Output: A Gradio app that allows users to classify SMS messages as spam or not spam.

## Conclusion
This project demonstrates how to build a machine learning model to classify SMS text messages as spam or not spam using a Support Vector Classification (SVC) model. The model is deployed as a web application using Gradio, allowing users to easily test the model by entering new text messages. This project provides a practical example of integrating machine learning with interactive web applications, enabling real-time predictions for end-users.
