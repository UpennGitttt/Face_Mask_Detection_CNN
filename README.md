# Face_Mask_Detection_CNN

The model designed achieves an overall of 95% test and validation accuracy, then Haar-Cascade Face Detection method is employed to crop faces in each image and make classifications upon cropped images using the trained CNN model.

# Project Environment Setup

Python is used as the programming language for this project, and the Python library numpy, pandas, matplotlib.pyplot, TensorFlow, and Keras were imported to provide helper functions.

# Data Cleaning and Preparation:

The images are cropped and only the area of the face is kept for the training, validation and testing. So the images are separated into three different folders: Train, Validation and Test. In each folder, there are images with two different labels that are with and without mask labels. ImageDataGenerator class from Tensor flow is employed to create objects of train, test validation dataset, the method called flow_from_directory() is used to read images from a big numpy array and folders containing images. There are also existing images taken from the bad angles such as right above or below the heads, these images are discarded to ensure the accuracy of the training. Some of the images that do not contain human faces are also discarded.The optimizer utilized for this project is Adam, which is an extension to stochastic gradient descent. Test accuracy of the model using SGD as optimization algorithm is 80% on average. After switching to Adam optimizer with Cross Entropy Loss, a clear leap on testing accuracy of the model which is approximately 95%. 

# CNN Model Construction and Training:

A multi-layer CNN network is constructed based on the models we learned in class. Three convolutional layers with 32, 64, 64 filters and a kernel size of 3 by 3 are used and each of the convolutional layers is followed by a max pooling layer of 2 by 2 pool size. Then three linear layers are applied with activation functions of Relu and Softmax, after that a binary output will be generated to indicate if the person is wearing a mask.

# Reults and Metrics:

<img width="1043" alt="Screen Shot 2023-05-03 at 12 04 58 PM" src="https://user-images.githubusercontent.com/98191838/235974238-e49fa9ab-42cb-428a-b132-33daea5af777.png">

<img width="552" alt="Screen Shot 2023-05-03 at 12 07 02 PM" src="https://user-images.githubusercontent.com/98191838/235974783-00f81b58-7652-4eea-b1b6-ef6a3d56087f.png">

<img width="424" alt="Screen Shot 2023-05-03 at 12 04 34 PM" src="https://user-images.githubusercontent.com/98191838/235974080-1805110d-fd31-4d93-9082-eb5129210fcf.png">

<img width="442" alt="Screen Shot 2023-05-03 at 12 04 41 PM" src="https://user-images.githubusercontent.com/98191838/235974126-55dda55c-91f6-4581-9eab-02fc5ab1fd53.png">
