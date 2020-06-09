# U5_Project: Automatic classification of the Big-Five personality traits from texts using embeddings and Long Short Term Memory

This repository contains experiments that helps to automatically determine the presence or absence for each one of the 5 personality traits using the transcripts of the audio from vlogs of a set of 404 YouTube vloggers that explicitly show themselves in front of the a webcam talking about a variety of topics including personal issues, politics, movies, books, etc. The traits are Openness to experience (Open), Conscientiousness (Cons), Extraversion (Extr), Agreeableness (Agr) and Emotional stability (Emot), also named Neuroticism. This database counts with personality scores for the 404 transcripts, with which, from the value of the median for each trait, the labels of absence or presence of the trait were constructed as follows: if the score of the text in the trait is less than or equal to the median, it will have a label of 0 (absence of the trait), and if the score is greater than the median, it will have a label of 1 (presence of the trait).

## Guideline
You can run each notebook in Google Colab.

## Content
The proposed work was divided in 2 experiments: 

- **Elmo_BLSTM:** We designed an architecture that contains 1 ELMo embedding layer downloaded from [tensorflow hub](https://tfhub.dev/google/elmo/2), followed by a bidirectional long short term memory and a dense layer for the classification of each personality trait. In this notebook you can change the 5 personality traits and the number of maximun words for each text.

- **Glove_BLSTM:** We designed an architecture that contains 1 Embedding layer that uses the pre-trained 300-dimensional embeddings of [Glove](https://nlp.stanford.edu/projects/glove/)developed by Stanford University, followed by a bidirectional long short term memory and a Dense layer for the classification of each personality trait. In this notebook you can change the 5 personality traits and the number of maximun words for each text.

- **Presentation Slides:** In this document you can see some slides with the summary of this work, highlighting the results obtained in each experiment and the conclusions.

## Conclusions
- As shown in the results, using the proposed architecture it was possible to improve up to 8% of the accuracy of the models with respect to the baseline, which proves the capacity of architectures like ELMo for the classification of personality traits.

- Preprocessing is an important phase in text analysis because depending on the content of our data when introduced into a neural network, the performance of the model will change, since words with similar semantic and syntactic meaning according to the context should be represented by nearby word embeddings.

- One of the great advantages of bidirectional long short term memory is that these allow embeddings as input (GloVe), and also capture context forward and backward. This considerably improves the performance of current models for the classification and prediction of personality traits.


## Authors
- Felipe Orlando López Pabón
- Cristian David Rios Urrego
