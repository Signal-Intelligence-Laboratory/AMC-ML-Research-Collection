# Unit 2 - Coding a convolution block

### 2.1 Convolution in Python from scratch
Follow along with [the Python code here](https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/conv_benchmark.py).

### 2.2 Comparison with NumPy convolution()
*No additional notes*

### 2.3 Create the convolution block Conv1D
To follow along, make sure [you have Cottonwood installed](https://gitlab.com/brohrer/cottonwood), up to date, and are working from version 19 using

`git checkout v19`

Alternatively you can walk though the [online repository](https://gitlab.com/brohrer/cottonwood/-/blob/v19/cottonwood/core/blocks/conv1d.py).

Neural network architecture images featured:

LeNet from [Gradient-Based Learning Applied to Document Recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf). 1998. Yann LeCun, Leon Bottou, and Patrick Haffner.

VGG16 from [Very Deep Convolutional Networks for Large-Scale Image Recognition](https://arxiv.org/abs/1409.1556). 2015. Karen Simonoyan and Andrew Zisserman.

ResNet from [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385). 2015. Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun.

Long Short-term Memory from [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/). colah's blog. 2015. Chris Olah.

Inception from [Going Deeper with Convolutions](https://arxiv.org/abs/1409.4842). 2014. Christian Szegedy, Wei Liu, Yangqing Jia, Pierre Sermanet, Scott Reed, Dragomir Anguelov, Dumitru Erhan, Vincent Vanhoucke, and Andrew Rabinovich.

### 2.4 Initialize the convolution block
*No additional notes*

### 2.5 Write the forward and backward pass
*No additional notes*

### 2.6 Write the multichannel, multikernel convolutions
*No additional notes*

### 2.7 Write the weight gradient and input gradient calculations
Postscript

After I published this course I found a bug in the computation of the weight gradients. The details of the bug are less important than the implications. Learning by building is a creative endeavor and by its nature involves a lot of trial and error. Due to their complexity, machine learning algorithms make excellent hiding places for bugs. So even though the code ran and appeared to perform well, it wasn’t as healthy as I believed. I’m leaving the original walkthrough video in place with [the link to the updated code](https://gitlab.com/brohrer/cottonwood/-/blob/main/cottonwood/conv1d.py#L265) here, in an effort to model transparency and public error correction.

If you are curious, the bug was in how I implemented the cross correlation between the output gradient and the inputs in the convolution layer to get the weight gradient (around 2:55 in the video above). Unlike convolution, the order of the arguments matters in cross correlation. I got them in the wrong order, and as a result the calculated weight gradient was reversed. I also needed to add some padding, as in the calculation for the input gradient, in order to get everything to work out right. This bug is fairly low level and doesn’t obscure the concepts involved, so I am less worried about it from a teaching point of view.

Still, it’s pretty embarrassing. My apologies if it tripped you up in any way.