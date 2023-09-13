# Face-Detection

Face detection is a critical component in computer vision applications, from security systems to social media filters. This project aims to create a deep-learning model for face detection using TensorFlow from scratch.

The face detection model is fundamentally composed of two distinct components:-

a) **Classification**
  
  This component determines whether an object exists in the image and classifies it.

b) **Localization**

  This component identifies the coordinates for the bounding box if an object is present.

## **Project Description:**

1. Data Collection and Preprocessing:

    Collected a diverse dataset of images that contain faces using opencv. The dataset includes images with varying lighting conditions and poses.
    
    Annotate the dataset with bounding box coordinates around the faces for localization.
    
    Split the dataset into training, validation, and testing sets.

2. Data Augmentation:

    Performed data augmentation to increase the diversity of the data set by applying random transformations, such as cropping, and flipping.

3. Model Architecture:

    Used VGG16 as the base model, which is a popular and well-established convolutional neural network (CNN) architecture.
    
    Removed the fully connected layers of VGG16, keeping only the convolutional layers.
    
    Add custom layers on top of the VGG16 base to perform classification and localization tasks.
    
    Design the classification head to predict whether a face is present in the input image or not, typically as a binary classification task (face or no face).
    
    Design the localization head to predict the bounding box coordinates around the detected face.

4. Training:

    Train the model on the training dataset using suitable loss functions for both classification and localization tasks.
    
    Implemented a custom localization loss function.
    
    Used binary cross-entropy for classification.

5. Evaluation:

    Evaluate the model's performance on the validation dataset.

6. Testing:

    Assess the model's performance on the testing dataset to estimate its real-world applicability.
    
    Visualize the detected faces and bounding boxes on test images to gauge the model's accuracy.
