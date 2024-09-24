# Introduction
Input a cifar image and train the encoder and decoder to regenerate the same data as an output with minimum loss

# Illustration
1) Training: We train a CNN autoencoder on an input images from cifar dataset 
2) Input features: 3*32*32 (RGB channels, width, heigth)
3) Output targets: ['airplane', 'automobile', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck']

# Model & Architecture
1) CNN DL Model
2) 2 convolution layers + latent layer + batchnorm + leaky_relu
3) CNN img size 32 -> 16 ->  7 -> 2  -> 7  -> 16 -> 32
4) CNN Kernels  3  -> 16 -> 32 -> 64 -> 32 -> 16 -> 3 
5) Linear layer + leaky_relu
6) inChans  = 3 # RGB => should be changed to 1
7) outChans = 64 # of feature maps / kernels
8) krnSize  = 4x4 #
9) padding  = 1 # No padding
10) stride   = 2 # used stride
11) batchnorm = 0
12) Use of MSELoss
13) Minibatches = 32
14) Adam Optimizer with weight decay of 1e-5

# Results
1) Loss: Got a smooth dropping loss
2) Need to check output images in the next run!

# Conclusions:
1) Need to check output images in next run!
