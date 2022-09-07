## Problem Statement
To use a neural network to recognize ten handwritten digits, i.e., 0-9
This is a multiclass classification task where one of n choices is selected  
  
## Dataset  
- The data set contains 5000 training examples of handwritten digits $^1$.  

    - Each training example is a 20-pixel x 20-pixel grayscale image of the digit. 
        - Each pixel is represented by a floating-point number indicating the grayscale intensity at that location. 
        - The 20 by 20 grid of pixels is “unrolled” into a 400-dimensional vector. 
        - Each training examples becomes a single row in our data matrix `X`. 
        - This gives us a 5000 x 400 matrix `X` where every row is a training example of a handwritten digit image.
  
- The second part of the training set is a 5000 x 1 dimensional vector `y` that contains labels for the training set
    - `y = 0` if the image is of the digit `0`, `y = 4` if the image is of the digit `4` and so on.

1 <sub> This is a subset of the MNIST handwritten digit dataset (http://yann.lecun.com/exdb/mnist/)</sub>
  
  
## Model Representation  
- The neural network has two dense layers with ReLU activations followed by an output layer with a linear activation. 
    - Our inputs are pixel values of digit images.
    - Since the images are of size 20 x 20, this gives us 400 inputs
    - The parameters have dimensions that are sized for a neural network with $25$ units in layer 1, $15$ units in layer 2 and $10$ output units in layer 3, one for each digit.
