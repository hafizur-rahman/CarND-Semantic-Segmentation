# CarND - Semantic Segmentation Rubrics
The goal of this project is to construct a fully convolutional neural network based on the VGG-16 image classifier architecture for performing semantic segmentation to identify drivable road area from an car dashcam image (trained and tested on the KITTI data set).

## Neural Network Architecture
A pre-trained VGG-16 network was converted to a fully convolutional network by converting the final fully connected layer to a 1x1 convolution and setting the depth equal to the number of desired classes (in this case, 2: road and not-road). Performance is improved through the use of skip connections, performing 1x1 convolutions on previous VGG layers (in this case, layers 3 and 4) and adding them element-wise to upsampled (through transposed convolution) lower-level layers (i.e. the 1x1-convolved layer 7 is upsampled before being added to the 1x1-convolved layer 4). Each convolution and transpose convolution layer includes a kernel initializer and regularizer.

### Optimizer
The loss function for the network is `cross-entropy`, and an `Adam optimizer` is used.

## Rubric Points

#### Does the project load the pretrained vgg model?
The pretrained `vgg` model is downloaded using helper fuction and loaded using Tensorflow API (v1.3.0) `tf.saved_model.loader.load()`. The function `load_vgg` at `main.py` is implemented to get references to important layers. See [load_vgg](main.py#L23..L46) implementation.

#### Does the project learn the correct features from the images?

#### Does the project optimize the neural network?

#### Does the project train the neural network?

### Does the project train the model correctly?
```
Model build successful, starting training
-----------------------
| Epoch # | Avg. Loss |
-----------------------
|       1 |     0.710 |
|       2 |     0.295 |
|       3 |     0.172 |
|       4 |     0.142 |
|       5 |     0.116 |
|       6 |     0.111 |
|       7 |     0.089 |
|       8 |     0.082 |
|       9 |     0.070 |
|      10 |     0.066 |
|      11 |     0.059 |
|      12 |     0.053 |
|      13 |     0.051 |
|      14 |     0.050 |
|      15 |     0.046 |
|      16 |     0.044 |
|      17 |     0.040 |
|      18 |     0.038 |
|      19 |     0.037 |
|      20 |     0.036 |
|      21 |     0.062 |
|      22 |     0.049 |
|      23 |     0.037 |
|      24 |     0.034 |
|      25 |     0.033 |
|      26 |     0.031 |
|      27 |     0.030 |
|      28 |     0.029 |
|      29 |     0.028 |
|      30 |     0.027 |
```

### Does the project use reasonable hyperparameters?

The hyperparameters used for training are:
* keep_prob: 0.8
* learning_rate: 0.0001
* epochs: 30
* batch_size: 8

### Does the project correctly label the road?