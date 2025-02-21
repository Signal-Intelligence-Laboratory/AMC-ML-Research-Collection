
Notes From: [Convolutional Radio Modulation Recognition Networks](https://arxiv.org/pdf/1602.04105)
- this is the paper that the repo is built from
- Feature learning/detection system
- Input to the CNN system is a 2xN array where the 2 dimensions are the I and Q inputs from sampling the signal
- This makes it a 2D CNN
- in section 3 they do mention that there are properties of radio communications that make simulated datasets acceptable and then they don't really explain futher
- 11 modulation types in the dataset
- The idea behind a CNN is that it will learn to form matched filters
- CNN network:
    - 2 convolutional layers with ReLUs 
        - first layer finds only 1x3 vectors to look for edges
        - second layer uses both I and Q to create many 2x3 snapshots, creating a full feature map
    - 2 fully connected layers
        - first is a dense ReLU
        - second is a dense SoftMax to feed into a OneHot block which determines the output guess
- there are two that they design of differing sizes
- 
