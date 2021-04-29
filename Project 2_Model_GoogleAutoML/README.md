# Build a Model with Google AutoML

## Project Overview

In this project, I build the classification model using [Google AutoML Vision platform](https://cloud.google.com/automl), an automated machine learning tool that will allow us to build the model and host it in the cloud. In order to appreciate how training data impact models, I've built models with 4 variants of the dataset.

## The Data

It is used [Kaggle chest x-ray dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) for this project.

## The Four Parts of the Project

Four different models will be trained using four variants of the pneumonia dataset. Recall that the dataset contains childrens' chest x-ray images, and that they are classified into two classes, "normal" and "pneumonia". The following sections describe the steps that are taken to create each model.

1) Binary classifier to detect pneumonia using chest x-rays
Train a model simply using 100 images from the “normal” class and 100 images from the “pneumonia” class.

2. Unbalanced binary classifier
Next, use 100 images from the “normal” class, and add 200 more "pneumonia" class images. At this moment, the total count of images must be:

- “normal” class = 100
- "pneumonia" class = 300

The model will be trained on very unbalanced classes

3. Binary classifier with dirty data
In this iteration, start with the original dataset of 100 "normal" and 100 "pneumonia" images. Then switch the labels of 30 images in each class.


4. Three-class model with the classes “normal”, “bacterial pneumonia”, and “viral pneumonia”
For this model, add 100 "normal" images, 100 "bacterial pneumonia" images, and 100 "viral pneumonia" images (for a total of 3 classes).
