# LeNet5-implementation
Implementation of a modified LeNet5 architecture from scratch on the MNIST  Dataset

This project implements the classic LeNet-5 architecture from scratch using Pytorch 

# Dataset
The dataset used in this project was the MNIST digit recognition dataset which contained 60,0000 training images and 10,000 testing images. The original LeNet5 architecture developed by Yann LeCun was developed to recognize hand written characters.

# Architecture
The Original LeNet 5 architecture had seven layers but due to severe overfitting more layers were added to curb it.
The basic layers in this modified Lenet 5 architecture are:

1. The input layer: The input layer has a size of 1x28x28 but was padded by 2 which gives us a dimension of 1x32x32. Normalization was added to  the input data.
2. The First Convolutional layer: The first Convolutional layer has the kerenel/filter size of 5*5 and 6 filters which were applied on the  image data.
3. The Activation Function: To improve  the model's performance i introduced the Rectified Linear units Activation functions instead of the Tanh activation function originally used in the LeNet 5 architecture and it showed a huge effect in improving the model's performance.
4. Subsampling layers 1: Average pooling of size 2 and the stride of 2 was used
5. The second Convolutional layer: The second convolutional layer had the kernel/filter size of 6*6 and 16 filters.
6. The Third Convolutional layer: The third Convolutional layer has 120 number of filter map before being fed into the Fully Connected layer.
7. The fully connected layer: The 120 feature maps were flattened into a 1d vector before being passed down to fully connected layer which has 84 neurons
8. The Output layer: The fully connected layer passes is down to the output laer which contained 10 neurons for the 10 digit classes.

# Overfitting
During training i encountered severe overfitting and here are the techniques i used to  solve it:
1. Dropout: I introduced the dropout layer to prevent my model for severely overfitting.
2. The ReLU Activation Function:Although it doesnt solve overfitting changing the Activation function from Tanh to ReLU helped improved my models performance.

# Results
The model was trained on 10 epochs and reached it's peak performance at Epoch 3 with the accuracy of 97.1%, slight overfitting was found but the models performance and accuracy  drastically improved.

