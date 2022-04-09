# Read-an-image-for-visually-challenged
## Table of Contents
* [Problem Statement](#section-1)
* [Importing libraries and reading data](#section-2)
* [Data Understanding](#section-3)
* [Pre-processing the captions](#section-4)
* [Pre-processing the images](#section-5)
* [Extracting the Feature vector](#section-6)
* [Model Building](#section-7)
    - [Data preperation](#subsect-1)
    - [Build the Encoder](#subsect-2)
    - [Build the Attention model](#subsect-3)
    - [Build the Decoder](#subsect-4)
* [Model training & optimization](#section-8)
* [Model Evaluation](#section-9)
* [Conclusions](#section-10)

# Problem Statement
## Introduction
​
   The World Health Organization (WHO) has reported that approximately 285 million people are visually impaired worldwide, and out of these 285 million, 39 million are completely blind. It gets extremely tough for them to carry out daily activities, one of which is reading. From reading a newspaper or a magazine to reading an important text message from your bank, it is tough for them to read the text written in it.
​
    A similar problem they also face is seeing and enjoying the beauty of pictures and images. Today, in the world of social media, millions of images are uploaded daily. Some of them are about your friends and family, while some of them are about nature and its beauty. Understanding what is present in that image is quite a challenge for certain people who are suffering from visual impairment or who are blind.
​
    In an initiative to help them experience the beauty of the images, Facebook had earlier launched a unique feature earlier that can help blind people operate the app on their mobile phones. The feature could explain the contents of an image that their friends have posted on Facebook. So, say, if someone posted a picture with their dog in the park, the application would speak out the contents and may describe it like, “This image may contain a dog standing with a man around the trees.”
​    
    In this project, the intention is to build a model that is similar to the one developed by Facebook so that a visually challenged person knows the contents of an image in the form of audio. 
    Flickr8K dataset is used in the project, the dataset is available in Kaggle.
    
## Approach
​    Firstly the information in an image is converted into a text description, then using a text to speech API, the audio output is extracted from the text description.
    
​    This problem statement is an application of both deep learning and natural language processing. The features of an image will be extracted by a CNN-based encoder and this will be decoded by an RNN model. To generate a more meaningful and descriptive caption
    The main important portion is to generate the text description. A deep learning model using a CNN-RNN model with an attention mechanism is employed to generate the caption 
