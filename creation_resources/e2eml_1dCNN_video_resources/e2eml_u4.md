# Unit 4 - Add the finishing touches: ReLU, Pooling, Batch Normalization 

### 4.1 The ReLU block
All the code for this section is taken from Cottonwood v21. If you're walking through in your local repository, make sure to

`git checkout v21`

If you're following along in the GitLab repository, you can find the right version here

https://gitlab.com/brohrer/cottonwood/-/blob/v21/cottonwood/core/blocks/activation.py


The Wikipedia page on Rectifiers is a great reference if you need to go deeper on the concepts behind the ReLU.

https://en.wikipedia.org/wiki/Rectifier_(neural_networks)

### 4.2 One dimensional max pooling block
Follow along in your local copy of Cottonwood in core/blocks/pooling.py or in the GitLab repo

https://gitlab.com/brohrer/cottonwood/-/blob/v21/cottonwood/core/blocks/pooling.py

### 4.3 One dimensional max pooling computations
Follow along in your local copy of Cottonwood in core/blocks/pooling.py or in the GitLab repo

https://gitlab.com/brohrer/cottonwood/-/blob/v21/cottonwood/core/blocks/pooling.py

### 4.4 How Batch Normalization works
Here's the original paper

Batch Normalization: Accelerating Deep Network Training byReducing Internal Covariate Shift

by Sergey Ioffe and Christian Szegedy

https://arxiv.org/pdf/1502.03167v3.pdf

The Wikipedia page is helpful too

https://en.wikipedia.org/wiki/Batch_normalization

### 4.5 Online Batch Normalization, initialization
Follow along in your local Cottonwood code at experimental/blocks/normalization.py or in the GitLab repository at

https://gitlab.com/brohrer/cottonwood/-/blob/v21/cottonwood/experimental/blocks/normalization.py

For a bit more information on Online Batch Normalization, check out the post

https://e2eml.school/online_batch_normalization.html

### 4.6 Online Batch Normalization, forward pass
For more explanation on exponential smoothing, check out this post

https://e2eml.school/exponential_smoothing.html

### 4.7 Online Batch Normalization, backward pass
*No additional notes*

### 4.8 All together now
The example we walk through here is in cottonwood/examples/convnet/blip_demo_batch_norm.py or online at

https://gitlab.com/brohrer/cottonwood/-/blob/v21/cottonwood/examples/convnet/blip_demo_batch_norm.py