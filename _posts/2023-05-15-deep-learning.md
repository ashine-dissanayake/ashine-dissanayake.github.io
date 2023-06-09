# <span style="color: rgb(84, 164, 162)">Deep Learning</span> 
This post will explore various deep learning algorithms. 

## <span style="color: rgb(84, 164, 162)">What is Deep Learning?</span> 
Deep Learning models are composed of multiple processing layers that aim to learn data representations with multiple levels of abstraction. These models are commonly utilized for visual object recognition and object detection. The use of deep convolutional nets has led to significant advancements in processing images, video, speech, and audio, while recurrent nets are particularly adept at handling text and speech data.

## <span style="color: rgb(84, 164, 162)">Convolutional Neural Networks (CNNs)</span> 
Convolutional Neural Network is apart of the artificial neural network. In many of the layer, matrixmulitplication occurs. However there is a mathematical operation referred to as **_convolution_**  that occurs in come of the layers. THe purpose of the convolutoin operation is to process pixel dat, making it a good algorithm for image recognition. 

Note that CNN is a multilayer perceptrons. **_Multilayer Perceptron_** is a fully conencted network that meanst hat all layer are connected (i.e., neuron previous layer is connected to a neuron on the next layer). 

CNN is a **_feed-forward neural network_** with around 20 to 30 layers and stacks many convolutional hidden layers on top of each other. The hidden layers comprise of many convolutional layers followed by activation function (and in some cases pooling layers). 

![](/images/cnn-model.png "CNN Model")

### Convolutional Layer
Convolutional layers are generally square templates, which slide over the image and look for specific patterns. If the image matches the pattern, it will return postive, other it returns 0. 

### Activation Functions 

#### Rectified Linear Unit [ReLU]
<img src="https://latex.codecogs.com/svg.image?&space;f(x)=\max{(0,&space;x)}" />


#### Sigmoidal Function
<img src="https://latex.codecogs.com/svg.image?S(x)=\frac{1}{1&space;&plus;&space;e^{-x}}" />


![](/images/af.jfif "Activation Functions")

## <span style="color: rgb(84, 164, 162)">Recurrent Neural Networks (RNNs)</span> 
RNNs uses sequential data or time series data. It is commonly used for language translation, natural language processing and, speech recognition, and image captioning. Some common applications inclde Siri and Google translate. RNN relies on its memory by account for previous inputs to influence the current input and output. Another dicerning characteristic of RNN is the parameters are shared acorss networks. Instead of feed-forward neural networks, RNN is a backpropagation through time. 

![](/images/nn.jfif "FF vs BPTT Model")
