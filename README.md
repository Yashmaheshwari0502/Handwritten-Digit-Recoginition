# Handwritten Digit Recognition with my_model

This repository contains the implementation of a neural network model for handwritten digit recognition. The model architecture includes three dense layers and is designed to classify handwritten digits from the MNIST dataset.

## Model Architecture

The architecture of `my_model` is as follows:

| Layer        | Output Shape | Parameters |
|--------------|--------------|------------|
| Dense (25)   | (None, 25)   | 10,025     |
| Dense (15)   | (None, 15)   | 390        |
| Dense (10)   | (None, 10)   | 160        |
| **Total parameters:** |   | **10,575 (41.31 KB)** |
| **Trainable parameters:** |   | **10,575 (41.31 KB)** |
| **Non-trainable parameters:** |   | **0 (0.00 Byte)** |

## Dataset

The model is trained on the MNIST dataset, which consists of 60,000 training images and 10,000 testing images of handwritten digits from 0 to 9. Each image is 28x28 pixels.

To load the dataset for this task, use the `load_data()` function, which loads the data into variables `X` and `y`. The dataset contains 5000 training examples of handwritten digits. Each training example is a 20-pixel x 20-pixel grayscale image of a digit. Each pixel is represented by a floating-point number indicating the grayscale intensity at that location. The 20 by 20 grid of pixels is “unrolled” into a 400-dimensional vector. Each training example becomes a single row in the data matrix `X`, giving us a 5000 x 400 matrix `X` where every row is a training example of a handwritten digit image.

\[ X = \begin{bmatrix}
\vdots & (x^{(1)}) & \vdots \\
\vdots & (x^{(2)}) & \vdots \\
& \vdots & \\
\vdots & (x^{(m)}) & \vdots \\
\end{bmatrix} \]

The second part of the training set is a 5000 x 1 dimensional vector `y` that contains labels for the training set, where `y = 0` if the image is of the digit 0, `y = 4` if the image is of the digit 4, and so on.

> This is a subset of the MNIST handwritten digit dataset ([http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/)).

## Requirements

To run this project, you need the following libraries:

- Python 3.x
- TensorFlow
- NumPy
- Matplotlib

## License

This project is licensed under the MIT License.

## Acknowledgements

The MNIST dataset is provided by Yann LeCun, Corinna Cortes, and Christopher J.C. Burges. Thanks to TensorFlow for providing the deep learning framework used in this project.
