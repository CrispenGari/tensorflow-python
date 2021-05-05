## Convolutional Neural Network (CNN).
* A layer of a deep neural network in which a convolutional filter passes along an input matrix.
The following animation shows a convolutional layer consisting of 9 convolutional operations involving the `5x5` input matrix. Notice that each convolutional operation works on a different `3x3` slice of the input matrix. The resulting `3x3` matrix (on the right) consists of the results of the 9 convolutional operations:

<p align="center">
   <img src="https://github.com/CrispenGari/TensorFlow-2.4.1-Python/blob/main/keras-nn/06_Conv_NN/AnimatedConvolution.gif" alt="conv"/> 
</p>

 * A neural network in which at least one layer is a convolutional layer. A typical convolutional neural network consists of some combination of the following layers:
    * convolutional layers
    * pooling layers
    * dense layers
    
### Why CNN?
Fully connected layers are not very efficient when it comes to working with n-dimenional data such as images. In that case CNN will come to help.

### Convolutionsl Layer
* This layers convolves an image by a matrix, called Kerner or filter. The proccess is as follows:
1. First, you overlay the kernel onto the image.
2. Then you multiply the kernel value by the image value.
3. After that, you calculate the product of the results of the previous step.
4. Finally, you move the kernel one pixel and repeat the process.

<p align="center">
   <img src="https://github.com/CrispenGari/TensorFlow-2.4.1-Python/blob/main/keras-nn/06_Conv_NN/1_ciDgQEjViWLnCbmX-EeSrA.gif" alt="conv"/> 
</p>


Once we have the result from the previous step, we will do as we do on fully connected layers: we add the bias parameter and then apply an activation function.

### Pooling Layers
- Conv NN detects shapes on an image keeping the image size the same. Large images implies more and slower work during training so we may want to reduce the image size during the process. This is achived using pooling layers.
- Pooling layers allow us to reduce the size of the image so that the neural network works faster. It basically creates a smaller image by dividing the image in several `n X n` matrices.
- Depending on the type of pooling layer, the way of calculating the result might vary. In Max Pooling layers, for example, the result will be the maximum value of each smaller matrix. In Average Layers, on the other hand, the result will be the average of the smaller matrix.

#### The Max-Pooling layer.

<p align="center">
   <img src="https://github.com/CrispenGari/TensorFlow-2.4.1-Python/blob/main/keras-nn/06_Conv_NN/MaxpoolSample2.png" alt="conv"/> 
</p>


By applying a max pooling layer we ensure that the shapes detected by the convolutional layer are maintained for the next layer. Because of this, Max Pooling layers are the most used pooling layers, as they are they usually give better results.















