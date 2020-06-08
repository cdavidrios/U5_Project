# U5_Project: Automatic classification of the Big-Five personality traits from texts using embeddings and Recurrent Neural Networks

This repository contains experiments for the classification of different Alzheimer's dementia stages from Magnetic Resonance Imaging using Deep Learning Techniques. The data was downloaded from [Kaggle](https://www.kaggle.com/tourist55/alzheimers-dataset-4-class-of-images). The data has four classes (Non demented, Very Mild Demented, Mild Demented, Moderate Demented) of images both in training as well as a testing set. Each image has a size of 208x176 pixels.

## Guideline
You can run each notebook in Google Colab.

## Content
The proposed work was divided in 4 experiments: 

- **Experiment 1:** We designed 4 differents architectures for Convolutional Neural Networks to classify the Dementia stages in Alzheimer taking into account the original 4 classes. Due to the low performance of these experiments, for the next 3 experiments, we only consider the first 3 classes (we excluded the Moderate Demented class).

- **Experiment 2:** We repeat the experiment 1 but with only 3 classes.

- **Experiment 3:** We used a TensorFlow Hub [model](https://tfhub.dev/google/imagenet/mobilenet_v2_075_96/feature_vector/4) to classify in two different ways the stages of Alzheimer: 1) using the embeddings as the input to a classic Support Vector Machine classifier and 2) adding to the output of TF Hub model a fully connected stage to classify the 3 classes.

- **Experiment 4:** We performed Transfer Learning from AlexNet. In this case, we designed a new architecture with the same first two layers of Alexnet. Four different tasks were implemented. The first is to train from scratch. The second experiment consist in making Transfer Learning without layer freezing. The third experiment consist in making Transfer Learning freezing only the first layer. And the last experiment, freezing the two layers from Alexnet.

- **Presentation Slides:** In this document you can see some slides with the summary of this work, highlighting the results obtained in each experiment and the conclusions.

## Conclusions
- The best result is obtained with TensorFlow Hub, we believe it is because this original model is trained with a large amount of images (1.2 million and  1000 categories) in order to obtain feature vectors or embeddings that are useful to classify images, which is our goal.

- The proposed methods using CNNs are useful to classify the different stages of severity of dementia in Alzheimer's disease based on MRI images, which would be very useful for support in the diagnosis and therapy of the disease.

- Different techniques such as dropout and L2 regularization are very useful when the models are implemented with real data, because these techniques allow a better generalization of the phenomenon and helps to avoid the overfitting of the network.

- Transfer learning uses feature maps of robust models and allows for adjustment in training. This is very useful for classifying small databases that do not have enough data to train deep learning models. 

## Authors
- Felipe Orlando López Pabón
- Cristian David Rios Urrego
