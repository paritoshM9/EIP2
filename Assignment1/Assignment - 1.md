​											**Assignment - 1**

Name - Paritosh Mahajan

Batch - 7



**1) Convolution** : 

Convolution is a mathematical transformation which transforms an input image into a new image with the help of a special matrix called kernel/filter . The new image generated from the convolution may contain certain features like edges, specific colours etc based on the kernel used. Convolution can also be termed as mapping of all individual or  set of pixels from the input image to  each pixel in the output image. The mapping is  based on the kernel matrix.

Generally, to find the value of one pixel of the output image , the element wise multiplication and then summation is done for *every part of the input image* on which the kernel slides, *with the kernel* and when this is done for the complete input image, we get a complete output image.

![1538648006035](C:\Users\parit\AppData\Roaming\Typora\typora-user-images\1538648006035.png)



**2) Filters/Kernels :**

Kernels/ Filters are small matrices which helps to extract important features from the input images by convolving throughout the input image. These kernels can help in extracting the edges, points , specific colours and much more. They slides over the entire input image and performs functions to generate output image. The kernel basically converts some input features into a single feature in the output. If the size of kernel is n X n and input image size is m X m. The output size is (m-n+1) X (m-n + 1)



**3) Epochs :**

One epoch is said to take place when the *complete dataset* is fed to the neural network *ONCE* i.e. our neural network has seen each and every data from the dataset ONCE. In general, the dataset is very large , so , we don't feed the complete dataset to the neural network at once. 

We break the dataset into smaller sets of data which are called batches. When all the batches are fed to the neural network once, 1 epoch is said to be done. In a neural network, 1 epoch leads to underfitting of the data due to which it is suggested to train the model for multiple epochs.



**4) 1X1 Convolution:**

1x1 Convolution is the mathematical transformation which transforms an input image to an output image by mapping every single input pixel to a single pixel in the output . We can say, that a 1x1 convolution is a convolution where the kernel size is 1x1.

It is used for dimensionality reduction of the input image which is mostly done before 3x3 or 5x5 convolution. 

For example - If the input image is 100x100x50 where we have 50 channels in the input image and we use 10 kernels of dimensions 1x1x50 . From the 50 feature-maps , our output is reduced to 100x100x10. In addition to this, these convolutions are generally followed by some non linear transformations which helps to add non-linearity. 

![Image result for 1x1 convolution](https://raw.githubusercontent.com/iamaaditya/iamaaditya.github.io/master/images/inception_1x1.png)



**5) 3X3 Convolution:**

3x3 Convolution is the most common convolution process where the kernel matrix is 3x3 . 

In this, the 3x3 kernel matrix slides over every (3x3) part of the input image and performs element wise multiplication with all the 9 corresponding pixels. Their sum is taken which creates 1 output pixel. This means that in 1 cycle of element wise multiplication and summation , we are creating a single output pixel. Hence, the output image is of smaller size and highlights a certain feature from the image. 

3x3 is the most common as it is compute friendly and it can behave as larger kernels just by using 3x3 kernel multiple times . For ex - If we want a 5x5 kernel , we can achieve that by doing 3x3 convolutions on the image twice and for 7x7 kernel, three convolutions with 3x3 kernel can give us the desired output.

 

![img](https://cdn-images-1.medium.com/max/800/1*Zx-ZMLKab7VOCQTxdZ1OAw.gif)



**6) Feature Maps:**



Every image contains of a large number of features like horizontal edge, vertical edges , curves , brighter areas , and many more features like this. For training a neural network for any kind of work , we need to extract the important features from the data and feed it to the neural network. 

In case of images, we do convolution over the entire input image with multiple kernels to extract the important features. Each kernel focusses on finding a particular feature and the generated output from each kernel is a *feature map or activation map.* A feature map is said to be high where the desired feature is found and low where it isn't . In the below image , Image(a) is the input image and images(b,c,d) are the feature maps for different features .

![Related image](https://www.researchgate.net/profile/Dong_Wang193/publication/303816027/figure/fig8/AS:371859007787009@1465669504312/Illustration-of-feature-maps-of-five-face-images-a-using-K-means-c-and-C-SVDD-d.png)



**7) Feature Engineering:**

Feature engineering is a very crucial step in any machine learning problem. It is an art of finding the most important and relevant features from the data, which optimises the accuracy of the model and gives a good predictive model. 

For a successful model, we need to feed only the best features to it so that it doesn't deviate because of redundant or random features .

Feature engineering comes into play here, it requires one to combine *domain knowledge* and *machine learning knowledge* , to create , modify  or mix the data features which makes the model successful in handling the data it hasn't seen before. 



**8) Activation Function**

A neural network is made up of multiple layers. Each layer is formed from the previous layer by doing some transformation and now the newly formed output layer acts as an input for the next layer until we get the final layer.

But, when a layer generates the next layer, before the new layer acts as the input for its subsequent layers, *a function is applied on the new layer and the output of that function then acts as the input for the next layer*. This function is called Activation function. 

Activation functions are functions which are applied on the output signals of each layer in a neural network to form input signals for the subsequent layers.

These functions help us to generate an output of the form  "yes" or "no" and are very helpful in the problems where we need to find probability for each label.

They also help to add non-linearity , otherwise our neural net will behave just like a regression model and we will not be able to add complex data to it. 

Some popular activation function are:

- **Sigmoid function** - It converts any value in the range of 0 - 1 . Its expression is

  >   	f(x) = 1/(1+e^(-x))

- **tanh** - It generates an output between -1 to 1.

- **ReLU** - its the most popular these days but has a lot of demerits . One of them being, it shows exagerated accuracy , which is dangerous when we are dealing with sensitive data.

  Its range is from 0 to infinity and its expression is : 

  >   	f(x) = max(0,x)





