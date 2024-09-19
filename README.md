# ifood-1M
 
This study compares three methods for food image classification on the [iFood-2019 dataset]([https://www.aicrowd.com/challenges/mapping-challenge](https://www.kaggle.com/c/ifood-2019-fgvc6/overview)): SIFT with Bag-of-Words
(BoW), Convolutional Neural Networks (CNNs), and Self-Supervised Learning (SSL).

## The dataset
The original iFood-2019 dataset consists of three subsets: training (118,475 samples), validation (11,994 images), and test (28,377 images), each containing images from 251 possible classes.
For the purpose of this project, I neglect the test set as the ground truth labels are not publicly available. I will use the original validation set as test set, and split the original training set into training and validation.  

## The task
The task consists in classifying food images into one of the 251 categories. To achieve this, I employ three different methods:
• _Feature Extraction Approach_: This method uses SIFT (Scale-Invariant Feature Transform) to extract key points
from images. These key points were then quantized into
visual words using the Bag of Words (BoW) model. A traditional classifier was then trained over those visual features to perform classification.
• _Convolutional Neural Network (CNN)_: This method leverages deep learning to build a model that learns feature representations from raw images, making it a popular choice
for image classification tasks.
• _Self-Supervised Learning_: This approach involves training a similar CNN model on a context-based pretext task
to make it learn useful features. These features are then
extracted and, along with the labels, used to train a traditional classifier

The **key challenge** of this project was that I was required to build a model with **less than one million parameters**.
The **goal** is to design and train a classifier that is able to distinguish among the different classes, while meeting the constraint on the number of parameters.

The code is developed using **Pytorch**.

### _Content:_
