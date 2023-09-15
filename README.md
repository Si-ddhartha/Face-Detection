# Face-Detection

Face detection is a critical component in computer vision applications, from security systems to social media filters. This project aims to create a deep-learning model for face detection using TensorFlow from scratch.


![collage3](https://github.com/Si-ddhartha/Face-Detection/assets/74449359/c6dc6fa2-17d4-4926-bbfc-30eb28034289)

*The images were resized, resulting in reduced quality.*


The face detection model is fundamentally composed of two distinct components:-

a) **Classification**

  This component determines whether an object exists in the image and classifies it.

b) **Localization**

  This component identifies the coordinates for the bounding box if an object is present.

We will use Keras Functional API, which allows us to have two different loss functions and combine them in the end.

## **Project Description:**

1. Data Collection and Preprocessing:

    Collected a diverse dataset of images that contain faces using OpenCV. The dataset includes images with varying lighting conditions and poses.
    
    Annotate the dataset with bounding box coordinates around the faces for localization.
    
    Split the dataset into training, validation, and testing sets.

2. Data Augmentation:

    Performed data augmentation to increase the diversity of the data set by applying random transformations, such as cropping, and flipping.

3. Model Architecture:

    Used VGG16 as the base model, which is a popular and well-established convolutional neural network (CNN) architecture.
    
    Removed the fully connected layers of VGG16, keeping only the convolutional layers.
    
    Add custom layers on top of the VGG16 base to perform classification and localization tasks.
       
    Designed the classification head to predict whether a face is present in the input image or not, typically as a binary classification task (face or no face).
    
    Designed the localization head to predict the bounding box coordinates around the detected face.

5. Training:

    Train the model on the training dataset using suitable loss functions for both classification and localization tasks.
    
    Implemented a custom localization loss function.
    
    Used binary cross-entropy for classification.

6. Evaluation:

    Evaluate the model's performance on the validation dataset.

7. Testing:

    Assess the model's performance on the testing dataset to estimate its real-world applicability.
    
    Visualize the detected faces and bounding boxes on test images to gauge the model's accuracy.
