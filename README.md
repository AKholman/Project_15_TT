Data Projects (TripleTen)
# Project_15 Computer Vision
Project-15:  Building a Computer Vision Model to Verify Age for Compliance with Alcohol Sales Laws

Project Overview
This project aims to develop a computer vision model that verifies the age of individuals purchasing alcohol, ensuring compliance with age-related sales regulations. The Good Seed supermarket chain is looking to automate the process of verifying the age of customers at checkout to prevent alcohol sales to underage individuals. Using images captured at checkout, we trained a machine learning model to predict the age of individuals, helping the supermarket chain adhere to alcohol laws.

Project Goal
The primary objective of this project is to build a reliable age verification system that automatically determines whether a customer is above the legal age for alcohol consumption. The model processes photographs taken during the transaction and provides an age estimate, which is then used to verify if the customer is legally allowed to purchase alcohol.

Dataset
The dataset used in this project consists of photographs of customers along with their real ages. The data includes images of customers from different age groups, ranging from 0 to 100 years old, and it is pre-labeled with the corresponding ages. For the purpose of training the model, we focused on customers aged between 12 and 90 years old.

Key Fields in the Dataset:
Image: A photograph of the customer.
real_age: The actual age of the person in the photo (target variable).
ds_part: Indicates whether the sample is part of the training or testing set.
Methodology
Exploratory Data Analysis (EDA):

The data was analyzed to understand the distribution of ages and characteristics of the images.
A histogram of the age distribution was created, and the age column was filtered to focus on customers aged between 12 and 90 years old.
Age values were normalized, and the final data was visualized to identify any potential issues or anomalies.
Model Development:

The dataset was split into training (75%) and validation (25%) sets.
We used Keras Sequential model to build the age verification system. The model was trained using image data augmentation techniques to enhance generalization.
The training process was carried out over 20 epochs, with the model evaluated on the validation data after each epoch. Key metrics such as loss and mean absolute error (MAE) were tracked during the training process to assess the model's performance.
Model Evaluation:

The model's performance was evaluated using mean absolute error (MAE) and loss metrics.
During the training process, loss decreased steadily over the first 18 epochs, after which the model began to show signs of overfitting, as evidenced by a slight increase in loss in the final epochs.
The model performed better on the training data, with lower loss and MAE compared to the validation data.
Results and Conclusions:

The model showed promising results with a decreasing trend in loss and MAE during training.
The slight increase in loss and MAE in the later epochs indicates potential overfitting, suggesting that further tuning or regularization techniques could improve generalization.

Conclusion
By building and evaluating a computer vision model for age verification, this project provides a framework for automating age checks at checkout counters. The model has shown promising results, with further improvements possible through tuning and addressing overfitting. With this system in place, the Good Seed supermarket chain can ensure that they comply with alcohol sales laws by automatically verifying customers' ages in real-time at the point of purchase.

Future Improvements
Investigate ways to handle overfitting, such as by introducing regularization or data augmentation techniques.
Explore the use of more advanced deep learning models, such as convolutional neural networks (CNNs), to improve accuracy.
Implement a real-time inference system for integration with the checkout systems.
