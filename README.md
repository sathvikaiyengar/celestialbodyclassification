# Celestial Body Classification

## Overview
This repository encompasses my case study in Celestial Body Classification, as the final project submission for CSCI S-89: Introduction to Deep Learning at Harvard Summer School. I chose this area of study because I am fascinated by the intersection of astronomy and computer science. With my background in Computer Science and Physics, I am particularly interested in developing automated methods for classifying celestial bodies, which play a crucial role in advancing scientific discovery.

The primary objective of this study revolves around addressing two pivotal questions:
  1. What specific criteria determine the classification of a celestial body as a galaxy, star, or quasar?
  2. Can these criteria be utilized to accurately predict and classify celestial bodies that have yet to be definitively categorized?

   
The study begins by collecting data from the Sloan Digital Sky Survey (SDSS), one of largest public astronomical datasets. Through SQL queries submitted to the SDSS database server, a dataset of 250,000 celestial object observations was used for training, validating, and testing the neural network built. Each observation had 17 feature columns and 1 class column indicating the type of celestial body (star, galaxy or quasar).

Next, the dataset was prepared for processing by dropping irrelevant columns, such as identifiers. In addition, one-hot encoding was applied to the class column, where dummy variables are created for each categorical value. The dataset was scaled and split into training (60% of the dataset), validation (20%), testing (20%) sets, to assess the model's performance on unseen data.

Then, a feedforward neural network model was constructed with two hidden layers, along with batch normalization and dropout layers to prevent overfitting. The dropout rates for the layers were determined through finding the optimal validation accuracy from sample dropout rate values. With the model trained with the training set, the accuracy of the model was evaluated on the unseen testing set. This resulted in a test loss of 4.26% and test accuracy of 98.85%, indicating the high accuracy performance of the model.

The model was then used to predict the class labels for the unseen validation dataset, for which a Confusion Matrix displayed significant results for the class types predicted correctly. In addition, using Principal Component Analysis (PCA) shed light on the reasoning behind the model’s high prediction accuracy. The first two principal components (PCs) explained 98.15% of the variance in the data, which were the most informative features for the neural network to learn the patterns of classification in the data. It was seen that original plate and run features contributed the most to each principal component, respectively.

Overall, the deep learning-based classification system proved to be effective in identifying celestial bodies with high accuracy. With an automized classification process, this approach can significantly aid in the handling and processing of observational data.

### Repository Details
This repository contains the source code for the classification in a Jupyter Notebook file, along with the final report detailing the process and analysis of the results.
