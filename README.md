# Handwritten-Digit-Recognition-using-CNN
This project implements a Handwritten Digit Recognition system using a Convolutional Neural Network (CNN) to classify handwritten digits from images. The model is trained on the MNIST dataset, a widely used dataset in machine learning that contains grayscale images of digits from 0 to 9.

<mark><b>DATASET</b></mark>



The project uses the famous MNIST dataset, which consists of 60,000 labeled images of handwritten digits for training and 10,000 labeled images for testing. Each image is 28x28 pixels in size and grayscale, with pixel values ranging from 0 to 255. The dataset is preprocessed to normalize pixel values.

<mark><b>MODEL ARCHITECTURE</b></mark>


The first layer is a convolutional layer (Conv2D) with 32 filters, a kernel size of (3, 3), and a ReLU activation function. It takes an input image of shape (28, 28, 1) where 1 represents grayscale channel.
The output from the convolutional layer is then passed through a max pooling layer (MaxPooling2D) with a pool size of (2, 2), which helps reduce spatial dimensions while preserving important features.
Another convolutional layer with 64 filters, a kernel size of (3, 3), and a ReLU activation function is added, followed by another max pooling layer with a pool size of (2, 2).
The output from the last max pooling layer is then flattened into a 1D array using a Flatten layer, which prepares the data for the fully connected layers.
Two fully connected layers (Dense) are added on top of the flattened output. The first dense layer has 128 units with a ReLU activation function, while the second dense layer has 10 units with a softmax activation function, which gives the probability of each class (0 to 9) being the correct digit.


<mark><b>Model Deployment</b></mark>


Streamit Front end
The Streamlit front-end provides a simple and interactive web-based user interface for users to draw digit and get predictions from the trained CNN model.
Draw a digit on a canvas: Users can use the mouse or touchpad to draw a digit on a canvas provided by the Streamlit app. The drawn image is then passed to the trained CNN model for prediction.

<mark><b>Model evaluation</b></mark>

<img width="1198" height="83" alt="proj 2" src="https://github.com/user-attachments/assets/8fe22c3f-2c32-4cbe-849f-a01c0fd6f34e" />



Display prediction results: The Streamlit app displays the predicted digit.
Sample output
<img width="1490" height="691" alt="proj" src="https://github.com/user-attachments/assets/e3ecdfd0-11c7-41f4-b703-ca4a794dfb4f" />
<img width="1239" height="578" alt="proj1" src="https://github.com/user-attachments/assets/9ca5f587-a6bc-4790-b4ea-527c1b84df3e" />




Project structure 
handwritten-digit-recognition-cnn
│
├── dataset
│

├──
train_model.py
├──
predict_digit.py
├──
model.h5
├──
requirements.txt
└── 
README.md


